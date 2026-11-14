# DatagramChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramChannel

```
abstract class DatagramChannel : AbstractSelectableChannel, ByteChannel, GatheringByteChannel, MulticastChannel, ScatteringByteChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) ||||
| | ↳ | [java.nio.channels.SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) |||
| | | ↳ | [java.nio.channels.spi.AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) ||
| | | | ↳ | [java.nio.channels.DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#) |

A selectable channel for datagram-oriented sockets.

A datagram channel is created by invoking one of the #open methods of this class. It is not possible to create a channel for an arbitrary, pre-existing datagram socket. A newly-created datagram channel is open but not connected. A datagram channel need not be connected in order for the [send](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#send(java.nio.ByteBuffer,%20java.net.SocketAddress))and [receive](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#receive(java.nio.ByteBuffer))methods to be used. A datagram channel may be connected, by invoking its [connect](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#connect(java.net.SocketAddress))method, in order to avoid the overhead of the security checks are otherwise performed as part of every send and receive operation. A datagram channel must be connected in order to use the [read](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#read(java.nio.ByteBuffer))and [write](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#write(java.nio.ByteBuffer))methods, since those methods do not accept or return socket addresses.

Once connected, a datagram channel remains connected until it is disconnected or closed. Whether or not a datagram channel is connected may be determined by invoking its [isConnected](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#isConnected())method.

Socket options are configured using the [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#setOption(java.net.SocketOption,%20java.nio.channels.DatagramChannel.setOption.T))method. A datagram channel to an Internet Protocol socket supports the following options:

| Option Name | Description |
| [SO_SNDBUF](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_SNDBUF:java.net.SocketOption) | The size of the socket send buffer |
| [SO_RCVBUF](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_RCVBUF:java.net.SocketOption) | The size of the socket receive buffer |
| [SO_REUSEADDR](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_REUSEADDR:java.net.SocketOption) | Re-use address |
| [SO_BROADCAST](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#SO_BROADCAST:java.net.SocketOption) | Allow transmission of broadcast datagrams |
| [IP_TOS](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#IP_TOS:java.net.SocketOption) | The Type of Service (ToS) octet in the Internet Protocol (IP) header |
| [IP_MULTICAST_IF](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#IP_MULTICAST_IF:java.net.SocketOption) | The network interface for Internet Protocol (IP) multicast datagrams |
| [IP_MULTICAST_TTL](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#IP_MULTICAST_TTL:java.net.SocketOption) | The*time-to-live*for Internet Protocol (IP) multicast datagrams |
| [IP_MULTICAST_LOOP](https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions.html#IP_MULTICAST_LOOP:java.net.SocketOption) | Loopback for Internet Protocol (IP) multicast datagrams |
|-------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|

Additional (implementation specific) options may also be supported.

Datagram channels are safe for use by multiple concurrent threads. They support concurrent reading and writing, though at most one thread may be reading and at most one thread may be writing at any given time.

## Summary

| Protected constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#DatagramChannel(java.nio.channels.spi.SelectorProvider))`(`provider:` ` [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!`)` Initializes a new instance of this class. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#bind(java.net.SocketAddress))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` <br /> |
| abstract [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | [connect](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#connect(java.net.SocketAddress))`(`remote:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` Connects this channel's socket. |
| abstract [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | [disconnect](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#disconnect())`()` Disconnects this channel's socket. |
| abstract [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#getLocalAddress())`()` Returns the socket address that this channel's socket is bound to. |
| abstract [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getRemoteAddress](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#getRemoteAddress())`()` Returns the remote address to which this channel's socket is connected. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#isConnected())`()` Tells whether or not this channel's socket is connected. |
| openstatic [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#open())`()` Opens a datagram channel. |
| openstatic [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#open(java.net.ProtocolFamily))`(`family:` ` [ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily.html#)!`)` Opens a datagram channel. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#read(java.nio.ByteBuffer))`(`dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Reads a datagram from this channel. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#read(kotlin.Array))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`)` Reads a datagram from this channel. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#read(kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads a datagram from this channel. |
| abstract [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [receive](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#receive(java.nio.ByteBuffer))`(`dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Receives a datagram via this channel. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [send](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#send(java.nio.ByteBuffer,%20java.net.SocketAddress))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`, `target:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` Sends a datagram via this channel. |
| abstract [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#setOption(java.net.SocketOption,%20java.nio.channels.DatagramChannel.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`, `value:` `T`)` <br /> |
| abstract [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)! | [socket](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#socket())`()` Retrieves a datagram socket associated with this channel. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#validOps())`()` Returns an operation set identifying this channel's supported operations. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#write(java.nio.ByteBuffer))`(`src:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Writes a datagram to this channel. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#write(kotlin.Array))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`)` Writes a datagram to this channel. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#write(kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a datagram to this channel. |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#close())`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())`()` <br /> | ||
| From class [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel)! | [bind](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))`(`local:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!`)` <br /> Binds the channel's socket to a local address. This method is used to establish an association between the socket and a local address. Once an association is established then the socket remains bound until the channel is closed. If the`local`parameter has the value`null`then the socket will be bound to an address that is assigned automatically. <br /> | | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | [getLocalAddress](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getLocalAddress())`()` <br /> Returns the socket address that this channel's socket is bound to. Where the channel is [bound](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))to an Internet Protocol socket address then the return value from this method is of type . <br /> | | T | [getOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#getOption(java.net.SocketOption))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [NetworkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel)! | [setOption](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#setOption(java.net.SocketOption,%20java.nio.channels.NetworkChannel.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<T>!`, `value:` `T`)` <br /> Sets the value of a socket option. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)<*>!>! | [supportedOptions](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#supportedOptions())`()` <br /> Returns a set of the socket options supported by this channel. This method will continue to return the set of options even after the channel has been closed. <br /> | ||
| From class [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) |------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#blockingLock())`()` <br /> | | [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel)! | [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#configureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. If the given blocking mode is different from the current blocking mode then this method invokes the [implConfigureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implConfigureBlocking(kotlin.Boolean))method, while holding the appropriate locks, in order to change the mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseChannel())`()` <br /> Closes this channel. This method, which is specified in the [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) class and is invoked by the java.nio.channels.Channel#close method, in turn invokes the [implCloseSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseSelectableChannel())method in order to perform the actual work of closing this channel. It then cancels all of this channel's keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseSelectableChannel())`()` <br /> Closes this selectable channel. This method is invoked by the java.nio.channels.Channel#close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implConfigureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implConfigureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Adjusts this channel's blocking mode. This method is invoked by the [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#configureBlocking(kotlin.Boolean))method in order to perform the actual work of changing the blocking mode. This method is only invoked if the new mode is different from the current mode. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#isBlocking())`()` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#isRegistered())`()` <br /> | | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [keyFor](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#keyFor(java.nio.channels.Selector))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`)` <br /> | | [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#provider())`()` <br /> Returns the provider that created this channel. <br /> | | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Registers this channel with the given selector, returning a selection key. This method first verifies that this channel is open and that the given initial interest set is valid. If this channel is already registered with the given selector then the selection key representing that registration is returned after setting its interest set to the given value. Otherwise this channel has not yet been registered with the given selector, so the [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#register(java.nio.channels.spi.AbstractSelectableChannel,%20kotlin.Int,%20kotlin.Any))method of the selector is invoked while holding the appropriate locks. The resulting key is added to this channel's key set before being returned. <br /> | ||
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close())`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | ||
| From class [MulticastChannel](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel) |--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey)! | [join](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#join(java.net.InetAddress,%20java.net.NetworkInterface))`(`group:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `interf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)!`)` <br /> Joins a multicast group to begin receiving all datagrams sent to the group, returning a membership key. If this channel is currently a member of the group on the given interface to receive all datagrams then the membership key, representing that membership, is returned. Otherwise this channel joins the group and the resulting new membership key is returned. The resulting membership key is not [source-specific](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#sourceAddress()). A multicast channel may join several multicast groups, including the same group on more than one interface. An implementation may impose a limit on the number of groups that may be joined at the same time. <br /> | | [MembershipKey](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey)! | [join](https://developer.android.com/reference/kotlin/java/nio/channels/MulticastChannel#join(java.net.InetAddress,%20java.net.NetworkInterface,%20java.net.InetAddress))`(`group:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`, `interf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface.html#)!`, `source:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` <br /> Joins a multicast group to begin receiving datagrams sent to the group from a given source address. If this channel is currently a member of the group on the given interface to receive datagrams from the given source address then the membership key, representing that membership, is returned. Otherwise this channel joins the group and the resulting new membership key is returned. The resulting membership key is [source-specific](https://developer.android.com/reference/kotlin/java/nio/channels/MembershipKey#sourceAddress()). Membership is*cumulative*and this method may be invoked again with the same group and interface to allow receiving datagrams sent by other source addresses to the group. <br /> | ||
| From class [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) |------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Registers this channel with the given selector, returning a selection key. An invocation of this convenience method of the form `sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#validOps())`()` <br /> Returns an [operation set](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#opsets) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class. <br /> | ||

## Protected constructors

### DatagramChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected DatagramChannel(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!:The provider that created this channel |

## Public methods

### bind

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun bind(local: SocketAddress!): DatagramChannel!
```

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `local` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!:The address to bind the socket, or`null`to bind the socket to an automatically assigned socket address |

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | This channel |

| Exceptions ||
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyBoundException` | If the socket is already bound |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given address is not supported |
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If some other I/O error occurs |
| `java.lang.SecurityException` | If a security manager has been installed and its [checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))method denies the operation |

### connect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connect(remote: SocketAddress!): DatagramChannel!
```

Connects this channel's socket.

The channel's socket is configured so that it only receives datagrams from, and sends datagrams to, the given remote*peer*address. Once connected, datagrams may not be received from or sent to any other address. A datagram socket remains connected until it is explicitly disconnected or until it is closed.

This method performs exactly the same security checks as the java.net.DatagramSocket#connect method of the class. That is, if a security manager has been installed then this method verifies that its [checkAccept](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkAccept(kotlin.String,%20kotlin.Int))and java.lang.SecurityManager#checkConnect methods permit datagrams to be received from and sent to, respectively, the given remote address.

This method may be invoked at any time. It will not have any effect on read or write operations that are already in progress at the moment that it is invoked. If this channel's socket is not bound then this method will first cause the socket to be bound to an address that is assigned automatically, as if invoking the [bind](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#bind(java.net.SocketAddress))method with a parameter of`null`.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `remote` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!:The remote address to which this channel is to be connected |

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | This datagram channel |

| Exceptions ||
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyConnectedException` | If this channel is already connected |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the connect operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the connect operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.nio.channels.UnresolvedAddressException` | If the given remote address is not fully resolved |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given remote address is not supported |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit access to the given remote address |
| `java.io.IOException` | If some other I/O error occurs |

### disconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun disconnect(): DatagramChannel!
```

Disconnects this channel's socket.

The channel's socket is configured so that it can receive datagrams from, and sends datagrams to, any remote address so long as the security manager, if installed, permits it.

This method may be invoked at any time. It will not have any effect on read or write operations that are already in progress at the moment that it is invoked.

If this channel's socket is not connected, or if the channel is closed, then invoking this method has no effect.

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | This datagram channel |

| Exceptions ||
|-----------------------|--------------------------------|
| `java.io.IOException` | If some other I/O error occurs |

### getLocalAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getLocalAddress(): SocketAddress!
```

Returns the socket address that this channel's socket is bound to.

Where the channel is [bound](https://developer.android.com/reference/kotlin/java/nio/channels/NetworkChannel#bind(java.net.SocketAddress))to an Internet Protocol socket address then the return value from this method is of type .

If there is a security manager set, its`checkConnect`method is called with the local address and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, a`SocketAddress`representing the [loopback](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#getLoopbackAddress())address and the local port of the channel's socket is returned.

| Return ||
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | The`SocketAddress`that the socket is bound to, or the`SocketAddress`representing the loopback address if denied by the security manager, or`null`if the channel's socket is not bound |

| Exceptions ||
|--------------------------------------------|--------------------------|
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### getRemoteAddress

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRemoteAddress(): SocketAddress!
```

Returns the remote address to which this channel's socket is connected.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | The remote address;`null`if the channel's socket is not connected |

| Exceptions ||
|--------------------------------------------|--------------------------|
| `java.nio.channels.ClosedChannelException` | If the channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### isConnected

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isConnected(): Boolean
```

Tells whether or not this channel's socket is connected.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel's socket is [open](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())and connected |

### open

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(): DatagramChannel!
```

Opens a datagram channel.

The new channel is created by invoking the [openDatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openDatagramChannel())method of the system-wide default object. The channel will not be connected.

The [ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily.html#) of the channel's socket is platform (and possibly configuration) dependent and therefore unspecified. The [open](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#open(java.net.ProtocolFamily))allows the protocol family to be selected when opening a datagram channel, and should be used to open datagram channels that are intended for Internet Protocol multicasting.

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | A new datagram channel |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### open

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun open(family: ProtocolFamily!): DatagramChannel!
```

Opens a datagram channel.

The`family`parameter is used to specify the [ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily.html#). If the datagram channel is to be used for IP multicasting then this should correspond to the address type of the multicast groups that this channel will join.

The new channel is created by invoking the [openDatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openDatagramChannel(java.net.ProtocolFamily))method of the system-wide default object. The channel will not be connected.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------|
| `family` | [ProtocolFamily](https://developer.android.com/reference/kotlin/java/net/ProtocolFamily.html#)!:The protocol family |

| Return ||
|-------------------------------------------------------------------------------------------------------|------------------------|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | A new datagram channel |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the specified protocol family is not supported. For example, suppose the parameter is specified as [StandardProtocolFamily.INET6](https://developer.android.com/reference/kotlin/java/net/StandardProtocolFamily.html#) but IPv6 is not enabled on the platform. |
| `java.io.IOException` | If an I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dst: ByteBuffer!): Int
```

Reads a datagram from this channel.

This method may only be invoked if this channel's socket is connected, and it only accepts datagrams from the socket's peer. If there are more bytes in the datagram than remain in the given buffer then the remainder of the datagram is silently discarded. Otherwise this method behaves exactly as specified in the [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel) interface.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer into which bytes are to be transferred |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel's socket is not connected |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun read(dsts: Array<ByteBuffer!>!): Long
```

Reads a datagram from this channel.

This method may only be invoked if this channel's socket is connected, and it only accepts datagrams from the socket's peer. If there are more bytes in the datagram than remain in the given buffers then the remainder of the datagram is silently discarded. Otherwise this method behaves exactly as specified in the [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) interface.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers into which bytes are to be transferred |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel's socket is not connected |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    dsts: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

Reads a datagram from this channel.

This method may only be invoked if this channel's socket is connected, and it only accepts datagrams from the socket's peer. If there are more bytes in the datagram than remain in the given buffers then the remainder of the datagram is silently discarded. Otherwise this method behaves exactly as specified in the [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) interface.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers into which bytes are to be transferred |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer into which bytes are to be transferred; must be non-negative and no larger than`dsts.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`dsts.length`-`offset` |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or`-1`if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel's socket is not connected |

### receive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun receive(dst: ByteBuffer!): SocketAddress!
```

Receives a datagram via this channel.

If a datagram is immediately available, or if this channel is in blocking mode and one eventually becomes available, then the datagram is copied into the given byte buffer and its source address is returned. If this channel is in non-blocking mode and a datagram is not immediately available then this method immediately returns`null`.

The datagram is transferred into the given byte buffer starting at its current position, as if by a regular [read](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel#read(java.nio.ByteBuffer))operation. If there are fewer bytes remaining in the buffer than are required to hold the datagram then the remainder of the datagram is silently discarded.

This method performs exactly the same security checks as the [receive](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#receive(java.net.DatagramPacket))method of the class. That is, if the socket is not connected to a specific remote address and a security manager has been installed then for each datagram received this method verifies that the source's address and port number are permitted by the security manager's [checkAccept](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkAccept(kotlin.String,%20kotlin.Int))method. The overhead of this security check can be avoided by first connecting the socket via the [connect](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#connect(java.net.SocketAddress))method.

This method may be invoked at any time. If another thread has already initiated a read operation upon this channel, however, then an invocation of this method will block until the first operation is complete. If this channel's socket is not bound then this method will first cause the socket to be bound to an address that is assigned automatically, as if invoking the [bind](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#bind(java.net.SocketAddress))method with a parameter of`null`.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `dst` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer into which the datagram is to be transferred |

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)! | The datagram's source address, or`null`if this channel is in non-blocking mode and no datagram was immediately available |

| Exceptions ||
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit datagrams to be accepted from the datagram's sender |
| `java.io.IOException` | If some other I/O error occurs |

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun send(
    src: ByteBuffer!, 
    target: SocketAddress!
): Int
```

Sends a datagram via this channel.

If this channel is in non-blocking mode and there is sufficient room in the underlying output buffer, or if this channel is in blocking mode and sufficient room becomes available, then the remaining bytes in the given buffer are transmitted as a single datagram to the given target address.

The datagram is transferred from the byte buffer as if by a regular [write](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel#write(java.nio.ByteBuffer))operation.

This method performs exactly the same security checks as the [send](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#send(java.net.DatagramPacket))method of the class. That is, if the socket is not connected to a specific remote address and a security manager has been installed then for each datagram sent this method verifies that the target address and port number are permitted by the security manager's java.lang.SecurityManager#checkConnect method. The overhead of this security check can be avoided by first connecting the socket via the [connect](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#connect(java.net.SocketAddress))method.

This method may be invoked at any time. If another thread has already initiated a write operation upon this channel, however, then an invocation of this method will block until the first operation is complete. If this channel's socket is not bound then this method will first cause the socket to be bound to an address that is assigned automatically, as if by invoking the [bind](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#bind(java.net.SocketAddress))method with a parameter of`null`.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer containing the datagram to be sent |
| `target` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress.html#)!:The address to which the datagram is to be sent |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes sent, which will be either the number of bytes that were remaining in the source buffer when this method was invoked or, if this channel is non-blocking, may be zero if there was insufficient room for the datagram in the underlying output buffer |

| Exceptions ||
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.AlreadyConnectedException` | If this channel is connected to a different address from that specified by`target` |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.nio.channels.UnresolvedAddressException` | If the given remote address is not fully resolved |
| `java.nio.channels.UnsupportedAddressTypeException` | If the type of the given remote address is not supported |
| `java.lang.SecurityException` | If a security manager has been installed and it does not permit datagrams to be sent to the given address |
| `java.io.IOException` | If some other I/O error occurs |

### setOption

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> setOption(
    name: SocketOption<T>!, 
    value: T
): DatagramChannel!
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------|
| `<T>` | The type of the socket option value |
| `name` | [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption.html#)\<T\>!:The socket option |
| `value` | T:The value of the socket option. A value of`null`may be a valid value for some socket options. |

| Return ||
|-------------------------------------------------------------------------------------------------------|--------------|
| [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel#)! | This channel |

| Exceptions ||
|--------------------------------------------|----------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | If the socket option is not supported by this channel |
| `java.lang.IllegalArgumentException` | If the value is not a valid value for this socket option |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.io.IOException` | If an I/O error occurs |

### socket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun socket(): DatagramSocket!
```

Retrieves a datagram socket associated with this channel.

The returned object will not declare any public methods that are not declared in the [java.net.DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#) class.

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------|
| [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket.html#)! | A datagram socket associated with this channel |

### validOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun validOps(): Int
```

Returns an operation set identifying this channel's supported operations.

Datagram channels support reading and writing, so this method returns`(` [SelectionKey.OP_READ](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_READ:kotlin.Int)`|` [java.nio.channels.SelectionKey#OP_WRITE](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_WRITE:kotlin.Int)`)`.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The valid-operation set |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(src: ByteBuffer!): Int
```

Writes a datagram to this channel.

This method may only be invoked if this channel's socket is connected, in which case it sends datagrams directly to the socket's peer. Otherwise it behaves exactly as specified in the [WritableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/WritableByteChannel) interface.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!:The buffer from which bytes are to be retrieved |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel's socket is not connected |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun write(srcs: Array<ByteBuffer!>!): Long
```

Writes a datagram to this channel.

This method may only be invoked if this channel's socket is connected, in which case it sends datagrams directly to the socket's peer. Otherwise it behaves exactly as specified in the [GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel) interface.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers from which bytes are to be retrieved |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes sent, which will be either the number of bytes that were remaining in the source buffer when this method was invoked or, if this channel is non-blocking, may be zero if there was insufficient room for the datagram in the underlying output buffer |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel's socket is not connected |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    srcs: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

Writes a datagram to this channel.

This method may only be invoked if this channel's socket is connected, in which case it sends datagrams directly to the socket's peer. Otherwise it behaves exactly as specified in the [GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel) interface.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!:The buffers from which bytes are to be retrieved |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer from which bytes are to be retrieved; must be non-negative and no larger than`srcs.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`srcs.length`-`offset` |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes sent, which will be either the number of bytes that were remaining in the source buffer when this method was invoked or, if this channel is non-blocking, may be zero if there was insufficient room for the datagram in the underlying output buffer |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| `java.nio.channels.NotYetConnectedException` | If this channel's socket is not connected |
