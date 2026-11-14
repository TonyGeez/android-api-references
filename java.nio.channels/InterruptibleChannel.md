# InterruptibleChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InterruptibleChannel

```
interface InterruptibleChannel : Channel
```

| [java.nio.channels.InterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/InterruptibleChannel#) |

| Known Direct Subclasses [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------| | [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) | Base implementation class for interruptible channels. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel), [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel), [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel), [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel), [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel), [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel), [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) |-----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------| | [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) | Base implementation class for selectable channels. | | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. | | [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel) | A channel for reading, writing, mapping, and manipulating a file. | | [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel) | A channel representing the writable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) | A channel that can be multiplexed via a [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector). | | [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A channel that can be asynchronously closed and interrupted.

A channel that implements this interface is*asynchronously closeable:* If a thread is blocked in an I/O operation on an interruptible channel then another thread may invoke the channel's #close method. This will cause the blocked thread to receive an [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException).

A channel that implements this interface is also*interruptible:* If a thread is blocked in an I/O operation on an interruptible channel then another thread may invoke the blocked thread's [interrupt](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())method. This will cause the channel to be closed, the blocked thread to receive a [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException), and the blocked thread's interrupt status to be set.

If a thread's interrupt status is already set and it invokes a blocking I/O operation upon a channel then the channel will be closed and the thread will immediately receive a [ClosedByInterruptException](https://developer.android.com/reference/kotlin/java/nio/channels/ClosedByInterruptException); its interrupt status will remain set.

A channel supports asynchronous closing and interruption if, and only if, it implements this interface. This can be tested at runtime, if necessary, via the`instanceof`operator.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/InterruptibleChannel#close())`()` Closes this channel. |

| Inherited functions ||
|---|---|
| From class [Channel](https://developer.android.com/reference/kotlin/java/nio/channels/Channel) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/Channel#isOpen())`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this channel.

Any thread currently blocked in an I/O operation upon this channel will receive an [AsynchronousCloseException](https://developer.android.com/reference/kotlin/java/nio/channels/AsynchronousCloseException).

This method otherwise behaves exactly as specified by the java.nio.channels.Channel#close interface.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |
