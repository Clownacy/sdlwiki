###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_GetGamepadSensorData

Get the current state of a gamepad sensor.

## Header File

Defined in [<SDL3/SDL_gamepad.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gamepad.h)

## Syntax

```c
SDL_bool SDL_GetGamepadSensorData(SDL_Gamepad *gamepad, SDL_SensorType type, float *data, int num_values);
```

## Function Parameters

|                                  |                |                                                 |
| -------------------------------- | -------------- | ----------------------------------------------- |
| [SDL_Gamepad](SDL_Gamepad) *     | **gamepad**    | the gamepad to query.                           |
| [SDL_SensorType](SDL_SensorType) | **type**       | the type of sensor to query.                    |
| float *                          | **data**       | a pointer filled with the current sensor state. |
| int                              | **num_values** | the number of values to write to data.          |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Remarks

The number of values and interpretation of the data is sensor dependent.
See [SDL_sensor](SDL_sensor).h for the details for each type of sensor.

## Version

This function is available since SDL 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryGamepad](CategoryGamepad)

