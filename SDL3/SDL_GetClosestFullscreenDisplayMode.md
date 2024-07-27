###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_GetClosestFullscreenDisplayMode

Get the closest match to the requested display mode.

## Header File

Defined in [<SDL3/SDL_video.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_video.h)

## Syntax

```c
int SDL_GetClosestFullscreenDisplayMode(SDL_DisplayID displayID, int w, int h, float refresh_rate, SDL_bool include_high_density_modes, SDL_DisplayMode *mode);
```

## Function Parameters

|                                      |                                |                                                                                             |
| ------------------------------------ | ------------------------------ | ------------------------------------------------------------------------------------------- |
| [SDL_DisplayID](SDL_DisplayID)       | **displayID**                  | the instance ID of the display to query.                                                    |
| int                                  | **w**                          | the width in pixels of the desired display mode.                                            |
| int                                  | **h**                          | the height in pixels of the desired display mode.                                           |
| float                                | **refresh_rate**               | the refresh rate of the desired display mode, or 0.0f for the desktop refresh rate.         |
| [SDL_bool](SDL_bool)                 | **include_high_density_modes** | boolean to include high density modes in the search.                                        |
| [SDL_DisplayMode](SDL_DisplayMode) * | **mode**                       | a pointer filled in with the closest display mode equal to or larger than the desired mode. |

## Return Value

(int) Returns 0 on success or a negative error code on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

The available display modes are scanned and `closest` is filled in with the
closest mode matching the requested mode and returned. The mode format and
refresh rate default to the desktop mode if they are set to 0. The modes
are scanned with size being first priority, format being second priority,
and finally checking the refresh rate. If all the available modes are too
small, then NULL is returned.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_GetDisplays](SDL_GetDisplays)
- [SDL_GetFullscreenDisplayModes](SDL_GetFullscreenDisplayModes)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryVideo](CategoryVideo)

