---
title: db_get_field
sidebar_label: db_get_field
description: Get the content of a field from db_query.
keywords:
  - sqlite
---

<LowercaseNote />

## Description

Get the content of a field from db_query

| Name              | Description                      |
| ----------------- | -------------------------------- |
| DBResult:dbresult | The result to get the data from. |
| field             | The field to get the data from.  |
| result[]          | The result.                      |
| maxlength         | The max length of the field.     |

## Returns

Returns 1 if result set handle is valid and the column is available, otherwise 0.

## Example

```c
// examples.inc

// ...

static FindFieldIndexByName(DBResult:dbResultSet, const fieldName[])
{
    // Return value variable with default return value
    new ret = -1;

    // Field count
    new field_count = db_num_fields(dbResultSet);

    // Current field name
    new current_field_name[32];

    // Iterate through all fields
    for (new field_index; field_index < field_count; field_index++)
    {
        // Get field name
        if (db_field_name(dbResultSet, field_index, current_field_name, sizeof current_field_name))
        {
            // Compare searched field name to current field name
            if (!strcmp(fieldName, current_field_name))
            {
                // Success, store field index to return value variable
                ret = field_index;

                // Break out of the loop
                break;
            }
        }
    }

    // Return found field index or "-1"
    return ret;
}

Examples_ListNames(DB:dbConnectionHandle)
{
    // Database result set
    new DBResult:db_result_set = db_query("SELECT `name` FROM `examples`");

    // If database result set is valid
    if (db_result_set)
    {
        // Get target field index
        new target_field_index = FindFieldIndexByName(db_result_set, "name");

        // Check if field index is valid
        if (target_field_index >= 0)
        {
            // Allocate some memory to store results
            new result[256];

            // Do operations
            do
            {
                // Add value from "example" field to the return value variable
                db_get_field(db_result_set, target_field_index, result, sizeof result);
            }

            // While next row could be fetched
            while (db_next_row(db_result_set));
        }

        // Free result set
        db_free_result(db_result_set);
    }
}
```

```c
// mode.pwn

// ...

#include <examples>

static DB:gDBConnectionHandle;

// ...

public OnGameModeInit()
{
    // ...

    // Create a connection to a database
    gDBConnectionHandle = db_open("example.db");

    // If connection to the database exists
    if (gDBConnectionHandle)
    {
        // Successfully created a connection to the database
        print("Successfully created a connection to database \"example.db\".");
        Examples_ListNames(gDBConnectionHandle);
    }
    else
    {
        // Failed to create a connection to the database
        print("Failed to open a connection to database \"example.db\".");
    }

    // ...

    return 1;
}

public OnGameModeExit()
{
    // Close the connection to the database if connection is open
    if (db_close(gDBConnectionHandle))
    {
        // Extra cleanup
        gDBConnectionHandle = DB:0;
    }

    // ...

    return 1;
}
```

## Notes

:::warning

Using an invalid handle other than zero will crash your server! Get a valid database connection handle by using [db_query](db_query).

:::

## Related Functions

- [db_open](db_open): Open a connection to an SQLite database
- [db_close](db_close): Close the connection to an SQLite database
- [db_query](db_query): Query an SQLite database
- [db_free_result](db_free_result): Free result memory from a db_query
- [db_num_rows](db_num_rows): Get the number of rows in a result
- [db_next_row](db_next_row): Move to the next row
- [db_num_fields](db_num_fields): Get the number of fields in a result
- [db_field_name](db_field_name): Returns the name of a field at a particular index
- [db_get_field_assoc](db_get_field_assoc): Get content of field with specified name from current result row
- [db_get_field_int](db_get_field_int): Get content of field as an integer with specified ID from current result row
- [db_get_field_assoc_int](db_get_field_assoc_int): Get content of field as an integer with specified name from current result row
- [db_get_field_float](db_get_field_float): Get content of field as a float with specified ID from current result row
- [db_get_field_assoc_float](db_get_field_assoc_float): Get content of field as a float with specified name from current result row
- [db_get_mem_handle](db_get_mem_handle): Get memory handle for an SQLite database that was opened with db_open.
- [db_get_result_mem_handle](db_get_result_mem_handle): Get memory handle for an SQLite query that was executed with db_query.
- [db_debug_openfiles](db_debug_openfiles): The function gets the number of open database connections for debugging purposes.
- [db_debug_openresults](db_debug_openresults): The function gets the number of open database results.
