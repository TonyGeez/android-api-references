Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractQueuedLongSynchronizer

```
abstract class AbstractQueuedLongSynchronizer : AbstractOwnableSynchronizer, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.concurrent.locks.AbstractOwnableSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer) ||
| | ↳ | [java.util.concurrent.locks.AbstractQueuedLongSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#) |

A version of `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer` in which synchronization state is maintained as a `long`. This class has exactly the same structure, properties, and methods as `AbstractQueuedSynchronizer` with the exception that all state-related parameters and results are defined as `long` rather than `int`. This class may be useful when creating synchronizers such as multilevel locks and barriers that require 64 bits of state.

See `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer` for usage notes and examples.

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject` Condition implementation for a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#` serving as the basis of a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock` implementation. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#AbstractQueuedLongSynchronizer()()` Constructor for subclasses to call. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#acquire(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Acquires in exclusive mode, ignoring interrupts. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#acquireInterruptibly(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Acquires in exclusive mode, aborting if interrupted. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#acquireShared(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Acquires in shared mode, ignoring interrupts. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#acquireSharedInterruptibly(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Acquires in shared mode, aborting if interrupted. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getExclusiveQueuedThreads()()` Returns a collection containing threads that may be waiting to acquire in exclusive mode. |
| [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getFirstQueuedThread()()` Returns the first (longest-waiting) thread in the queue, or `null` if no threads are currently queued. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getQueueLength()()` Returns an estimate of the number of threads waiting to acquire. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getQueuedThreads()()` Returns a collection containing threads that may be waiting to acquire. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getSharedQueuedThreads()()` Returns a collection containing threads that may be waiting to acquire in shared mode. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getWaitQueueLength(java.util.concurrent.locks.AbstractQueuedLongSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject!)` Returns an estimate of the number of threads waiting on the given condition associated with this synchronizer. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getWaitingThreads(java.util.concurrent.locks.AbstractQueuedLongSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject!)` Returns a collection containing those threads that may be waiting on the given condition associated with this synchronizer. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#hasContended()()` Queries whether any threads have ever contended to acquire this synchronizer; that is, if an acquire method has ever blocked. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#hasQueuedPredecessors()()` Queries whether any threads have been waiting to acquire longer than the current thread. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#hasQueuedThreads()()` Queries whether any threads are waiting to acquire. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#hasWaiters(java.util.concurrent.locks.AbstractQueuedLongSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject!)` Queries whether any threads are waiting on the given condition associated with this synchronizer. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#isQueued(java.lang.Thread)(thread: https://developer.android.com/reference/kotlin/java/lang/Thread.html#!)` Returns true if the given thread is currently queued. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#owns(java.util.concurrent.locks.AbstractQueuedLongSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject!)` Queries whether the given ConditionObject uses this synchronizer as its lock. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#release(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Releases in exclusive mode. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#releaseShared(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Releases in shared mode. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#toString()()` Returns a string identifying this synchronizer, as well as its state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireNanos(kotlin.Long,%20kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, nanosTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to acquire in exclusive mode, aborting if interrupted, and failing if the given timeout elapses. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireSharedNanos(kotlin.Long,%20kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, nanosTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to acquire in shared mode, aborting if interrupted, and failing if the given timeout elapses. |

| Protected methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#compareAndSetState(kotlin.Long,%20kotlin.Long)(expect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, update: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically sets synchronization state to the given updated value if the current state value equals the expected value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getState()()` Returns the current value of synchronization state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#isHeldExclusively()()` Returns `true` if synchronization is held exclusively with respect to the current (calling) thread. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#setState(kotlin.Long)(newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the value of synchronization state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to acquire in exclusive mode. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to acquire in shared mode. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryRelease(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to set the state to reflect a release in exclusive mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryReleaseShared(kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to set the state to reflect a release in shared mode. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#!` `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer#getExclusiveOwnerThread()()`

Returns the thread last set by `setExclusiveOwnerThread`, or `null` if never set. This method does not otherwise impose any synchronization or `volatile` field accesses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer#setExclusiveOwnerThread(java.lang.Thread)(thread: https://developer.android.com/reference/kotlin/java/lang/Thread.html#!)`

Sets the thread that currently owns exclusive access. A `null` argument indicates that no thread owns access. This method does not otherwise impose any synchronization or `volatile` field accesses.

<br />

## Protected constructors

### AbstractQueuedLongSynchronizer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AbstractQueuedLongSynchronizer()
```

Constructor for subclasses to call.

## Public methods

### acquire

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquire(arg: Long): Unit
```

Acquires in exclusive mode, ignoring interrupts. Implemented by invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` until success. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#lock()`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |

### acquireInterruptibly

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquireInterruptibly(arg: Long): Unit
```

Acquires in exclusive mode, aborting if interrupted. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` until success or the thread is interrupted. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#lockInterruptibly()`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### acquireShared

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquireShared(arg: Long): Unit
```

Acquires in shared mode, ignoring interrupts. Implemented by first invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` until success.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |

### acquireSharedInterruptibly

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquireSharedInterruptibly(arg: Long): Unit
```

Acquires in shared mode, aborting if interrupted. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` until success or the thread is interrupted.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### getExclusiveQueuedThreads

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExclusiveQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire in exclusive mode. This has the same properties as `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getQueuedThreads()` except that it only returns those threads waiting due to an exclusive acquire.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

### getFirstQueuedThread

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFirstQueuedThread(): Thread!
```

Returns the first (longest-waiting) thread in the queue, or `null` if no threads are currently queued.

In this implementation, this operation normally returns in constant time, but may iterate upon contention if other threads are concurrently modifying the queue.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Thread.html#!` | the first (longest-waiting) thread in the queue, or `null` if no threads are currently queued |

### getQueueLength

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQueueLength(): Int
```

Returns an estimate of the number of threads waiting to acquire. The value is only an estimate because the number of threads may change dynamically while this method traverses internal data structures. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the estimated number of threads waiting to acquire |

### getQueuedThreads

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive monitoring facilities.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

### getSharedQueuedThreads

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSharedQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire in shared mode. This has the same properties as `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getQueuedThreads()` except that it only returns those threads waiting due to a shared acquire.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

### getWaitQueueLength

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWaitQueueLength(condition: AbstractQueuedLongSynchronizer.ConditionObject!): Int
```

Returns an estimate of the number of threads waiting on the given condition associated with this synchronizer. Note that because timeouts and interrupts may occur at any time, the estimate serves only as an upper bound on the actual number of waiters. This method is designed for use in monitoring system state, not for synchronization control.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedLongSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the estimated number of waiting threads |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this synchronizer |
| `java.lang.IllegalMonitorStateException` | if exclusive synchronization is not held |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |

### getWaitingThreads

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWaitingThreads(condition: AbstractQueuedLongSynchronizer.ConditionObject!): MutableCollection<Thread!>!
```

Returns a collection containing those threads that may be waiting on the given condition associated with this synchronizer. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedLongSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this synchronizer |
| `java.lang.IllegalMonitorStateException` | if exclusive synchronization is not held |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |

### hasContended

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasContended(): Boolean
```

Queries whether any threads have ever contended to acquire this synchronizer; that is, if an acquire method has ever blocked.

In this implementation, this operation returns in constant time.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there has ever been contention |

### hasQueuedPredecessors

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasQueuedPredecessors(): Boolean
```

Queries whether any threads have been waiting to acquire longer than the current thread.

An invocation of this method is equivalent to (but may be more efficient than):

```kotlin
<code>getFirstQueuedThread() != Thread.currentThread()
    &amp;&amp; hasQueuedThreads()</code>
```

Note that because cancellations due to interrupts and timeouts may occur at any time, a `true` return does not guarantee that some other thread will acquire before the current thread. Likewise, it is possible for another thread to win a race to enqueue after this method has returned `false`, due to the queue being empty.

This method is designed to be used by a fair synchronizer to avoid [barging](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#barging). Such a synchronizer's `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` method should return `false`, and its `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` method should return a negative value, if this method returns `true` (unless this is a reentrant acquire). For example, the `tryAcquire` method for a fair, reentrant, exclusive mode synchronizer might look like this:

```kotlin
<code>protected boolean tryAcquire(long arg) {
    if (isHeldExclusively()) {
      // A reentrant acquire; increment hold count
      return true;
    } else if (hasQueuedPredecessors()) {
      return false;
    } else {
      // try to acquire normally
    }
  }</code>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there is a queued thread preceding the current thread, and `false` if the current thread is at the head of the queue or the queue is empty |

### hasQueuedThreads

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasQueuedThreads(): Boolean
```

Queries whether any threads are waiting to acquire. Note that because cancellations due to interrupts and timeouts may occur at any time, a `true` return does not guarantee that any other thread will ever acquire.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there may be other threads waiting to acquire |

### hasWaiters

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasWaiters(condition: AbstractQueuedLongSynchronizer.ConditionObject!): Boolean
```

Queries whether any threads are waiting on the given condition associated with this synchronizer. Note that because timeouts and interrupts may occur at any time, a `true` return does not guarantee that a future `signal` will awaken any threads. This method is designed primarily for use in monitoring of the system state.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedLongSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there are any waiting threads |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this synchronizer |
| `java.lang.IllegalMonitorStateException` | if exclusive synchronization is not held |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |

### isQueued

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isQueued(thread: Thread!): Boolean
```

Returns true if the given thread is currently queued.

This implementation traverses the queue to determine presence of the given thread.

| Parameters ||
|---|---|
| `thread` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!: the thread |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the given thread is on the queue |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the thread is null |

### owns

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun owns(condition: AbstractQueuedLongSynchronizer.ConditionObject!): Boolean
```

Queries whether the given ConditionObject uses this synchronizer as its lock.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedLongSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if owned |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the condition is null |

### release

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(arg: Long): Boolean
```

Releases in exclusive mode. Implemented by unblocking one or more threads if `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryRelease(kotlin.Long)` returns true. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#unlock()`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the release argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryRelease(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value returned from `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryRelease(kotlin.Long)` |

### releaseShared

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun releaseShared(arg: Long): Boolean
```

Releases in shared mode. Implemented by unblocking one or more threads if `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryReleaseShared(kotlin.Long)` returns true.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the release argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryReleaseShared(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value returned from `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryReleaseShared(kotlin.Long)` |

### toString

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string identifying this synchronizer, as well as its state. The state, in brackets, includes the String `"State ="` followed by the current value of `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#getState()`, and either `"nonempty"` or `"empty"` depending on whether the queue is empty.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string identifying this synchronizer, as well as its state |

### tryAcquireNanos

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun tryAcquireNanos(
    arg: Long, 
    nanosTimeout: Long
): Boolean
```

Attempts to acquire in exclusive mode, aborting if interrupted, and failing if the given timeout elapses. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)`, returning on success. Otherwise, the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` until success or the thread is interrupted or the timeout elapses. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#tryLock(kotlin.Long,%20java.util.concurrent.TimeUnit)`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquire(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |
| `nanosTimeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum number of nanoseconds to wait |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if acquired; `false` if timed out |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### tryAcquireSharedNanos

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun tryAcquireSharedNanos(
    arg: Long, 
    nanosTimeout: Long
): Boolean
```

Attempts to acquire in shared mode, aborting if interrupted, and failing if the given timeout elapses. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)`, returning on success. Otherwise, the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` until success or the thread is interrupted or the timeout elapses.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer#tryAcquireShared(kotlin.Long)` but is otherwise uninterpreted and can represent anything you like. |
| `nanosTimeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum number of nanoseconds to wait |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if acquired; `false` if timed out |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

## Protected methods

### compareAndSetState

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun compareAndSetState(
    expect: Long, 
    update: Long
): Boolean
```

Atomically sets synchronization state to the given updated value if the current state value equals the expected value. This operation has memory semantics of a `volatile` read and write.

| Parameters ||
|---|---|
| `expect` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `update` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful. False return indicates that the actual value was not equal to the expected value. |

### getState

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getState(): Long
```

Returns the current value of synchronization state. This operation has memory semantics of a `volatile` read.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | current state value |

### isHeldExclusively

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun isHeldExclusively(): Boolean
```

Returns `true` if synchronization is held exclusively with respect to the current (calling) thread. This method is invoked upon each call to a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject` method.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. This method is invoked internally only within `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject` methods, so need not be defined if conditions are not used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if synchronization is held exclusively; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if conditions are not supported |

### setState

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun setState(newState: Long): Unit
```

Sets the value of synchronization state. This operation has memory semantics of a `volatile` write.

| Parameters ||
|---|---|
| `newState` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new state value |

### tryAcquire

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryAcquire(arg: Long): Boolean
```

Attempts to acquire in exclusive mode. This method should query if the state of the object permits it to be acquired in the exclusive mode, and if so to acquire it.

This method is always invoked by the thread performing acquire. If this method reports failure, the acquire method may queue the thread, if it is not already queued, until it is signalled by a release from some other thread. This can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#tryLock()`.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is always the one passed to an acquire method, or is the value saved on entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful. Upon success, this object has been acquired. |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if acquiring would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if exclusive mode is not supported |

### tryAcquireShared

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryAcquireShared(arg: Long): Long
```

Attempts to acquire in shared mode. This method should query if the state of the object permits it to be acquired in the shared mode, and if so to acquire it.

This method is always invoked by the thread performing acquire. If this method reports failure, the acquire method may queue the thread, if it is not already queued, until it is signalled by a release from some other thread.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the acquire argument. This value is always the one passed to an acquire method, or is the value saved on entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | a negative value on failure; zero if acquisition in shared mode succeeded but no subsequent shared-mode acquire can succeed; and a positive value if acquisition in shared mode succeeded and subsequent shared-mode acquires might also succeed, in which case a subsequent waiting thread must check availability. (Support for three different return values enables this method to be used in contexts where acquires only sometimes act exclusively.) Upon success, this object has been acquired. |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if acquiring would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if shared mode is not supported |

### tryRelease

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryRelease(arg: Long): Boolean
```

Attempts to set the state to reflect a release in exclusive mode.

This method is always invoked by the thread performing release.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the release argument. This value is always the one passed to a release method, or the current state value upon entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is now in a fully released state, so that any waiting threads may attempt to acquire; and `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if releasing would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if exclusive mode is not supported |

### tryReleaseShared

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryReleaseShared(arg: Long): Boolean
```

Attempts to set the state to reflect a release in shared mode.

This method is always invoked by the thread performing release.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the release argument. This value is always the one passed to a release method, or the current state value upon entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this release of shared mode may permit a waiting acquire (shared or exclusive) to succeed; and `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if releasing would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if shared mode is not supported |
