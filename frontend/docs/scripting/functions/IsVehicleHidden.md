---
title: IsVehicleHidden
sidebar_label: IsVehicleHidden
description: Checks if a vehicle is hidden.
tags: ["vehicle"]
---

<VersionWarn version='omp v1.1.0.2612' />

:::warning

This function has not yet been implemented.

:::

## Description

Checks if a vehicle is hidden.

## Parameters

| Name      | Description                     |
|-----------|---------------------------------|
| vehicleid | The ID of the vehicle to check. |

## Return Values

**true** - Vehicle is hidden.

**false** - Vehicle is not hidden.

## Examples

```c
if (IsVehicleHidden(vehicleid))
{
    // Vehicle is hidden
}
else
{
    // Vehicle is not hidden
}
```

## Related Functions

- [HideVehicle](HideVehicle): Hides a vehicle from the game.
- [ShowVehicle](ShowVehicle): Shows the hidden vehicle.
