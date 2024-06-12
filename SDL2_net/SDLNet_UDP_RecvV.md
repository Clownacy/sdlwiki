###### (This function is part of SDL_net, a separate library from SDL.)
# SDLNet_UDP_RecvV

Receive a vector of pending packets from a UDP socket.

## Header File

Defined in [<SDL_net.h>](https://github.com/libsdl-org/SDL_net/blob/SDL2/include/SDL_net.h)

## Syntax

```c
int SDLNet_UDP_RecvV(UDPsocket sock, UDPpacket **packets);
```

## Function Parameters

|              |             |                                       |
| ------------ | ----------- | ------------------------------------- |
| UDPsocket    | **sock**    | the UDP socket to receive packets on. |
| UDPpacket ** | **packets** | an array of packets, NULL terminated. |

## Return Value

(int) Returns the number of packets read from the network, or -1 on error.
0 means no packets were currently available.

## Remarks

The returned packets contain the source address and the channel they
arrived on. If they did not arrive on a bound channel, the the channel will
be set to -1.

The channels are checked in highest to lowest order, so if an address is
bound to multiple channels, the highest channel with the source address
bound will be returned.

This function takes an array of packets but does not need to be allocated
through [SDLNet_AllocPacketV](SDLNet_AllocPacketV); if you supply your own
array of packets you allocated individually, that is okay, as long as the
last element in the array is NULL, so SDL_net knows the array bounds. The
arrays returned by [SDLNet_AllocPacketV](SDLNet_AllocPacketV) are properly
NULL-terminated for these purposes.

This function does not block, so it can return 0 packets pending, which is
not an error condition.

## Version

This function is available since SDL_net 2.0.0.

## See Also

- [SDLNet_UDP_SendV](SDLNet_UDP_SendV)
- [SDLNet_UDP_Recv](SDLNet_UDP_Recv)

----
[CategoryAPI](CategoryAPI), [CategoryAPIFunction](CategoryAPIFunction)

