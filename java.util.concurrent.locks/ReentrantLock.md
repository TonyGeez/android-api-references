# ReentrantLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReentrantLock

```
open class ReentrantLock : Lock, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.locks.ReentrantLock](ReentrantLock.md) |

A reentrant mutual exclusion [Lock](Lock.md) with the same basic behavior and semantics as the implicit monitor lock accessed using`synchronized`methods and statements, but with extended capabilities.

A`ReentrantLock`is*owned* by the thread last successfully locking, but not yet unlocking it. A thread invoking`lock`will return, successfully acquiring the lock, when the lock is not owned by another thread. The method will return immediately if the current thread already owns the lock. This can be checked using methods [isHeldByCurrentThread](ReentrantLock.md)), and [getHoldCount](ReentrantLock.md)).

The constructor for this class accepts an optional*fairness* parameter. When set`true`, under contention, locks favor granting access to the longest-waiting thread. Otherwise this lock does not guarantee any particular access order. Programs using fair locks accessed by many threads may display lower overall throughput (i.e., are slower; often much slower) than those using the default setting, but have smaller variances in times to obtain locks and guarantee lack of starvation. Note however, that fairness of locks does not guarantee fairness of thread scheduling. Thus, one of many threads using a fair lock may obtain it multiple times in succession while other active threads are not progressing and not currently holding the lock. Also note that the untimed [tryLock()](ReentrantLock.md))method does not honor the fairness setting. It will succeed if the lock is available even if other threads are waiting.

It is recommended practice to*always* immediately follow a call to`lock`with a`try`block, most typically in a before/after construction such as: 

```kotlin
<code>class X {
    private final ReentrantLock lock = new ReentrantLock();
    // ...
 
    public void m() {
      lock.lock();  // block until condition holds
      try {
        // ... method body
      } finally {
        lock.unlock();
      }
    }
  }</code>
```

In addition to implementing the [Lock](Lock.md) interface, this class defines a number of`public`and`protected`methods for inspecting the state of the lock. Some of these methods are only useful for instrumentation and monitoring.

Serialization of this class behaves in the same way as built-in locks: a deserialized lock is in the unlocked state, regardless of its state when serialized.

This lock supports a maximum of 2147483647 recursive locks by the same thread. Attempts to exceed this limit result in [Error](../java.lang/Error.md) throws from locking methods.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReentrantLock](ReentrantLock.md))`()` Creates an instance of`ReentrantLock`. |
| [ReentrantLock](ReentrantLock.md))`(`fair:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates an instance of`ReentrantLock`with the given fairness policy. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHoldCount](ReentrantLock.md))`()` Queries the number of holds on this lock by the current thread. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueueLength](ReentrantLock.md))`()` Returns an estimate of the number of threads waiting to acquire this lock. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWaitQueueLength](ReentrantLock.md))`(`condition:` ` [Condition](Condition.md)!`)` Returns an estimate of the number of threads waiting on the given condition associated with this lock. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasQueuedThread](ReentrantLock.md))`(`thread:` ` [Thread](../java.lang/Thread.md)!`)` Queries whether the given thread is waiting to acquire this lock. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasQueuedThreads](ReentrantLock.md))`()` Queries whether any threads are waiting to acquire this lock. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWaiters](ReentrantLock.md))`(`condition:` ` [Condition](Condition.md)!`)` Queries whether any threads are waiting on the given condition associated with this lock. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFair](ReentrantLock.md))`()` Returns`true`if this lock has fairness set true. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isHeldByCurrentThread](ReentrantLock.md))`()` Queries if this lock is held by the current thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLocked](ReentrantLock.md))`()` Queries if this lock is held by any thread. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lock](ReentrantLock.md))`()` Acquires the lock. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lockInterruptibly](ReentrantLock.md))`()` Acquires the lock unless the current thread is [interrupted](../java.lang/Thread.md)). |
| open [Condition](Condition.md)! | [newCondition](ReentrantLock.md))`()` Returns a [Condition](Condition.md) instance for use with this [Lock](Lock.md) instance. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](ReentrantLock.md))`()` Returns a string identifying this lock, as well as its lock state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryLock](ReentrantLock.md))`()` Acquires the lock only if it is not held by another thread at the time of invocation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryLock](ReentrantLock.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java.util.concurrent/TimeUnit.md)!`)` Acquires the lock if it is not held by another thread within the given waiting time and the current thread has not been [interrupted](../java.lang/Thread.md)). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlock](ReentrantLock.md))`()` Attempts to release this lock. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Thread](../java.lang/Thread.md)! | [getOwner](ReentrantLock.md))`()` Returns the thread that currently owns this lock, or`null`if not owned. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](../java.lang/Thread.md)!\>! | [getQueuedThreads](ReentrantLock.md))`()` Returns a collection containing threads that may be waiting to acquire this lock. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](../java.lang/Thread.md)!\>! | [getWaitingThreads](ReentrantLock.md))`(`condition:` ` [Condition](Condition.md)!`)` Returns a collection containing those threads that may be waiting on the given condition associated with this lock. |
| --- | --- |

## Public constructors

### ReentrantLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReentrantLock()
```

