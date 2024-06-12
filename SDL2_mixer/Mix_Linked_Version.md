###### (This function is part of SDL_mixer, a separate library from SDL.)
# Mix_Linked_Version

Query the version of SDL_mixer that the program is linked against.

## Header File

Defined in [<SDL_mixer.h>](https://github.com/libsdl-org/SDL_mixer/blob/SDL2/include/SDL_mixer.h)

## Syntax

```c
const SDL_version * Mix_Linked_Version(void);
```

## Return Value

(const SDL_version *) Returns a pointer to the version information.

## Remarks

This function gets the version of the dynamically linked SDL_mixer library.
This is separate from the SDL_MIXER_VERSION() macro, which tells you what
version of the SDL_mixer headers you compiled against.

This returns static internal data; do not free or modify it!

## Version

This function is available since SDL_mixer 2.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

