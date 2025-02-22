---
title: OnActorStreamIn
description: This callback is called when an actor is streamed in by a player's client.
tags: []
---

<VersionWarn name='callback' version='SA-MP 0.3.7' />

## Description

This callback is called when an actor is streamed in by a player's client.

| Name        | Description                                                   |
| ----------- | ------------------------------------------------------------- |
| actorid     | The ID of the actor that has been streamed in for the player. |
| forplayerid | The ID of the player that streamed the actor in.              |

## Returns

It is always called first in filterscripts.

## Examples

```c
public OnActorStreamIn(actorid, forplayerid)
{
    new string[40];
    format(string, sizeof(string), "Actor %d is now streamed in for you.", actorid);
    SendClientMessage(forplayerid, 0xFFFFFFFF, string);
    return 1;
}
```

## Notes

<TipNPCCallbacks />

## Related Callbacks

The following callbacks might be useful, as they're related to this callback in one way or another. 

- [OnActorStreamOut](OnActorStreamOut): This callback is called when an actor is streamed out by a player's client.
