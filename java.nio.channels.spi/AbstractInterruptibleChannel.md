# AbstractInterruptibleChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractInterruptibleChannel

```
abstract class AbstractInterruptibleChannel : Channel, InterruptibleChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#) |

| Known Direct Subclasses [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#), [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------| | [FileChannel](https://developer.android.com/reference/kotlin/java/nio/channels/FileChannel.html#) | A channel for reading, writing, mapping, and manipulating a file. | | [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#) | A channel that can be multiplexed via a [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#). | |

| Known Indirect Subclasses [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel), [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#), [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel.html#), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel.html#), [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#), [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) | Base implementation class for selectable channels. | | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#) | A selectable channel for datagram-oriented sockets. | | [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel.html#) | A channel representing the writable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#). | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel.html#) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#). | | [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#) | A selectable channel for stream-oriented connecting sockets. | |

Base implementation class for interruptible channels.

This class encapsulates the low-level machinery required to implement the asynchronous closing and interruption of channels. A concrete channel class must invoke the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())and [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))methods before and after, respectively, invoking an I/O operation that might block indefinitely. In order to ensure that the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method is always invoked, these methods should be used within a`try`...`finally`block: 

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

The`completed`argument to the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method tells whether or not the I/O operation actually completed, that is, whether it had any effect that would be visible to the invoker. In the case of an operation that reads bytes, for example, this argument should be`true`if, and only if, some bytes were actually transferred into the invoker's target buffer.

A concrete channel class must also implement the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in such a way that if it is invoked while another thread is blocked in a native I/O operation upon the channel then that operation will immediately return, either by throwing an exception or by returning normally. If a thread is interrupted or the channel upon which it is blocked is asynchronously closed then the channel's [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method will throw the appropriate exception.

This class performs the synchronization required to implement the specification. Implementations of the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method need not synchronize against other threads that might be attempting to close the channel.

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#AbstractInterruptibleChannel())`()` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#close())`()` Closes this channel. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())`()` Marks the beginning of an I/O operation that might block indefinitely. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Marks the end of an I/O operation that might block indefinitely. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())`()` Closes this channel. |

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

If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in order to complete the close operation.

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

This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. 

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun end(completed: Boolean): Unit
```

Marks the end of an I/O operation that might block indefinitely.

This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel.

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
