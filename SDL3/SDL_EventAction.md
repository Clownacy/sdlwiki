###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_EventAction

The type of action to request from [SDL_PeepEvents](SDL_PeepEvents)().

## Header File

Defined in [<SDL3/SDL_events.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_events.h)

## Syntax

```c
typedef enum SDL_EventAction
{
    SDL_ADDEVENT,  /**< Add events to the back of the queue. */
    SDL_PEEKEVENT, /**< Check but don't remove events from the queue front. */
    SDL_GETEVENT   /**< Retrieve/remove events from the front of the queue. */
} SDL_EventAction;
```

## Version

This enum is available since SDL 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIEnum](CategoryAPIEnum), [CategoryEvents](CategoryEvents)

