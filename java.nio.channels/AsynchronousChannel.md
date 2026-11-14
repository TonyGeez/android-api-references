# AsynchronousChannel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AsynchronousChannel

```
interface AsynchronousChannel : Channel
```

| [java.nio.channels.AsynchronousChannel](../java/nio/channels/AsynchronousChannel.md) |

| Known Direct Subclasses [AsynchronousByteChannel](../java/nio/channels/AsynchronousByteChannel.md), [AsynchronousFileChannel](../java/nio/channels/AsynchronousFileChannel.md), [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) |-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------| | [AsynchronousByteChannel](../java/nio/channels/AsynchronousByteChannel.md) | An asynchronous channel that can read and write bytes. | | [AsynchronousFileChannel](../java/nio/channels/AsynchronousFileChannel.md) | An asynchronous channel for reading, writing, and manipulating a file. | | [AsynchronousServerSocketChannel](../java/nio/channels/AsynchronousServerSocketChannel.md) | An asynchronous channel for stream-oriented listening sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) |-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------| | [AsynchronousSocketChannel](../java/nio/channels/AsynchronousSocketChannel.md) | An asynchronous channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- |

A channel that supports asynchronous I/O operations. Asynchronous I/O operations will usually take one of two forms:

1.

   ```kotlin
   <code><a docref="java.util.concurrent.Future">Future</a></code><V> <em>operation</em>(<em>...</em>)
   ```
2.

   ```kotlin
   void <em>operation</em>(<em>...</em>A attachment, <code><a docref="java.nio.channels.CompletionHandler">CompletionHandler</a></code><V,? super A> handler)
   ```

where*operation* is the name of the I/O operation (read or write for example),*V* is the result type of the I/O operation, and*A* is the type of an object attached to the I/O operation to provide context when consuming the result. The attachment is important for cases where a*state-less* `CompletionHandler`is used to consume the result of many I/O operations.

<br />

In the first form, the methods defined by the [Future](../java/util/concurrent/Future.md) interface may be used to check if the operation has completed, wait for its completion, and to retrieve the result. In the second form, a [CompletionHandler](../java/nio/channels/CompletionHandler.md) is invoked to consume the result of the I/O operation when it completes or fails.

A channel that implements this interface is*asynchronously closeable* : If an I/O operation is outstanding on the channel and the channel's #close method is invoked, then the I/O operation fails with the exception [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md).

Asynchronous channels are safe for use by multiple concurrent threads. Some channel implementations may support concurrent reading and writing, but may not allow more than one read and one write operation to be outstanding at any given time.

## Cancellation

The`Future`interface defines the [cancel](../java/util/concurrent/Future.md))method to cancel execution. This causes all threads waiting on the result of the I/O operation to throw [java.util.concurrent.CancellationException](../java/util/concurrent/CancellationException.md). Whether the underlying I/O operation can be cancelled is highly implementation specific and therefore not specified. Where cancellation leaves the channel, or the entity to which it is connected, in an inconsistent state, then the channel is put into an implementation specific*error state* that prevents further attempts to initiate I/O operations that are*similar* to the operation that was cancelled. For example, if a read operation is cancelled but the implementation cannot guarantee that bytes have not been read from the channel then it puts the channel into an error state; further attempts to initiate a`read`operation cause an unspecified runtime exception to be thrown. Similarly, if a write operation is cancelled but the implementation cannot guarantee that bytes have not been written to the channel then subsequent attempts to initiate a`write`will fail with an unspecified runtime exception.

Where the [cancel](../java/util/concurrent/Future.md))method is invoked with the`mayInterruptIfRunning`parameter set to`true`then the I/O operation may be interrupted by closing the channel. In that case all threads waiting on the result of the I/O operation throw`CancellationException`and any other I/O operations outstanding on the channel complete with the exception [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md).

Where the`cancel`method is invoked to cancel read or write operations then it is recommended that all buffers used in the I/O operations be discarded or care taken to ensure that the buffers are not accessed while the channel remains open.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/AsynchronousChannel.md))`()` Closes this channel. |

| Inherited functions ||
|---|---|
| From class [Channel](../java/nio/channels/Channel.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/Channel.md))`()` <br /> Tells whether or not this channel is open. <br /> | ||

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this channel.

Any outstanding asynchronous operations upon this channel will complete with the exception [AsynchronousCloseException](../java/nio/channels/AsynchronousCloseException.md). After a channel is closed, further attempts to initiate asynchronous I/O operations complete immediately with cause [ClosedChannelException](../java/nio/channels/ClosedChannelException.md).

This method otherwise behaves exactly as specified by the [Channel](../java/nio/channels/Channel.md) interface.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |
