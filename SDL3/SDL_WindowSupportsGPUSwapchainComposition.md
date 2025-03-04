###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_WindowSupportsGPUSwapchainComposition

Determines whether a swapchain composition is supported by the window.

## Header File

Defined in [<SDL3/SDL_gpu.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gpu.h)

## Syntax

```c
bool SDL_WindowSupportsGPUSwapchainComposition(
    SDL_GPUDevice *device,
    SDL_Window *window,
    SDL_GPUSwapchainComposition swapchain_composition);
```

## Function Parameters

|                                                            |                           |                                     |
| ---------------------------------------------------------- | ------------------------- | ----------------------------------- |
| [SDL_GPUDevice](SDL_GPUDevice) *                           | **device**                | a GPU context.                      |
| [SDL_Window](SDL_Window) *                                 | **window**                | an [SDL_Window](SDL_Window).        |
| [SDL_GPUSwapchainComposition](SDL_GPUSwapchainComposition) | **swapchain_composition** | the swapchain composition to check. |

## Return Value

(bool) Returns true if supported, false if unsupported (or on error).

## Remarks

The window must be claimed before calling this function.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_ClaimWindowForGPUDevice](SDL_ClaimWindowForGPUDevice)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryGPU](CategoryGPU)

