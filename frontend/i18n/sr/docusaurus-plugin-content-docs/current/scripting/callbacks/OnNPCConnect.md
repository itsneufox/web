---
title: OnNPCConnect
sidebar_label: OnNPCConnect
description: Ова повратна функција се позива када NPC успешно изврши повезивање на сервер.
tags: ["npc"]
---

## Опис

Ова повратна функција се позива када NPC успешно изврши повезивање на сервер.

| Име          | Опис                                               |
| ------------ | -------------------------------------------------- |
| myplayerid   | ID играча који је додељен NPC-у.                  |

## Пример

```c
public OnNPCConnect(myplayerid)
{
    printf("Uspesno sam se povezao na server sa ID-em %i!", myplayerid);
}
```

## Повезане повртане функције

Следеће повратне функције могу бити корисне, јер су на неки начин повезане са овом повратном функцијом.

- [OnNPCDisconnect](OnNPCDisconnect): Ова повратна функција се позива када се NPC одвеже са сервера.
- [OnPlayerConnect](OnPlayerConnect): Ова повратна функција се позива када се играч повезује на сервер.
- [OnPlayerDisconnect](OnPlayerDisconnect): Ова повратна функција се позива када играч напусти сервер.
