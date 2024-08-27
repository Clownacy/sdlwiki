###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_PutAudioStreamData

Add data to the stream.

## Header File

Defined in [<SDL3/SDL_audio.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_audio.h)

## Syntax

```c
SDL_bool SDL_PutAudioStreamData(SDL_AudioStream *stream, const void *buf, int len);
```

## Function Parameters

|                                      |            |                                              |
| ------------------------------------ | ---------- | -------------------------------------------- |
| [SDL_AudioStream](SDL_AudioStream) * | **stream** | the stream the audio data is being added to. |
| const void *                         | **buf**    | a pointer to the audio data to add.          |
| int                                  | **len**    | the number of bytes to write to the stream.  |

## Return Value

([SDL_bool](SDL_bool)) Returns [SDL_TRUE](SDL_TRUE) on success or
[SDL_FALSE](SDL_FALSE) on failure; call [SDL_GetError](SDL_GetError)() for
more information.

## Remarks

This data must match the format/channels/samplerate specified in the latest
call to [SDL_SetAudioStreamFormat](SDL_SetAudioStreamFormat), or the format
specified when creating the stream if it hasn't been changed.

Note that this call simply copies the unconverted data for later. This is
different than SDL2, where data was converted during the Put call and the
Get call would just dequeue the previously-converted data.

## Thread Safety

It is safe to call this function from any thread, but if the stream has a
callback set, the caller might need to manage extra locking.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_ClearAudioStream](SDL_ClearAudioStream)
- [SDL_FlushAudioStream](SDL_FlushAudioStream)
- [SDL_GetAudioStreamData](SDL_GetAudioStreamData)
- [SDL_GetAudioStreamQueued](SDL_GetAudioStreamQueued)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryAudio](CategoryAudio)

