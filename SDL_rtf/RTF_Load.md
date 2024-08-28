###### (This function is part of SDL_rtf, a separate library from SDL.)
# RTF_Load

Set the text of an RTF context, with data loaded from a filename.

## Header File

Defined in [<SDL3_rtf/SDL_rtf.h>](https://github.com/libsdl-org/SDL_rtf/blob/main/include/SDL3_rtf/SDL_rtf.h)

## Syntax

```c
SDL_bool RTF_Load(RTF_Context *ctx, const char *file);
```

## Function Parameters

|                              |          |                                      |
| ---------------------------- | -------- | ------------------------------------ |
| [RTF_Context](RTF_Context) * | **ctx**  | the RTF context to update.           |
| const char *                 | **file** | the file path to load RTF data from. |

## Return Value

(SDL_bool) Returns SDL_TRUE on success or SDL_FALSE on failure; call
SDL_GetError() for more information.

## Remarks

This can be called multiple times to change the text displayed.

On failure, call [RTF_GetError](RTF_GetError)() to get a human-readable
text message corresponding to the error.

## Version

This function is available since SDL_rtf 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

