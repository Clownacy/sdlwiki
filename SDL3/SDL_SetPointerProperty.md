###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_SetPointerProperty

Set a pointer property in a group of properties.

## Header File

Defined in [<SDL3/SDL_properties.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_properties.h)

## Syntax

```c
SDL_bool SDL_SetPointerProperty(SDL_PropertiesID props, const char *name, void *value);
```

## Function Parameters

|                                      |           |                                                                |
| ------------------------------------ | --------- | -------------------------------------------------------------- |
| [SDL_PropertiesID](SDL_PropertiesID) | **props** | the properties to modify.                                      |
| const char *                         | **name**  | the name of the property to modify.                            |
| void *                               | **value** | the new value of the property, or NULL to delete the property. |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Thread Safety

It is safe to call this function from any thread.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_GetPointerProperty](SDL_GetPointerProperty)
- [SDL_HasProperty](SDL_HasProperty)
- [SDL_SetBooleanProperty](SDL_SetBooleanProperty)
- [SDL_SetFloatProperty](SDL_SetFloatProperty)
- [SDL_SetNumberProperty](SDL_SetNumberProperty)
- [SDL_SetPointerPropertyWithCleanup](SDL_SetPointerPropertyWithCleanup)
- [SDL_SetStringProperty](SDL_SetStringProperty)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryProperties](CategoryProperties)

