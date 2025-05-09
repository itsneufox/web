---
title: OnPlayerEnterVehicle
sidebar_label: OnPlayerEnterVehicle
description: Ова функција се позива када играч почне да улази у возило, што значи да играч још увек није у возилу у тренутку када се функција позива.
tags: ["player", "vehicle"]
---

## Опис

Ова функција се позива када играч почне да улази у возило, што значи да играч још увек није у возилу у тренутку када се функција позива.

| Име         | Опис                                                 |
| ----------- | ---------------------------------------------------- |
| playerid    | ID играча који покушава да уђе у возило.             |
| vehicleid   | ID возила у које играч покушава да уђе.              |
| ispassenger | 0 ако улази као возач. 1 ако улази као путник.       |

## Враћа

Увек се позива прва у филтер скрипти.

## Пример

```c
public OnPlayerEnterVehicle(playerid, vehicleid, ispassenger)
{
    new string[128];
    format(string, sizeof(string), "You are entering vehicle %i", vehicleid);
    SendClientMessage(playerid, 0xFFFFFFFF, string);
    return 1;
}
```

## Белешке

:::tip

- Ова функција се позива када играч ПОЧНЕ да улази у возило, а не када је УШАО у њега. Погледајте [OnPlayerStateChange](OnPlayerStateChange).
- Ова функција ће се и даље позвати ако играчу буде одбијен улазак у возило (нпр. ако је закључано или пуно).

:::

## Повезане повратне функције

Следеће повратне функције могу бити корисне, јер су на један или други начин повезане са овим позивом.

- [OnPlayerExitVehicle](OnPlayerExitVehicle): Ова функција се позива када играч изађе из возила.
- [OnPlayerStateChange](OnPlayerStateChange): Ова функција се позива када играч промени стање.

## Повезане функције

Следеће функције могу бити корисне, јер су на један или други начин повезане са овим позивом.

- [PutPlayerInVehicle](../functions/PutPlayerInVehicle): Ставите играча у возило.
- [GetPlayerVehicleSeat](../functions/GetPlayerVehicleSeat): Проверавајте у којем седишту се играч налази.
