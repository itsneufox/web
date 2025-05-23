---
title: GetNetworkStats
sidebar_label: GetNetworkStats
description: Gets the server's network stats and stores them in a string.
tags: []
---

## คำอธิบาย

Gets the server's network stats and stores them in a string.

| Name        | Description                                                    |
| ----------- | -------------------------------------------------------------- |
| retstr[]    | The string to store the network stats in, passed by reference. |
| retstr_size | The length of the string to be stored.                         |

## ส่งคืน

This function always returns 1.

## ตัวอย่าง

```c
public OnPlayerCommandText(playerid,cmdtext[])
{
    if (!strcmp(cmdtext, "/netstats"))
    {
        new stats[400+1];
        GetNetworkStats(stats, sizeof(stats)); // get the servers networkstats
        ShowPlayerDialog(playerid, 0, DIALOG_STYLE_MSGBOX, "Server Network Stats", stats, "Close", "");
    }
    return 1;
}
```

```
Server Ticks: 200
Messages in Send buffer: 0
Messages sent: 142
Bytes sent: 8203
Acks sent: 11
Acks in send buffer: 0
Messages waiting for ack: 0
Messages resent: 0
Bytes resent: 0
Packetloss: 0.0%
Messages received: 54
Bytes received: 2204
Acks received: 0
Duplicate acks received: 0
Inst. KBits per second: 28.8
KBits per second sent: 10.0
KBits per second received: 2.7
```

## ฟังก์ชั่นที่เกี่ยวข้องกัน

- [GetPlayerNetworkStats](../functions/GetPlayerNetworkStats): Gets a player networkstats and saves it into a string.
- [NetStats_GetConnectedTime](../functions/NetStats_GetConnectedTime): Get the time that a player has been connected for.
- [NetStats_MessagesReceived](../functions/NetStats_MessagesReceived): Get the number of network messages the server has received from the player.
- [NetStats_BytesReceived](../functions/NetStats_BytesReceived): Get the amount of information (in bytes) that the server has received from the player.
- [NetStats_MessagesSent](../functions/NetStats_MessagesSent): Get the number of network messages the server has sent to the player.
- [NetStats_BytesSent](../functions/NetStats_BytesSent): Get the amount of information (in bytes) that the server has sent to the player.
- [NetStats_MessagesRecvPerSecond](../functions/NetStats_MessagesRecvPerSecond): Get the number of network messages the server has received from the player in the last second.
- [NetStats_PacketLossPercent](../functions/NetStats_PacketLossPercent): Get a player's packet loss percent.
- [NetStats_ConnectionStatus](../functions/NetStats_ConnectionStatus): Get a player's connection status.
- [NetStats_GetIpPort](../functions/NetStats_GetIpPort): Get a player's IP and port.
