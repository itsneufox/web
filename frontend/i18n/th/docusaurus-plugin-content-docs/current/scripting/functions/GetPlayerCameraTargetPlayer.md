---
title: GetPlayerCameraTargetPlayer
sidebar_label: GetPlayerCameraTargetPlayer
description: Allows you to retrieve the ID of the player the playerid is looking at.
tags: ["player"]
---

:::warning

ฟังก์ชั่นนี้ถูกเพิ่มใน SA-MP 0.3.7 และจะไม่ทำงานในเวอร์ชั่นก่อนหน้านี้!

:::

## คำอธิบาย

Allows you to retrieve the ID of the player the playerid is looking at.

| Name     | Description                   |
| -------- | ----------------------------- |
| playerid | The ID of the player to check |

## ส่งคืน

The ID of the player the playerid is looking at

## ตัวอย่าง

```c
new playerTarget = GetPlayerCameraTargetPlayer(playerid);

if (IsPlayerAdmin(playerTarget))
{
    GameTextForPlayer(playerid, "Looking at an admin", 3000, 3);
}
```

## บันทึก

:::warning

Do not confuse this function with GetPlayerTargetPlayer. GetPlayerTargetPlayer returns the ID of the player playerid is aming at (with a weapon). GetPlayerCameraTargetPlayer returns the ID of the player playerid is looking at (reference point is the center of the screen).

:::

## ฟังก์ชั่นที่เกี่ยวข้องกัน

- [GetPlayerCameraTargetActor](../functions/GetPlayerCameraTargetActor): Get the ID of the actor (if any) a player is looking at.
- [GetPlayerCameraTargetVehicle](../functions/GetPlayerCameraTargetVehicle): Get the ID of the vehicle a player is looking at.
- [GetPlayerCameraTargetObject](../functions/GetplayerCameraTargetObject): Get the ID of the object a player is looking at.
- [GetPlayerCameraFrontVector](../functions/GetPlayercameraFrontVector): Get the player's camera front vector
