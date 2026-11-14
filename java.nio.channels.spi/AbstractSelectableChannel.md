# AbstractSelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractSelectableChannel

```
abstract class AbstractSelectableChannel : SelectableChannel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) |||
| | ↳ | [java.nio.channels.SelectableChannel](../java/nio/channels/SelectableChannel.md) ||
| | | ↳ | [java.nio.channels.spi.AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [DatagramChannel](../java/nio/channels/DatagramChannel.md), [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md), [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md), [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md), [SocketChannel](../java/nio/channels/SocketChannel.md) |-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](../java/nio/channels/DatagramChannel.md) | A selectable channel for datagram-oriented sockets. | | [Pipe.SinkChannel](../java/nio/channels/Pipe.SinkChannel.md) | A channel representing the writable end of a [Pipe](../java/nio/channels/Pipe.md). | | [Pipe.SourceChannel](../java/nio/channels/Pipe.SourceChannel.md) | A channel representing the readable end of a [Pipe](../java/nio/channels/Pipe.md). | | [ServerSocketChannel](../java/nio/channels/ServerSocketChannel.md) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](../java/nio/channels/SocketChannel.md) | A selectable channel for stream-oriented connecting sockets. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base implementation class for selectable channels.

This class defines methods that handle the mechanics of channel registration, deregistration, and closing. It maintains the current blocking mode of this channel as well as its current set of selection keys. It performs all of the synchronization required to implement the specification. Implementations of the abstract protected methods defined in this class need not synchronize against other threads that might be engaged in the same operations.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`provider:` ` [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)!`)` Initializes a new instance of this class. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> |
| [SelectableChannel](../java/nio/channels/SelectableChannel.md)! | [configureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adjusts this channel's blocking mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` <br /> |
| [SelectionKey](../java/nio/channels/SelectionKey.md)! | [keyFor](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`sel:` ` [Selector](../java/nio/channels/Selector.md)!`)` <br /> |
| [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)! | [provider](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` Returns the provider that created this channel. |
| --- | --- |
| [SelectionKey](../java/nio/channels/SelectionKey.md)! | [register](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`sel:` ` [Selector](../java/nio/channels/Selector.md)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Registers this channel with the given selector, returning a selection key. |

| Protected methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` Closes this channel. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))`()` Closes this selectable channel. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implConfigureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adjusts this channel's blocking mode. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java/nio/channels/spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](../java/nio/channels/spi/AbstractInterruptibleChannel.md))method, using a`try`...`finally`block as shown [above](../java/nio/channels/spi/AbstractInterruptibleChannel.md), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](../java/nio/channels/spi/AbstractInterruptibleChannel.md))`()` <br /> | ||
| From class [SelectableChannel](../java/nio/channels/SelectableChannel.md) |------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [SelectionKey](../java/nio/channels/SelectionKey.md)! | [register](../java/nio/channels/SelectableChannel.md))`(`sel:` ` [Selector](../java/nio/channels/Selector.md)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Registers this channel with the given selector, returning a selection key. An invocation of this convenience method of the form `sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](../java/nio/channels/SelectableChannel.md)) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](../java/nio/channels/SelectableChannel.md))`()` <br /> Returns an [operation set](../java/nio/channels/SelectionKey.md) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class. <br /> | ||

## Protected constructors

### AbstractSelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractSelectableChannel(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)!:The provider that created this channel |

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

If the given blocking mode is different from the current blocking mode then this method invokes the [implConfigureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))method, while holding the appropriate locks, in order to change the mode.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this channel will be placed in blocking mode; if`false`then it will be placed non-blocking mode |

| Return ||
|----------------------------------------------------------------------------------------------------------------|-------------------------|
| [SelectableChannel](../java/nio/channels/SelectableChannel.md)! | This selectable channel |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.IllegalBlockingModeException` | If`block`is`true`and this channel is registered with one or more selectors |
| `java.io.IOException` | If an I/O error occurs |
| --- | --- |

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
| `sel` | [Selector](../java/nio/channels/Selector.md)!:The selector |

| Return ||
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SelectionKey](../java/nio/channels/SelectionKey.md)! | The key returned when this channel was last registered with the given selector, or`null`if this channel is not currently registered with that selector |

### provider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provider(): SelectorProvider!
```

Returns the provider that created this channel.

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [SelectorProvider](../java/nio/channels/spi/SelectorProvider.md)! | The provider that created this channel |

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

Otherwise this channel has not yet been registered with the given selector, so the [register](../java/nio/channels/spi/AbstractSelector.md))method of the selector is invoked while holding the appropriate locks. The resulting key is added to this channel's key set before being returned.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sel` | [Selector](../java/nio/channels/Selector.md)!:The selector with which this channel is to be registered |
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interest set for the resulting key |
| `att` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The attachment for the resulting key; may be`null` |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [SelectionKey](../java/nio/channels/SelectionKey.md)! | A key representing the registration of this channel with the given selector |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.ClosedSelectorException` | If the selector is closed |
| `java.nio.channels.IllegalBlockingModeException` | If this channel is in blocking mode |
| --- | --- |
| `java.nio.channels.IllegalSelectorException` | If this channel was not created by the same provider as the given selector |
| `java.nio.channels.CancelledKeyException` | If this channel is currently registered with the given selector but the corresponding key has already been cancelled |
| `java.lang.IllegalArgumentException` | If a bit in the`ops`set does not correspond to an operation that is supported by this channel, that is, if`set & ~validOps() != 0` |
| --- | --- |

## Protected methods

### implCloseChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun implCloseChannel(): Unit
```

Closes this channel.

This method, which is specified in the [AbstractInterruptibleChannel](../java/nio/channels/spi/AbstractInterruptibleChannel.md) class and is invoked by the java.nio.channels.Channel#close method, in turn invokes the [implCloseSelectableChannel](../java/nio/channels/spi/AbstractSelectableChannel.md))method in order to perform the actual work of closing this channel. It then cancels all of this channel's keys.

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

This method is invoked by the [configureBlocking](../java/nio/channels/spi/AbstractSelectableChannel.md))method in order to perform the actual work of changing the blocking mode. This method is only invoked if the new mode is different from the current mode.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this channel will be placed in blocking mode; if`false`then it will be placed non-blocking mode |

| Exceptions ||
|-----------------------|------------------------|
| `java.io.IOException` | If an I/O error occurs |
