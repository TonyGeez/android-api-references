Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractQueuedSynchronizer

```
abstract class AbstractQueuedSynchronizer : AbstractOwnableSynchronizer, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.util.concurrent.locks.AbstractOwnableSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer) ||
| | ↳ | [java.util.concurrent.locks.AbstractQueuedSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#) |

Provides a framework for implementing blocking locks and related synchronizers (semaphores, events, etc) that rely on first-in-first-out (FIFO) wait queues. This class is designed to be a useful basis for most kinds of synchronizers that rely on a single atomic `int` value to represent state. Subclasses must define the protected methods that change this state, and which define what that state means in terms of this object being acquired or released. Given these, the other methods in this class carry out all queuing and blocking mechanics. Subclasses can maintain other state fields, but only the atomically updated `int` value manipulated using methods `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getState()`, `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#setState(kotlin.Int)` and `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#compareAndSetState(kotlin.Int,%20kotlin.Int)` is tracked with respect to synchronization.

Subclasses should be defined as non-public internal helper classes that are used to implement the synchronization properties of their enclosing class. Class `AbstractQueuedSynchronizer` does not implement any synchronization interface. Instead it defines methods such as `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#acquireInterruptibly(kotlin.Int)` that can be invoked as appropriate by concrete locks and related synchronizers to implement their public methods.

This class supports either or both a default *exclusive* mode and a *shared* mode. When acquired in exclusive mode, attempted acquires by other threads cannot succeed. Shared mode acquires by multiple threads may (but need not) succeed. This class does not "understand" these differences except in the mechanical sense that when a shared mode acquire succeeds, the next waiting thread (if one exists) must also determine whether it can acquire as well. Threads waiting in the different modes share the same FIFO queue. Usually, implementation subclasses support only one of these modes, but both can come into play for example in a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReadWriteLock`. Subclasses that support only exclusive or only shared modes need not define the methods supporting the unused mode.

This class defines a nested `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject` class that can be used as a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition` implementation by subclasses supporting exclusive mode for which method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#isHeldExclusively()` reports whether synchronization is exclusively held with respect to the current thread, method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#release(kotlin.Int)` invoked with the current `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getState()` value fully releases this object, and the underlying version of `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#acquire(kotlin.Int)`, given this saved state value, eventually restores this object to its previous acquired state. No `AbstractQueuedSynchronizer` method otherwise creates such a condition, so if this constraint cannot be met, do not use it. The behavior of `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject` depends of course on the semantics of its synchronizer implementation.

This class provides inspection, instrumentation, and monitoring methods for the internal queue, as well as similar methods for condition objects. These can be exported as desired into classes using an `AbstractQueuedSynchronizer` for their synchronization mechanics.

Serialization of this class stores only the underlying atomic integer maintaining state, so deserialized objects have empty thread queues. Typical subclasses requiring serializability will define a `readObject` method that restores this to a known initial state upon deserialization.

## Usage

To use this class as the basis of a synchronizer, redefine the following methods, as applicable, by inspecting and/or modifying the synchronization state using `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getState()`, `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#setState(kotlin.Int)` and/or `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#compareAndSetState(kotlin.Int,%20kotlin.Int)`:

- `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryRelease(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryReleaseShared(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#isHeldExclusively()`

Each of these methods by default throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. Implementations of these methods must be internally thread-safe, and should in general be short and not block. Defining these methods is the *only* supported means of using this class. All other methods are declared `final` because they cannot be independently varied.

You may also find the inherited methods from `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer` useful to keep track of the thread owning an exclusive synchronizer. You are encouraged to use them -- this enables monitoring and diagnostic tools to assist users in determining which threads hold locks.

Even though this class is based on an internal FIFO queue, it does not automatically enforce FIFO acquisition policies. The core of exclusive synchronization takes the form:

