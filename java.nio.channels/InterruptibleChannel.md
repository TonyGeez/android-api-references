# InterruptibleChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InterruptibleChannel

```
interface InterruptibleChannel : Channel
```

| [java.nio.channels.InterruptibleChannel](../java/nio/channels/InterruptibleChannel.md) |

| Known Direct Subclasses [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) |-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------| | [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) | Base implementation class for interruptible channels. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md), [DatagramChannel](../java/nio/channels/DatagramChannel.md), [FileChannel](../java/nio/channels/FileChannel.md), [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md), [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md), [SelectableChannel](../java/nio/channels/SelectableChannel.md), [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md), [SocketChannel](../java/nio/channels/SocketChannel.md) |-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) | Base implementation class for selectable channels. | | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](../java/nio/channels/Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](../java/nio/channels/Pipe.md). | | [SelectableChannel](../java/nio/channels/SelectableChannel.md) | A channel that can be multiplexed via a [Selector](../java/nio/channels/Selector.md). | | [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A channel that can be asynchronously closed and interrupted.

A channel that implements this interface is*asynchronously closeable:* If a thread is blocked in an I/O operation on an interruptible channel then another thread may invoke the channel's #close method. This will cause the blocked thread to receive an [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md).

A channel that implements this interface is also*interruptible:* If a thread is blocked in an I/O operation on an interruptible channel then another thread may invoke the blocked thread's [interrupt](../java/lang/Thread.md))method. This will cause the channel to be closed, the blocked thread to receive a [ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md), and the blocked thread's interrupt status to be set.

If a thread's interrupt status is already set and it invokes a blocking I/O operation upon a channel then the channel will be closed and the thread will immediately receive a [ClosedByInterruptException](../java/nio/channels/ClosedByInterruptException.md); its interrupt status will remain set.

A channel supports asynchronous closing and interruption if, and only if, it implements this interface. This can be tested at runtime, if necessary, via the`instanceof`operator.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/InterruptibleChannel.md))`()` Closes this channel. |

| Inherited functions ||
|---|---|
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this channel.

Any thread currently blocked in an I/O operation upon this channel will receive an [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md).

This method otherwise behaves exactly as specified by the java.nio.channels.Channel#close interface.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |
