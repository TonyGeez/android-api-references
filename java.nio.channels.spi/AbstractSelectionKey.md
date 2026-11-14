Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractSelectionKey

```
abstract class AbstractSelectionKey : SelectionKey
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.nio.channels.SelectionKey](../java/nio/channels/SelectionKey.md) ||
| | ↳ | [java.nio.channels.spi.AbstractSelectionKey](../java/nio/channels/spi/AbstractSelectionKey.md) |

Base implementation class for selection keys.

This class tracks the validity of the key and implements cancellation.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#OP_ACCEPT:kotlin.Int` Operation-set bit for socket-accept operations. Suppose that a selection key's interest set contains `OP_ACCEPT` at the start of a [selection operation](../java/nio/channels/Selector.md). If the selector detects that the corresponding server-socket channel is ready to accept another connection, or has an error pending, then it will add `OP_ACCEPT` to the key's ready set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#OP_CONNECT:kotlin.Int` Operation-set bit for socket-connect operations. Suppose that a selection key's interest set contains `OP_CONNECT` at the start of a [selection operation](../java/nio/channels/Selector.md). If the selector detects that the corresponding socket channel is ready to complete its connection sequence, or has an error pending, then it will add `OP_CONNECT` to the key's ready set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#OP_READ:kotlin.Int` Operation-set bit for read operations. Suppose that a selection key's interest set contains `OP_READ` at the start of a [selection operation](../java/nio/channels/Selector.md). If the selector detects that the corresponding channel is ready for reading, has reached end-of-stream, has been remotely shut down for further reading, or has an error pending, then it will add `OP_READ` to the key's ready-operation set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#OP_WRITE:kotlin.Int` Operation-set bit for write operations. Suppose that a selection key's interest set contains `OP_WRITE` at the start of a [selection operation](../java/nio/channels/Selector.md). If the selector detects that the corresponding channel is ready for writing, has been remotely shut down for further writing, or has an error pending, then it will add `OP_WRITE` to the key's ready set. <br /> | ||

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey#AbstractSelectionKey()()` Initializes a new instance of this class. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey#cancel()()` Cancels this key. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey#isValid()()` Tells whether or not this key is valid. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#attach(kotlin.Any)(ob: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Attaches the given object to this key. An attached object may later be retrieved via the `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#attachment()` method. Only one object may be attached at a time; invoking this method causes any previous attachment to be discarded. The current attachment may be discarded by attaching `null`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#attachment()()` Retrieves the current attachment. <br /> | | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectableChannel.html#!` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#channel()()` Returns the channel for which this key was created. This method will continue to return the channel even after the key is cancelled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#interestOps()()` Retrieves this key's interest set. It is guaranteed that the returned set will only contain operation bits that are valid for this key's channel. <br /> | | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#!` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#interestOps(kotlin.Int)(ops: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets this key's interest set to the given value. This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the change to the key's interest set will be seen by the next selection operation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#interestOpsAnd(kotlin.Int)(ops: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically sets this key's interest set to the bitwise intersection ("and") of the existing interest set and the given value. This method is guaranteed to be atomic with respect to other concurrent calls to this method or to `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#interestOpsOr(kotlin.Int)`. This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the change to the key's interest set will be seen by the next selection operation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#interestOpsOr(kotlin.Int)(ops: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically sets this key's interest set to the bitwise union ("or") of the existing interest set and the given value. This method is guaranteed to be atomic with respect to other concurrent calls to this method or to `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#interestOpsAnd(kotlin.Int)`. This method may be invoked at any time. If this method is invoked while a selection operation is in progress then it has no effect upon that operation; the change to the key's interest set will be seen by the next selection operation. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#isAcceptable()()` Tests whether this key's channel is ready to accept a new socket connection. An invocation of this method of the form `k.isAcceptable()` behaves in exactly the same way as the expression ```kotlin <code>k.readyOps() &amp; OP_ACCEPT != 0 </code> ``` If this key's channel does not support socket-accept operations then this method always returns `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#isConnectable()()` Tests whether this key's channel has either finished, or failed to finish, its socket-connection operation. An invocation of this method of the form `k.isConnectable()` behaves in exactly the same way as the expression ```kotlin <code>k.readyOps() &amp; OP_CONNECT != 0 </code> ``` If this key's channel does not support socket-connect operations then this method always returns `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#isReadable()()` Tests whether this key's channel is ready for reading. An invocation of this method of the form `k.isReadable()` behaves in exactly the same way as the expression ```kotlin <code>k.readyOps() &amp; OP_READ != 0 </code> ``` If this key's channel does not support read operations then this method always returns `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#isWritable()()` Tests whether this key's channel is ready for writing. An invocation of this method of the form `k.isWritable()` behaves in exactly the same way as the expression ```kotlin <code>k.readyOps() &amp; OP_WRITE != 0 </code> ``` If this key's channel does not support write operations then this method always returns `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#readyOps()()` Retrieves this key's ready-operation set. It is guaranteed that the returned set will only contain operation bits that are valid for this key's channel. <br /> | | `https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#!` | `https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#selector()()` Returns the selector for which this key was created. This method will continue to return the selector even after the key is cancelled. <br /> | ||

## Protected constructors

### AbstractSelectionKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AbstractSelectionKey()
```

Initializes a new instance of this class.

## Public methods

### cancel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancel(): Unit
```

Cancels this key.

If this key has not yet been cancelled then it is added to its selector's cancelled-key set while synchronized on that set.

### isValid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isValid(): Boolean
```

Tells whether or not this key is valid.

A key is valid upon creation and remains so until it is cancelled, its channel is closed, or its selector is closed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if, and only if, this key is valid |
