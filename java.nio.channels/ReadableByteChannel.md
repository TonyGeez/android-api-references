# ReadableByteChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReadableByteChannel

```
interface ReadableByteChannel : Channel
```

| [java.nio.channels.ReadableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel#) |

| Known Direct Subclasses [ByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ByteChannel), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel), [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) |-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [ByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ByteChannel) | A channel that can read and write bytes. | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [ScatteringByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ScatteringByteChannel) | A channel that can read bytes into a sequence of buffers. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel), [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel), [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel), [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel), [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel), [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) |-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. | | [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel) | A channel for reading, writing, mapping, and manipulating a file. | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [SeekableByteChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SeekableByteChannel) | A byte channel that maintains a current*position*and allows the position to be changed. | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A channel that can read bytes.

Only one read operation upon a readable channel may be in progress at any given time. If one thread initiates a read operation upon a channel then any other thread that attempts to initiate another read operation will block until the first operation is complete. Whether or not other kinds of I/O operations may proceed concurrently with a read operation depends upon the type of the channel.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [read](https://developer.android.com/reference/kotlin/java/nio/channels/ReadableByteChannel#read(java.nio.ByteBuffer))`(`dst:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)!`)` Reads a sequence of bytes from this channel into the given buffer. |

| Inherited functions ||
|---|---|
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#close())`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedChannelException) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### read

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun read(dst: ByteBuffer!): Int
```

Reads a sequence of bytes from this channel into the given buffer.

An attempt is made to read up to*r* bytes from the channel, where*r* is the number of bytes remaining in the buffer, that is,`dst.remaining()`, at the moment this method is invoked.

Suppose that a byte sequence of length*n* is read, where`0``<=`*n* `<=`*r* . This byte sequence will be transferred into the buffer so that the first byte in the sequence is at index*p* and the last byte is at index*p* `+`*n* `-``1`, where*p* is the buffer's position at the moment this method is invoked. Upon return the buffer's position will be equal to*p* `+`*n*; its limit will not have changed.

A read operation might not fill the buffer, and in fact it might not read any bytes at all. Whether or not it does so depends upon the nature and state of the channel. A socket channel in non-blocking mode, for example, cannot read any more bytes than are immediately available from the socket's input buffer; similarly, a file channel cannot read any more bytes than remain in the file. It is guaranteed, however, that if a channel is in blocking mode and there is at least one byte remaining in the buffer then this method will block until at least one byte is read.

This method may be invoked at any time. If another thread has already initiated a read operation upon this channel, however, then an invocation of this method will block until the first operation is complete.

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
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the read operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
