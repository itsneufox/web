---
title: IsGangZoneVisibleForPlayer
sidebar_label: IsGangZoneVisibleForPlayer
description: Check if the gangzone is visible for player
tags: ["player", "gangzone"]
---

<VersionWarn version='omp v1.1.0.2612' />

## Description

Check if the gangzone is visible for player.

| Name        | Description                               |
| ----------- | ----------------------------------------- |
| playerid    | The ID of the player to check for.        |
| zoneid      | The ID of the gangzone.                   |

## Returns

**true** - The gangzone is visible for player.

**false** - The gangzone is not visible for player.

## Related Functions

- [GangZoneDestroy](GangZoneDestroy): Destroy a gangzone.
- [GangZoneShowForPlayer](GangZoneShowForPlayer): Show a gangzone for a player.
- [GangZoneShowForAll](GangZoneShowForAll): Show a gangzone for all players.
- [GangZoneHideForPlayer](GangZoneHideForPlayer): Hide a gangzone for a player.
- [GangZoneHideForAll](GangZoneHideForAll): Hide a gangzone for all players.
- [GangZoneFlashForPlayer](GangZoneFlashForPlayer): Make a gangzone flash for a player.
- [GangZoneFlashForAll](GangZoneFlashForAll): Make a gangzone flash for all players.
- [GangZoneStopFlashForPlayer](GangZoneStopFlashForPlayer): Stop a gangzone flashing for a player.
- [GangZoneStopFlashForAll](GangZoneStopFlashForAll): Stop a gangzone flashing for all players.
- [IsValidGangZone](IsValidGangZone): Check if the gangzone valid.
- [IsPlayerInGangZone](IsPlayerInGangZone): Check if the player in gangzone.