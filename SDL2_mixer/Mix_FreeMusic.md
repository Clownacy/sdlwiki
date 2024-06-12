###### (This function is part of SDL_mixer, a separate library from SDL.)
# Mix_FreeMusic

Free a music object.

## Header File

Defined in [<SDL_mixer.h>](https://github.com/libsdl-org/SDL_mixer/blob/SDL2/include/SDL_mixer.h)

## Syntax

```c
void Mix_FreeMusic(Mix_Music *music);
```

## Function Parameters

|                          |           |                           |
| ------------------------ | --------- | ------------------------- |
| [Mix_Music](Mix_Music) * | **music** | the music object to free. |

## Remarks

If this music is currently playing, it will be stopped.

If this music is in the process of fading out (via
[Mix_FadeOutMusic](Mix_FadeOutMusic)()), this function will *block* until
the fade completes. If you need to avoid this, be sure to call
[Mix_HaltMusic](Mix_HaltMusic)() before freeing the music.

## Version

This function is available since SDL_mixer 2.0.0.

## See Also

- [Mix_LoadMUS](Mix_LoadMUS)
- [Mix_LoadMUS_RW](Mix_LoadMUS_RW)
- [Mix_LoadMUSType_RW](Mix_LoadMUSType_RW)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

