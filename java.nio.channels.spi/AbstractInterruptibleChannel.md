# AbstractInterruptibleChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractInterruptibleChannel

```
abstract class AbstractInterruptibleChannel : Channel, InterruptibleChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) |

| Known Direct Subclasses [FileChannel](../java/nio/channels/FileChannel.md), [SelectableChannel](../java/nio/channels/SelectableChannel.md) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------| | [FileChannel](../java/nio/channels/FileChannel.md) | A channel for reading, writing, mapping, and manipulating a file. | | [SelectableChannel](../java/nio/channels/SelectableChannel.md) | A channel that can be multiplexed via a [Selector](../java/nio/channels/Selector.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md), [DatagramChannel](../java/nio/channels/DatagramChannel.md), [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md), [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md), [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md), [SocketChannel](../java/nio/channels/SocketChannel.md) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) | Base implementation class for selectable channels. | | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](../java/nio/channels/Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](../java/nio/channels/Pipe.md). | | [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base implementation class for interruptible channels.

This class encapsulates the low-level machinery required to implement the asynchronous closing and interruption of channels. A concrete channel class must invoke the [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))and [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))methods before and after, respectively, invoking an I/O operation that might block indefinitely. In order to ensure that the [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method is always invoked, these methods should be used within a`try`...`finally`block: 

```kotlin
boolean completed = false;
  try {
      begin();
      completed = ...;    // Perform blocking I/O operation
      return ...;         // Return result
  } finally {
      end(completed);
  }
```

The`completed`argument to the [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method tells whether or not the I/O operation actually completed, that is, whether it had any effect that would be visible to the invoker. In the case of an operation that reads bytes, for example, this argument should be`true`if, and only if, some bytes were actually transferred into the invoker's target buffer.

A concrete channel class must also implement the [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method in such a way that if it is invoked while another thread is blocked in a native I/O operation upon the channel then that operation will immediately return, either by throwing an exception or by returning normally. If a thread is interrupted or the channel upon which it is blocked is asynchronously closed then the channel's [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method will throw the appropriate exception.

This class performs the synchronization required to implement the specification. Implementations of the [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method need not synchronize against other threads that might be attempting to close the channel.

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` Closes this channel. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` Marks the beginning of an I/O operation that might block indefinitely. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Marks the end of an I/O operation that might block indefinitely. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` Closes this channel. |
| --- | --- |

## Protected constructors

### AbstractInterruptibleChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractInterruptibleChannel()
```

Initializes a new instance of this class.

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes this channel.

If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method in order to complete the close operation.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | If an I/O error occurs |

### isOpen

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isOpen(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel is open |

## Protected methods

### begin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun begin(): Unit
```

Marks the beginning of an I/O operation that might block indefinitely.

This method should be invoked in tandem with the [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java/nio/channels/spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. 

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun end(completed: Boolean): Unit
```

Marks the end of an I/O operation that might block indefinitely.

This method should be invoked in tandem with the [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java/nio/channels/spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `completed` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if, and only if, the I/O operation completed successfully, that is, had some effect that would be visible to the operation's invoker |

| Exceptions ||
|------------------------------------------------|------------------------------------------------------------|
| `java.nio.channels.AsynchronousCloseException` | If the channel was asynchronously closed |
| `java.nio.channels.ClosedByInterruptException` | If the thread blocked in the I/O operation was interrupted |

### implCloseChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun implCloseChannel(): Unit
```

Closes this channel.

This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once.

An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally.

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs while closing the channel |
