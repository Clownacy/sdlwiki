###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetRenderColorScale

Set the color scale used for render operations.

## Header File

Defined in [<SDL3/SDL_render.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_render.h)

## Syntax

```c
SDL_bool SDL_SetRenderColorScale(SDL_Renderer *renderer, float scale);
```

## Function Parameters

|                                |              |                        |
| ------------------------------ | ------------ | ---------------------- |
| [SDL_Renderer](SDL_Renderer) * | **renderer** | the rendering context. |
| float                          | **scale**    | the color scale value. |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Remarks

The color scale is an additional scale multiplied into the pixel color
value while rendering. This can be used to adjust the brightness of colors
during HDR rendering, or changing HDR video brightness when playing on an
SDR display.

The color scale does not affect the alpha channel, only the color
brightness.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_GetRenderColorScale](SDL_GetRenderColorScale)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryRender](CategoryRender)

