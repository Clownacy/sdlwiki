###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_RenameStoragePath

Rename a file or directory in a writable storage container.

## Header File

Defined in [<SDL3/SDL_storage.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_storage.h)

## Syntax

```c
SDL_bool SDL_RenameStoragePath(SDL_Storage *storage, const char *oldpath, const char *newpath);
```

## Function Parameters

|                              |             |                      |
| ---------------------------- | ----------- | -------------------- |
| [SDL_Storage](SDL_Storage) * | **storage** | a storage container. |
| const char *                 | **oldpath** | the old path.        |
| const char *                 | **newpath** | the new path.        |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_StorageReady](SDL_StorageReady)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryStorage](CategoryStorage)

