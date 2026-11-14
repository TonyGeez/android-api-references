# WritableByteChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WritableByteChannel

```
interface WritableByteChannel : Channel
```

| [java.nio.channels.WritableByteChannel](../java/nio/channels/WritableByteChannel.md) |

| Known Direct Subclasses [ByteChannel](../java/nio/channels/ByteChannel.md), [GatheringByteChannel](../java/nio/channels/GatheringByteChannel.md), [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [ByteChannel](../java/nio/channels/ByteChannel.md) | A channel that can read and write bytes. | | [GatheringByteChannel](../java/nio/channels/GatheringByteChannel.md) | A channel that can write bytes from a sequence of buffers. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](../java/nio/channels/Pipe.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DatagramChannel](../java/nio/channels/DatagramChannel.md), [DatagramChannel](../java/nio/channels/DatagramChannel.md), [FileChannel](../java/nio/channels/FileChannel.md), [FileChannel](../java/nio/channels/FileChannel.md), [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md), [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md), [SocketChannel](../java/nio/channels/SocketChannel.md) [SocketChannel](../java/nio/channels/SocketChannel.md) |-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](../java/nio/channels/Pipe.md). | | [SeekableByteChannel](../java/nio/channels/SeekableByteChannel.md) | A byte channel that maintains a current*position*and allows the position to be changed. | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A channel that can write bytes.

Only one write operation upon a writable channel may be in progress at any given time. If one thread initiates a write operation upon a channel then any other thread that attempts to initiate another write operation will block until the first operation is complete. Whether or not other kinds of I/O operations may proceed concurrently with a write operation depends upon the type of the channel.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [write](../java/nio/channels/WritableByteChannel.md))`(`src:` ` [ByteBuffer](../java/nio/ByteBuffer.md)!`)` Writes a sequence of bytes to this channel from the given buffer. |

| Inherited functions ||
|---|---|
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/Channel.md))`()` <br /> Closes this channel. After a channel is closed, any further attempt to invoke I/O operations upon it will cause a [ClosedChannelException](../java/nio/channels/ClosedChannelException.md) to be thrown. If this channel is already closed then invoking this method has no effect. This method may be invoked at any time. If some other thread has already invoked it, however, then another invocation will block until the first invocation is complete, after which it will return without effect. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### write

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun write(src: ByteBuffer!): Int
```

Writes a sequence of bytes to this channel from the given buffer.

An attempt is made to write up to*r* bytes to the channel, where*r* is the number of bytes remaining in the buffer, that is,`src.remaining()`, at the moment this method is invoked.

Suppose that a byte sequence of length*n* is written, where`0``<=`*n* `<=`*r* . This byte sequence will be transferred from the buffer starting at index*p* , where*p* is the buffer's position at the moment this method is invoked; the index of the last byte written will be*p* `+`*n* `-``1`. Upon return the buffer's position will be equal to*p* `+`*n*; its limit will not have changed.

Unless otherwise specified, a write operation will return only after writing all of the*r*requested bytes. Some types of channels, depending upon their state, may write only some of the bytes or possibly none at all. A socket channel in non-blocking mode, for example, cannot write any more bytes than are free in the socket's output buffer.

This method may be invoked at any time. If another thread has already initiated a write operation upon this channel, however, then an invocation of this method will block until the first operation is complete.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `src` | [ByteBuffer](../java/nio/ByteBuffer.md)!:The buffer from which bytes are to be retrieved |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The number of bytes written, possibly zero |

| Exceptions ||
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.NonWritableChannelException` | If this channel was not opened for writing |
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.AsynchronousCloseException` | If another thread closes this channel while the write operation is in progress |
| --- | --- |
| `java.nio.channels.ClosedByInterruptException` | If another thread interrupts the current thread while the write operation is in progress, thereby closing the channel and setting the current thread's interrupt status |
| `java.io.IOException` | If some other I/O error occurs |
