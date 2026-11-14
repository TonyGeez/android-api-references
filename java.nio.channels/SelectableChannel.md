# SelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectableChannel

```
abstract class SelectableChannel : AbstractInterruptibleChannel, Channel
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.nio.channels.spi.AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) ||
| | ↳ | [java.nio.channels.SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#) |

| Known Direct Subclasses [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------| | [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel) | Base implementation class for selectable channels. | |

| Known Indirect Subclasses [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel), [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel), [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel), [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel), [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) |-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------| | [DatagramChannel](https://developer.android.com/reference/kotlin/java/nio/channels/DatagramChannel) | A selectable channel for datagram-oriented sockets. | | [Pipe.SinkChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SinkChannel) | A channel representing the writable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [Pipe.SourceChannel](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe.SourceChannel) | A channel representing the readable end of a [Pipe](https://developer.android.com/reference/kotlin/java/nio/channels/Pipe). | | [ServerSocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/ServerSocketChannel) | A selectable channel for stream-oriented listening sockets. | | [SocketChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SocketChannel) | A selectable channel for stream-oriented connecting sockets. | |

A channel that can be multiplexed via a [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector).

In order to be used with a selector, an instance of this class must first be*registered* via the [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any))method. This method returns a new [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey) object that represents the channel's registration with the selector.

Once registered with a selector, a channel remains registered until it is*deregistered*. This involves deallocating whatever resources were allocated to the channel by the selector.

A channel cannot be deregistered directly; instead, the key representing its registration must be*cancelled* . Cancelling a key requests that the channel be deregistered during the selector's next selection operation. A key may be cancelled explicitly by invoking its [cancel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#cancel())method. All of a channel's keys are cancelled implicitly when the channel is closed, whether by invoking its java.nio.channels.Channel#close method or by interrupting a thread blocked in an I/O operation upon the channel.

If the selector itself is closed then the channel will be deregistered, and the key representing its registration will be invalidated, without further delay.

A channel may be registered at most once with any particular selector.

Whether or not a channel is registered with one or more selectors may be determined by invoking the [isRegistered](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#isRegistered())method.

Selectable channels are safe for use by multiple concurrent threads.

## Blocking mode

A selectable channel is either in*blocking* mode or in*non-blocking* mode. In blocking mode, every I/O operation invoked upon the channel will block until it completes. In non-blocking mode an I/O operation will never block and may transfer fewer bytes than were requested or possibly no bytes at all. The blocking mode of a selectable channel may be determined by invoking its [isBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#isBlocking())method.

Newly-created selectable channels are always in blocking mode. Non-blocking mode is most useful in conjunction with selector-based multiplexing. A channel must be placed into non-blocking mode before being registered with a selector, and may not be returned to blocking mode until it has been deregistered.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#SelectableChannel())`()` Initializes a new instance of this class. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [blockingLock](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#blockingLock())`()` Retrieves the object upon which the [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#configureBlocking(kotlin.Boolean))and #register methods synchronize. |
| abstract [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#)! | [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#configureBlocking(kotlin.Boolean))`(`block:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Adjusts this channel's blocking mode. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#isBlocking())`()` Tells whether or not every I/O operation on this channel will block until it completes. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isRegistered](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#isRegistered())`()` Tells whether or not this channel is currently registered with any selectors. |
| abstract [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [keyFor](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#keyFor(java.nio.channels.Selector))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`)` Retrieves the key representing the channel's registration with the given selector. |
| abstract [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#provider())`()` Returns the provider that created this channel. |
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Registers this channel with the given selector, returning a selection key. |
| abstract [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any))`(`sel:` ` [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Registers this channel with the given selector, returning a selection key. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [validOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#validOps())`()` Returns an [operation set](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#opsets) identifying this channel's supported operations. |

| Inherited functions ||
|---|---|
| From class [AbstractInterruptibleChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())`()` <br /> Marks the beginning of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#close())`()` <br /> Closes this channel. If the channel has already been closed then this method returns immediately. Otherwise it marks the channel as closed and then invokes the [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())method in order to complete the close operation. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#end(kotlin.Boolean))`(`completed:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Marks the end of an I/O operation that might block indefinitely. This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#be), in order to implement asynchronous closing and interruption for this channel. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#implCloseChannel())`()` <br /> Closes this channel. This method is invoked by the #close method in order to perform the actual work of closing the channel. This method is only invoked if the channel has not yet been closed, and it is never invoked more than once. An implementation of this method must arrange for any other thread that is blocked in an I/O operation upon this channel to return immediately, either by throwing an exception or by returning normally. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractInterruptibleChannel#isOpen())`()` <br /> | ||

## Protected constructors

### SelectableChannel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SelectableChannel()
```

Initializes a new instance of this class.

## Public methods

### blockingLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun blockingLock(): Any!
```

Retrieves the object upon which the [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#configureBlocking(kotlin.Boolean))and #register methods synchronize. This is often useful in the implementation of adaptors that require a specific blocking mode to be maintained for a short period of time.

| Return ||
|-----------------------------------------------------------------------------|-------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The blocking-mode lock object |

### configureBlocking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun configureBlocking(block: Boolean): SelectableChannel!
```

Adjusts this channel's blocking mode.

If this channel is registered with one or more selectors then an attempt to place it into blocking mode will cause an [IllegalBlockingModeException](https://developer.android.com/reference/kotlin/java/nio/channels/IllegalBlockingModeException) to be thrown.

This method may be invoked at any time. The new blocking mode will only affect I/O operations that are initiated after this method returns. For some implementations this may require blocking until all pending I/O operations are complete.

If this method is invoked while another invocation of this method or of the [register](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int))method is in progress then it will first block until the other operation is complete.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `block` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If`true`then this channel will be placed in blocking mode; if`false`then it will be placed non-blocking mode |

| Return ||
|-----------------------------------------------------------------------------------------------------------|-------------------------|
| [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#)! | This selectable channel |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.IllegalBlockingModeException` | If`block`is`true`and this channel is registered with one or more selectors |
| `java.io.IOException` | If an I/O error occurs |

### isBlocking

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isBlocking(): Boolean
```

Tells whether or not every I/O operation on this channel will block until it completes. A newly-created channel is always in blocking mode.

If this channel is closed then the value returned by this method is not specified.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel is in blocking mode |

### isRegistered

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isRegistered(): Boolean
```

Tells whether or not this channel is currently registered with any selectors. A newly-created channel is not registered.

Due to the inherent delay between key cancellation and channel deregistration, a channel may remain registered for some time after all of its keys have been cancelled. A channel may also remain registered for some time after it is closed.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this channel is registered |

### keyFor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun keyFor(sel: Selector!): SelectionKey!
```

Retrieves the key representing the channel's registration with the given selector.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------|
| `sel` | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!:The selector |

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | The key returned when this channel was last registered with the given selector, or`null`if this channel is not currently registered with that selector |

### provider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun provider(): SelectorProvider!
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
    ops: Int
): SelectionKey!
```

Registers this channel with the given selector, returning a selection key.

An invocation of this convenience method of the form
`sc.register(sel, ops)`behaves in exactly the same way as the invocation`sc.` [register(sel, ops, null)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#register(java.nio.channels.Selector,%20kotlin.Int,%20kotlin.Any))

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `sel` | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!:The selector with which this channel is to be registered |
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interest set for the resulting key |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | A key representing the registration of this channel with the given selector |

| Exceptions ||
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.ClosedSelectorException` | If the selector is closed |
| `java.nio.channels.IllegalBlockingModeException` | If this channel is in blocking mode |
| `java.nio.channels.IllegalSelectorException` | If this channel was not created by the same provider as the given selector |
| `java.nio.channels.CancelledKeyException` | If this channel is currently registered with the given selector but the corresponding key has already been cancelled |
| `java.lang.IllegalArgumentException` | If a bit in`ops`does not correspond to an operation that is supported by this channel, that is, if`set & ~validOps() != 0` |

### register

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun register(
    sel: Selector!, 
    ops: Int, 
    att: Any!
): SelectionKey!
```

Registers this channel with the given selector, returning a selection key.

If this channel is currently registered with the given selector then the selection key representing that registration is returned. The key's interest set will have been changed to`ops`, as if by invoking the [interestOps(int)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOps(kotlin.Int))method. If the`att`argument is not`null`then the key's attachment will have been set to that value. A [CancelledKeyException](https://developer.android.com/reference/kotlin/java/nio/channels/CancelledKeyException) will be thrown if the key has already been cancelled.

Otherwise this channel has not yet been registered with the given selector, so it is registered and the resulting new key is returned. The key's initial interest set will be`ops`and its attachment will be`att`.

This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the new registration or change to the key's interest set will be seen by the next selection operation. If this method is invoked while an invocation of [configureBlocking](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#configureBlocking(kotlin.Boolean))is in progress then it will block until the channel's blocking mode has been adjusted.

If this channel is closed while this operation is in progress then the key returned by this method will have been cancelled and will therefore be invalid.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `sel` | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)!:The selector with which this channel is to be registered |
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interest set for the resulting key |
| `att` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The attachment for the resulting key; may be`null` |

| Return ||
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey)! | A key representing the registration of this channel with the given selector |

| Exceptions ||
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| `java.nio.channels.ClosedChannelException` | If this channel is closed |
| `java.nio.channels.ClosedSelectorException` | If the selector is closed |
| `java.nio.channels.IllegalBlockingModeException` | If this channel is in blocking mode |
| `java.nio.channels.IllegalSelectorException` | If this channel was not created by the same provider as the given selector |
| `java.nio.channels.CancelledKeyException` | If this channel is currently registered with the given selector but the corresponding key has already been cancelled |
| `java.lang.IllegalArgumentException` | If a bit in the`ops`set does not correspond to an operation that is supported by this channel, that is, if`set & ~validOps() != 0` |

### validOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun validOps(): Int
```

Returns an [operation set](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#opsets) identifying this channel's supported operations. The bits that are set in this integer value denote exactly the operations that are valid for this channel. This method always returns the same value for a given concrete channel class.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The valid-operation set |
