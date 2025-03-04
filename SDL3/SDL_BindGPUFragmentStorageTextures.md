###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_BindGPUFragmentStorageTextures

Binds storage textures for use on the fragment shader.

## Header File

Defined in [<SDL3/SDL_gpu.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_gpu.h)

## Syntax

```c
void SDL_BindGPUFragmentStorageTextures(
    SDL_GPURenderPass *render_pass,
    Uint32 first_slot,
    SDL_GPUTexture *const *storage_textures,
    Uint32 num_bindings);
```

## Function Parameters

|                                           |                      |                                                          |
| ----------------------------------------- | -------------------- | -------------------------------------------------------- |
| [SDL_GPURenderPass](SDL_GPURenderPass) *  | **render_pass**      | a render pass handle.                                    |
| Uint32                                    | **first_slot**       | the fragment storage texture slot to begin binding from. |
| [SDL_GPUTexture](SDL_GPUTexture) *const * | **storage_textures** | an array of storage textures.                            |
| Uint32                                    | **num_bindings**     | the number of storage textures to bind from the array.   |

## Remarks

These textures must have been created with
[SDL_GPU_TEXTUREUSAGE_GRAPHICS_STORAGE_READ](SDL_GPU_TEXTUREUSAGE_GRAPHICS_STORAGE_READ).

## Version

This function is available since SDL 3.0.0.

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryGPU](CategoryGPU)

