Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SocketOptions

```
interface SocketOptions
```

| [java.net.SocketOptions](https://developer.android.com/reference/kotlin/java/net/SocketOptions#) |

| Known Direct Subclasses [DatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl), [SocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImpl) |---|---| | [DatagramSocketImpl](https://developer.android.com/reference/kotlin/java/net/DatagramSocketImpl) | Abstract datagram and multicast socket implementation base class. | | [SocketImpl](https://developer.android.com/reference/kotlin/java/net/SocketImpl) | The abstract class `SocketImpl` is a common superclass of all classes that actually implement sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface of methods to get/set socket options. This interface is implemented by: **SocketImpl** and **DatagramSocketImpl**. Subclasses of these should override the methods of this interface in order to support their own options.

The methods and constants which specify options in this interface are for implementation only. If you're not subclassing SocketImpl or DatagramSocketImpl, **you won't use these directly.** There are type-safe methods to get/set each of these options in Socket, ServerSocket, DatagramSocket and MulticastSocket.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_IF:kotlin.Int` Set which outgoing interface on which to send multicast packets. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_IF2:kotlin.Int` Same as above. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_MULTICAST_LOOP:kotlin.Int` This option enables or disables local loopback of multicast datagrams. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#IP_TOS:kotlin.Int` This option sets the type-of-service or traffic class field in the IP header for a TCP or UDP socket. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BINDADDR:kotlin.Int` Fetch the local address binding of a socket (this option cannot be "set" only "gotten", since sockets are bound at creation time, and so the locally bound address cannot be changed). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_BROADCAST:kotlin.Int` Sets SO_BROADCAST for a socket. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_KEEPALIVE:kotlin.Int` When the keepalive option is set for a TCP socket and no data has been exchanged across the socket in either direction for 2 hours (NOTE: the actual value is implementation dependent), TCP automatically sends a keepalive probe to the peer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_LINGER:kotlin.Int` Specify a linger-on-close timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_OOBINLINE:kotlin.Int` When the OOBINLINE option is set, any TCP urgent data received on the socket will be received through the socket input stream. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_RCVBUF:kotlin.Int` Set a hint the size of the underlying buffers used by the platform for incoming network I/O. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_REUSEADDR:kotlin.Int` Sets SO_REUSEADDR for a socket. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_REUSEPORT:kotlin.Int` Sets SO_REUSEPORT for a socket. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_SNDBUF:kotlin.Int` Set a hint the size of the underlying buffers used by the platform for outgoing network I/O. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#SO_TIMEOUT:kotlin.Int` Set a timeout on blocking Socket operations: ```kotlin ServerSocket.accept(); SocketInputStream.read(); DatagramSocket.receive(); ``` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#TCP_NODELAY:kotlin.Int` Disable Nagle's algorithm for this connection. |
| --- | --- |

| Public methods ||
|---|---|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#getOption(kotlin.Int)(optID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Fetch the value of an option. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/SocketOptions#setOption(kotlin.Int,%20kotlin.Any)(optID: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Enable/disable the option specified by *optID*. |

## Constants

### IP_MULTICAST_IF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IP_MULTICAST_IF: Int
```

Set which outgoing interface on which to send multicast packets. Useful on hosts with multiple network interfaces, where applications want to use other than the system default. Takes/returns an InetAddress.

Valid for Multicast: DatagramSocketImpl

 Value: 16

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setInterface(java.net.InetAddress)`
- `https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getInterface()`

### IP_MULTICAST_IF2

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IP_MULTICAST_IF2: Int
```

Same as above. This option is introduced so that the behaviour with IP_MULTICAST_IF will be kept the same as before, while this new option can support setting outgoing interfaces with either IPv4 and IPv6 addresses. NOTE: make sure there is no conflict with this

 Value: 31

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/MulticastSocket#setNetworkInterface(java.net.NetworkInterface)`
- `https://developer.android.com/reference/kotlin/java/net/MulticastSocket#getNetworkInterface()`

### IP_MULTICAST_LOOP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IP_MULTICAST_LOOP: Int
```

This option enables or disables local loopback of multicast datagrams. This option is enabled by default for Multicast Sockets.

 Value: 18

### IP_TOS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IP_TOS: Int
```

This option sets the type-of-service or traffic class field in the IP header for a TCP or UDP socket.

 Value: 3

### SO_BINDADDR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_BINDADDR: Int
```

Fetch the local address binding of a socket (this option cannot be "set" only "gotten", since sockets are bound at creation time, and so the locally bound address cannot be changed). The default local address of a socket is INADDR_ANY, meaning any local address on a multi-homed host. A multi-homed host can use this option to accept connections to only one of its addresses (in the case of a ServerSocket or DatagramSocket), or to specify its return address to the peer (for a Socket or DatagramSocket). The parameter of this option is an InetAddress.

This option **must** be specified in the constructor.

Valid for: SocketImpl, DatagramSocketImpl

 Value: 15

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#getLocalAddress()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getLocalAddress()`

### SO_BROADCAST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_BROADCAST: Int
```

Sets SO_BROADCAST for a socket. This option enables and disables the ability of the process to send broadcast messages. It is supported for only datagram sockets and only on networks that support the concept of a broadcast message (e.g. Ethernet, token ring, etc.), and it is set by default for DatagramSockets.

 Value: 32

### SO_KEEPALIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_KEEPALIVE: Int
```

When the keepalive option is set for a TCP socket and no data has been exchanged across the socket in either direction for 2 hours (NOTE: the actual value is implementation dependent), TCP automatically sends a keepalive probe to the peer. This probe is a TCP segment to which the peer must respond. One of three responses is expected: 1. The peer responds with the expected ACK. The application is not notified (since everything is OK). TCP will send another probe following another 2 hours of inactivity. 2. The peer responds with an RST, which tells the local TCP that the peer host has crashed and rebooted. The socket is closed. 3. There is no response from the peer. The socket is closed. The purpose of this option is to detect if the peer host crashes. Valid only for TCP socket: SocketImpl

 Value: 8

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setKeepAlive(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/net/Socket#getKeepAlive()`

### SO_LINGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_LINGER: Int
```

Specify a linger-on-close timeout. This option disables/enables immediate return from a **close()** of a TCP Socket. Enabling this option with a non-zero Integer *timeout* means that a **close()** will block pending the transmission and acknowledgement of all data written to the peer, at which point the socket is closed *gracefully* . Upon reaching the linger timeout, the socket is closed *forcefully*, with a TCP RST. Enabling the option with a timeout of zero does a forceful close immediately. If the specified timeout value exceeds 65,535 it will be reduced to 65,535.

Valid only for TCP: SocketImpl

 Value: 128

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setSoLinger(kotlin.Boolean,%20kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/Socket#getSoLinger()`

### SO_OOBINLINE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_OOBINLINE: Int
```

When the OOBINLINE option is set, any TCP urgent data received on the socket will be received through the socket input stream. When the option is disabled (which is the default) urgent data is silently discarded.

 Value: 4099

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setOOBInline(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/net/Socket#getOOBInline()`

### SO_RCVBUF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_RCVBUF: Int
```

Set a hint the size of the underlying buffers used by the platform for incoming network I/O. When used in set, this is a suggestion to the kernel from the application about the size of buffers to use for the data to be received over the socket. When used in get, this must return the size of the buffer actually used by the platform when receiving in data on this socket. Valid for all sockets: SocketImpl, DatagramSocketImpl

 Value: 4098

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setReceiveBufferSize(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/Socket#getReceiveBufferSize()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setReceiveBufferSize(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getReceiveBufferSize()`

### SO_REUSEADDR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_REUSEADDR: Int
```

Sets SO_REUSEADDR for a socket. This is used only for MulticastSockets in java, and it is set by default for MulticastSockets.

Valid for: DatagramSocketImpl

 Value: 4

### SO_REUSEPORT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_REUSEPORT: Int
```

Sets SO_REUSEPORT for a socket. This option enables and disables the ability to have multiple sockets listen to the same address and port.

Valid for: SocketImpl, DatagramSocketImpl

 Value: 14

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/StandardSocketOptions#SO_REUSEPORT:java.net.SocketOption`

### SO_SNDBUF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_SNDBUF: Int
```

Set a hint the size of the underlying buffers used by the platform for outgoing network I/O. When used in set, this is a suggestion to the kernel from the application about the size of buffers to use for the data to be sent over the socket. When used in get, this must return the size of the buffer actually used by the platform when sending out data on this socket. Valid for all sockets: SocketImpl, DatagramSocketImpl

 Value: 4097

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setSendBufferSize(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/Socket#getSendBufferSize()`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSendBufferSize(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#getSendBufferSize()`

### SO_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SO_TIMEOUT: Int
```

Set a timeout on blocking Socket operations:

```kotlin
ServerSocket.accept();
  SocketInputStream.read();
  DatagramSocket.receive();
  
```

<br />

The option must be set prior to entering a blocking operation to take effect. If the timeout expires and the operation would continue to block, **java.io.InterruptedIOException** is raised. The Socket is not closed in this case.

Valid for all sockets: SocketImpl, DatagramSocketImpl

 Value: 4102

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setSoTimeout(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/ServerSocket#setSoTimeout(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/net/DatagramSocket#setSoTimeout(kotlin.Int)`

### TCP_NODELAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TCP_NODELAY: Int
```

Disable Nagle's algorithm for this connection. Written data to the network is not buffered pending acknowledgement of previously written data.

Valid for TCP only: SocketImpl.

 Value: 1

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/Socket#setTcpNoDelay(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/net/Socket#getTcpNoDelay()`

## Public methods

### getOption

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getOption(optID: Int): Any!
```

Fetch the value of an option. Binary options will return java.lang.Boolean.TRUE if enabled, java.lang.Boolean.FALSE if disabled, e.g.: 

```kotlin
SocketImpl s;
  ...
  Boolean noDelay = (Boolean)(s.getOption(TCP_NODELAY));
  if (noDelay.booleanValue()) {
      // true if TCP_NODELAY is enabled...
  ...
  }
  
```

<br />

For options that take a particular type as a parameter, getOption(int) will return the parameter's value, else it will return java.lang.Boolean.FALSE:

```kotlin
Object o = s.getOption(SO_LINGER);
  if (o instanceof Integer) {
      System.out.print("Linger time is " + ((Integer)o).intValue());
  } else {
    // the true type of o is java.lang.Boolean.FALSE;
  }
  
```

| Parameters ||
|---|---|
| `optID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an `int` identifying the option to fetch |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | the value of the option |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if *optID* is unknown along the protocol stack (including the SocketImpl) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketOptions#setOption(kotlin.Int,%20kotlin.Any)`

### setOption

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun setOption(
    optID: Int, 
    value: Any!
): Unit
```

Enable/disable the option specified by *optID* . If the option is to be enabled, and it takes an option-specific "value", this is passed in *value* . The actual type of value is option-specific, and it is an error to pass something that isn't of the expected type: 

```kotlin
SocketImpl s;
  ...
  s.setOption(SO_LINGER, new Integer(10));
     // OK - set SO_LINGER w/ timeout of 10 sec.
  s.setOption(SO_LINGER, new Double(10));
     // ERROR - expects java.lang.Integer
 
```
If the requested option is binary, it can be set using this method by a java.lang.Boolean: 

```kotlin
s.setOption(TCP_NODELAY, Boolean.TRUE);
     // OK - enables TCP_NODELAY, a binary option
  
```

Any option can be disabled using this method with a Boolean.FALSE: 

```kotlin
s.setOption(TCP_NODELAY, Boolean.FALSE);
     // OK - disables TCP_NODELAY
  s.setOption(SO_LINGER, Boolean.FALSE);
     // OK - disables SO_LINGER
  
```

For an option that has a notion of on and off, and requires a non-boolean parameter, setting its value to anything other than *Boolean.FALSE* implicitly enables it. 
Throws SocketException if the option is unrecognized, the socket is closed, or some low-level error occurred 

<br />

| Parameters ||
|---|---|
| `optID` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): identifies the option |
| `value` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: the parameter of the socket option |

| Exceptions ||
|---|---|
| `java.net.SocketException` | if the option is unrecognized, the socket is closed, or some low-level error occurred |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/SocketOptions#getOption(kotlin.Int)`
