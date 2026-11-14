# DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DatagramPacket

```
class DatagramPacket
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.DatagramPacket](DatagramPacket.md) |

This class represents a datagram packet.

Datagram packets are used to implement a connectionless packet delivery service. Each message is routed from one machine to another based solely on information contained within that packet. Multiple packets sent from one machine to another might be routed differently, and might arrive in any order. Packet delivery is not guaranteed.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DatagramPacket](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`DatagramPacket`for receiving packets of length`length`. |
| [DatagramPacket](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a`DatagramPacket`for receiving packets of length`length`, specifying an offset into the buffer. |
| [DatagramPacket](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `address:` ` [InetAddress](InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a datagram packet for sending packets of length`length`with offset`ioffset`to the specified port number on the specified host. |
| [DatagramPacket](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `address:` ` [SocketAddress](SocketAddress.md)!`)` Constructs a datagram packet for sending packets of length`length`with offset`ioffset`to the specified port number on the specified host. |
| [DatagramPacket](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `address:` ` [InetAddress](InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a datagram packet for sending packets of length`length`to the specified port number on the specified host. |
| [DatagramPacket](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `address:` ` [SocketAddress](SocketAddress.md)!`)` Constructs a datagram packet for sending packets of length`length`to the specified port number on the specified host. |

| Public methods ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [InetAddress](InetAddress.md)! | [getAddress](DatagramPacket.md))`()` Returns the IP address of the machine to which this datagram is being sent or from which the datagram was received. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getData](DatagramPacket.md))`()` Returns the data buffer. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLength](DatagramPacket.md))`()` Returns the length of the data to be sent or the length of the data received. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffset](DatagramPacket.md))`()` Returns the offset of the data to be sent or the offset of the data received. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](DatagramPacket.md))`()` Returns the port number on the remote host to which this datagram is being sent or from which the datagram was received. |
| [SocketAddress](SocketAddress.md)! | [getSocketAddress](DatagramPacket.md))`()` Gets the SocketAddress (usually IP address + port number) of the remote host that this packet is being sent to or is coming from. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAddress](DatagramPacket.md))`(`iaddr:` ` [InetAddress](InetAddress.md)!`)` Sets the IP address of the machine to which this datagram is being sent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setData](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Set the data buffer for this packet. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setData](DatagramPacket.md))`(`buf:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the data buffer for this packet. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLength](DatagramPacket.md))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the length for this packet. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPort](DatagramPacket.md))`(`iport:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the port number on the remote host to which this datagram is being sent. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSocketAddress](DatagramPacket.md))`(`address:` ` [SocketAddress](SocketAddress.md)!`)` Sets the SocketAddress (usually IP address + port number) of the remote host to which this datagram is being sent. |
| --- | --- |

## Public constructors

### DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatagramPacket(
    buf: ByteArray!, 
    length: Int)
```

Constructs a`DatagramPacket`for receiving packets of length`length`.

The`length`argument must be less than or equal to`buf.length`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer for holding the incoming datagram. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to read. |

### DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatagramPacket(
    buf: ByteArray!, 
    offset: Int, 
    length: Int)
```

Constructs a`DatagramPacket`for receiving packets of length`length`, specifying an offset into the buffer.

The`length`argument must be less than or equal to`buf.length`.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:buffer for holding the incoming datagram. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset for the buffer |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to read. |
| --- | --- |

### DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatagramPacket(
    buf: ByteArray!, 
    offset: Int, 
    length: Int, 
    address: InetAddress!, 
    port: Int)
```

Constructs a datagram packet for sending packets of length`length`with offset`ioffset`to the specified port number on the specified host. The`length`argument must be less than or equal to`buf.length`.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the packet data. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the packet data offset. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the packet data length. |
| --- | --- |
| `address` | [InetAddress](InetAddress.md)!:the destination address. |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the destination port number. |

**See Also**

- [java.net.InetAddress](InetAddress.md) 

### DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatagramPacket(
    buf: ByteArray!, 
    offset: Int, 
    length: Int, 
    address: SocketAddress!)
```

Constructs a datagram packet for sending packets of length`length`with offset`ioffset`to the specified port number on the specified host. The`length`argument must be less than or equal to`buf.length`.

*Android note*: Up to and including API 25 this method declared that a SocketException can be thrown, although the exception is never thrown. Code compiled against a newer SDK does not need to catch the exception and will be binary compatible with older versions of Android.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the packet data. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the packet data offset. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the packet data length. |
| --- | --- |
| `address` | [SocketAddress](SocketAddress.md)!:the destination socket address. |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if address type is not supported |

**See Also**

- [java.net.InetAddress](InetAddress.md) 

### DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatagramPacket(
    buf: ByteArray!, 
    length: Int, 
    address: InetAddress!, 
    port: Int)
```

Constructs a datagram packet for sending packets of length`length`to the specified port number on the specified host. The`length`argument must be less than or equal to`buf.length`.

*Android note*: Up to and including API 25 this method declared that a SocketException can be thrown, although the exception is never thrown. Code compiled against a newer SDK does not need to catch the exception and will be binary compatible with older versions of Android.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the packet data. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the packet length. |
| `address` | [InetAddress](InetAddress.md)!:the destination address. |
| --- | --- |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the destination port number. |

**See Also**

- [java.net.InetAddress](InetAddress.md) 

### DatagramPacket

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DatagramPacket(
    buf: ByteArray!, 
    length: Int, 
    address: SocketAddress!)
```

Constructs a datagram packet for sending packets of length`length`to the specified port number on the specified host. The`length`argument must be less than or equal to`buf.length`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the packet data. |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the packet length. |
| `address` | [SocketAddress](SocketAddress.md)!:the destination address. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------------|
| `java.lang.IllegalArgumentException` | if address type is not supported |

**See Also**

- [java.net.InetAddress](InetAddress.md)

## Public methods

### getAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddress(): InetAddress!
```

Returns the IP address of the machine to which this datagram is being sent or from which the datagram was received.

| Return ||
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [InetAddress](InetAddress.md)! | the IP address of the machine to which this datagram is being sent or from which the datagram was received. |

**See Also**

- [java.net.InetAddress](InetAddress.md)
- <https://developer.android.com/reference/kotlin/java/net/DatagramPacket#setAddress(java.net.InetAddress)> 

### getData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getData(): ByteArray!
```

Returns the data buffer. The data received or the data to be sent starts from the`offset`in the buffer, and runs for`length`long.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the buffer used to receive or send data |

**See Also**

- [#setData(byte[], int, int)](https://developer.android.com/reference/kotlin/java/net/DatagramPacket#setData(kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int)) 

### getLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLength(): Int
```

Returns the length of the data to be sent or the length of the data received.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the data to be sent or the length of the data received. |

**See Also**

- [#setLength(int)](DatagramPacket.md)) 

### getOffset

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffset(): Int
```

Returns the offset of the data to be sent or the offset of the data received.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the offset of the data to be sent or the offset of the data received. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPort(): Int
```

Returns the port number on the remote host to which this datagram is being sent or from which the datagram was received.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number on the remote host to which this datagram is being sent or from which the datagram was received. |

**See Also**

- [#setPort(int)](DatagramPacket.md)) 

### getSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSocketAddress(): SocketAddress!
```

Gets the SocketAddress (usually IP address + port number) of the remote host that this packet is being sent to or is coming from.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------|
| [SocketAddress](SocketAddress.md)! | the`SocketAddress` |

**See Also**

- [#setSocketAddress](DatagramPacket.md)) 

### setAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAddress(iaddr: InetAddress!): Unit
```

Sets the IP address of the machine to which this datagram is being sent.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `iaddr` | [InetAddress](InetAddress.md)!:the`InetAddress` |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/DatagramPacket#getAddress()> 

### setData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setData(buf: ByteArray!): Unit
```

Set the data buffer for this packet. With the offset of this DatagramPacket set to 0, and the length set to the length of`buf`.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer to set for this packet. |

| Exceptions ||
|----------------------------------|--------------------------|
| `java.lang.NullPointerException` | if the argument is null. |

**See Also**

- [#getLength](DatagramPacket.md))
- [#getData](DatagramPacket.md)) 

### setData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setData(
    buf: ByteArray!, 
    offset: Int, 
    length: Int
): Unit
```

Set the data buffer for this packet. This sets the data, length and offset of the packet.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `buf` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer to set for this packet |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into the data |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the data and/or the length of the buffer used to receive data |
| --- | --- |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the argument is null |

**See Also**

- [#getData](DatagramPacket.md))
- [#getOffset](DatagramPacket.md))
- [#getLength](DatagramPacket.md)) 

### setLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLength(length: Int): Unit
```

Set the length for this packet. The length of the packet is the number of bytes from the packet's data buffer that will be sent, or the number of bytes of the packet's data buffer that will be used for receiving data. The length must be lesser or equal to the offset plus the length of the packet's buffer.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length to set for this packet. |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the length is negative of if the length is greater than the packet's data buffer length. |

**See Also**

- [#getLength](DatagramPacket.md)) 

### setPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPort(iport: Int): Unit
```

Sets the port number on the remote host to which this datagram is being sent.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------|
| `iport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port number |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/DatagramPacket#getPort()> 

### setSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setSocketAddress(address: SocketAddress!): Unit
```

Sets the SocketAddress (usually IP address + port number) of the remote host to which this datagram is being sent.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `address` | [SocketAddress](SocketAddress.md)!:the`SocketAddress` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if address is null or is a SocketAddress subclass not supported by this socket |

**See Also**

- [#getSocketAddress](DatagramPacket.md))
