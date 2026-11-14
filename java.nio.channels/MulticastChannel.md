# MulticastChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MulticastChannel

```
interface MulticastChannel : NetworkChannel
```

| [java.nio.channels.MulticastChannel](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#) |

| Known Direct Subclasses [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) |-----------------------------------------------------------------------------------------------------|-----------------------------------------------------| | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. | |
| --- | --- | --- | --- | --- | --- | --- |

A network channel that supports Internet Protocol (IP) multicasting.

IP multicasting is the transmission of IP datagrams to members of a*group*that is zero or more hosts identified by a single destination address.

In the case of a channel to an [IPv4](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily.html#) socket, the underlying operating system optionally supports [*RFC 2236: Internet Group Management Protocol, Version 2 (IGMPv2)*](http://www.ietf.org/rfc/rfc2236.txt). When IGMPv2 is supported then the operating system may additionally support source filtering as specified by [*RFC 3376: Internet Group Management Protocol, Version 3 (IGMPv3)*](http://www.ietf.org/rfc/rfc3376.txt). For channels to an [IPv6](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily.html#) socket, the equivalent standards are [*RFC 2710: Multicast Listener Discovery (MLD) for IPv6*](http://www.ietf.org/rfc/rfc2710.txt) and [*RFC 3810: Multicast Listener Discovery Version 2 (MLDv2) for IPv6*](http://www.ietf.org/rfc/rfc3810.txt).

The [join(java.net.InetAddress,java.net.NetworkInterface)](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#join(java.net.InetAddress,%20java.net.NetworkInterface))method is used to join a group and receive all multicast datagrams sent to the group. A channel may join several multicast groups and may join the same group on several [interfaces](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#). Membership is dropped by invoking the [drop](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#drop())method on the returned [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey). If the underlying platform supports source filtering then the [block](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#block(java.net.InetAddress))and [unblock](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#unblock(java.net.InetAddress))methods can be used to block or unblock multicast datagrams from particular source addresses.

The [join(java.net.InetAddress,java.net.NetworkInterface,java.net.InetAddress)](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#join(java.net.InetAddress,%20java.net.NetworkInterface,%20java.net.InetAddress))method is used to begin receiving datagrams sent to a group whose source address matches a given source address. This method throws [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) if the underlying platform does not support source filtering. Membership is*cumulative* and this method may be invoked again with the same group and interface to allow receiving datagrams from other source addresses. The method returns a [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey) that represents membership to receive datagrams from the given source address. Invoking the key's [drop](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#drop())method drops membership so that datagrams from the source address can no longer be received.

## Platform dependencies

The multicast implementation is intended to map directly to the native multicasting facility. Consequently, the following items should be considered when developing an application that receives IP multicast datagrams:

1. The creation of the channel should specify the [ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily.html#) that corresponds to the address type of the multicast groups that the channel will join. There is no guarantee that a channel to a socket in one protocol family can join and receive multicast datagrams when the address of the multicast group corresponds to another protocol family. For example, it is implementation specific if a channel to an [IPv6](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily.html#) socket can join an [IPv4](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily.html#) multicast group and receive multicast datagrams sent to the group.
2. The channel's socket should be bound to the [wildcard](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#isAnyLocalAddress())address. If the socket is bound to a specific address, rather than the wildcard address then it is implementation specific if multicast datagrams are received by the socket.
3. The [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_REUSEADDR:java.net.SocketOption) option should be enabled prior to [binding](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))the socket. This is required to allow multiple members of the group to bind to the same address.

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
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#close())`()` Closes this channel. |
| abstract [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey)! | [join](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#join(java.net.InetAddress,%20java.net.NetworkInterface))`(`group:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `interf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)!`)` Joins a multicast group to begin receiving all datagrams sent to the group, returning a membership key. |
| abstract [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey)! | [join](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#join(java.net.InetAddress,%20java.net.NetworkInterface,%20java.net.InetAddress))`(`group:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `interf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)!`, `source:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Joins a multicast group to begin receiving datagrams sent to the group from a given source address. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` <br /> Binds the channel's socket to a local address. This method is used to establish an association between the socket and a local address. Once an association is established then the socket remains bound until the channel is closed. If the`local`parameter has the value`null`then the socket will be bound to an address that is assigned automatically. <br /> | | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getLocalAddress())`()` <br /> Returns the socket address that this channel's socket is bound to. Where the channel is [bound](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))to an Internet Protocol socket address then the return value from this method is of type . <br /> | | T | [getOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel)! | [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#setOption(java.net.SocketOption,%20java.nio.channels.NetworkChannel.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`, `value:` `T`)` <br /> Sets the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<*>!>! | [supportedOptions](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#supportedOptions())`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close())`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this channel.

If the channel is a member of a multicast group then the membership is [dropped](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#drop()). Upon return, the [membership-key](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey) will be [invalid](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#isValid()).

This method otherwise behaves exactly as specified by the [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) interface.

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

If this channel is currently a member of the group on the given interface to receive all datagrams then the membership key, representing that membership, is returned. Otherwise this channel joins the group and the resulting new membership key is returned. The resulting membership key is not [source-specific](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#sourceAddress()).

A multicast channel may join several multicast groups, including the same group on more than one interface. An implementation may impose a limit on the number of groups that may be joined at the same time.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The multicast address to join |
| `interf` | [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)!:The network interface on which to join the group |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey)! | The membership key |

| Exceptions ||
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the group parameter is not a [multicast](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#isMulticastAddress())address, or the group parameter is an address type that is not supported by this channel |
| `java.lang.IllegalStateException` | If the channel already has source-specific membership of the group on the interface |
| `java.lang.UnsupportedOperationException` | If the channel's socket is not an Internet Protocol socket, or the platform does not support multicasting |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is set, and its [checkMulticast](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress))method denies access to the multiast group |
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

If this channel is currently a member of the group on the given interface to receive datagrams from the given source address then the membership key, representing that membership, is returned. Otherwise this channel joins the group and the resulting new membership key is returned. The resulting membership key is [source-specific](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#sourceAddress()).

Membership is*cumulative*and this method may be invoked again with the same group and interface to allow receiving datagrams sent by other source addresses to the group.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `group` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The multicast address to join |
| `interf` | [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)!:The network interface on which to join the group |
| `source` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!:The source address |
| --- | --- |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------|
| [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey)! | The membership key |

| Exceptions ||
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If the group parameter is not a [multicast](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#isMulticastAddress())address, the source parameter is not a unicast address, the group parameter is an address type that is not supported by this channel, or the source parameter is not the same address type as the group |
| `java.lang.IllegalStateException` | If the channel is currently a member of the group on the given interface to receive all datagrams |
| `java.lang.UnsupportedOperationException` | If the channel's socket is not an Internet Protocol socket, or source filtering is not supported, or the platform does not support multicasting |
| --- | --- |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |
| `java.lang.SecurityException` | If a security manager is set, and its [checkMulticast](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress))method denies access to the multiast group |
| --- | --- |