```kotlin
<em>Acquire:</em>while (!tryAcquire(arg)) {
         <em>enqueue thread if it is not already queued</em>;
         <em>possibly block current thread</em>;
      }
 
  <em>Release:</em>if (tryRelease(arg))
         <em>unblock the first queued thread</em>;
  
```
(Shared mode is similar but may involve cascading signals.)

Because checks in acquire are invoked before enqueuing, a newly acquiring thread may *barge* ahead of others that are blocked and queued. However, you can, if desired, define `tryAcquire` and/or `tryAcquireShared` to disable barging by internally invoking one or more of the inspection methods, thereby providing a *fair* FIFO acquisition order. In particular, most fair synchronizers can define `tryAcquire` to return `false` if `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasQueuedPredecessors()` (a method specifically designed to be used by fair synchronizers) returns `true`. Other variations are possible.

Throughput and scalability are generally highest for the default barging (also known as *greedy* , *renouncement* , and *convoy-avoidance* ) strategy. While this is not guaranteed to be fair or starvation-free, earlier queued threads are allowed to recontend before later queued threads, and each recontention has an unbiased chance to succeed against incoming threads. Also, while acquires do not "spin" in the usual sense, they may perform multiple invocations of `tryAcquire` interspersed with other computations before blocking. This gives most of the benefits of spins when exclusive synchronization is only briefly held, without most of the liabilities when it isn't. If so desired, you can augment this by preceding calls to acquire methods with "fast-path" checks, possibly prechecking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasContended()` and/or `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasQueuedThreads()` to only do so if the synchronizer is likely not to be contended.

This class provides an efficient and scalable basis for synchronization in part by specializing its range of use to synchronizers that can rely on `int` state, acquire, and release parameters, and an internal FIFO wait queue. When this does not suffice, you can build synchronizers from a lower level using `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/package-summary.html` classes, your own custom `https://developer.android.com/reference/kotlin/java/util/Queue.html#` classes, and `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport` blocking support.

## Usage Examples

Here is a non-reentrant mutual exclusion lock class that uses the value zero to represent the unlocked state, and one to represent the locked state. While a non-reentrant lock does not strictly require recording of the current owner thread, this class does so anyway to make usage easier to monitor. It also supports conditions and exposes some instrumentation methods:

```kotlin
<code>class Mutex implements Lock, java.io.Serializable {
 
    // Our internal helper class
    private static class Sync extends AbstractQueuedSynchronizer {
      // Acquires the lock if state is zero
      public boolean tryAcquire(int acquires) {
        assert acquires == 1; // Otherwise unused
        if (compareAndSetState(0, 1)) {
          setExclusiveOwnerThread(Thread.currentThread());
          return true;
        }
        return false;
      }
 
      // Releases the lock by setting state to zero
      protected boolean tryRelease(int releases) {
        assert releases == 1; // Otherwise unused
        if (!isHeldExclusively())
          throw new IllegalMonitorStateException();
        setExclusiveOwnerThread(null);
        setState(0);
        return true;
      }
 
      // Reports whether in locked state
      public boolean isLocked() {
        return getState() != 0;
      }
 
      public boolean isHeldExclusively() {
        // a data race, but safe due to out-of-thin-air guarantees
        return getExclusiveOwnerThread() == Thread.currentThread();
      }
 
      // Provides a Condition
      public Condition newCondition() {
        return new ConditionObject();
      }
 
      // Deserializes properly
      private void readObject(ObjectInputStream s)
          throws IOException, ClassNotFoundException {
        s.defaultReadObject();
        setState(0); // reset to unlocked state
      }
    }
 
    // The sync object does all the hard work. We just forward to it.
    private final Sync sync = new Sync();
 
    public void lock()              { sync.acquire(1); }
    public boolean tryLock()        { return sync.tryAcquire(1); }
    public void unlock()            { sync.release(1); }
    public Condition newCondition() { return sync.newCondition(); }
    public boolean isLocked()       { return sync.isLocked(); }
    public boolean isHeldByCurrentThread() {
      return sync.isHeldExclusively();
    }
    public boolean hasQueuedThreads() {
      return sync.hasQueuedThreads();
    }
    public void lockInterruptibly() throws InterruptedException {
      sync.acquireInterruptibly(1);
    }
    public boolean tryLock(long timeout, TimeUnit unit)
        throws InterruptedException {
      return sync.tryAcquireNanos(1, unit.toNanos(timeout));
    }
  }</code>
```

