# ScatteringByteChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScatteringByteChannel

```
interface ScatteringByteChannel : ReadableByteChannel
```

| [java.nio.channels.ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel#) |

| Known Direct Subclasses [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel), [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel), [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) |-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. | | [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel) | A channel for reading, writing, mapping, and manipulating a file. | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A channel that can read bytes into a sequence of buffers.

A *scattering* read operation reads, in a single invocation, a sequence of bytes into one or more of a given sequence of buffers. Scattering reads are often useful when implementing network protocols or file formats that, for example, group data into segments consisting of one or more fixed-length headers followed by a variable-length body. Similar *gathering* write operations are defined in the [GatheringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/GatheringByteChannel) interface.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel#read(kotlin.Array))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`)` Reads a sequence of bytes from this channel into the given buffers. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel#read(kotlin.Array,%20kotlin.Int,%20kotlin.Int))`(`dsts:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!>!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Reads a sequence of bytes from this channel into a subsequence of the given buffers. |

| Inherited functions ||
|---|---|
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close())`()` Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` Tells whether or not this channel is open. <br /> | ||
| From class [ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel#read(java.nio.ByteBuffer))`(`dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Reads a sequence of bytes from this channel into the given buffer. An attempt is made to read up to *r* bytes from the channel, where *r* is the number of bytes remaining in the buffer, that is, `dst.remaining()`, at the moment this method is invoked. Suppose that a byte sequence of length *n* is read, where `0` `<=` *n* `<=` *r* . This byte sequence will be transferred into the buffer so that the first byte in the sequence is at index *p* and the last byte is at index *p* `+` *n* `-` `1`, where *p* is the buffer's position at the moment this method is invoked. Upon return the buffer's position will be equal to *p* `+` *n*; its limit will not have changed. A read operation might not fill the buffer, and in fact it might not read any bytes at all. Whether or not it does so depends upon the nature and state of the channel. A socket channel in non-blocking mode, for example, cannot read any more bytes than are immediately available from the socket's input buffer; similarly, a file channel cannot read any more bytes than remain in the file. It is guaranteed, however, that if a channel is in blocking mode and there is at least one byte remaining in the buffer then this method will block until at least one byte is read. This method may be invoked at any time. If another thread has already initiated a read operation upon this channel, however, then an invocation of this method will block until the first operation is complete. <br /> | ||

## Public methods

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dsts: Array<ByteBuffer!>!): Long
```

Reads a sequence of bytes from this channel into the given buffers.

An invocation of this method of the form `c.read(dsts)` behaves in exactly the same manner as the invocation 

```kotlin
c.read(dsts, 0, dsts.length);
```

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!: The buffers into which bytes are to be transferred |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or `-1` if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(
    dsts: Array<ByteBuffer!>!, 
    offset: Int, 
    length: Int
): Long
```

Reads a sequence of bytes from this channel into a subsequence of the given buffers.

An invocation of this method attempts to read up to *r* bytes from this channel, where *r* is the total number of bytes remaining the specified subsequence of the given buffer array, that is, 

```kotlin
dsts[offset].remaining()
      + dsts[offset+1].remaining()
      + ... + dsts[offset+length-1].remaining()
```
at the moment that this method is invoked.

Suppose that a byte sequence of length *n* is read, where `0` `<=` *n* `<=` *r* . Up to the first `dsts[offset].remaining()` bytes of this sequence are transferred into buffer `dsts[offset]`, up to the next `dsts[offset+1].remaining()` bytes are transferred into buffer `dsts[offset+1]`, and so forth, until the entire byte sequence is transferred into the given buffers. As many bytes as possible are transferred into each buffer, hence the final position of each updated buffer, except the last updated buffer, is guaranteed to be equal to that buffer's limit.

This method may be invoked at any time. If another thread has already initiated a read operation upon this channel, however, then an invocation of this method will block until the first operation is complete.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dsts` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!\>!: The buffers into which bytes are to be transferred |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The offset within the buffer array of the first buffer into which bytes are to be transferred; must be non-negative and no larger than `dsts.length` |
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The maximum number of buffers to be accessed; must be non-negative and no larger than `dsts.length` - `offset` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The number of bytes read, possibly zero, or `-1` if the channel has reached end-of-stream |

| Exceptions ||
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the preconditions on the `offset` and `length` parameters do not hold |
| `java.nio.channels.NonReadableChannelException` | If this channel was not opened for reading |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| --- | --- |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the read operation is in progress |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
| --- | --- |
