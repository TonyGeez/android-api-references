# MulticastSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MulticastSocket

```
open class MulticastSocket : DatagramSocket
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.net.DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket) ||
| | ↳ | [java.net.MulticastSocket](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#) |

The multicast datagram socket class is useful for sending and receiving IP multicast packets. A MulticastSocket is a (UDP) DatagramSocket, with additional capabilities for joining "groups" of other multicast hosts on the internet.

A multicast group is specified by a class D IP address and by a standard UDP port number. Class D IP addresses are in the range`224.0.0.0`to`239.255.255.255`, inclusive. The address 224.0.0.0 is reserved and should not be used.

One would join a multicast group by first creating a MulticastSocket with the desired port, then invoking the`joinGroup(InetAddress groupAddr)`method: 

```kotlin
// join a Multicast group and send the group salutations
  ...
  String msg = "Hello";
  InetAddress group = InetAddress.getByName("228.5.6.7");
  MulticastSocket s = new MulticastSocket(6789);
  s.joinGroup(group);
  byte[] bytes = msg.getBytes(StandardCharsets.UTF_8);
  DatagramPacket hi = new DatagramPacket(bytes, bytes.length,
                              group, 6789);
  s.send(hi);
  // get their responses!
  byte[] buf = new byte[1000];
  DatagramPacket recv = new DatagramPacket(buf, buf.length);
  s.receive(recv);
  ...
  // OK, I'm done talking - leave the group...
  s.leaveGroup(group);
  