Here is a latch class that is like a `https://developer.android.com/reference/kotlin/java/util/concurrent/CountDownLatch.html#` except that it only requires a single `signal` to fire. Because a latch is non-exclusive, it uses the `shared` acquire and release methods.

```kotlin
<code>class BooleanLatch {
 
    private static class Sync extends AbstractQueuedSynchronizer {
      boolean isSignalled() { return getState() != 0; }
 
      protected int tryAcquireShared(int ignore) {
        return isSignalled() ? 1 : -1;
      }
 
      protected boolean tryReleaseShared(int ignore) {
        setState(1);
        return true;
      }
    }
 
    private final Sync sync = new Sync();
    public boolean isSignalled() { return sync.isSignalled(); }
    public void signal()         { sync.releaseShared(1); }
    public void await() throws InterruptedException {
      sync.acquireSharedInterruptibly(1);
    }
  }</code>
```

## Summary

| Nested classes ||
|---|---|
| open | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject` Condition implementation for a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#` serving as the basis of a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock` implementation. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#AbstractQueuedSynchronizer()()` Creates a new `AbstractQueuedSynchronizer` instance with initial synchronization state of zero. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#acquire(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Acquires in exclusive mode, ignoring interrupts. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#acquireInterruptibly(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Acquires in exclusive mode, aborting if interrupted. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#acquireShared(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Acquires in shared mode, ignoring interrupts. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#acquireSharedInterruptibly(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Acquires in shared mode, aborting if interrupted. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getExclusiveQueuedThreads()()` Returns a collection containing threads that may be waiting to acquire in exclusive mode. |
| [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getFirstQueuedThread()()` Returns the first (longest-waiting) thread in the queue, or `null` if no threads are currently queued. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getQueueLength()()` Returns an estimate of the number of threads waiting to acquire. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getQueuedThreads()()` Returns a collection containing threads that may be waiting to acquire. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getSharedQueuedThreads()()` Returns a collection containing threads that may be waiting to acquire in shared mode. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getWaitQueueLength(java.util.concurrent.locks.AbstractQueuedSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject!)` Returns an estimate of the number of threads waiting on the given condition associated with this synchronizer. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getWaitingThreads(java.util.concurrent.locks.AbstractQueuedSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject!)` Returns a collection containing those threads that may be waiting on the given condition associated with this synchronizer. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasContended()()` Queries whether any threads have ever contended to acquire this synchronizer; that is, if an acquire method has ever blocked. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasQueuedPredecessors()()` Queries whether any threads have been waiting to acquire longer than the current thread. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasQueuedThreads()()` Queries whether any threads are waiting to acquire. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#hasWaiters(java.util.concurrent.locks.AbstractQueuedSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject!)` Queries whether any threads are waiting on the given condition associated with this synchronizer. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#isQueued(java.lang.Thread)(thread: https://developer.android.com/reference/kotlin/java/lang/Thread.html#!)` Returns true if the given thread is currently queued. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#owns(java.util.concurrent.locks.AbstractQueuedSynchronizer.ConditionObject)(condition: https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject!)` Queries whether the given ConditionObject uses this synchronizer as its lock. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#release(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Releases in exclusive mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#releaseShared(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Releases in shared mode. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#toString()()` Returns a string identifying this synchronizer, as well as its state. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireNanos(kotlin.Int,%20kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, nanosTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to acquire in exclusive mode, aborting if interrupted, and failing if the given timeout elapses. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireSharedNanos(kotlin.Int,%20kotlin.Long)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, nanosTimeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Attempts to acquire in shared mode, aborting if interrupted, and failing if the given timeout elapses. |

| Protected methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#compareAndSetState(kotlin.Int,%20kotlin.Int)(expect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, update: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically sets synchronization state to the given updated value if the current state value equals the expected value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getState()()` Returns the current value of synchronization state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#isHeldExclusively()()` Returns `true` if synchronization is held exclusively with respect to the current (calling) thread. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#setState(kotlin.Int)(newState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the value of synchronization state. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to acquire in exclusive mode. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to acquire in shared mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryRelease(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to set the state to reflect a release in exclusive mode. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryReleaseShared(kotlin.Int)(arg: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Attempts to set the state to reflect a release in shared mode. |

Inherited functions From class `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer` `https://developer.android.com/reference/kotlin/java/lang/Thread.html#!` `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer#getExclusiveOwnerThread()()`

Returns the thread last set by `setExclusiveOwnerThread`, or `null` if never set. This method does not otherwise impose any synchronization or `volatile` field accesses.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer#setExclusiveOwnerThread(java.lang.Thread)(thread: https://developer.android.com/reference/kotlin/java/lang/Thread.html#!)`

Sets the thread that currently owns exclusive access. A `null` argument indicates that no thread owns access. This method does not otherwise impose any synchronization or `volatile` field accesses.

<br />

## Protected constructors

### AbstractQueuedSynchronizer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected AbstractQueuedSynchronizer()
```

Creates a new `AbstractQueuedSynchronizer` instance with initial synchronization state of zero.

## Public methods

### acquire

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquire(arg: Int): Unit
```

Acquires in exclusive mode, ignoring interrupts. Implemented by invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` until success. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#lock()`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |

### acquireInterruptibly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquireInterruptibly(arg: Int): Unit
```

Acquires in exclusive mode, aborting if interrupted. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` until success or the thread is interrupted. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#lockInterruptibly()`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### acquireShared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquireShared(arg: Int): Unit
```

Acquires in shared mode, ignoring interrupts. Implemented by first invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` until success.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |

### acquireSharedInterruptibly

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun acquireSharedInterruptibly(arg: Int): Unit
```

Acquires in shared mode, aborting if interrupted. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)`, returning on success. Otherwise the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` until success or the thread is interrupted.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### getExclusiveQueuedThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExclusiveQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire in exclusive mode. This has the same properties as `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getQueuedThreads()` except that it only returns those threads waiting due to an exclusive acquire.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

### getFirstQueuedThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getFirstQueuedThread(): Thread!
```

Returns the first (longest-waiting) thread in the queue, or `null` if no threads are currently queued.

In this implementation, this operation normally returns in constant time, but may iterate upon contention if other threads are concurrently modifying the queue.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/lang/Thread.html#!` | the first (longest-waiting) thread in the queue, or `null` if no threads are currently queued |

### getQueueLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQueueLength(): Int
```

Returns an estimate of the number of threads waiting to acquire. The value is only an estimate because the number of threads may change dynamically while this method traverses internal data structures. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the estimated number of threads waiting to acquire |

### getQueuedThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive monitoring facilities.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

### getSharedQueuedThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSharedQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire in shared mode. This has the same properties as `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getQueuedThreads()` except that it only returns those threads waiting due to a shared acquire.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

### getWaitQueueLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWaitQueueLength(condition: AbstractQueuedSynchronizer.ConditionObject!): Int
```

Returns an estimate of the number of threads waiting on the given condition associated with this synchronizer. Note that because timeouts and interrupts may occur at any time, the estimate serves only as an upper bound on the actual number of waiters. This method is designed for use in monitoring system state, not for synchronization control.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the estimated number of waiting threads |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this synchronizer |
| `java.lang.IllegalMonitorStateException` | if exclusive synchronization is not held |
| `java.lang.NullPointerException` | if the condition is null |

### getWaitingThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getWaitingThreads(condition: AbstractQueuedSynchronizer.ConditionObject!): MutableCollection<Thread!>!
```

Returns a collection containing those threads that may be waiting on the given condition associated with this synchronizer. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<https://developer.android.com/reference/kotlin/java/lang/Thread.html#!>!` | the collection of threads |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this synchronizer |
| `java.lang.IllegalMonitorStateException` | if exclusive synchronization is not held |
| `java.lang.NullPointerException` | if the condition is null |

### hasContended

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

This method is designed to be used by a fair synchronizer to avoid [barging](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#barging). Such a synchronizer's `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` method should return `false`, and its `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` method should return a negative value, if this method returns `true` (unless this is a reentrant acquire). For example, the `tryAcquire` method for a fair, reentrant, exclusive mode synchronizer might look like this:

```kotlin
<code>protected boolean tryAcquire(int arg) {
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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasQueuedThreads(): Boolean
```

Queries whether any threads are waiting to acquire. Note that because cancellations due to interrupts and timeouts may occur at any time, a `true` return does not guarantee that any other thread will ever acquire.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there may be other threads waiting to acquire |

### hasWaiters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hasWaiters(condition: AbstractQueuedSynchronizer.ConditionObject!): Boolean
```

Queries whether any threads are waiting on the given condition associated with this synchronizer. Note that because timeouts and interrupts may occur at any time, a `true` return does not guarantee that a future `signal` will awaken any threads. This method is designed primarily for use in monitoring of the system state.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if there are any waiting threads |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this synchronizer |
| `java.lang.IllegalMonitorStateException` | if exclusive synchronization is not held |
| `java.lang.NullPointerException` | if the condition is null |

### isQueued

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun owns(condition: AbstractQueuedSynchronizer.ConditionObject!): Boolean
```

Queries whether the given ConditionObject uses this synchronizer as its lock.

| Parameters ||
|---|---|
| `condition` | [AbstractQueuedSynchronizer.ConditionObject](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject)!: the condition |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if owned |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the condition is null |

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(arg: Int): Boolean
```

Releases in exclusive mode. Implemented by unblocking one or more threads if `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryRelease(kotlin.Int)` returns true. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#unlock()`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the release argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryRelease(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value returned from `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryRelease(kotlin.Int)` |

### releaseShared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun releaseShared(arg: Int): Boolean
```

Releases in shared mode. Implemented by unblocking one or more threads if `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryReleaseShared(kotlin.Int)` returns true.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the release argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryReleaseShared(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value returned from `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryReleaseShared(kotlin.Int)` |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string identifying this synchronizer, as well as its state. The state, in brackets, includes the String `"State ="` followed by the current value of `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#getState()`, and either `"nonempty"` or `"empty"` depending on whether the queue is empty.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string identifying this synchronizer, as well as its state |

### tryAcquireNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun tryAcquireNanos(
    arg: Int, 
    nanosTimeout: Long
): Boolean
```

Attempts to acquire in exclusive mode, aborting if interrupted, and failing if the given timeout elapses. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)`, returning on success. Otherwise, the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` until success or the thread is interrupted or the timeout elapses. This method can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#tryLock(kotlin.Long,%20java.util.concurrent.TimeUnit)`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquire(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |
| `nanosTimeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum number of nanoseconds to wait |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if acquired; `false` if timed out |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

### tryAcquireSharedNanos

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun tryAcquireSharedNanos(
    arg: Int, 
    nanosTimeout: Long
): Boolean
```

Attempts to acquire in shared mode, aborting if interrupted, and failing if the given timeout elapses. Implemented by first checking interrupt status, then invoking at least once `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)`, returning on success. Otherwise, the thread is queued, possibly repeatedly blocking and unblocking, invoking `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` until success or the thread is interrupted or the timeout elapses.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is conveyed to `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer#tryAcquireShared(kotlin.Int)` but is otherwise uninterpreted and can represent anything you like. |
| `nanosTimeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the maximum number of nanoseconds to wait |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if acquired; `false` if timed out |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if the current thread is interrupted |

## Protected methods

### compareAndSetState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun compareAndSetState(
    expect: Int, 
    update: Int
): Boolean
```

Atomically sets synchronization state to the given updated value if the current state value equals the expected value. This operation has memory semantics of a `volatile` read and write.

| Parameters ||
|---|---|
| `expect` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the expected value |
| `update` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful. False return indicates that the actual value was not equal to the expected value. |

### getState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun getState(): Int
```

Returns the current value of synchronization state. This operation has memory semantics of a `volatile` read.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | current state value |

### isHeldExclusively

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun isHeldExclusively(): Boolean
```

Returns `true` if synchronization is held exclusively with respect to the current (calling) thread. This method is invoked upon each call to a `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject` method.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`. This method is invoked internally only within `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer.ConditionObject` methods, so need not be defined if conditions are not used.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if synchronization is held exclusively; `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if conditions are not supported |

### setState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun setState(newState: Int): Unit
```

Sets the value of synchronization state. This operation has memory semantics of a `volatile` write.

| Parameters ||
|---|---|
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the new state value |

### tryAcquire

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryAcquire(arg: Int): Boolean
```

Attempts to acquire in exclusive mode. This method should query if the state of the object permits it to be acquired in the exclusive mode, and if so to acquire it.

This method is always invoked by the thread performing acquire. If this method reports failure, the acquire method may queue the thread, if it is not already queued, until it is signalled by a release from some other thread. This can be used to implement method `https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock#tryLock()`.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is always the one passed to an acquire method, or is the value saved on entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful. Upon success, this object has been acquired. |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if acquiring would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if exclusive mode is not supported |

### tryAcquireShared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryAcquireShared(arg: Int): Int
```

Attempts to acquire in shared mode. This method should query if the state of the object permits it to be acquired in the shared mode, and if so to acquire it.

This method is always invoked by the thread performing acquire. If this method reports failure, the acquire method may queue the thread, if it is not already queued, until it is signalled by a release from some other thread.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the acquire argument. This value is always the one passed to an acquire method, or is the value saved on entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative value on failure; zero if acquisition in shared mode succeeded but no subsequent shared-mode acquire can succeed; and a positive value if acquisition in shared mode succeeded and subsequent shared-mode acquires might also succeed, in which case a subsequent waiting thread must check availability. (Support for three different return values enables this method to be used in contexts where acquires only sometimes act exclusively.) Upon success, this object has been acquired. |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if acquiring would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if shared mode is not supported |

### tryRelease

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryRelease(arg: Int): Boolean
```

Attempts to set the state to reflect a release in exclusive mode.

This method is always invoked by the thread performing release.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the release argument. This value is always the one passed to a release method, or the current state value upon entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is now in a fully released state, so that any waiting threads may attempt to acquire; and `false` otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if releasing would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if exclusive mode is not supported |

### tryReleaseShared

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun tryReleaseShared(arg: Int): Boolean
```

Attempts to set the state to reflect a release in shared mode.

This method is always invoked by the thread performing release.

The default implementation throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `arg` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the release argument. This value is always the one passed to a release method, or the current state value upon entry to a condition wait. The value is otherwise uninterpreted and can represent anything you like. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this release of shared mode may permit a waiting acquire (shared or exclusive) to succeed; and `false` otherwise |

| Exceptions ||
|---|---|
| `java.lang.IllegalMonitorStateException` | if releasing would place this synchronizer in an illegal state. This exception must be thrown in a consistent fashion for synchronization to work correctly. |
| `java.lang.UnsupportedOperationException` | if shared mode is not supported |
