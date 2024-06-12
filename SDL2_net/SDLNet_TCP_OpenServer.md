###### (This function is part of SDL_net, a separate library from SDL.)
# SDLNet_TCP_OpenServer

Open a server TCP network socket.

## Header File

Defined in [<SDL_net.h>](https://github.com/libsdl-org/SDL_net/blob/SDL2/include/SDL_net.h)

## Syntax

```c
TCPsocket SDLNet_TCP_OpenServer(IPaddress *ip);
```

## Function Parameters

|             |        |                                  |
| ----------- | ------ | -------------------------------- |
| IPaddress * | **ip** | The address to host a server on. |

## Return Value

(TCPsocket) Returns the newly created socket, or NULL if there was an
error.

## Remarks

If `ip->host` is INADDR_NONE or INADDR_ANY, the socket is bound to all
interfaces, otherwise it is bound to the specified interface. The address
passed in should already be swapped to network byte order (addresses
returned from [SDLNet_ResolveHost](SDLNet_ResolveHost)() are already in the
correct form).

## Version

This function is available since SDL_net 2.4.0.

## See Also

- [SDLNet_TCP_Close](SDLNet_TCP_Close)
- [SDLNet_TCP_OpenClient](SDLNet_TCP_OpenClient)
- [SDLNet_TCP_Open](SDLNet_TCP_Open)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

