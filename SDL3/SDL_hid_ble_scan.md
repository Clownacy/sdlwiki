###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_hid_ble_scan

Start or stop a BLE scan on iOS and tvOS to pair Steam Controllers.

## Header File

Defined in [<SDL3/SDL_hidapi.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_hidapi.h)

## Syntax

```c
void SDL_hid_ble_scan(bool active);
```

## Function Parameters

|      |            |                                                 |
| ---- | ---------- | ----------------------------------------------- |
| bool | **active** | true to start the scan, false to stop the scan. |

## Version

This function is available since SDL 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryHIDAPI](CategoryHIDAPI)

