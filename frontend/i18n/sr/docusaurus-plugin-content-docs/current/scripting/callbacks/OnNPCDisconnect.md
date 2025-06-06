---
title: OnNPCDisconnect
sidebar_label: OnNPCDisconnect
description: Ова повратна функција се позива када се NPC дисконектује са сервера.
tags: ["npc"]
---

## Опис

Ова повратна функција се позива када се NPC дисконектује са сервера.

| Име          | Опис                                                    |
| ------------ | ------------------------------------------------------- |
| reason[]     | Разлог због којег је бот дисконектован са сервера.      |

## Пример

```c
public OnNPCDisconnect(reason[])
{
    printf("Disconnected from the server. %s", reason);
}
```

## Повезане повратне функције

Следеће повратне функције могу бити корисне, јер су на неки начин повезане са овом повратном функцијом.

- [OnNPCConnect](OnNPCConnect): Ова повратна функција се позива када NPC успешно изврши повезивање на сервер.
- [OnPlayerDisconnect](OnPlayerDisconnect): Ова повратна функција се позива када играч напусти сервер.
- [OnPlayerConnect](OnPlayerConnect): Ова повратна функција се позива када се играч повезује на сервер.
