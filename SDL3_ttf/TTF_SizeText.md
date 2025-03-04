###### (This function is part of SDL_ttf, a separate library from SDL.)
# TTF_SizeText

Calculate the dimensions of a rendered string of Latin1 text.

## Header File

Defined in [<SDL3_ttf/SDL_ttf.h>](https://github.com/libsdl-org/SDL_ttf/blob/main/include/SDL3_ttf/SDL_ttf.h)

## Syntax

```c
bool TTF_SizeText(TTF_Font *font, const char *text, int *w, int *h);
```

## Function Parameters

|                        |          |                                                   |
| ---------------------- | -------- | ------------------------------------------------- |
| [TTF_Font](TTF_Font) * | **font** | the font to query.                                |
| const char *           | **text** | text to calculate, in Latin1 encoding.            |
| int *                  | **w**    | will be filled with width, in pixels, on return.  |
| int *                  | **h**    | will be filled with height, in pixels, on return. |

## Return Value

(bool) Returns true on success or false on failure; call SDL_GetError() for
more information.

## Remarks

This will report the width and height, in pixels, of the space that the
specified string will take to fully render.

This does not need to render the string to do this calculation.

You almost certainly want [TTF_SizeUTF8](TTF_SizeUTF8)() unless you're sure
you have a 1-byte Latin1 encoding. US ASCII characters will work with
either function, but most other Unicode characters packed into a `const
char *` will need UTF-8.

## Version

This function is available since SDL_ttf 3.0.0.

## See Also

- [TTF_SizeUTF8](TTF_SizeUTF8)
- [TTF_SizeUNICODE](TTF_SizeUNICODE)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

