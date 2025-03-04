###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetRenderDrawBlendMode

Set the blend mode used for drawing operations (Fill and Line).

## Header File

Defined in [<SDL3/SDL_render.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_render.h)

## Syntax

```c
bool SDL_SetRenderDrawBlendMode(SDL_Renderer *renderer, SDL_BlendMode blendMode);
```

## Function Parameters

|                                |               |                                                         |
| ------------------------------ | ------------- | ------------------------------------------------------- |
| [SDL_Renderer](SDL_Renderer) * | **renderer**  | the rendering context.                                  |
| [SDL_BlendMode](SDL_BlendMode) | **blendMode** | the [SDL_BlendMode](SDL_BlendMode) to use for blending. |

## Return Value

(bool) Returns true on success or false on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

If the blend mode is not supported, the closest supported mode is chosen.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_GetRenderDrawBlendMode](SDL_GetRenderDrawBlendMode)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryRender](CategoryRender)

