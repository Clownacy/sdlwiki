###### (This function is part of SDL_ttf, a separate library from SDL.)
# TTF_MeasureText

Calculate how much of a Latin1 string will fit in a given width.

## Header File

Defined in [<SDL3_ttf/SDL_ttf.h>](https://github.com/libsdl-org/SDL_ttf/blob/main/include/SDL3_ttf/SDL_ttf.h)

## Syntax

```c
SDL_bool TTF_MeasureText(TTF_Font *font, const char *text, int measure_width, int *extent, int *count);
```

## Function Parameters

|                        |                   |                                                                   |
| ---------------------- | ----------------- | ----------------------------------------------------------------- |
| [TTF_Font](TTF_Font) * | **font**          | the font to query.                                                |
| const char *           | **text**          | text to calculate, in Latin1 encoding.                            |
| int                    | **measure_width** | maximum width, in pixels, available for the string.               |
| int *                  | **extent**        | on return, filled with latest calculated width.                   |
| int *                  | **count**         | on return, filled with number of characters that can be rendered. |

## Return Value

(SDL_bool) Returns SDL_TRUE on success or SDL_FALSE on failure; call
SDL_GetError() for more information.

## Remarks

This reports the number of characters that can be rendered before reaching
`measure_width`.

This does not need to render the string to do this calculation.

You almost certainly want [TTF_MeasureUTF8](TTF_MeasureUTF8)() unless
you're sure you have a 1-byte Latin1 encoding. US ASCII characters will
work with either function, but most other Unicode characters packed into a
`const char *` will need UTF-8.

## Version

This function is available since SDL_ttf 3.0.0.

## See Also

- [TTF_MeasureText](TTF_MeasureText)
- [TTF_MeasureUTF8](TTF_MeasureUTF8)
- [TTF_MeasureUNICODE](TTF_MeasureUNICODE)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