```
When one sends a message to a multicast group,**all** subscribing recipients to that host and port receive the message (within the time-to-live range of the packet, see below). The socket needn't be a member of the multicast group to send messages to it.

When a socket subscribes to a multicast group/port, it receives datagrams sent by other hosts to the group/port, as do all other members of the group and port. A socket relinquishes membership in a group by the leaveGroup(InetAddress addr) method.**Multiple MulticastSocket's**may subscribe to a multicast group and port concurrently, and they will all receive group datagrams.

Currently applets are not allowed to use multicast sockets.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MulticastSocket](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#MulticastSocket())`()` Create a multicast socket. |
| [MulticastSocket](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#MulticastSocket(kotlin.Int))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a multicast socket and bind it to a specific port. |
| [MulticastSocket](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#MulticastSocket(java.net.SocketAddress))`(`bindaddr:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`)` Create a MulticastSocket bound to the specified socket address. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)! | [getInterface](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getInterface())`()` Retrieve the address of the network interface used for multicast packets. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLoopbackMode](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getLoopbackMode())`()` Get the setting for local loopback of multicast datagrams. |
| open [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)! | [getNetworkInterface](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getNetworkInterface())`()` Get the multicast network interface set. |
| open [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | [getTTL](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getTTL())`()` Get the default time-to-live for multicast packets sent out on the socket. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTimeToLive](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getTimeToLive())`()` Get the default time-to-live for multicast packets sent out on the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [joinGroup](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#joinGroup(java.net.InetAddress))`(`mcastaddr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!`)` Joins a multicast group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [joinGroup](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#joinGroup(java.net.SocketAddress,%20java.net.NetworkInterface))`(`mcastaddr:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`, `netIf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)!`)` Joins the specified multicast group at the specified interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [leaveGroup](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#leaveGroup(java.net.InetAddress))`(`mcastaddr:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!`)` Leave a multicast group. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [leaveGroup](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#leaveGroup(java.net.SocketAddress,%20java.net.NetworkInterface))`(`mcastaddr:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`, `netIf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)!`)` Leave a multicast group on a specified local interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#send(java.net.DatagramPacket,%20kotlin.Byte))`(`p:` ` [DatagramPacket](https://developer.android.com/reference/kotlin/java/net/DatagramPacket)!`, `ttl:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Sends a datagram packet to the destination, with a TTL (time- to-live) other than the default for the socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterface](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setInterface(java.net.InetAddress))`(`inf:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!`)` Set the multicast network interface used by methods whose behavior would be affected by the value of the network interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLoopbackMode](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setLoopbackMode(kotlin.Boolean))`(`disable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Disable/Enable local loopback of multicast datagrams The option is used by the platform's networking code as a hint for setting whether multicast data will be looped back to the local socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNetworkInterface](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setNetworkInterface(java.net.NetworkInterface))`(`netIf:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)!`)` Specify the network interface for outgoing multicast datagrams sent on this socket. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTTL](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setTTL(kotlin.Byte))`(`ttl:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Set the default time-to-live for multicast packets sent out on this`MulticastSocket`in order to control the scope of the multicasts. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTimeToLive](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setTimeToLive(kotlin.Int))`(`ttl:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the default time-to-live for multicast packets sent out on this`MulticastSocket`in order to control the scope of the multicasts. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption)\<\*\>!\>! | [supportedOptions](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#supportedOptions())`()` <br /> |

| Inherited functions ||
|---|---|
| From class [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket) |------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bind](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#bind(java.net.SocketAddress))`(`addr:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`)` <br /> Binds this DatagramSocket to a specific address and port. If the address is`null`, then the system will pick up an ephemeral port and a valid local address to bind the socket. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#close())`()` <br /> Closes this datagram socket. Any thread currently blocked in [receive](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket))upon this socket will throw a [SocketException](https://developer.android.com/reference/kotlin/java/net/SocketException). If this socket has an associated channel then the channel is closed as well. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.InetAddress,%20kotlin.Int))`(`address:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Connects the socket to a remote address for this socket. When a socket is connected to a remote address, packets may only be sent to or received from that address. By default a datagram socket is not connected. If the remote destination to which the socket is connected does not exist, or is otherwise unreachable, and if an ICMP destination unreachable packet has been received for that address, then a subsequent call to send or receive may throw a PortUnreachableException. Note, there is no guarantee that the exception will be thrown. If a security manager has been installed then it is invoked to check access to the remote address. Specifically, if the given`address`is a [multicast address](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMulticastAddress()), the security manager's [checkMulticast](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress))method is invoked with the given`address`. Otherwise, the security manager's [checkConnect](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkConnect(kotlin.String,%20kotlin.Int))and [checkAccept](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkAccept(kotlin.String,%20kotlin.Int))methods are invoked, with the given`address`and`port`, to verify that datagrams are permitted to be sent and received respectively. When a socket is connected, [receive](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket))and [send](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket))**will not perform any security checks** on incoming and outgoing packets, other than matching the packet's and the socket's address and port. On a send operation, if the packet's address is set and the packet's address and the socket's address do not match, an`IllegalArgumentException`will be thrown. A socket connected to a multicast address may only be used to send packets. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connect](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.SocketAddress))`(`addr:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`)` <br /> Connects this socket to a remote socket address (IP address + port number). If given an [InetSocketAddress](https://developer.android.com/reference/kotlin/java/net/InetSocketAddress), this method behaves as if invoking [connect(InetAddress,int)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#connect(java.net.InetAddress,%20kotlin.Int))with the given socket addresses IP address and port number. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [disconnect](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#disconnect())`()` <br /> Disconnects the socket. If the socket is closed or not connected, then this method has no effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getBroadcast](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getBroadcast())`()` <br /> Tests if SO_BROADCAST is enabled. <br /> | | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#)! | [getChannel](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getChannel())`()` <br /> Returns the unique [java.nio.channels.DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#) object associated with this datagram socket, if any. A datagram socket will have a channel if, and only if, the channel itself was created via the java.nio.channels.DatagramChannel#open method. <br /> | | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)! | [getInetAddress](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getInetAddress())`()` <br /> Returns the address to which this socket is connected. Returns`null`if the socket is not connected. If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed. <br /> | | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)! | [getLocalAddress](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalAddress())`()` <br /> Gets the local address to which the socket is bound. If there is a security manager, its`checkConnect`method is first called with the host address and`-1`as its arguments to see if the operation is allowed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocalPort](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalPort())`()` <br /> Returns the port number on the local host to which this socket is bound. <br /> | | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)! | [getLocalSocketAddress](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalSocketAddress())`()` <br /> Returns the address of the endpoint this socket is bound to. <br /> | | T | [getOption](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getOption(java.net.SocketOption))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption)<T>!`)` <br /> Returns the value of a socket option. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getPort())`()` <br /> Returns the port number to which this socket is connected. Returns`-1`if the socket is not connected. If the socket was connected prior to being #close, then this method will continue to return the connected port number after the socket is closed. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReceiveBufferSize](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReceiveBufferSize())`()` <br /> Get value of the SO_RCVBUF option for this`DatagramSocket`, that is the buffer size used by the platform for input on this`DatagramSocket`. <br /> | | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)! | [getRemoteSocketAddress](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getRemoteSocketAddress())`()` <br /> Returns the address of the endpoint this socket is connected to, or`null`if it is unconnected. If the socket was connected prior to being #close, then this method will continue to return the connected address after the socket is closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getReuseAddress](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReuseAddress())`()` <br /> Tests if SO_REUSEADDR is enabled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSendBufferSize](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSendBufferSize())`()` <br /> Get value of the SO_SNDBUF option for this`DatagramSocket`, that is the buffer size used by the platform for output on this`DatagramSocket`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSoTimeout())`()` <br /> Retrieve setting for SO_TIMEOUT. 0 returns implies that the option is disabled (i.e., timeout of infinity). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTrafficClass](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getTrafficClass())`()` <br /> Gets traffic class or type-of-service in the IP datagram header for packets sent from this DatagramSocket. As the underlying network implementation may ignore the traffic class or type-of-service set using [setTrafficClass(int)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int))this method may return a different value than was previously set using the [setTrafficClass(int)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int))method on this DatagramSocket. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBound](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isBound())`()` <br /> Returns the binding state of the socket. If the socket was bound prior to being #close, then this method will continue to return`true`after the socket is closed. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isClosed())`()` <br /> Returns whether the socket is closed or not. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnected](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isConnected())`()` <br /> Returns the connection state of the socket. If the socket was connected prior to being #close, then this method will continue to return`true`after the socket is closed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [receive](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket))`(`p:` ` [DatagramPacket](https://developer.android.com/reference/kotlin/java/net/DatagramPacket)!`)` <br /> Receives a datagram packet from this socket. When this method returns, the`DatagramPacket`'s buffer is filled with the data received. The datagram packet also contains the sender's IP address, and the port number on the sender's machine. This method blocks until a datagram is received. The`length`field of the datagram packet object contains the length of the received message. If the message is longer than the packet's length, the message is truncated. If there is a security manager, a packet cannot be received if the security manager's`checkAccept`method does not allow it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [send](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket))`(`p:` ` [DatagramPacket](https://developer.android.com/reference/kotlin/java/net/DatagramPacket)!`)` <br /> Sends a datagram packet from this socket. The`DatagramPacket`includes information indicating the data to be sent, its length, the IP address of the remote host, and the port number on the remote host. If there is a security manager, and the socket is not currently connected to a remote address, this method first performs some security checks. First, if`p.getAddress().isMulticastAddress()`is true, this method calls the security manager's`checkMulticast`method with`p.getAddress()`as its argument. If the evaluation of that expression is false, this method instead calls the security manager's`checkConnect`method with arguments`p.getAddress().getHostAddress()`and`p.getPort()`. Each call to a security manager method could result in a SecurityException if the operation is not allowed. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBroadcast](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setBroadcast(kotlin.Boolean))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable/disable SO_BROADCAST. Some operating systems may require that the Java virtual machine be started with implementation specific privileges to enable this option or send broadcast datagrams. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDatagramSocketImplFactory](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setDatagramSocketImplFactory(java.net.DatagramSocketImplFactory))`(`fac:` ` [DatagramSocketImplFactory](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImplFactory)!`)` <br /> Sets the datagram socket implementation factory for the application. The factory can be specified only once. When an application creates a new datagram socket, the socket implementation factory's`createDatagramSocketImpl`method is called to create the actual datagram socket implementation. Passing`null`to the method is a no-op unless the factory was already set. If there is a security manager, this method first calls the security manager's`checkSetFactory`method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | [DatagramSocket](https://developer.android.com/reference/kotlin/java/net/DatagramSocket)! | [setOption](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setOption(java.net.SocketOption,%20java.net.DatagramSocket.setOption.T))`(`name:` ` [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption)<T>!`, `value:` `T`)` <br /> Sets the value of a socket option. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReceiveBufferSize](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReceiveBufferSize(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the SO_RCVBUF option to the specified value for this`DatagramSocket`. The SO_RCVBUF option is used by the network implementation as a hint to size the underlying network I/O buffers. The SO_RCVBUF setting may also be used by the network implementation to determine the maximum size of the packet that can be received on this socket. Because SO_RCVBUF is a hint, applications that want to verify what size the buffers were set to should call [getReceiveBufferSize()](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReceiveBufferSize()). Increasing SO_RCVBUF may allow the network implementation to buffer multiple packets when packets arrive faster than are being received using [receive(java.net.DatagramPacket)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket)). Note: It is implementation specific if a packet larger than SO_RCVBUF can be received. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setReuseAddress](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean))`(`on:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Enable/disable the SO_REUSEADDR socket option. For UDP sockets it may be necessary to bind more than one socket to the same socket address. This is typically for the purpose of receiving multicast packets (See [java.net.MulticastSocket](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#)). The`SO_REUSEADDR`socket option allows multiple sockets to be bound to the same socket address if the`SO_REUSEADDR`socket option is enabled prior to binding the socket using [bind(java.net.SocketAddress)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#bind(java.net.SocketAddress)). Note: This functionality is not supported by all existing platforms, so it is implementation specific whether this option will be ignored or not. However, if it is not supported then [getReuseAddress()](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReuseAddress())will always return`false`. When a`DatagramSocket`is created the initial setting of`SO_REUSEADDR`is disabled. The behaviour when`SO_REUSEADDR`is enabled or disabled after a socket is bound (See [isBound()](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#isBound())) is not defined. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSendBufferSize](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSendBufferSize(kotlin.Int))`(`size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets the SO_SNDBUF option to the specified value for this`DatagramSocket`. The SO_SNDBUF option is used by the network implementation as a hint to size the underlying network I/O buffers. The SO_SNDBUF setting may also be used by the network implementation to determine the maximum size of the packet that can be sent on this socket. As SO_SNDBUF is a hint, applications that want to verify what size the buffer is should call [getSendBufferSize()](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSendBufferSize()). Increasing the buffer size may allow multiple outgoing packets to be queued by the network implementation when the send rate is high. Note: If [send(java.net.DatagramPacket)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket))is used to send a`DatagramPacket`that is larger than the setting of SO_SNDBUF then it is implementation specific if the packet is sent or discarded. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSoTimeout(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Enable/disable SO_TIMEOUT with the specified timeout, in milliseconds. With this option set to a non-zero timeout, a call to receive() for this DatagramSocket will block for only this amount of time. If the timeout expires, a**java.net.SocketTimeoutException** is raised, though the DatagramSocket is still valid. The option**must** be enabled prior to entering the blocking operation to have effect. The timeout must be`> 0`. A timeout of zero is interpreted as an infinite timeout. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTrafficClass](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setTrafficClass(kotlin.Int))`(`tc:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Sets traffic class or type-of-service octet in the IP datagram header for datagrams sent from this DatagramSocket. As the underlying network implementation may ignore this value applications should consider it a hint. The tc**must** be in the range`0 <= tc <= 255`or an IllegalArgumentException will be thrown. Notes: For Internet Protocol v4 the value consists of an`integer`, the least significant 8 bits of which represent the value of the TOS octet in IP packets sent by the socket. RFC 1349 defines the TOS values as follows: - `IPTOS_LOWCOST (0x02)` - `IPTOS_RELIABILITY (0x04)` - `IPTOS_THROUGHPUT (0x08)` - `IPTOS_LOWDELAY (0x10)` The last low order bit is always ignored as this corresponds to the MBZ (must be zero) bit. Setting bits in the precedence field may result in a SocketException indicating that the operation is not permitted. for Internet Protocol v6`tc`is the value that would be placed into the sin6_flowinfo field of the IP header. <br /> | ||

## Public constructors

### MulticastSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MulticastSocket()
```

Create a multicast socket.

If there is a security manager, its`checkListen`method is first called with 0 as its argument to ensure the operation is allowed. This could result in a SecurityException.

When the socket is created the [DatagramSocket.setReuseAddress(boolean)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean))method is called to enable the SO_REUSEADDR socket option.

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while creating the MulticastSocket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |

**See Also**

- [java.lang.SecurityManager#checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))
- [java.net.DatagramSocket#setReuseAddress(boolean)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean))
- [java.net.DatagramSocketImpl#setOption(SocketOption, Object)](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl#setOption(java.net.SocketOption,%20java.net.DatagramSocketImpl.setOption.T)) 

### MulticastSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MulticastSocket(port: Int)
```

Create a multicast socket and bind it to a specific port.

If there is a security manager, its`checkListen`method is first called with the`port`argument as its argument to ensure the operation is allowed. This could result in a SecurityException.

When the socket is created the [DatagramSocket.setReuseAddress(boolean)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean))method is called to enable the SO_REUSEADDR socket option.

| Parameters ||
|--------|----------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):port to use |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while creating the MulticastSocket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |

**See Also**

- [java.lang.SecurityManager#checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))
- [java.net.DatagramSocket#setReuseAddress(boolean)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean)) 

### MulticastSocket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MulticastSocket(bindaddr: SocketAddress!)
```

Create a MulticastSocket bound to the specified socket address.

Or, if the address is`null`, create an unbound socket.

If there is a security manager, its`checkListen`method is first called with the SocketAddress port as its argument to ensure the operation is allowed. This could result in a SecurityException.

When the socket is created the [DatagramSocket.setReuseAddress(boolean)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean))method is called to enable the SO_REUSEADDR socket option.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `bindaddr` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!:Socket address to bind to, or`null`for an unbound socket. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while creating the MulticastSocket |
| `java.lang.SecurityException` | if a security manager exists and its`checkListen`method doesn't allow the operation. |

**See Also**

- [java.lang.SecurityManager#checkListen](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkListen(kotlin.Int))
- [java.net.DatagramSocket#setReuseAddress(boolean)](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReuseAddress(kotlin.Boolean))

## Public methods

### getInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterface(): InetAddress!
```

Retrieve the address of the network interface used for multicast packets.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)! | An`InetAddress`representing the address of the network interface used for multicast packets. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setInterface(java.net.InetAddress)> 

### getLoopbackMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLoopbackMode(): Boolean
```

Get the setting for local loopback of multicast datagrams.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the LoopbackMode has been disabled |

| Exceptions ||
|----------------------------|--------------------------------------------|
| `java.net.SocketException` | if an error occurs while getting the value |

**See Also**

- [#setLoopbackMode](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setLoopbackMode(kotlin.Boolean)) 

### getNetworkInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkInterface(): NetworkInterface!
```

Get the multicast network interface set.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)! | the multicast`NetworkInterface`currently set or`null`when no interface is set. |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- [#setNetworkInterface(NetworkInterface)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setNetworkInterface(java.net.NetworkInterface)) 

### getTTL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTTL(): Byte
```

**Deprecated:** *use the getTimeToLive method instead, which returns an**int** instead of a**byte**.*

Get the default time-to-live for multicast packets sent out on the socket.

| Return ||
|------------------------------------------------------------------------------|--------------------------------|
| [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html) | the default time-to-live value |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while getting the default time-to-live value |

**See Also**

- [#setTTL(byte)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setTTL(kotlin.Byte)) 

### getTimeToLive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeToLive(): Int
```

Get the default time-to-live for multicast packets sent out on the socket.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default time-to-live value |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while getting the default time-to-live value |

**See Also**

- [#setTimeToLive(int)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setTimeToLive(kotlin.Int)) 

### joinGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun joinGroup(mcastaddr: InetAddress!): Unit
```

Joins a multicast group. Its behavior may be affected by`setInterface`or`setNetworkInterface`.

If there is a security manager, this method first calls its`checkMulticast`method with the`mcastaddr`argument as its argument.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `mcastaddr` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!:is the multicast address to join |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is an error joining, or when the address is not a multicast address, or the platform does not support multicasting |
| `java.lang.SecurityException` | if a security manager exists and its`checkMulticast`method doesn't allow the join. |

**See Also**

- [java.lang.SecurityManager#checkMulticast(InetAddress)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress)) 

### joinGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun joinGroup(
    mcastaddr: SocketAddress!, 
    netIf: NetworkInterface!
): Unit
```

Joins the specified multicast group at the specified interface.

If there is a security manager, this method first calls its`checkMulticast`method with the`mcastaddr`argument as its argument.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mcastaddr` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!:is the multicast address to join |
| `netIf` | [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)!:specifies the local interface to receive multicast datagram packets, or*null* to defer to the interface set by [MulticastSocket.setInterface(InetAddress)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setInterface(java.net.InetAddress))or [MulticastSocket.setNetworkInterface(NetworkInterface)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setNetworkInterface(java.net.NetworkInterface)) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if mcastaddr is null or is a SocketAddress subclass not supported by this socket |
| `java.io.IOException` | if there is an error joining, or when the address is not a multicast address, or the platform does not support multicasting |
| `java.lang.SecurityException` | if a security manager exists and its`checkMulticast`method doesn't allow the join. |

**See Also**

- [java.lang.SecurityManager#checkMulticast(InetAddress)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress)) 

### leaveGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun leaveGroup(mcastaddr: InetAddress!): Unit
```

Leave a multicast group. Its behavior may be affected by`setInterface`or`setNetworkInterface`.

If there is a security manager, this method first calls its`checkMulticast`method with the`mcastaddr`argument as its argument.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------|
| `mcastaddr` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!:is the multicast address to leave |

| Exceptions ||
|-------------------------------|-----------------------------------------------------------------------------------------|
| `java.io.IOException` | if there is an error leaving or when the address is not a multicast address. |
| `java.lang.SecurityException` | if a security manager exists and its`checkMulticast`method doesn't allow the operation. |

**See Also**

- [java.lang.SecurityManager#checkMulticast(InetAddress)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress)) 

### leaveGroup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun leaveGroup(
    mcastaddr: SocketAddress!, 
    netIf: NetworkInterface!
): Unit
```

Leave a multicast group on a specified local interface.

If there is a security manager, this method first calls its`checkMulticast`method with the`mcastaddr`argument as its argument.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mcastaddr` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!:is the multicast address to leave |
| `netIf` | [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)!:specifies the local interface or*null* to defer to the interface set by [MulticastSocket.setInterface(InetAddress)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setInterface(java.net.InetAddress))or [MulticastSocket.setNetworkInterface(NetworkInterface)](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setNetworkInterface(java.net.NetworkInterface)) |

| Exceptions ||
|--------------------------------------|-----------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if mcastaddr is null or is a SocketAddress subclass not supported by this socket |
| `java.io.IOException` | if there is an error leaving or when the address is not a multicast address. |
| `java.lang.SecurityException` | if a security manager exists and its`checkMulticast`method doesn't allow the operation. |

**See Also**

- [java.lang.SecurityManager#checkMulticast(InetAddress)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress)) 

### send

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun send(
    p: DatagramPacket!, 
    ttl: Byte
): Unit
```

**Deprecated:** *Use the following code or its equivalent instead: ...... int ttl = mcastSocket.getTimeToLive(); mcastSocket.setTimeToLive(newttl); mcastSocket.send(p); mcastSocket.setTimeToLive(ttl); ......*

Sends a datagram packet to the destination, with a TTL (time- to-live) other than the default for the socket. This method need only be used in instances where a particular TTL is desired; otherwise it is preferable to set a TTL once on the socket, and use that default TTL for all packets. This method does**not** alter the default TTL for the socket. Its behavior may be affected by`setInterface`.

If there is a security manager, this method first performs some security checks. First, if`p.getAddress().isMulticastAddress()`is true, this method calls the security manager's`checkMulticast`method with`p.getAddress()`and`ttl`as its arguments. If the evaluation of that expression is false, this method instead calls the security manager's`checkConnect`method with arguments`p.getAddress().getHostAddress()`and`p.getPort()`. Each call to a security manager method could result in a SecurityException if the operation is not allowed.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `p` | [DatagramPacket](https://developer.android.com/reference/kotlin/java/net/DatagramPacket)!:is the packet to be sent. The packet should contain the destination multicast ip address and the data to be sent. One does not need to be the member of the group to send packets to a destination multicast address. |
| `ttl` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):optional time to live for multicast packet. default ttl is 1. |

| Exceptions ||
|-------------------------------|----------------------------------------------------------------------------------------------------|
| `java.io.IOException` | is raised if an error occurs i.e error while setting ttl. |
| `java.lang.SecurityException` | if a security manager exists and its`checkMulticast`or`checkConnect`method doesn't allow the send. |

**See Also**

- [java.net.DatagramSocket#send](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#send(java.net.DatagramPacket))
- [java.net.DatagramSocket#receive](https://developer.android.com/reference/kotlin/java/net/DatagramSocket#receive(java.net.DatagramPacket))
- [java.lang.SecurityManager#checkMulticast(java.net.InetAddress, byte)](https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkMulticast(java.net.InetAddress,%20kotlin.Byte)) 

### setInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setInterface(inf: InetAddress!): Unit
```

Set the multicast network interface used by methods whose behavior would be affected by the value of the network interface. Useful for multihomed hosts.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `inf` | [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress)!:the InetAddress |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getInterface()> 

### setLoopbackMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setLoopbackMode(disable: Boolean): Unit
```

Disable/Enable local loopback of multicast datagrams The option is used by the platform's networking code as a hint for setting whether multicast data will be looped back to the local socket.

Because this option is a hint, applications that want to verify what loopback mode is set to should call [getLoopbackMode()](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getLoopbackMode())

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------|
| `disable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`to disable the LoopbackMode |

| Exceptions ||
|----------------------------|--------------------------------------------|
| `java.net.SocketException` | if an error occurs while setting the value |

**See Also**

- [#getLoopbackMode](https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getLoopbackMode()) 

### setNetworkInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setNetworkInterface(netIf: NetworkInterface!): Unit
```

Specify the network interface for outgoing multicast datagrams sent on this socket.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `netIf` | [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)!:the interface |

| Exceptions ||
|----------------------------|-----------------------------------------------------------------------|
| `java.net.SocketException` | if there is an error in the underlying protocol, such as a TCP error. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getNetworkInterface()> 

### setTTL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTTL(ttl: Byte): Unit
```

**Deprecated:** *use the setTimeToLive method instead, which uses**int** instead of**byte**as the type for ttl.*

Set the default time-to-live for multicast packets sent out on this`MulticastSocket`in order to control the scope of the multicasts.

The ttl is an**unsigned** 8-bit quantity, and so**must** be in the range`0 <= ttl <= 0xFF `.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `ttl` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):the time-to-live |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while setting the default time-to-live value |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getTTL()> 

### setTimeToLive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTimeToLive(ttl: Int): Unit
```

Set the default time-to-live for multicast packets sent out on this`MulticastSocket`in order to control the scope of the multicasts.

The ttl**must** be in the range`0 <= ttl <= 255`or an`IllegalArgumentException`will be thrown. Multicast packets sent with a TTL of`0`are not transmitted on the network but may be delivered locally.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------|
| `ttl` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the time-to-live |

| Exceptions ||
|-----------------------|-------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O exception occurs while setting the default time-to-live value |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getTimeToLive()> 

### supportedOptions

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun supportedOptions(): MutableSet<SocketOption<*>!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SocketOption](https://developer.android.com/reference/kotlin/java/net/SocketOption)<*>!>! | A set of the socket options supported by this socket. This set may be empty if the socket's DatagramSocketImpl cannot be created. |
