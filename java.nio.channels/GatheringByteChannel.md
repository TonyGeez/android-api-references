# GatheringByteChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GatheringByteChannel

```
interface GatheringByteChannel : WritableByteChannel
```

| [java.nio.channels.GatheringByteChannel](../java/nio/channels/GatheringByteChannel.md) |

| Known Direct Subclasses [DatagramChannel](../java/nio/channels/DatagramChannel.md), [FileChannel](../java/nio/channels/FileChannel.md), [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md), [SocketChannel](../java/nio/channels/SocketChannel.md) |-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](../java/nio/channels/Pipe.md). | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A channel that can write bytes from a sequence of buffers.

A*gathering* write operation writes, in a single invocation, a sequence of bytes from one or more of a given sequence of buffers. Gathering writes are often useful when implementing network protocols or file formats that, for example, group data into segments consisting of one or more fixed-length headers followed by a variable-length body. Similar*scattering* read operations are defined in the [ScatteringByteChannel](../java/nio/channels/ScatteringByteChannel.md) interface.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](../java/nio/channels/GatheringByteChannel.md))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java/nio/ByteBuffer.md)!>!`)` Writes a sequence of bytes to this channel from the given buffers. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [write](../java/nio/channels/GatheringByteChannel.md))`(`srcs:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](../java/nio/ByteBuffer.md)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Writes a sequence of bytes to this channel from a subsequence of the given buffers. |

| Inherited functions ||
|---|---|
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/Channel.md))`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](../java/nio/channels/ClosedChannelException.md) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||
| From class [WritableByteChannel](../java/nio/channels/WritableByteChannel.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](../java/nio/channels/WritableByteChannel.md))`(`src:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` <br /> Writes a sequence of bytes to this channel from the given buffer. An attempt is made to write up to*r* bytes to the channel, where*r* is the number of bytes remaining in the buffer, that is,`src.remaining()`, at the moment this method is invoked. Suppose that a byte sequence of length*n* is written, where`0``<=`*n* `<=`*r* . This byte sequence will be transferred from the buffer starting at index*p* , where*p* is the buffer's position at the moment this method is invoked; the index of the last byte written will be*p* `+`*n* `-``1`. Upon return the buffer's position will be equal to*p* `+`*n*; its limit will not have changed. Unless otherwise specified, a write operation will return only after writing all of the*r*requested bytes. Some types of channels, depending upon their state, may write only some of the bytes or possibly none at all. A socket channel in non-blocking mode, for example, cannot write any more bytes than are free in the socket's output buffer. This method may be invoked at any time. If another thread has already initiated a write operation upon this channel, however, then an invocation of this method will block until the first operation is complete. <br /> | ||

## Public methods

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(srcs: Array<ByteBuffer!>!): Long
```

Writes a sequence of bytes to this channel from the given buffers.

An invocation of this method of the form`c.write(srcs)`behaves in exactly the same manner as the invocation 

```kotlin
c.write(srcs, 0, srcs.length);
```

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!:The buffers from which bytes are to be retrieved |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(
    srcs: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

Writes a sequence of bytes to this channel from a subsequence of the given buffers.

An attempt is made to write up to*r* bytes to this channel, where*r*is the total number of bytes remaining in the specified subsequence of the given buffer array, that is, 

```kotlin
srcs[offset].remaining()
      + srcs[offset+1].remaining()
      + ... + srcs[offset+length-1].remaining()
```
at the moment that this method is invoked.

Suppose that a byte sequence of length*n* is written, where`0``<=`*n* `<=`*r* . Up to the first`srcs[offset].remaining()`bytes of this sequence are written from buffer`srcs[offset]`, up to the next`srcs[offset+1].remaining()`bytes are written from buffer`srcs[offset+1]`, and so forth, until the entire byte sequence is written. As many bytes as possible are written from each buffer, hence the final position of each updated buffer, except the last updated buffer, is guaranteed to be equal to that buffer's limit.

Unless otherwise specified, a write operation will return only after writing all of the*r*requested bytes. Some types of channels, depending upon their state, may write only some of the bytes or possibly none at all. A socket channel in non-blocking mode, for example, cannot write any more bytes than are free in the socket's output buffer.

This method may be invoked at any time. If another thread has already initiated a write operation upon this channel, however, then an invocation of this method will block until the first operation is complete.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `srcs` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](../java/nio/ByteBuffer.md)!\>!:The buffers from which bytes are to be retrieved |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The offset within the buffer array of the first buffer from which bytes are to be retrieved; must be non-negative and no larger than`srcs.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The maximum number of buffers to be accessed; must be non-negative and no larger than`srcs.length`-`offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the`offset`and`length`parameters do not hold |
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |
