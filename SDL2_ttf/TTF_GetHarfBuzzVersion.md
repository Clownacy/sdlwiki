###### (This function is part of SDL_ttf, a separate library from SDL.)
# TTF_GetHarfBuzzVersion

Query the version of the HarfBuzz library in use.

## Header File

Defined in [<SDL_ttf.h>](https://github.com/libsdl-org/SDL_ttf/blob/SDL2/include/SDL_ttf.h)

## Syntax

```c
void TTF_GetHarfBuzzVersion(int *major, int *minor, int *patch);
```

## Function Parameters

|       |           |                                                             |
| ----- | --------- | ----------------------------------------------------------- |
| int * | **major** | to be filled in with the major version number. Can be NULL. |
| int * | **minor** | to be filled in with the minor version number. Can be NULL. |
| int * | **patch** | to be filled in with the param version number. Can be NULL. |

## Remarks

If HarfBuzz is not available, the version reported is 0.0.0.

## Version

This function is available since SDL_ttf 2.0.18.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

