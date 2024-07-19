###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_AllocateTemporaryMemory

Allocate temporary memory.

## Header File

Defined in [<SDL3/SDL_events.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_events.h)

## Syntax

```c
void * SDL_AllocateTemporaryMemory(size_t size);
```

## Function Parameters

|        |          |                                   |
| ------ | -------- | --------------------------------- |
| size_t | **size** | the amount of memory to allocate. |

## Return Value

(void *) Returns a pointer to the memory allocated or NULL on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

You can use this to allocate memory that will be automatically freed later,
after event processing is complete.

## Thread Safety

It is safe to call this function from any thread.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_ClaimTemporaryMemory](SDL_ClaimTemporaryMemory)
- [SDL_FreeTemporaryMemory](SDL_FreeTemporaryMemory)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryEvents](CategoryEvents)

