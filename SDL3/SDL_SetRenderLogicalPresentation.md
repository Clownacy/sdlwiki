###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetRenderLogicalPresentation

Set a device independent resolution and presentation mode for rendering.

## Header File

Defined in [<SDL3/SDL_render.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_render.h)

## Syntax

```c
SDL_bool SDL_SetRenderLogicalPresentation(SDL_Renderer *renderer, int w, int h, SDL_RendererLogicalPresentation mode, SDL_ScaleMode scale_mode);
```

## Function Parameters

|                                                                    |                |                                       |
| ------------------------------------------------------------------ | -------------- | ------------------------------------- |
| [SDL_Renderer](SDL_Renderer) *                                     | **renderer**   | the rendering context.                |
| int                                                                | **w**          | the width of the logical resolution.  |
| int                                                                | **h**          | the height of the logical resolution. |
| [SDL_RendererLogicalPresentation](SDL_RendererLogicalPresentation) | **mode**       | the presentation mode used.           |
| [SDL_ScaleMode](SDL_ScaleMode)                                     | **scale_mode** | the scale mode used.                  |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Remarks

This function sets the width and height of the logical rendering output. A
render target is created at the specified size and used for rendering and
then copied to the output during presentation.

You can disable logical coordinates by setting the mode to
[SDL_LOGICAL_PRESENTATION_DISABLED](SDL_LOGICAL_PRESENTATION_DISABLED), and
in that case you get the full pixel resolution of the output window.

You can convert coordinates in an event into rendering coordinates using
[SDL_ConvertEventToRenderCoordinates](SDL_ConvertEventToRenderCoordinates)().

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_ConvertEventToRenderCoordinates](SDL_ConvertEventToRenderCoordinates)
- [SDL_GetRenderLogicalPresentation](SDL_GetRenderLogicalPresentation)
- [SDL_GetRenderLogicalPresentationRect](SDL_GetRenderLogicalPresentationRect)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryRender](CategoryRender)

