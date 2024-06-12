###### (This function is part of SDL_mixer, a separate library from SDL.)
# Mix_LoadWAV_RW

Load a supported audio format into a chunk.

## Header File

Defined in [<SDL_mixer.h>](https://github.com/libsdl-org/SDL_mixer/blob/SDL2/include/SDL_mixer.h)

## Syntax

```c
Mix_Chunk * Mix_LoadWAV_RW(SDL_RWops *src, int freesrc);
```

## Function Parameters

|             |             |                                                                               |
| ----------- | ----------- | ----------------------------------------------------------------------------- |
| SDL_RWops * | **src**     | an SDL_RWops that data will be read from.                                     |
| int         | **freesrc** | non-zero to close/free the SDL_RWops before returning, zero to leave it open. |

## Return Value

([Mix_Chunk](Mix_Chunk) *) Returns a new chunk, or NULL on error.

## Remarks

SDL_mixer has two separate data structures for audio data. One it calls a
"chunk," which is meant to be a file completely decoded into memory up
front, and the other it calls "music" which is a file intended to be
decoded on demand. Originally, simple formats like uncompressed WAV files
were meant to be chunks and compressed things, like MP3s, were meant to be
music, and you would stream one thing for a game's music and make repeating
sound effects with the chunks.

In modern times, this isn't split by format anymore, and most are
interchangeable, so the question is what the app thinks is worth
predecoding or not. Chunks might take more memory, but once they are loaded
won't need to decode again, whereas music always needs to be decoded on the
fly. Also, crucially, there are as many channels for chunks as the app can
allocate, but SDL_mixer only offers a single "music" channel.

If `freesrc` is non-zero, the RWops will be closed before returning,
whether this function succeeds or not. SDL_mixer reads everything it needs
from the RWops during this call in any case.

There is a separate function (a macro, before SDL_mixer 2.6.0) to read
files from disk without having to deal with SDL_RWops:
`Mix_LoadWAV("filename.wav")` will call this function and manage those
details for you.

When done with a chunk, the app should dispose of it with a call to
[Mix_FreeChunk](Mix_FreeChunk)().

## Version

This function is available since SDL_mixer 2.6.0 (and as a macro since
2.0.0).

## See Also

- [Mix_LoadWAV](Mix_LoadWAV)
- [Mix_FreeChunk](Mix_FreeChunk)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

