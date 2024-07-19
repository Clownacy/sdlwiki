###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_WriteS8

Use this function to write a signed byte to an [SDL_IOStream](SDL_IOStream).

## Header File

Defined in [<SDL3/SDL_iostream.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_iostream.h)

## Syntax

```c
SDL_bool SDL_WriteS8(SDL_IOStream *dst, Sint8 value);
```

## Function Parameters

|                                |           |                                               |
| ------------------------------ | --------- | --------------------------------------------- |
| [SDL_IOStream](SDL_IOStream) * | **dst**   | the [SDL_IOStream](SDL_IOStream) to write to. |
| Sint8                          | **value** | the byte value to write.                      |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on successful write or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Version

This function is available since SDL 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryIOStream](CategoryIOStream)

