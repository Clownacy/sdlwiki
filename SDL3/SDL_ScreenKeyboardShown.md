###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_ScreenKeyboardShown

Check whether the screen keyboard is shown for given window.

## Header File

Defined in [<SDL3/SDL_keyboard.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_keyboard.h)

## Syntax

```c
bool SDL_ScreenKeyboardShown(SDL_Window *window);
```

## Function Parameters

|                            |            |                                                         |
| -------------------------- | ---------- | ------------------------------------------------------- |
| [SDL_Window](SDL_Window) * | **window** | the window for which screen keyboard should be queried. |

## Return Value

(bool) Returns true if screen keyboard is shown or false if not.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_HasScreenKeyboardSupport](SDL_HasScreenKeyboardSupport)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryKeyboard](CategoryKeyboard)