Creates an instance of`ReentrantLock`. This is equivalent to using`ReentrantLock(false)`. 

### ReentrantLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReentrantLock(fair: Boolean)
```

Creates an instance of`ReentrantLock`with the given fairness policy.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `fair` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if this lock should use a fair ordering policy |

## Public methods

### getHoldCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHoldCount(): Int
```

Queries the number of holds on this lock by the current thread.

A thread has a hold on a lock for each lock action that is not matched by an unlock action.

The hold count information is typically only used for testing and debugging purposes. For example, if a certain section of code should not be entered with the lock already held then we can assert that fact: 

```kotlin
<code>class X {
    final ReentrantLock lock = new ReentrantLock();
    // ...
    public void m() {
      assert lock.getHoldCount() == 0;
      lock.lock();
      try {
        // ... method body
      } finally {
        lock.unlock();
      }
    }
  }</code>
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of holds on this lock by the current thread, or zero if this lock is not held by the current thread |

### getQueueLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQueueLength(): Int
```

Returns an estimate of the number of threads waiting to acquire this lock. The value is only an estimate because the number of threads may change dynamically while this method traverses internal data structures. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the estimated number of threads waiting for this lock |

### getWaitQueueLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWaitQueueLength(condition: Condition!): Int
```

Returns an estimate of the number of threads waiting on the given condition associated with this lock. Note that because timeouts and interrupts may occur at any time, the estimate serves only as an upper bound on the actual number of waiters. This method is designed for use in monitoring of the system state, not for synchronization control.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `condition` | [Condition](Condition.md)!:the condition |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the estimated number of waiting threads |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if this lock is not held |
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this lock |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |

### hasQueuedThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasQueuedThread(thread: Thread!): Boolean
```

Queries whether the given thread is waiting to acquire this lock. Note that because cancellations may occur at any time, a`true`return does not guarantee that this thread will ever acquire this lock. This method is designed primarily for use in monitoring of the system state.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `thread` | [Thread](../java.lang/Thread.md)!:the thread |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the given thread is queued waiting for this lock |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if the thread is null |

### hasQueuedThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasQueuedThreads(): Boolean
```

Queries whether any threads are waiting to acquire this lock. Note that because cancellations may occur at any time, a`true`return does not guarantee that any other thread will ever acquire this lock. This method is designed primarily for use in monitoring of the system state.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there may be other threads waiting to acquire the lock |

### hasWaiters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasWaiters(condition: Condition!): Boolean
```

Queries whether any threads are waiting on the given condition associated with this lock. Note that because timeouts and interrupts may occur at any time, a`true`return does not guarantee that a future`signal`will awaken any threads. This method is designed primarily for use in monitoring of the system state.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `condition` | [Condition](Condition.md)!:the condition |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there are any waiting threads |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if this lock is not held |
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this lock |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |

### isFair

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFair(): Boolean
```

Returns`true`if this lock has fairness set true.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this lock has fairness set true |

### isHeldByCurrentThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isHeldByCurrentThread(): Boolean
```

Queries if this lock is held by the current thread.

