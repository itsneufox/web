---
title: 回调函数序列
sidebar_label: 回调函数序列
description: SA-MP/open.mp中可用的回调函数列表及其调用顺序
tags: []
---

以下是 SA-MP/open.mp 中可用的回调函数列表及其调用顺序。勾选框表示优先调用。

| 回调函数                                                                | 滤镜脚本 | 游戏模式 |
| ----------------------------------------------------------------------- | -------- | -------- |
| [OnActorStreamIn](../callbacks/OnActorStreamIn)                         | ✅       |          |
| [OnActorStreamOut](../callbacks/OnActorStreamOut)                       | ✅       |          |
| [OnClientCheckResponse](../callbacks/OnClientCheckResponse)             | ✅       |          |
| [OnClientMessage](../callbacks/OnClientMessage)                         | ✅       |          |
| [OnDialogResponse](../callbacks/OnDialogResponse)                       | ✅       |          |
| [OnEnterExitModShop](../callbacks/OnEnterExitModShop)                   | ✅       |          |
| [OnFilterScriptExit](../callbacks/OnFilterScriptExit)                   | ✅       |          |
| [OnFilterScriptInit](../callbacks/OnFilterScriptInit)                   | ✅       |          |
| [OnGameModeExit](../callbacks/OnGameModeExit)                           | ✅       |          |
| [OnGameModeInit](../callbacks/OnGameModeInit)                           | ✅       |          |
| [OnIncomingConnection](../callbacks/OnIncomingConnection)               | ✅       |          |
| [OnObjectMoved](../callbacks/OnObjectMoved)                             | ✅       |          |
| [OnPlayerClickMap](../callbacks/OnPlayerClickMap)                       |          | ✅       |
| [OnPlayerClickPlayer](../callbacks/OnPlayerClickPlayer)                 | ✅       |          |
| [OnPlayerClickPlayerTextDraw](../callbacks/OnPlayerClickPlayerTextDraw) | ✅       |          |
| [OnPlayerClickTextDraw](../callbacks/OnPlayerClickTextDraw)             | ✅       |          |
| [OnPlayerCommandText](../callbacks/OnPlayerCommandText)                 | ✅       |          |
| [OnPlayerConnect](../callbacks/OnPlayerConnect)                         | ✅       |          |
| [OnPlayerDeath](../callbacks/OnPlayerDeath)                             | ✅       |          |
| [OnPlayerDisconnect](../callbacks/OnPlayerDisconnect)                   | ✅       |          |
| [OnPlayerEditAttachedObject](../callbacks/OnPlayerEditAttachedObject)   | ✅       |          |
| [OnPlayerEditObject](../callbacks/OnPlayerEditObject)                   | ✅       |          |
| [OnPlayerEnterCheckpoint](../callbacks/OnPlayerEnterCheckpoint)         | ✅       |          |
| [OnPlayerEnterRaceCheckpoint](../callbacks/OnPlayerEnterRaceCheckpoint) | ✅       |          |
| [OnPlayerEnterVehicle](../callbacks/OnPlayerEnterVehicle)               | ✅       |          |
| [OnPlayerExitedMenu](../callbacks/OnPlayerExitedMenu)                   |          | ✅       |
| [OnPlayerExitVehicle](../callbacks/OnPlayerExitVehicle)                 | ✅       |          |
| [OnPlayerFinishedDownloading](../callbacks/OnPlayerFinishedDownloading) | ✅       |          |
| [OnPlayerGiveDamage](../callbacks/OnPlayerGiveDamage)                   | ✅       |          |
| [OnPlayerGiveDamageActor](../callbacks/OnPlayerGiveDamageActor)         | ✅       |          |
| [OnPlayerInteriorChange](../callbacks/OnPlayerInteriorChange)           |          | ✅       |
| [OnPlayerKeyStateChange](../callbacks/OnPlayerKeyStateChange)           |          | ✅       |
| [OnPlayerLeaveCheckpoint](../callbacks/OnPlayerLeaveCheckpoint)         | ✅       |          |
| [OnPlayerLeaveRaceCheckpoint](../callbacks/OnPlayerLeaveRaceCheckpoint) | ✅       |          |
| [OnPlayerObjectMoved](../callbacks/OnPlayerObjectMoved)                 | ✅       |          |
| [OnPlayerPickUpPickup](../callbacks/OnPlayerPickUpPickup)               |          | ✅       |
| [OnPickupStreamIn](../callbacks/OnPickupStreamIn)                       | ✅       |          |
| [OnPickupStreamOut](../callbacks/OnPickupStreamOut)                     | ✅       |          |
| [OnPlayerPickUpPlayerPickup](../callbacks/OnPlayerPickUpPlayerPickup)   |          | ✅       |
| [OnPlayerPickupStreamIn](../callbacks/OnPlayerPickupStreamIn)           | ✅       |          |
| [OnPlayerPickupStreamOut](../callbacks/OnPlayerPickupStreamOut)         | ✅       |          |
| [OnPlayerRequestClass](../callbacks/OnPlayerRequestClass)               | ✅       |          |
| [OnPlayerRequestDownload](../callbacks/OnPlayerRequestDownload)         | ✅       |          |
| [OnPlayerRequestSpawn](../callbacks/OnPlayerRequestSpawn)               | ✅       |          |
| [OnPlayerSelectedMenuRow](../callbacks/OnPlayerSelectedMenuRow)         |          | ✅       |
| [OnPlayerSelectObject](../callbacks/OnPlayerSelectObject)               | ✅       |          |
| [OnPlayerSpawn](../callbacks/OnPlayerSpawn)                             | ✅       |          |
| [OnPlayerStateChange](../callbacks/OnPlayerStateChange)                 | ✅       |          |
| [OnPlayerStreamIn](../callbacks/OnPlayerStreamIn)                       | ✅       |          |
| [OnPlayerStreamOut](../callbacks/OnPlayerStreamOut)                     | ✅       |          |
| [OnPlayerTakeDamage](../callbacks/OnPlayerTakeDamage)                   | ✅       |          |
| [OnPlayerText](../callbacks/OnPlayerText)                               | ✅       |          |
| [OnPlayerUpdate](../callbacks/OnPlayerUpdate)                           | ✅       |          |
| [OnPlayerWeaponShot](../callbacks/OnPlayerWeaponShot)                   | ✅       |          |
| [OnRconCommand](../callbacks/OnRconCommand)                             | ✅       |          |
| [OnRconLoginAttempt](../callbacks/OnRconLoginAttempt)                   | ✅       |          |
| [OnRecordingPlaybackEnd](../callbacks/OnRecordingPlaybackEnd)           | ✅       |          |
| [OnTrailerUpdate](../callbacks/OnTrailerUpdate)                         | ✅       |          |
| [OnUnoccupiedVehicleUpdate](../callbacks/OnUnoccupiedVehicleUpdate)     | ✅       |          |
| [OnVehicleDamageStatusUpdate](../callbacks/OnVehicleDamageStatusUpdate) | ✅       |          |
| [OnVehicleDeath](../callbacks/OnVehicleDeath)                           | ✅       |          |
| [OnVehicleMod](../callbacks/OnVehicleMod)                               |          | ✅       |
| [OnVehiclePaintjob](../callbacks/OnVehiclePaintjob)                     |          | ✅       |
| [OnVehicleRespray](../callbacks/OnVehicleRespray)                       |          | ✅       |
| [OnVehicleSirenStateChange](../callbacks/OnVehicleSirenStateChange)     | ✅       |          |
| [OnVehicleSpawn](../callbacks/OnVehicleSpawn)                           | ✅       |          |
| [OnVehicleStreamIn](../callbacks/OnVehicleStreamIn)                     | ✅       |          |
| [OnVehicleStreamOut](../callbacks/OnVehicleStreamOut)                   | ✅       |          |
