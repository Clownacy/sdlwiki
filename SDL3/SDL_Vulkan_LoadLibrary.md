###### (This is the documentation for SDL3, which is under heavy development and the API is changing! [SDL2](https://wiki.libsdl.org/SDL2/) is the current stable version!)
# SDL_Vulkan_LoadLibrary

Dynamically load the Vulkan loader library.

## Header File

Defined in [<SDL3/SDL_vulkan.h>](https://github.com/libsdl-org/SDL/blob/main/include/SDL3/SDL_vulkan.h)

## Syntax

```c
bool SDL_Vulkan_LoadLibrary(const char *path);
```

## Function Parameters

|              |          |                                                            |
| ------------ | -------- | ---------------------------------------------------------- |
| const char * | **path** | the platform dependent Vulkan loader library name or NULL. |

## Return Value

(bool) Returns true on success or false on failure; call
[SDL_GetError](SDL_GetError)() for more information.

## Remarks

This should be called after initializing the video driver, but before
creating any Vulkan windows. If no Vulkan loader library is loaded, the
default library will be loaded upon creation of the first Vulkan window.

It is fairly common for Vulkan applications to link with libvulkan instead
of explicitly loading it at run time. This will work with SDL provided the
application links to a dynamic library and both it and SDL use the same
search path.

If you specify a non-NULL `path`, an application should retrieve all of the
Vulkan functions it uses from the dynamic library using
[SDL_Vulkan_GetVkGetInstanceProcAddr](SDL_Vulkan_GetVkGetInstanceProcAddr)
unless you can guarantee `path` points to the same vulkan loader library
the application linked to.

On Apple devices, if `path` is NULL, SDL will attempt to find the
`vkGetInstanceProcAddr` address within all the Mach-O images of the current
process. This is because it is fairly common for Vulkan applications to
link with libvulkan (and historically MoltenVK was provided as a static
library). If it is not found, on macOS, SDL will attempt to load
`vulkan.framework/vulkan`, `libvulkan.1.dylib`,
`MoltenVK.framework/MoltenVK`, and `libMoltenVK.dylib`, in that order. On
iOS, SDL will attempt to load `libMoltenVK.dylib`. Applications using a
dynamic framework or .dylib must ensure it is included in its application
bundle.

On non-Apple devices, application linking with a static libvulkan is not
supported. Either do not link to the Vulkan loader or link to a dynamic
library version.

## Version

This function is available since SDL 3.0.0.

## See Also

- [SDL_Vulkan_GetVkGetInstanceProcAddr](SDL_Vulkan_GetVkGetInstanceProcAddr)
- [SDL_Vulkan_UnloadLibrary](SDL_Vulkan_UnloadLibrary)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction), [CategoryVulkan](CategoryVulkan)

