###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_PLATFORM_WIN32

A preprocessor macro that is only defined if compiling for desktop Windows.

## Header File

Defined in [<SDL3/SDL_platform_defines.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_platform_defines.h)

## Syntax

```c
#define SDL_PLATFORM_WIN32 1
```

## Remarks

Despite the "32", this also covers 64-bit Windows; as an informal
convention, its system layer tends to still be referred to as "the Win32
API."

## Version

This macro is available since SDL 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIMacro](CategoryAPIMacro), [CategoryPlatform](CategoryPlatform)

