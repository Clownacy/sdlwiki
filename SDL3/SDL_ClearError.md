###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_ClearError

Clear any previous error message for this thread.

## Header File

Defined in [<SDL3/SDL_error.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_error.h)

## Syntax

```c
SDL_bool SDL_ClearError(void);
```

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE).

## Version

This function is available since SDL 3.0.0.

## Code Examples

```c
const char *error = SDL_GetError();
if (*error) {
  SDL_Log("SDL error: %s", error);
  SDL_ClearError();
}
```

## See Also

- [SDL_GetError](SDL_GetError)
- [SDL_SetError](SDL_SetError)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryError](CategoryError)

