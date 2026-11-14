# MulticastChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MulticastChannel

```
interface MulticastChannel : NetworkChannel
```

| [java.nio.channels.MulticastChannel](../java/nio/channels/MulticastChannel.md) |

| Known Direct Subclasses [DatagramChannel](../java/nio/channels/DatagramChannel.md) |-----------------------------------------------------------------------------------------------------|-----------------------------------------------------| | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | |
| --- | --- | --- | --- | --- | --- | --- |

A network channel that supports Internet Protocol (IP) multicasting.

IP multicasting is the transmission of IP datagrams to members of a*group*that is zero or more hosts identified by a single destination address.

In the case of a channel to an [IPv4](../java/net/StandardProtocolFamily.md) socket, the underlying operating system optionally supports [*RFC 2236: Internet Group Management Protocol, Version 2 (IGMPv2)*](http://www.ietf.org/rfc/rfc2236.txt). When IGMPv2 is supported then the operating system may additionally support source filtering as specified by [*RFC 3376: Internet Group Management Protocol, Version 3 (IGMPv3)*](http://www.ietf.org/rfc/rfc3376.txt). For channels to an [IPv6](../java/net/StandardProtocolFamily.md) socket, the equivalent standards are [*RFC 2710: Multicast Listener Discovery (MLD) for IPv6*](http://www.ietf.org/rfc/rfc2710.txt) and [*RFC 3810: Multicast Listener Discovery Version 2 (MLDv2) for IPv6*](http://www.ietf.org/rfc/rfc3810.txt).

The [join(java.net.InetAddress,java.net.NetworkInterface)](../java/nio/channels/MulticastChannel.md))method is used to join a group and receive all multicast datagrams sent to the group. A channel may join several multicast groups and may join the same group on several [interfaces](../java/net/NetworkInterface.md). Membership is dropped by invoking the [drop](../java/nio/channels/MembershipKey.md))method on the returned [MembershipKey](../java/nio/channels/MembershipKey.md). If the underlying platform supports source filtering then the [block](../java/nio/channels/MembershipKey.md))and [unblock](../java/nio/channels/MembershipKey.md))methods can be used to block or unblock multicast datagrams from particular source addresses.

The [join(java.net.InetAddress,java.net.NetworkInterface,java.net.InetAddress)](../java/nio/channels/MulticastChannel.md))method is used to begin receiving datagrams sent to a group whose source address matches a given source address. This method throws [UnsupportedOperationException](../java/lang/UnsupportedOperationException.md) if the underlying platform does not support source filtering. Membership is*cumulative* and this method may be invoked again with the same group and interface to allow receiving datagrams from other source addresses. The method returns a [MembershipKey](../java/nio/channels/MembershipKey.md) that represents membership to receive datagrams from the given source address. Invoking the key's [drop](../java/nio/channels/MembershipKey.md))method drops membership so that datagrams from the source address can no longer be received.

## Platform dependencies

The multicast implementation is intended to map directly to the native multicasting facility. Consequently, the following items should be considered when developing an application that receives IP multicast datagrams:

1. The creation of the channel should specify the [ProtocolFamily](../java/net/ProtocolFamily.md) that corresponds to the address type of the multicast groups that the channel will join. There is no guarantee that a channel to a socket in one protocol family can join and receive multicast datagrams when the address of the multicast group corresponds to another protocol family. For example, it is implementation specific if a channel to an [IPv6](../java/net/StandardProtocolFamily.md) socket can join an [IPv4](../java/net/StandardProtocolFamily.md) multicast group and receive multicast datagrams sent to the group.
2. The channel's socket should be bound to the [wildcard](../java/net/InetAddress.md))address. If the socket is bound to a specific address, rather than the wildcard address then it is implementation specific if multicast datagrams are received by the socket.
3. The [SO_REUSEADDR](../java/net/StandardSocketOptions.md) option should be enabled prior to [binding](../java/nio/channels/NetworkChannel.md))the socket. This is required to allow multiple members of the group to bind to the same address.

**Usage Example:** 