Analogous to the [Thread.holdsLock(Object)](../java.lang/Thread.md))method for built-in monitor locks, this method is typically used for debugging and testing. For example, a method that should only be called while a lock is held can assert that this is the case: 

```kotlin
<code>class X {
    final ReentrantLock lock = new ReentrantLock();
    // ...
 
    public void m() {
        assert lock.isHeldByCurrentThread();
        // ... method body
    }
  }</code>
```

It can also be used to ensure that a reentrant lock is used in a non-reentrant manner, for example: 

```kotlin
<code>class X {
    final ReentrantLock lock = new ReentrantLock();
    // ...
 
    public void m() {
        assert !lock.isHeldByCurrentThread();
        lock.lock();
        try {
            // ... method body
        } finally {
            lock.unlock();
        }
    }
  }</code>
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if current thread holds this lock and`false`otherwise |

### isLocked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLocked(): Boolean
```

Queries if this lock is held by any thread. This method is designed for use in monitoring of the system state, not for synchronization control.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any thread holds this lock and`false`otherwise |

### lock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lock(): Unit
```

Acquires the lock.

Acquires the lock if it is not held by another thread and returns immediately, setting the lock hold count to one.

If the current thread already holds the lock then the hold count is incremented by one and the method returns immediately.

If the lock is held by another thread then the current thread becomes disabled for thread scheduling purposes and lies dormant until the lock has been acquired, at which time the lock hold count is set to one. 

### lockInterruptibly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lockInterruptibly(): Unit
```

Acquires the lock unless the current thread is [interrupted](../java.lang/Thread.md)).

Acquires the lock if it is not held by another thread and returns immediately, setting the lock hold count to one.

If the current thread already holds this lock then the hold count is incremented by one and the method returns immediately.

If the lock is held by another thread then the current thread becomes disabled for thread scheduling purposes and lies dormant until one of two things happens:

- The lock is acquired by the current thread; or
- Some other thread [interrupts](../java.lang/Thread.md))the current thread.

If the lock is acquired by the current thread then the lock hold count is set to one.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](../java.lang/Thread.md))while acquiring the lock,

then [InterruptedException](../java.lang/InterruptedException.md) is thrown and the current thread's interrupted status is cleared.

In this implementation, as this method is an explicit interruption point, preference is given to responding to the interrupt over normal or reentrant acquisition of the lock.

| Exceptions ||
|----------------------------------|--------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### newCondition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun newCondition(): Condition!
```

Returns a [Condition](Condition.md) instance for use with this [Lock](Lock.md) instance.

The returned [Condition](Condition.md) instance supports the same usages as do the [Object](../java.lang/Object.md) monitor methods ([wait](../java.lang/Object.md)), [notify](../java.lang/Object.md)), and [notifyAll](../java.lang/Object.md))) when used with the built-in monitor lock.

- If this lock is not held when any of the [Condition](Condition.md) [waiting](Condition.md))or [signalling](Condition.md))methods are called, then an [IllegalMonitorStateException](../java.lang/IllegalMonitorStateException.md) is thrown.
- When the condition [waiting](Condition.md))methods are called the lock is released and, before they return, the lock is reacquired and the lock hold count restored to what it was when the method was called.
- If a thread is [interrupted](../java.lang/Thread.md))while waiting then the wait will terminate, an [InterruptedException](../java.lang/InterruptedException.md) will be thrown, and the thread's interrupted status will be cleared.
- Waiting threads are signalled in FIFO order.
- The ordering of lock reacquisition for threads returning from waiting methods is the same as for threads initially acquiring the lock, which is in the default case not specified, but for*fair*locks favors those threads that have been waiting the longest.

| Return ||
|---------------------------------------------------------------------------------------------------|----------------------|
| [Condition](Condition.md)! | the Condition object |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this`Lock`implementation does not support conditions |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string identifying this lock, as well as its lock state. The state, in brackets, includes either the String`"Unlocked"`or the String`"Locked by"`followed by the [name](../java.lang/Thread.md))of the owning thread.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string identifying this lock, as well as its lock state |

### tryLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryLock(): Boolean
```

Acquires the lock only if it is not held by another thread at the time of invocation.

