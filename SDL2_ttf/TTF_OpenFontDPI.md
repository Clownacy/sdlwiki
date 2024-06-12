###### (This function is part of SDL_ttf, a separate library from SDL.)
# TTF_OpenFontDPI

Create a font from a file, using target resolutions (in DPI).

## Header File

Defined in [<SDL_ttf.h>](https://github.com/libsdl-org/SDL_ttf/blob/SDL2/include/SDL_ttf.h)

## Syntax

```c
TTF_Font * TTF_OpenFontDPI(const char *file, int ptsize, unsigned int hdpi, unsigned int vdpi);
```

## Function Parameters

|              |            |                                              |
| ------------ | ---------- | -------------------------------------------- |
| const char * | **file**   | path to font file.                           |
| int          | **ptsize** | point size to use for the newly-opened font. |
| unsigned int | **hdpi**   | the target horizontal DPI.                   |
| unsigned int | **vdpi**   | the target vertical DPI.                     |

## Return Value

([TTF_Font](TTF_Font) *) Returns a valid [TTF_Font](TTF_Font), or NULL on
error.

## Remarks

DPI scaling only applies to scalable fonts (e.g. TrueType).

Some .fon fonts will have several sizes embedded in the file, so the point
size becomes the index of choosing which size. If the value is too high,
the last indexed size will be the default.

When done with the returned [TTF_Font](TTF_Font), use
[TTF_CloseFont](TTF_CloseFont)() to dispose of it.

## Version

This function is available since SDL_ttf 2.0.18.

## See Also

- [TTF_CloseFont](TTF_CloseFont)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

