###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_GPUComputePass

An opaque handle representing a compute pass.

## Header File

Defined in [<SDL3/SDL_gpu.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gpu.h)

## Syntax

```c
typedef struct SDL_GPUComputePass SDL_GPUComputePass;
```

## Remarks

This handle is transient and should not be held or referenced after
[SDL_EndGPUComputePass](SDL_EndGPUComputePass) is called.

## Version

This struct is available since SDL 3.0.0

## See Also

- [SDL_BeginGPUComputePass](SDL_BeginGPUComputePass)
- [SDL_EndGPUComputePass](SDL_EndGPUComputePass)

----
[CategoryAPI](CategoryAPI), [CategoryAPIDatatype](CategoryAPIDatatype), [CategoryGPU](CategoryGPU)

