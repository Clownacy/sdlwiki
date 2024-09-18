###### (This function is part of SDL_ttf, a separate library from SDL.)
# TTF_Init

Initialize SDL_ttf.

## Header File

Defined in [<SDL3_ttf/SDL_ttf.h>](https://github.com/libsdl-org/SDL_ttf/blob/main/include/SDL3_ttf/SDL_ttf.h)

## Syntax

```c
bool TTF_Init(void);
```

## Return Value

(bool) Returns true on success or false on failure; call SDL_GetError() for
more information.

## Remarks

You must successfully call this function before it is safe to call any
other function in this library, with one exception: a human-readable error
message can be retrieved from SDL_GetError() if this function fails.

SDL must be initialized before calls to functions in this library, because
this library uses utility functions from the SDL library.

It is safe to call this more than once; the library keeps a counter of init
calls, and decrements it on each call to [TTF_Quit](TTF_Quit), so you must
pair your init and quit calls.

## Version

This function is available since SDL_ttf 3.0.0.

## See Also

- [TTF_Quit](TTF_Quit)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

