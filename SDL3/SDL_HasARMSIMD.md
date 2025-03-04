###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_HasARMSIMD

Determine whether the CPU has ARM SIMD (ARMv6) features.

## Header File

Defined in [<SDL3/SDL_cpuinfo.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_cpuinfo.h)

## Syntax

```c
bool SDL_HasARMSIMD(void);
```

## Return Value

(bool) Returns true if the CPU has ARM SIMD features or false if not.

## Remarks

This is different from ARM NEON, which is a different instruction set.

This always returns false on CPUs that aren't using ARM instruction sets.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_HasNEON](SDL_HasNEON)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryCPUInfo](CategoryCPUInfo)

