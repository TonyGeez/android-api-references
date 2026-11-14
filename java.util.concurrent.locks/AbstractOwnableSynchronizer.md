Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractOwnableSynchronizer

```
abstract class AbstractOwnableSynchronizer : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.locks.AbstractOwnableSynchronizer](AbstractOwnableSynchronizer.md) |

Known Direct Subclasses [AbstractQueuedLongSynchronizer](AbstractQueuedLongSynchronizer.md), [AbstractQueuedSynchronizer](AbstractQueuedSynchronizer.md) [AbstractQueuedLongSynchronizer](AbstractQueuedLongSynchronizer.md) A version of AbstractQueuedSynchronizer in which synchronization state is maintained as a `long`.
[AbstractQueuedSynchronizer](AbstractQueuedSynchronizer.md) Provides a framework for implementing blocking locks and related synchronizers (semaphores, events, etc) that rely on first-in-first-out (FIFO) wait queues.

A synchronizer that may be exclusively owned by a thread. This class provides a basis for creating locks and related synchronizers that may entail a notion of ownership. The `AbstractOwnableSynchronizer` class itself does not manage or use this information. However, subclasses and tools may use appropriately maintained values to help control and monitor access and provide diagnostics.

## Summary

| Protected constructors ||
|---|---|
| AbstractOwnableSynchronizer Empty constructor for use by subclasses. |

| Protected methods ||
|---|---|
| [Thread](../java.lang/Thread.md)! | getExclusiveOwnerThread Returns the thread last set by `setExclusiveOwnerThread`, or `null` if never set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExclusiveOwnerThread Sets the thread that currently owns exclusive access. |

## Protected constructors

### AbstractOwnableSynchronizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AbstractOwnableSynchronizer()
```

Empty constructor for use by subclasses.

## Protected methods

### getExclusiveOwnerThread

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getExclusiveOwnerThread(): Thread!
```

Returns the thread last set by `setExclusiveOwnerThread`, or `null` if never set. This method does not otherwise impose any synchronization or `volatile` field accesses.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Thread.html#!` | the owner thread |

### setExclusiveOwnerThread

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun setExclusiveOwnerThread(thread: Thread!): Unit
```

Sets the thread that currently owns exclusive access. A `null` argument indicates that no thread owns access. This method does not otherwise impose any synchronization or `volatile` field accesses.

| Parameters ||
|---|---|
| `thread` | [Thread](../java.lang/Thread.md)!: the owner thread |
