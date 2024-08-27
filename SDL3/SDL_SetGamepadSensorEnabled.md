###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetGamepadSensorEnabled

Set whether data reporting for a gamepad sensor is enabled.

## Header File

Defined in [<SDL3/SDL_gamepad.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gamepad.h)

## Syntax

```c
SDL_bool SDL_SetGamepadSensorEnabled(SDL_Gamepad *gamepad, SDL_SensorType type, SDL_bool enabled);
```

## Function Parameters

|                                  |             |                                           |
| -------------------------------- | ----------- | ----------------------------------------- |
| [SDL_Gamepad](SDL_Gamepad) *     | **gamepad** | the gamepad to update.                    |
| [SDL_SensorType](SDL_SensorType) | **type**    | the type of sensor to enable/disable.     |
| [SDL_bool](SDL_bool)             | **enabled** | whether data reporting should be enabled. |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_GamepadHasSensor](SDL_GamepadHasSensor)
- [SDL_GamepadSensorEnabled](SDL_GamepadSensorEnabled)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryGamepad](CategoryGamepad)

