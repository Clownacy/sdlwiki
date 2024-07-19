###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_GetHaptics

Get a list of currently connected haptic devices.

## Header File

Defined in [<SDL3/SDL_haptic.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_haptic.h)

## Syntax

```c
const SDL_HapticID * SDL_GetHaptics(int *count);
```

## Function Parameters

|       |           |                                                                              |
| ----- | --------- | ---------------------------------------------------------------------------- |
| int * | **count** | a pointer filled in with the number of haptic devices returned, may be NULL. |

## Return Value

(const [SDL_HapticID](SDL_HapticID) *) Returns a 0 terminated array of
haptic device instance IDs or NULL on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

This returns temporary memory which will be automatically freed later, and
can be claimed with [SDL_ClaimTemporaryMemory](SDL_ClaimTemporaryMemory)().

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_OpenHaptic](SDL_OpenHaptic)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryHaptic](CategoryHaptic)

