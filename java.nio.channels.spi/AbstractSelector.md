# AbstractSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractSelector

```
abstract class AbstractSelector : Selector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.nio.channels.Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#) ||
| | ↳ | [java.nio.channels.spi.AbstractSelector](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#) |

Base implementation class for selectors.

This class encapsulates the low-level machinery required to implement the interruption of selection operations. A concrete selector class must invoke the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#begin())and [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#end())methods before and after, respectively, invoking an I/O operation that might block indefinitely. In order to ensure that the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#end())method is always invoked, these methods should be used within a`try`...`finally`block: 

```kotlin
try {
      begin();
      // Perform blocking I/O operation here
      ...
  } finally {
      end();
  }
```

This class also defines methods for maintaining a selector's cancelled-key set and for removing a key from its channel's key set, and declares the abstract [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#register(java.nio.channels.spi.AbstractSelectableChannel,%20kotlin.Int,%20kotlin.Any))method that is invoked by a selectable channel's java.nio.channels.spi.AbstractSelectableChannel#register method in order to perform the actual work of registering a channel.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractSelector](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#AbstractSelector(java.nio.channels.spi.SelectorProvider))`(`provider:` ` [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!`)` Initializes a new instance of this class. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#close())`()` Closes this selector. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOpen](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#isOpen())`()` <br /> |
| [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | [provider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#provider())`()` Returns the provider that created this channel. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#begin())`()` Marks the beginning of an I/O operation that might block indefinitely. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!\>! | [cancelledKeys](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#cancelledKeys())`()` Retrieves this selector's cancelled-key set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deregister](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#deregister(java.nio.channels.spi.AbstractSelectionKey))`(`key:` ` [AbstractSelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey)!`)` Removes the given key from its channel's key set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#end())`()` Marks the end of an I/O operation that might block indefinitely. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [implCloseSelector](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#implCloseSelector())`()` Closes this selector. |
| abstract [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | [register](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#register(java.nio.channels.spi.AbstractSelectableChannel,%20kotlin.Int,%20kotlin.Any))`(`ch:` ` [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel)!`, `ops:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `att:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Registers the given channel with this selector. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#) |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!>! | [keys](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#keys())`()` <br /> Returns this selector's key set. The key set is not directly modifiable. A key is removed only after it has been cancelled and its channel has been deregistered. Any attempt to modify the key set will cause an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) to be thrown. The set is [safe](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#ksc) for use by multiple concurrent threads. <br /> | | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)! | [open](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#open())`()` <br /> Opens a selector. The new selector is created by invoking the [openSelector](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider#openSelector())method of the system-wide default object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [select](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#select())`()` <br /> Selects a set of keys whose corresponding channels are ready for I/O operations. This method performs a blocking [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selop). It returns only after at least one channel is selected, this selector's [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method is invoked, or the current thread is interrupted, whichever comes first. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [select](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#select(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!>!`)` <br /> Selects and performs an action on the keys whose corresponding channels are ready for I/O operations. This method performs a blocking [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selop). It wakes up from querying the operating system only when at least one channel is selected, this selector's [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method is invoked, or the current thread is interrupted, whichever comes first. This method is equivalent to invoking the 2-arg [select](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#select(java.util.function.Consumer,%20kotlin.Long))method with a timeout of`0`to block indefinitely. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [select](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#select(java.util.function.Consumer,%20kotlin.Long))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!>!`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Selects and performs an action on the keys whose corresponding channels are ready for I/O operations. This method performs a blocking [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selop). It wakes up from querying the operating system only when at least one channel is selected, this selector's [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method is invoked, the current thread is interrupted, or the given timeout period expires, whichever comes first. The specified*action* 's [accept](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#accept(java.util.function.Consumer.T))method is invoked with the key for each channel that is ready to perform an operation identified by its key's interest set. The`accept`method may be invoked more than once for the same key but with the ready-operation set containing a subset of the operations for which the channel is ready (as described above). The`accept`method is invoked while synchronized on the selector and its selected-key set. Great care must be taken to avoid deadlocking with other threads that also synchronize on these objects. Selection operations are not reentrant in general and consequently the*action* should take great care not to attempt a selection operation on the same selector. The behavior when attempting a reentrant selection operation is implementation specific and therefore not specified. If the*action* closes the selector then`ClosedSelectorException`is thrown when the action completes. The*action* is not prohibited from closing channels registered with the selector, nor prohibited from cancelling keys or changing a key's interest set. If a channel is selected but its key is cancelled or its interest set changed before the*action* is performed on the key then it is implementation specific as to whether the*action* is invoked (it may be invoked with an [invalid](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#isValid())key). Exceptions thrown by the action are relayed to the caller. This method does not offer real-time guarantees: It schedules the timeout as if by invoking the [Object.wait(long)](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long))method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [select](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#select(kotlin.Long))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Selects a set of keys whose corresponding channels are ready for I/O operations. This method performs a blocking [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selop). It returns only after at least one channel is selected, this selector's [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method is invoked, the current thread is interrupted, or the given timeout period expires, whichever comes first. This method does not offer real-time guarantees: It schedules the timeout as if by invoking the [Object.wait(long)](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait(kotlin.Long))method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [selectNow](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selectNow())`()` <br /> Selects a set of keys whose corresponding channels are ready for I/O operations. This method performs a non-blocking [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selop). If no channels have become selectable since the previous selection operation then this method immediately returns zero. Invoking this method clears the effect of any previous invocations of the [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [selectNow](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selectNow(java.util.function.Consumer))`(`action:` ` [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!>!`)` <br /> Selects and performs an action on the keys whose corresponding channels are ready for I/O operations. This method performs a non-blocking [selection operation](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selop). Invoking this method clears the effect of any previous invocations of the [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method. <br /> | | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!>! | [selectedKeys](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selectedKeys())`()` <br /> Returns this selector's selected-key set. Keys may be removed from, but not directly added to, the selected-key set. Any attempt to add an object to the key set will cause an [UnsupportedOperationException](https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#) to be thrown. The selected-key set is [not thread-safe](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#sksc). <br /> | | [Selector](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#)! | [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())`()` <br /> Causes the first selection operation that has not yet returned to return immediately. If another thread is currently blocked in a selection operation then that invocation will return immediately. If no selection operation is currently in progress then the next invocation of a selection operation will return immediately unless [selectNow()](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selectNow())or [selectNow(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#selectNow(java.util.function.Consumer))is invoked in the meantime. In any case the value returned by that invocation may be non-zero. Subsequent selection operations will block as usual unless this method is invoked again in the meantime. Invoking this method more than once between two successive selection operations has the same effect as invoking it just once. <br /> | ||

## Protected constructors

### AbstractSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractSelector(provider: SelectorProvider!)
```

Initializes a new instance of this class.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `provider` | [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)!:The provider that created this selector |

## Public methods

### close

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun close(): Unit
```

Closes this selector.

If the selector has already been closed then this method returns immediately. Otherwise it marks the selector as closed and then invokes the [implCloseSelector](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#implCloseSelector())method in order to complete the close operation.

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
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this selector is open |

### provider

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun provider(): SelectorProvider!
```

Returns the provider that created this channel.

| Return ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------|
| [SelectorProvider](https://developer.android.com/reference/kotlin/java/nio/channels/spi/SelectorProvider)! | The provider that created this channel |

## Protected methods

### begin

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun begin(): Unit
```

Marks the beginning of an I/O operation that might block indefinitely.

This method should be invoked in tandem with the [end](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#end())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#be), in order to implement interruption for this selector.

Invoking this method arranges for the selector's [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method to be invoked if a thread's [interrupt](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())method is invoked while the thread is blocked in an I/O operation upon the selector. 

### cancelledKeys

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun cancelledKeys(): MutableSet<SelectionKey!>!
```

Retrieves this selector's cancelled-key set.

This set should only be used while synchronized upon it.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)!>! | The cancelled-key set |

### deregister

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun deregister(key: AbstractSelectionKey!): Unit
```

Removes the given key from its channel's key set.

This method must be invoked by the selector for each channel that it deregisters.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `key` | [AbstractSelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectionKey)!:The selection key to be removed |

### end

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected fun end(): Unit
```

Marks the end of an I/O operation that might block indefinitely.

This method should be invoked in tandem with the [begin](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#begin())method, using a`try`...`finally`block as shown [above](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelector#be), in order to implement interruption for this selector. 

### implCloseSelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun implCloseSelector(): Unit
```

Closes this selector.

This method is invoked by the #close method in order to perform the actual work of closing the selector. This method is only invoked if the selector has not yet been closed, and it is never invoked more than once.

An implementation of this method must arrange for any other thread that is blocked in a selection operation upon this selector to return immediately as if by invoking the [wakeup](https://developer.android.com/reference/kotlin/java/nio/channels/Selector.html#wakeup())method.

| Exceptions ||
|-----------------------|---------------------------------------------------|
| `java.io.IOException` | If an I/O error occurs while closing the selector |

### register

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun register(
    ch: AbstractSelectableChannel!, 
    ops: Int, 
    att: Any!
): SelectionKey!
```

Registers the given channel with this selector.

This method is invoked by a channel's java.nio.channels.spi.AbstractSelectableChannel#register method in order to perform the actual work of registering the channel with this selector.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ch` | [AbstractSelectableChannel](https://developer.android.com/reference/kotlin/java/nio/channels/spi/AbstractSelectableChannel)!:The channel to be registered |
| `ops` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The initial interest set, which must be valid |
| `att` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!:The initial attachment for the resulting key |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [SelectionKey](https://developer.android.com/reference/kotlin/java/nio/channels/SelectionKey.html#)! | A new key representing the registration of the given channel with this selector |
