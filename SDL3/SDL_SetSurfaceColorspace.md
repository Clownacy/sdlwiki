###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetSurfaceColorspace

Set the colorspace used by a surface.

## Header File

Defined in [<SDL3/SDL_surface.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_surface.h)

## Syntax

```c
bool SDL_SetSurfaceColorspace(SDL_Surface *surface, SDL_Colorspace colorspace);
```

## Function Parameters

|                                  |                |                                                                              |
| -------------------------------- | -------------- | ---------------------------------------------------------------------------- |
| [SDL_Surface](SDL_Surface) *     | **surface**    | the [SDL_Surface](SDL_Surface) structure to update.                          |
| [SDL_Colorspace](SDL_Colorspace) | **colorspace** | an [SDL_ColorSpace](SDL_ColorSpace) value describing the surface colorspace. |

## Return Value

(bool) Returns true on success or false on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

Setting the colorspace doesn't change the pixels, only how they are
interpreted in color operations.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_GetSurfaceColorspace](SDL_GetSurfaceColorspace)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategorySurface](CategorySurface)

