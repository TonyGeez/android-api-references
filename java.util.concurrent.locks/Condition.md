# Condition

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Condition

```
interface Condition
```

| [java.util.concurrent.locks.Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#) |

| Known Direct Subclasses [AbstractQueuedLongSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject), [AbstractQueuedSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractQueuedLongSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer.ConditionObject) | Condition implementation for a [AbstractQueuedLongSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer) serving as the basis of a [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) implementation. | | [AbstractQueuedSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject) | Condition implementation for a [AbstractQueuedSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer) serving as the basis of a [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) implementation. | |

`Condition`factors out the`Object`monitor methods ([wait](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait()), [notify](https://developer.android.com/reference/kotlin/java/lang/Object.html#notify())and [notifyAll](https://developer.android.com/reference/kotlin/java/lang/Object.html#notifyAll())) into distinct objects to give the effect of having multiple wait-sets per object, by combining them with the use of arbitrary [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) implementations. Where a`Lock`replaces the use of`synchronized`methods and statements, a`Condition`replaces the use of the Object monitor methods.

Conditions (also known as*condition queues* or*condition variables* ) provide a means for one thread to suspend execution (to "wait") until notified by another thread that some state condition may now be true. Because access to this shared state information occurs in different threads, it must be protected, so a lock of some form is associated with the condition. The key property that waiting for a condition provides is that it*atomically* releases the associated lock and suspends the current thread, just like`Object.wait`.

A`Condition`instance is intrinsically bound to a lock. To obtain a`Condition`instance for a particular [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) instance use its [newCondition()](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#newCondition())method.

As an example, suppose we have a bounded buffer which supports`put`and`take`methods. If a`take`is attempted on an empty buffer, then the thread will block until an item becomes available; if a`put`is attempted on a full buffer, then the thread will block until a space becomes available. We would like to keep waiting`put`threads and`take`threads in separate wait-sets so that we can use the optimization of only notifying a single thread at a time when items or spaces become available in the buffer. This can be achieved using two [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#) instances. 

```kotlin
class BoundedBuffer<E> {
    <b>final Lock lock = new ReentrantLock();</b>final Condition notFull  = <b>lock.newCondition(); </b>final Condition notEmpty = <b>lock.newCondition(); </b>final Object[] items = new Object[100];
    int putptr, takeptr, count;
 
    public void put(E x) throws InterruptedException {
      <b>lock.lock();
      try {</b>while (count == items.length)
          <b>notFull.await();</b>items[putptr] = x;
        if (++putptr == items.length) putptr = 0;
        ++count;
        <b>notEmpty.signal();</b><b>} finally {
        lock.unlock();
      }</b>}
 
    public E take() throws InterruptedException {
      <b>lock.lock();
      try {</b>while (count == 0)
          <b>notEmpty.await();</b>E x = (E) items[takeptr];
        if (++takeptr == items.length) takeptr = 0;
        --count;
        <b>notFull.signal();</b>return x;
      <b>} finally {
        lock.unlock();
      }</b>}
  }
  
```
(The [java.util.concurrent.ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue.html#) class provides this functionality, so there is no reason to implement this sample usage class.)

A`Condition`implementation can provide behavior and semantics that is different from that of the`Object`monitor methods, such as guaranteed ordering for notifications, or not requiring a lock to be held when performing notifications. If an implementation provides such specialized semantics then the implementation must document those semantics.

Note that`Condition`instances are just normal objects and can themselves be used as the target in a`synchronized`statement, and can have their own monitor java.lang.Object#wait and [notify](https://developer.android.com/reference/kotlin/java/lang/Object.html#notify())methods invoked. Acquiring the monitor lock of a`Condition`instance, or using its monitor methods, has no specified relationship with acquiring the [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) associated with that`Condition`or the use of its #await and [signalling](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signal())methods. It is recommended that to avoid confusion you never use`Condition`instances in this way, except perhaps within their own implementation.

Except where noted, passing a`null`value for any parameter will result in a [NullPointerException](https://developer.android.com/reference/kotlin/java/lang/NullPointerException.html#) being thrown.

## Implementation Considerations

When waiting upon a`Condition`, a "*spurious wakeup* " is permitted to occur, in general, as a concession to the underlying platform semantics. This has little practical impact on most application programs as a`Condition`should always be waited upon in a loop, testing the state predicate that is being waited for. An implementation is free to remove the possibility of spurious wakeups but it is recommended that applications programmers always assume that they can occur and so always wait in a loop.

The three forms of condition waiting (interruptible, non-interruptible, and timed) may differ in their ease of implementation on some platforms and in their performance characteristics. In particular, it may be difficult to provide these features and maintain specific semantics such as ordering guarantees. Further, the ability to interrupt the actual suspension of the thread may not always be feasible to implement on all platforms.

Consequently, an implementation is not required to define exactly the same guarantees or semantics for all three forms of waiting, nor is it required to support interruption of the actual suspension of the thread.

An implementation is required to clearly document the semantics and guarantees provided by each of the waiting methods, and when an implementation does support interruption of thread suspension then it must obey the interruption semantics as defined in this interface.

As interruption generally implies cancellation, and checks for interruption are often infrequent, an implementation can favor responding to an interrupt over normal method return. This is true even if it can be shown that the interrupt occurred after another action that may have unblocked the thread. An implementation should document this behavior.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [await](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#await())`()` Causes the current thread to wait until it is signalled or [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [await](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#await(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!`)` Causes the current thread to wait until it is signalled or interrupted, or the specified waiting time elapses. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [awaitNanos](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#awaitNanos(kotlin.Long))`(`nanosTimeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Causes the current thread to wait until it is signalled or interrupted, or the specified waiting time elapses. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [awaitUninterruptibly](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#awaitUninterruptibly())`()` Causes the current thread to wait until it is signalled. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [awaitUntil](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#awaitUntil(java.util.Date))`(`deadline:` ` [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!`)` Causes the current thread to wait until it is signalled or interrupted, or the specified deadline elapses. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [signal](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signal())`()` Wakes up one waiting thread. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [signalAll](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signalAll())`()` Wakes up all waiting threads. |

## Public methods

### await

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun await(): Unit
```

Causes the current thread to wait until it is signalled or [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt()).

The lock associated with this`Condition`is atomically released and the current thread becomes disabled for thread scheduling purposes and lies dormant until*one*of four things happens:

- Some other thread invokes the [signal](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signal())method for this`Condition`and the current thread happens to be chosen as the thread to be awakened; or
- Some other thread invokes the [signalAll](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signalAll())method for this`Condition`; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread, and interruption of thread suspension is supported; or
- A "*spurious wakeup*" occurs.

In all cases, before this method can return the current thread must re-acquire the lock associated with this condition. When the thread returns it is*guaranteed*to hold this lock.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting and interruption of thread suspension is supported,

then [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#) is thrown and the current thread's interrupted status is cleared. It is not specified, in the first case, whether or not the test for interruption occurs before the lock is released.

**Implementation Considerations**

The current thread is assumed to hold the lock associated with this`Condition`when this method is called. It is up to the implementation to determine if this is the case and if not, how to respond. Typically, an exception will be thrown (such as [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException.html#)) and the implementation must document that fact.

An implementation can favor responding to an interrupt over normal method return in response to a signal. In that case the implementation must ensure that the signal is redirected to another waiting thread, if there is one.

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted (and interruption of thread suspension is supported) |

### await

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun await(
    time: Long, 
    unit: TimeUnit!
): Boolean
```

Causes the current thread to wait until it is signalled or interrupted, or the specified waiting time elapses. This method is behaviorally equivalent to: 

```kotlin
<code>awaitNanos(unit.toNanos(time)) &gt; 0</code>
```

<br />

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!:the time unit of the`time`argument |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if the waiting time detectably elapsed before return from the method, else`true` |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted (and interruption of thread suspension is supported) |

### awaitNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun awaitNanos(nanosTimeout: Long): Long
```

Causes the current thread to wait until it is signalled or interrupted, or the specified waiting time elapses.

The lock associated with this condition is atomically released and the current thread becomes disabled for thread scheduling purposes and lies dormant until*one*of five things happens:

- Some other thread invokes the [signal](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signal())method for this`Condition`and the current thread happens to be chosen as the thread to be awakened; or
- Some other thread invokes the [signalAll](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signalAll())method for this`Condition`; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread, and interruption of thread suspension is supported; or
- The specified waiting time elapses; or
- A "*spurious wakeup*" occurs.

In all cases, before this method can return the current thread must re-acquire the lock associated with this condition. When the thread returns it is*guaranteed*to hold this lock.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting and interruption of thread suspension is supported,

then [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#) is thrown and the current thread's interrupted status is cleared. It is not specified, in the first case, whether or not the test for interruption occurs before the lock is released.

The method returns an estimate of the number of nanoseconds remaining to wait given the supplied`nanosTimeout`value upon return, or a value less than or equal to zero if it timed out. This value can be used to determine whether and how long to re-wait in cases where the wait returns but an awaited condition still does not hold. Typical uses of this method take the following form: 

```kotlin
<code>boolean aMethod(long timeout, TimeUnit unit)
      throws InterruptedException {
    long nanosRemaining = unit.toNanos(timeout);
    lock.lock();
    try {
      while (!conditionBeingWaitedFor()) {
        if (nanosRemaining &lt;= 0L)
          return false;
        nanosRemaining = theCondition.awaitNanos(nanosRemaining);
      }
      // ...
      return true;
    } finally {
      lock.unlock();
    }
  }</code>
```

Design note: This method requires a nanosecond argument so as to avoid truncation errors in reporting remaining times. Such precision loss would make it difficult for programmers to ensure that total waiting times are not systematically shorter than specified when re-waits occur.

**Implementation Considerations**

The current thread is assumed to hold the lock associated with this`Condition`when this method is called. It is up to the implementation to determine if this is the case and if not, how to respond. Typically, an exception will be thrown (such as [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException.html#)) and the implementation must document that fact.

An implementation can favor responding to an interrupt over normal method return in response to a signal, or over indicating the elapse of the specified waiting time. In either case the implementation must ensure that the signal is redirected to another waiting thread, if there is one.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------|
| `nanosTimeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait, in nanoseconds |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | an estimate of the`nanosTimeout`value minus the time spent waiting upon return from this method. A positive value may be used as the argument to a subsequent call to this method to finish waiting out the desired time. A value less than or equal to zero indicates that no time remains. |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted (and interruption of thread suspension is supported) |

### awaitUninterruptibly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun awaitUninterruptibly(): Unit
```

Causes the current thread to wait until it is signalled.

The lock associated with this condition is atomically released and the current thread becomes disabled for thread scheduling purposes and lies dormant until*one*of three things happens:

- Some other thread invokes the [signal](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signal())method for this`Condition`and the current thread happens to be chosen as the thread to be awakened; or
- Some other thread invokes the [signalAll](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signalAll())method for this`Condition`; or
- A "*spurious wakeup*" occurs.

In all cases, before this method can return the current thread must re-acquire the lock associated with this condition. When the thread returns it is*guaranteed*to hold this lock.

If the current thread's interrupted status is set when it enters this method, or it is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting, it will continue to wait until signalled. When it finally returns from this method its interrupted status will still be set.

**Implementation Considerations**

The current thread is assumed to hold the lock associated with this`Condition`when this method is called. It is up to the implementation to determine if this is the case and if not, how to respond. Typically, an exception will be thrown (such as [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException.html#)) and the implementation must document that fact. 

### awaitUntil

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun awaitUntil(deadline: Date!): Boolean
```

Causes the current thread to wait until it is signalled or interrupted, or the specified deadline elapses.

The lock associated with this condition is atomically released and the current thread becomes disabled for thread scheduling purposes and lies dormant until*one*of five things happens:

- Some other thread invokes the [signal](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signal())method for this`Condition`and the current thread happens to be chosen as the thread to be awakened; or
- Some other thread invokes the [signalAll](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition#signalAll())method for this`Condition`; or
- Some other thread [interrupts](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())the current thread, and interruption of thread suspension is supported; or
- The specified deadline elapses; or
- A "*spurious wakeup*" occurs.

In all cases, before this method can return the current thread must re-acquire the lock associated with this condition. When the thread returns it is*guaranteed*to hold this lock.

If the current thread:

- has its interrupted status set on entry to this method; or
- is [interrupted](https://developer.android.com/reference/kotlin/java/lang/Thread.html#interrupt())while waiting and interruption of thread suspension is supported,

then [InterruptedException](https://developer.android.com/reference/kotlin/java/lang/InterruptedException.html#) is thrown and the current thread's interrupted status is cleared. It is not specified, in the first case, whether or not the test for interruption occurs before the lock is released.

The return value indicates whether the deadline has elapsed, which can be used as follows: 

```kotlin
<code>boolean aMethod(Date deadline)
      throws InterruptedException {
    boolean stillWaiting = true;
    lock.lock();
    try {
      while (!conditionBeingWaitedFor()) {
        if (!stillWaiting)
          return false;
        stillWaiting = theCondition.awaitUntil(deadline);
      }
      // ...
      return true;
    } finally {
      lock.unlock();
    }
  }</code>
```

**Implementation Considerations**

The current thread is assumed to hold the lock associated with this`Condition`when this method is called. It is up to the implementation to determine if this is the case and if not, how to respond. Typically, an exception will be thrown (such as [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException.html#)) and the implementation must document that fact.

An implementation can favor responding to an interrupt over normal method return in response to a signal, or over indicating the passing of the specified deadline. In either case the implementation must ensure that the signal is redirected to another waiting thread, if there is one.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------|
| `deadline` | [Date](https://developer.android.com/reference/kotlin/java/util/Date.html#)!:the absolute time to wait until |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`if the deadline has elapsed upon return, else`true` |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted (and interruption of thread suspension is supported) |

### signal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun signal(): Unit
```

Wakes up one waiting thread.

If any threads are waiting on this condition then one is selected for waking up. That thread must then re-acquire the lock before returning from`await`.

**Implementation Considerations**

An implementation may (and typically does) require that the current thread hold the lock associated with this`Condition`when this method is called. Implementations must document this precondition and any actions taken if the lock is not held. Typically, an exception such as [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException.html#) will be thrown. 

### signalAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun signalAll(): Unit
```

Wakes up all waiting threads.

If any threads are waiting on this condition then they are all woken up. Each thread must re-acquire the lock before it can return from`await`.

**Implementation Considerations**

An implementation may (and typically does) require that the current thread hold the lock associated with this`Condition`when this method is called. Implementations must document this precondition and any actions taken if the lock is not held. Typically, an exception such as [IllegalMonitorStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalMonitorStateException.html#) will be thrown.
