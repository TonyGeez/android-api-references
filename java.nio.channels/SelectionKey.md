# SelectionKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectionKey

```
abstract class SelectionKey
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.channels.SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#) |

| Known Direct Subclasses [AbstractSelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey) |-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------| | [AbstractSelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey) | Base implementation class for selection keys. | |
| --- | --- | --- | --- | --- | --- | --- |

A token representing the registration of a [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) with a [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector).

A selection key is created each time a channel is registered with a selector. A key remains valid until it is*cancelled* by invoking its [cancel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#cancel())method, by closing its channel, or by closing its selector. Cancelling a key does not immediately remove it from its selector; it is instead added to the selector's [*cancelled-key set*](https://developer.android.com/reference/kotlin/java/nio/channels/Selector#ks) for removal during the next selection operation. The validity of a key may be tested by invoking its [isValid](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#isValid())method.

A selection key contains two*operation sets*represented as integer values. Each bit of an operation set denotes a category of selectable operations that are supported by the key's channel.

- The*interest set* determines which operation categories will be tested for readiness the next time one of the selector's selection methods is invoked. The interest set is initialized with the value given when the key is created; it may later be changed via the [interestOps(int)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOps(kotlin.Int))method.
- The*ready set*identifies the operation categories for which the key's channel has been detected to be ready by the key's selector. The ready set is initialized to zero when the key is created; it may later be updated by the selector during a selection operation, but it cannot be updated directly.

That a selection key's ready set indicates that its channel is ready for some operation category is a hint, but not a guarantee, that an operation in such a category may be performed by a thread without causing the thread to block. A ready set is most likely to be accurate immediately after the completion of a selection operation. It is likely to be made inaccurate by external events and by I/O operations that are invoked upon the corresponding channel.

This class defines all known operation-set bits, but precisely which bits are supported by a given channel depends upon the type of the channel. Each subclass of [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel) defines an [validOps()](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel#validOps())method which returns a set identifying just those operations that are supported by the channel. An attempt to set or test an operation-set bit that is not supported by a key's channel will result in an appropriate run-time exception.

It is often necessary to associate some application-specific data with a selection key, for example an object that represents the state of a higher-level protocol and handles readiness notifications in order to implement that protocol. Selection keys therefore support the*attachment* of a single arbitrary object to a key. An object can be attached via the [attach](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#attach(kotlin.Any))method and then later retrieved via the [attachment](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#attachment())method.

Selection keys are safe for use by multiple concurrent threads. A selection operation will always use the interest-set value that was current at the moment that the operation began.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_ACCEPT](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_ACCEPT:kotlin.Int) Operation-set bit for socket-accept operations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_CONNECT](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_CONNECT:kotlin.Int) Operation-set bit for socket-connect operations. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_READ](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_READ:kotlin.Int) Operation-set bit for read operations. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OP_WRITE](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#OP_WRITE:kotlin.Int) Operation-set bit for write operations. |

| Protected constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#SelectionKey())`()` Constructs an instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [attach](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#attach(kotlin.Any))`(`ob:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Attaches the given object to this key. |
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [attachment](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#attachment())`()` Retrieves the current attachment. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#cancel())`()` Requests that the registration of this key's channel with its selector be cancelled. |
| --- | --- |
| abstract [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel)! | [channel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#channel())`()` Returns the channel for which this key was created. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [interestOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOps())`()` Retrieves this key's interest set. |
| abstract [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#)! | [interestOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOps(kotlin.Int))`(`ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets this key's interest set to the given value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [interestOpsAnd](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOpsAnd(kotlin.Int))`(`ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets this key's interest set to the bitwise intersection ("and") of the existing interest set and the given value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [interestOpsOr](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOpsOr(kotlin.Int))`(`ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets this key's interest set to the bitwise union ("or") of the existing interest set and the given value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAcceptable](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#isAcceptable())`()` Tests whether this key's channel is ready to accept a new socket connection. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnectable](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#isConnectable())`()` Tests whether this key's channel has either finished, or failed to finish, its socket-connection operation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadable](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#isReadable())`()` Tests whether this key's channel is ready for reading. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#isValid())`()` Tells whether or not this key is valid. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWritable](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#isWritable())`()` Tests whether this key's channel is ready for writing. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readyOps](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#readyOps())`()` Retrieves this key's ready-operation set. |
| abstract [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)! | [selector](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#selector())`()` Returns the selector for which this key was created. |
| --- | --- |

## Constants

### OP_ACCEPT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_ACCEPT: Int
```

Operation-set bit for socket-accept operations.

Suppose that a selection key's interest set contains`OP_ACCEPT`at the start of a [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector#selop). If the selector detects that the corresponding server-socket channel is ready to accept another connection, or has an error pending, then it will add`OP_ACCEPT`to the key's ready set. 

 Value: 16

### OP_CONNECT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_CONNECT: Int
```

Operation-set bit for socket-connect operations.

Suppose that a selection key's interest set contains`OP_CONNECT`at the start of a [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector#selop). If the selector detects that the corresponding socket channel is ready to complete its connection sequence, or has an error pending, then it will add`OP_CONNECT`to the key's ready set. 

 Value: 8

### OP_READ

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_READ: Int
```

Operation-set bit for read operations.

Suppose that a selection key's interest set contains`OP_READ`at the start of a [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector#selop). If the selector detects that the corresponding channel is ready for reading, has reached end-of-stream, has been remotely shut down for further reading, or has an error pending, then it will add`OP_READ`to the key's ready-operation set. 

 Value: 1

### OP_WRITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OP_WRITE: Int
```

Operation-set bit for write operations.

Suppose that a selection key's interest set contains`OP_WRITE`at the start of a [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector#selop). If the selector detects that the corresponding channel is ready for writing, has been remotely shut down for further writing, or has an error pending, then it will add`OP_WRITE`to the key's ready set. 

 Value: 4

## Protected constructors

### SelectionKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected SelectionKey()
```

Constructs an instance of this class.

## Public methods

### attach

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun attach(ob: Any!): Any!
```

Attaches the given object to this key.

An attached object may later be retrieved via the [attachment](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#attachment())method. Only one object may be attached at a time; invoking this method causes any previous attachment to be discarded. The current attachment may be discarded by attaching`null`.

| Parameters ||
|------|---------------------------------------------------------------------------------------------------------------------|
| `ob` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The object to be attached; may be`null` |

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The previously-attached object, if any, otherwise`null` |

### attachment

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun attachment(): Any!
```

Retrieves the current attachment.

| Return ||
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | The object currently attached to this key, or`null`if there is no attachment |

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Requests that the registration of this key's channel with its selector be cancelled. Upon return the key will be invalid and will have been added to its selector's cancelled-key set. The key will be removed from all of the selector's key sets during the next selection operation.

If this key has already been cancelled then invoking this method has no effect. Once cancelled, a key remains forever invalid.

This method may be invoked at any time. It synchronizes on the selector's cancelled-key set, and therefore may block briefly if invoked concurrently with a cancellation or selection operation involving the same selector. 

### channel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun channel(): SelectableChannel!
```

Returns the channel for which this key was created. This method will continue to return the channel even after the key is cancelled.

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------|
| [SelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel)! | This key's channel |

### interestOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun interestOps(): Int
```

Retrieves this key's interest set.

It is guaranteed that the returned set will only contain operation bits that are valid for this key's channel.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | This key's interest set |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### interestOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun interestOps(ops: Int): SelectionKey!
```

Sets this key's interest set to the given value.

This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the change to the key's interest set will be seen by the next selection operation.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------|
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new interest set |

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#)! | This selection key |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If a bit in the set does not correspond to an operation that is supported by this key's channel, that is, if`(ops & ~channel().validOps()) != 0` |
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### interestOpsAnd

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun interestOpsAnd(ops: Int): Int
```

Atomically sets this key's interest set to the bitwise intersection ("and") of the existing interest set and the given value. This method is guaranteed to be atomic with respect to other concurrent calls to this method or to [interestOpsOr(int)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOpsOr(kotlin.Int)).

This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the change to the key's interest set will be seen by the next selection operation.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interest set to apply |

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The previous interest set |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### interestOpsOr

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun interestOpsOr(ops: Int): Int
```

Atomically sets this key's interest set to the bitwise union ("or") of the existing interest set and the given value. This method is guaranteed to be atomic with respect to other concurrent calls to this method or to [interestOpsAnd(int)](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey#interestOpsAnd(kotlin.Int)).

This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the change to the key's interest set will be seen by the next selection operation.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------|
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The interest set to apply |

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The previous interest set |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | If a bit in the set does not correspond to an operation that is supported by this key's channel, that is, if`(ops & ~channel().validOps()) != 0` |
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### isAcceptable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAcceptable(): Boolean
```

Tests whether this key's channel is ready to accept a new socket connection.

An invocation of this method of the form`k.isAcceptable()`behaves in exactly the same way as the expression 

```kotlin
<code>k.readyOps() &amp; OP_ACCEPT != 0
  </code>
```

If this key's channel does not support socket-accept operations then this method always returns`false`.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if,`readyOps() & OP_ACCEPT`is nonzero |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### isConnectable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnectable(): Boolean
```

Tests whether this key's channel has either finished, or failed to finish, its socket-connection operation.

An invocation of this method of the form`k.isConnectable()`behaves in exactly the same way as the expression 

```kotlin
<code>k.readyOps() &amp; OP_CONNECT != 0
  </code>
```

If this key's channel does not support socket-connect operations then this method always returns`false`.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if,`readyOps() & OP_CONNECT`is nonzero |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### isReadable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isReadable(): Boolean
```

Tests whether this key's channel is ready for reading.

An invocation of this method of the form`k.isReadable()`behaves in exactly the same way as the expression 

```kotlin
<code>k.readyOps() &amp; OP_READ != 0
  </code>
```

If this key's channel does not support read operations then this method always returns`false`.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if,`readyOps() & OP_READ`is nonzero |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### isValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(): Boolean
```

Tells whether or not this key is valid.

A key is valid upon creation and remains so until it is cancelled, its channel is closed, or its selector is closed.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this key is valid |

### isWritable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWritable(): Boolean
```

Tests whether this key's channel is ready for writing.

An invocation of this method of the form`k.isWritable()`behaves in exactly the same way as the expression 

```kotlin
<code>k.readyOps() &amp; OP_WRITE != 0
  </code>
```

If this key's channel does not support write operations then this method always returns`false`.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if,`readyOps() & OP_WRITE`is nonzero |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### readyOps

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readyOps(): Int
```

Retrieves this key's ready-operation set.

It is guaranteed that the returned set will only contain operation bits that are valid for this key's channel.

| Return ||
|----------------------------------------------------------------------------|--------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | This key's ready-operation set |

| Exceptions ||
|-------------------------------------------|--------------------------------|
| `java.nio.channels.CancelledKeyException` | If this key has been cancelled |

### selector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun selector(): Selector!
```

Returns the selector for which this key was created. This method will continue to return the selector even after the key is cancelled.

| Return ||
|----------------------------------------------------------------------------------------|---------------------|
| [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector)! | This key's selector |
