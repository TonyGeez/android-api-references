# AbstractSelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractSelectableChannel

```
abstract class AbstractSelectableChannel : SelectableChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |||
| | ↳ | [java.nio.channels.SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#) ||
| | | ↳ | [java.nio.channels.spi.AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#) |

| Known Direct Subclasses [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#), [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel.html#), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel.html#), [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#), [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#) |-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel.html#) | A selectable channel for datagram-oriented sockets. | | [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel.html#) | A channel representing the writable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#). | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel.html#) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.html#). | | [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel.html#) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel.html#) | A selectable channel for stream-oriented connecting sockets. | |

Base implementation class for selectable channels.

This class defines methods that handle the mechanics of channel registration, deregistration, and closing. It maintains the current blocking mode of this channel as well as its current set of selection keys. It performs all of the synchronization required to implement the specification. Implementations of the abstract protected methods defined in this class need not synchronize against other threads that might be engaged in the same operations.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#AbstractSelectableChannel(java.nio.channels.spi.SelectorProvider))`(`provider:` ` [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!`)` Initializes a new instance of this class. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#blockingLock())`()` <br /> |
| [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#)! | [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#configureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adjusts this channel's blocking mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#isBlocking())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#isRegistered())`()` <br /> |
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | [keyFor](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#keyFor(java.nio.channels.Selector))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)!`)` <br /> |
| [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#provider())`()` Returns the provider that created this channel. |
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Registers this channel with the given selector, returning a selection key. |

| Protected methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseChannel())`()` Closes this channel. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseSelectableChannel())`()` Closes this selectable channel. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implConfigureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implConfigureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adjusts this channel's blocking mode. |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#close())`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())`()` <br /> | ||
| From class [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#register(java.nio.channels.Selector,%20kotlin.Int))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Registers this channel with the given selector, returning a selection key. An invocation of this convenience method of the form `sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#validOps())`()` <br /> Returns an [operation set](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#opsets) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class. <br /> | ||

## Protected constructors

### AbstractSelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractSelectableChannel(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!:The provider that created this channel |

## Public methods

### blockingLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun blockingLock(): Any!
```

| Return ||
|-----------------------------------------------------------------------------|-------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The blocking-mode lock object |

### configureBlocking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun configureBlocking(block: Boolean): SelectableChannel!
```

Adjusts this channel's blocking mode.

If the given blocking mode is different from the current blocking mode then this method invokes the [implConfigureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implConfigureBlocking(kotlin.Boolean))method, while holding the appropriate locks, in order to change the mode.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this channel will be placed in blocking mode; if`false`then it will be placed non-blocking mode |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------|
| [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#)! | This selectable channel |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.IllegalBlockingModeException` | If`block`is`true`and this channel is registered with one or more selectors |
| `java.io.IOException` | If an I/O error occurs |

### isBlocking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isBlocking(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel is in blocking mode |

### isRegistered

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isRegistered(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel is registered |

### keyFor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun keyFor(sel: Selector!): SelectionKey!
```

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------|
| `sel` | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)!:The selector |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | The key returned when this channel was last registered with the given selector, or`null`if this channel is not currently registered with that selector |

### provider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provider(): SelectorProvider!
```

Returns the provider that created this channel.

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | The provider that created this channel |

### register

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun register(
    sel: Selector!, 
    ops: Int, 
    att: Any!
): SelectionKey!
```

Registers this channel with the given selector, returning a selection key.

This method first verifies that this channel is open and that the given initial interest set is valid.

If this channel is already registered with the given selector then the selection key representing that registration is returned after setting its interest set to the given value.

Otherwise this channel has not yet been registered with the given selector, so the [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#register(java.nio.channels.spi.AbstractSelectableChannel,%20kotlin.Int,%20kotlin.Any))method of the selector is invoked while holding the appropriate locks. The resulting key is added to this channel's key set before being returned.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sel` | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)!:The selector with which this channel is to be registered |
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interest set for the resulting key |
| `att` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The attachment for the resulting key; may be`null` |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | A key representing the registration of this channel with the given selector |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.ClosedSelectorException` | If the selector is closed |
| `java.nio.channels.IllegalBlockingModeException` | If this channel is in blocking mode |
| `java.nio.channels.IllegalSelectorException` | If this channel was not created by the same provider as the given selector |
| `java.nio.channels.CancelledKeyException` | If this channel is currently registered with the given selector but the corresponding key has already been cancelled |
| `java.lang.IllegalArgumentException` | If a bit in the`ops`set does not correspond to an operation that is supported by this channel, that is, if`set & ~validOps() != 0` |

## Protected methods

### implCloseChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun implCloseChannel(): Unit
```

Closes this channel.

This method, which is specified in the [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) class and is invoked by the java.nio.channels.Channel#close method, in turn invokes the [implCloseSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#implCloseSelectableChannel())method in order to perform the actual work of closing this channel. It then cancels all of this channel's keys.

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs while closing the channel |

### implCloseSelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun implCloseSelectableChannel(): Unit
```

Closes this selectable channel.

This method is invoked by the java.nio.channels.Channel#close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once.

An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally.

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |

### implConfigureBlocking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun implConfigureBlocking(block: Boolean): Unit
```

Adjusts this channel's blocking mode.

This method is invoked by the [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel#configureBlocking(kotlin.Boolean))method in order to perform the actual work of changing the blocking mode. This method is only invoked if the new mode is different from the current mode.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this channel will be placed in blocking mode; if`false`then it will be placed non-blocking mode |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
