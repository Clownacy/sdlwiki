###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetSurfaceRLE

Set the RLE acceleration hint for a surface.

## Header File

Defined in [<SDL3/SDL_surface.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_surface.h)

## Syntax

```c
SDL_bool SDL_SetSurfaceRLE(SDL_Surface *surface, SDL_bool enabled);
```

## Function Parameters

|                              |             |                                                                                        |
| ---------------------------- | ----------- | -------------------------------------------------------------------------------------- |
| [SDL_Surface](SDL_Surface) * | **surface** | the [SDL_Surface](SDL_Surface) structure to optimize.                                  |
| [SDL_bool](SDL_bool)         | **enabled** | [SDL_TRUE](SDL_TRUE) to enable RLE acceleration, [SDL_FALSE](SDL_FALSE) to disable it. |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Remarks

If RLE is enabled, color key and alpha blending blits are much faster, but
the surface must be locked before directly accessing the pixels.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_BlitSurface](SDL_BlitSurface)
- [SDL_LockSurface](SDL_LockSurface)
- [SDL_UnlockSurface](SDL_UnlockSurface)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategorySurface](CategorySurface)

