---
title: PlayerTextDrawColour
sidebar_label: PlayerTextDrawColour
description: 设置玩家文本绘图的文字颜色。
tags: ["玩家", "文本绘图", "玩家文本绘图"]
---

<VersionWarnZH_CN version='omp v1.1.0.2612' />

## 描述

设置玩家文本绘图的文字颜色。

| 名称              | 描述                                        |
| ----------------- | ------------------------------------------- |
| playerid          | 要设置文字颜色的玩家文本绘图所属玩家的 ID   |
| PlayerText:textid | 要设置文字颜色的玩家文本绘图的 ID           |
| textColour        | 需要设置的文字颜色数值（ARGB 十六进制格式） |

## 返回值

该函数不返回任何特定值。

## 示例

```c
new PlayerText:pTextdraw[MAX_PLAYERS];

public OnPlayerConnect(playerid)
{
    pTextdraw[playerid] = CreatePlayerTextDraw(playerid, 320.0, 240.0, "示例文本");
    PlayerTextDrawColour(playerid, pTextdraw[playerid], 0xFF0000FF); // 设置不透明红色文字

    PlayerTextDrawShow(playerid, pTextdraw[playerid]);
    return 1;
}
```

## 注意事项

:::tip

- 可在文本内容中使用游戏文本颜色代码（例如 `~r~` 红色、`~g~` 绿色、`~b~` 蓝色）
- 修改颜色后需调用 PlayerTextDrawShow 重新显示文本绘图才能生效

:::

## 相关函数

- [CreatePlayerTextDraw](CreatePlayerTextDraw): 创建玩家文本绘图
- [PlayerTextDrawDestroy](PlayerTextDrawDestroy): 销毁玩家文本绘图
- [PlayerTextDrawBoxColour](PlayerTextDrawBoxColour): 设置玩家文本绘图方框颜色
- [PlayerTextDrawBackgroundColour](PlayerTextDrawBackgroundColour): 设置玩家文本绘图的背景颜色
- [PlayerTextDrawAlignment](PlayerTextDrawAlignment): 设置玩家文本绘图对齐方式
- [PlayerTextDrawFont](PlayerTextDrawFont): 设置玩家文本绘图的字体样式
- [PlayerTextDrawLetterSize](PlayerTextDrawLetterSize): 设置玩家文本绘图的字符尺寸
- [PlayerTextDrawTextSize](PlayerTextDrawTextSize): 设置玩家文本绘图方框尺寸（或 PlayerTextDrawSetSelectable 的可点击区域）
- [PlayerTextDrawSetOutline](PlayerTextDrawSetOutline): 切换玩家文本绘图的轮廓显示
- [PlayerTextDrawSetShadow](PlayerTextDrawSetShadow): 设置玩家文本绘图的阴影效果
- [PlayerTextDrawSetProportional](PlayerTextDrawSetProportional): 按比例缩放玩家文本绘图的文字间距
- [PlayerTextDrawUseBox](PlayerTextDrawUseBox): 切换玩家文本绘图的方框显示
- [PlayerTextDrawSetString](PlayerTextDrawSetString): 设置玩家文本绘图的显示内容
- [PlayerTextDrawShow](PlayerTextDrawShow): 显示玩家文本绘图
- [PlayerTextDrawHide](PlayerTextDrawHide): 隐藏玩家文本绘图