Acquires the lock if it is not held by another thread and returns immediately with the value`true`, setting the lock hold count to one. Even when this lock has been set to use a fair ordering policy, a call to`tryLock()`*will* immediately acquire the lock if it is available, whether or not other threads are currently waiting for the lock. This "barging" behavior can be useful in certain circumstances, even though it breaks fairness. If you want to honor the fairness setting for this lock, then use [tryLock(0, TimeUnit.SECONDS)](ReentrantLock.md))which is almost equivalent (it also detects interruption).

If the current thread already holds this lock then the hold count is incremented by one and the method returns`true`.

If the lock is held by another thread then this method will return immediately with the value`false`.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the lock was free and was acquired by the current thread, or the lock was already held by the current thread; and`false`otherwise |

### tryLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryLock(
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Acquires the lock if it is not held by another thread within the given waiting time and the current thread has not been [interrupted](../java.lang/Thread.md)).

Acquires the lock if it is not held by another thread and returns immediately with the value`true`, setting the lock hold count to one. If this lock has been set to use a fair ordering policy then an available lock*will not* be acquired if any other threads are waiting for the lock. This is in contrast to the [tryLock()](ReentrantLock.md))method. If you want a timed`tryLock`that does permit barging on a fair lock then combine the timed and un-timed forms together: 

```kotlin
<code>if (lock.tryLock() ||
      lock.tryLock(timeout, unit)) {
    ...
  }</code>
```

If the current thread already holds this lock then the hold count is incremented by one and the method returns`true`.

If the lock is held by another thread then the current thread becomes disabled for thread scheduling purposes and lies dormant until one of three things happens:

- The lock is acquired by the current thread; or
- Some other thread [interrupts](../java.lang/Thread.md))the current thread; or
- The specified waiting time elapses

If the lock is acquired then the value`true`is returned and the lock hold count is set to one.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](../java.lang/Thread.md))while acquiring the lock,

then [InterruptedException](../java.lang/InterruptedException.md) is thrown and the current thread's interrupted status is cleared.

If the specified waiting time elapses then the value`false`is returned. If the time is less than or equal to zero, the method will not wait at all.

In this implementation, as this method is an explicit interruption point, preference is given to responding to the interrupt over normal or reentrant acquisition of the lock, and over reporting the elapse of the waiting time.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------|
| `time` | the maximum time to wait for the lock |
| `unit` | [TimeUnit](../java.util.concurrent/TimeUnit.md)!:the time unit of the timeout argument |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the time to wait for the lock |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the lock was free and was acquired by the current thread, or the lock was already held by the current thread; and`false`if the waiting time elapsed before the lock could be acquired |

| Exceptions ||
|----------------------------------|--------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted |
| `java.lang.NullPointerException` | if the time unit is null |

### unlock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlock(): Unit
```

Attempts to release this lock.

If the current thread is the holder of this lock then the hold count is decremented. If the hold count is now zero then the lock is released. If the current thread is not the holder of this lock then [IllegalMonitorStateException](../java.lang/IllegalMonitorStateException.md) is thrown.

| Exceptions ||
|------------------------------------------|-----------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if the current thread does not hold this lock |

## Protected methods

### getOwner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getOwner(): Thread!
```

Returns the thread that currently owns this lock, or`null`if not owned. When this method is called by a thread that is not the owner, the return value reflects a best-effort approximation of current lock status. For example, the owner may be momentarily`null`even if there are threads trying to acquire the lock but have not yet done so. This method is designed to facilitate construction of subclasses that provide more extensive lock monitoring facilities.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------|
| [Thread](../java.lang/Thread.md)! | the owner, or`null`if not owned |

### getQueuedThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire this lock. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive monitoring facilities.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Thread](../java.lang/Thread.md)!>! | the collection of threads |

### getWaitingThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getWaitingThreads(condition: Condition!): MutableCollection<Thread!>!
```

Returns a collection containing those threads that may be waiting on the given condition associated with this lock. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive condition monitoring facilities.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `condition` | [Condition](Condition.md)!:the condition |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Thread](../java.lang/Thread.md)!>! | the collection of threads |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if this lock is not held |
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this lock |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |
