###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_LoadFile_IO

Load all the data from an SDL data stream.

## Header File

Defined in [<SDL3/SDL_iostream.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_iostream.h)

## Syntax

```c
void * SDL_LoadFile_IO(SDL_IOStream *src, size_t *datasize, bool closeio);
```

## Function Parameters

|                                |              |                                                                                                      |
| ------------------------------ | ------------ | ---------------------------------------------------------------------------------------------------- |
| [SDL_IOStream](SDL_IOStream) * | **src**      | the [SDL_IOStream](SDL_IOStream) to read all available data from.                                    |
| size_t *                       | **datasize** | a pointer filled in with the number of bytes read, may be NULL.                                      |
| bool                           | **closeio**  | if true, calls [SDL_CloseIO](SDL_CloseIO)() on `src` before returning, even in the case of an error. |

## Return Value

(void *) Returns the data or NULL on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

The data is allocated with a zero byte at the end (null terminated) for
convenience. This extra byte is not included in the value reported via
`datasize`.

The data should be freed with [SDL_free](SDL_free)().

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_LoadFile](SDL_LoadFile)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryIOStream](CategoryIOStream)

