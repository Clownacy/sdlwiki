###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_HINT_JOYSTICK_HIDAPI_STEAM_HORI

A variable controlling whether the HIDAPI driver for HORI licensed Steam controllers should be used.

## Header File

Defined in [<SDL3/SDL_hints.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_hints.h)

## Syntax

```c
#define SDL_HINT_JOYSTICK_HIDAPI_STEAM_HORI "SDL_JOYSTICK_HIDAPI_STEAM_HORI"
```

## Remarks

This variable can be set to the following values: "0" - HIDAPI driver is
not used "1" - HIDAPI driver is used

The default is the value of
[SDL_HINT_JOYSTICK_HIDAPI](SDL_HINT_JOYSTICK_HIDAPI)

----
[CategoryAPI](CategoryAPI), [CategoryAPIMacro](CategoryAPIMacro), [CategoryHints](CategoryHints)

