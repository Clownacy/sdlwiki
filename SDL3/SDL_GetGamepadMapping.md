###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_GetGamepadMapping

Get the current mapping of a gamepad.

## Header File

Defined in [<SDL3/SDL_gamepad.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gamepad.h)

## Syntax

```c
const char * SDL_GetGamepadMapping(SDL_Gamepad *gamepad);
```

## Function Parameters

|                              |             |                                                      |
| ---------------------------- | ----------- | ---------------------------------------------------- |
| [SDL_Gamepad](SDL_Gamepad) * | **gamepad** | the gamepad you want to get the current mapping for. |

## Return Value

(const char *) Returns a string that has the gamepad's mapping or NULL if
no mapping is available; call [SDL_GetError](SDL_GetError)() for more
information.

## Remarks

This returns temporary memory which will be automatically freed later, and
can be claimed with [SDL_ClaimTemporaryMemory](SDL_ClaimTemporaryMemory)().

Details about mappings are discussed with
[SDL_AddGamepadMapping](SDL_AddGamepadMapping)().

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_AddGamepadMapping](SDL_AddGamepadMapping)
- [SDL_GetGamepadMappingForID](SDL_GetGamepadMappingForID)
- [SDL_GetGamepadMappingForGUID](SDL_GetGamepadMappingForGUID)
- [SDL_SetGamepadMapping](SDL_SetGamepadMapping)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryGamepad](CategoryGamepad)

