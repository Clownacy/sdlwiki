###### (This function is part of SDL_mixer, a separate library from SDL.)
# Mix_HaltChannel

Halt playing of a particular channel.

## Header File

Defined in [<SDL_mixer.h>](https://github.com/libsdl-org/SDL_mixer/blob/SDL2/include/SDL_mixer.h)

## Syntax

```c
int Mix_HaltChannel(int channel);
```

## Function Parameters

|     |             |                                              |
| --- | ----------- | -------------------------------------------- |
| int | **channel** | channel to halt, or -1 to halt all channels. |

## Return Value

(int) Returns 0 on success, or -1 on error.

## Remarks

This will stop further playback on that channel until a new chunk is
started there.

Specifying a channel of -1 will halt _all_ channels, except for any playing
music.

Any halted channels will have any currently-registered effects
deregistered, and will call any callback specified by
[Mix_ChannelFinished](Mix_ChannelFinished)() before this function returns.

You may not specify MAX_CHANNEL_POST for a channel.

## Version

This function is available since SDL_mixer 2.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