```kotlin
// join multicast group on this interface, and also use this
      // interface for outgoing multicast datagrams
      NetworkInterface ni = NetworkInterface.getByName("hme0");
 
      DatagramChannel dc = DatagramChannel.open(StandardProtocolFamily.INET)
          .setOption(StandardSocketOptions.SO_REUSEADDR, true)
          .bind(new InetSocketAddress(5000))
          .setOption(StandardSocketOptions.IP_MULTICAST_IF, ni);
 
      InetAddress group = InetAddress.getByName("225.4.5.6");
 
      MembershipKey key = dc.join(group, ni);
  
```

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/MulticastChannel.md))`()` Closes this channel. |
| abstract [MembershipKey](../java/nio/channels/MembershipKey.md)! | [join](../java/nio/channels/MulticastChannel.md))`(`group:` ` [InetAddress](../java/net/InetAddress.md)!`, `interf:` ` [NetworkInterface](../java/net/NetworkInterface.md)!`)` Joins a multicast group to begin receiving all datagrams sent to the group, returning a membership key. |
| abstract [MembershipKey](../java/nio/channels/MembershipKey.md)! | [join](../java/nio/channels/MulticastChannel.md))`(`group:` ` [InetAddress](../java/net/InetAddress.md)!`, `interf:` ` [NetworkInterface](../java/net/NetworkInterface.md)!`, `source:` ` [InetAddress](../java/net/InetAddress.md)!`)` Joins a multicast group to begin receiving datagrams sent to the group from a given source address. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [NetworkChannel](../java/nio/channels/NetworkChannel.md) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NetworkChannel](../java/nio/channels/NetworkChannel.md)! | [bind](../java/nio/channels/NetworkChannel.md))`(`local:` ` [SocketAddress](../java/net/SocketAddress.md)!`)` <br /> Binds the channel's socket to a local address. This method is used to establish an association between the socket and a local address. Once an association is established then the socket remains bound until the channel is closed. If the`local`parameter has the value`null`then the socket will be bound to an address that is assigned automatically. <br /> | | [SocketAddress](../java/net/SocketAddress.md)! | [getLocalAddress](../java/nio/channels/NetworkChannel.md))`()` <br /> Returns the socket address that this channel's socket is bound to. Where the channel is [bound](../java/nio/channels/NetworkChannel.md))to an Internet Protocol socket address then the return value from this method is of type . <br /> | | T | [getOption](../java/nio/channels/NetworkChannel.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [NetworkChannel](../java/nio/channels/NetworkChannel.md)! | [setOption](../java/nio/channels/NetworkChannel.md))`(`name:` ` [SocketOption](../java/net/SocketOption.md)<T>!`, `value:` `T`)` <br /> Sets the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](../java/net/SocketOption.md)<*>!>! | [supportedOptions](../java/nio/channels/NetworkChannel.md))`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/Channel.md))`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](../java/nio/channels/ClosedChannelException.md) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this channel.

If the channel is a member of a multicast group then the membership is [dropped](../java/nio/channels/MembershipKey.md)). Upon return, the [membership-key](../java/nio/channels/MembershipKey.md) will be [invalid](../java/nio/channels/MembershipKey.md)).

This method otherwise behaves exactly as specified by the [Channel](../java/nio/channels/Channel.md) interface.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### join

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun join(
    group: InetAddress!, 
    interf: NetworkInterface!
): MembershipKey!
```

Joins a multicast group to begin receiving all datagrams sent to the group, returning a membership key.

If this channel is currently a member of the group on the given interface to receive all datagrams then the membership key, representing that membership, is returned. Otherwise this channel joins the group and the resulting new membership key is returned. The resulting membership key is not [source-specific](../java/nio/channels/MembershipKey.md)).

A multicast channel may join several multicast groups, including the same group on more than one interface. An implementation may impose a limit on the number of groups that may be joined at the same time.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [InetAddress](../java/net/InetAddress.md)!:The multicast address to join |
| `interf` | [NetworkInterface](../java/net/NetworkInterface.md)!:The network interface on which to join the group |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MembershipKey](../java/nio/channels/MembershipKey.md)! | The membership key |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the group parameter is not a [multicast](../java/net/InetAddress.md))address, or the group parameter is an address type that is not supported by this channel |
| `java.lang.IllegalStateException` | If the channel already has source-specific membership of the group on the interface |
| `java.lang.UnsupportedOperationException` | If the channel's socket is not an Internet Protocol socket, or the platform does not support multicasting |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is set, and its [checkMulticast](../java/lang/SecurityManager.md))method denies access to the multiast group |
| --- | --- |

### join

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun join(
    group: InetAddress!, 
    interf: NetworkInterface!, 
    source: InetAddress!
): MembershipKey!
```

Joins a multicast group to begin receiving datagrams sent to the group from a given source address.

If this channel is currently a member of the group on the given interface to receive datagrams from the given source address then the membership key, representing that membership, is returned. Otherwise this channel joins the group and the resulting new membership key is returned. The resulting membership key is [source-specific](../java/nio/channels/MembershipKey.md)).

Membership is*cumulative*and this method may be invoked again with the same group and interface to allow receiving datagrams sent by other source addresses to the group.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [InetAddress](../java/net/InetAddress.md)!:The multicast address to join |
| `interf` | [NetworkInterface](../java/net/NetworkInterface.md)!:The network interface on which to join the group |
| `source` | [InetAddress](../java/net/InetAddress.md)!:The source address |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MembershipKey](../java/nio/channels/MembershipKey.md)! | The membership key |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the group parameter is not a [multicast](../java/net/InetAddress.md))address, the source parameter is not a unicast address, the group parameter is an address type that is not supported by this channel, or the source parameter is not the same address type as the group |
| `java.lang.IllegalStateException` | If the channel is currently a member of the group on the given interface to receive all datagrams |
| `java.lang.UnsupportedOperationException` | If the channel's socket is not an Internet Protocol socket, or source filtering is not supported, or the platform does not support multicasting |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is set, and its [checkMulticast](../java/lang/SecurityManager.md))method denies access to the multiast group |
| --- | --- |
