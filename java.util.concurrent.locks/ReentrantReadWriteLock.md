# ReentrantReadWriteLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ReentrantReadWriteLock

```
open class ReentrantReadWriteLock : ReadWriteLock, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.locks.ReentrantReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#) |

An implementation of [ReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReadWriteLock) supporting similar semantics to [ReentrantLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantLock).

This class has the following properties:

- **Acquisition order**

 This class does not impose a reader or writer preference ordering for lock access. However, it does support an optional*fairness*policy.

 ***Non-fair mode (default)***
 : When constructed as non-fair (the default), the order of entry to the read and write lock is unspecified, subject to reentrancy constraints. A nonfair lock that is continuously contended may indefinitely postpone one or more reader or writer threads, but will normally have higher throughput than a fair lock.

 ***Fair mode***

 : When constructed as fair, threads contend for entry using an approximately arrival-order policy. When the currently held lock is released, either the longest-waiting single writer thread will be assigned the write lock, or if there is a group of reader threads waiting longer than all waiting writer threads, that group will be assigned the read lock.A thread that tries to acquire a fair read lock (non-reentrantly) will block if either the write lock is held, or there is a waiting writer thread. The thread will not acquire the read lock until after the oldest currently waiting writer thread has acquired and released the write lock. Of course, if a waiting writer abandons its wait, leaving one or more reader threads as the longest waiters in the queue with the write lock free, then those readers will be assigned the read lock.

 A thread that tries to acquire a fair write lock (non-reentrantly) will block unless both the read lock and write lock are free (which implies there are no waiting threads). (Note that the non-blocking [ReadLock.tryLock()](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.ReadLock#tryLock())and [WriteLock.tryLock()](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.WriteLock#tryLock())methods do not honor this fair setting and will immediately acquire the lock if it is possible, regardless of waiting threads.)
- **Reentrancy**

 This lock allows both readers and writers to reacquire read or write locks in the style of a [ReentrantLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantLock). Non-reentrant readers are not allowed until all write locks held by the writing thread have been released.

 Additionally, a writer can acquire the read lock, but not vice-versa. Among other applications, reentrancy can be useful when write locks are held during calls or callbacks to methods that perform reads under read locks. If a reader tries to acquire the write lock it will never succeed.
- **Lock downgrading**

 Reentrancy also allows downgrading from the write lock to a read lock, by acquiring the write lock, then the read lock and then releasing the write lock. However, upgrading from a read lock to the write lock is**not**possible.
- **Interruption of lock acquisition**

 The read lock and write lock both support interruption during lock acquisition.
- ** [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition) support**

 The write lock provides a [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition) implementation that behaves in the same way, with respect to the write lock, as the [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition) implementation provided by [ReentrantLock.newCondition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantLock#newCondition())does for [ReentrantLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantLock). This [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition) can, of course, only be used with the write lock.

 The read lock does not support a [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition) and`readLock().newCondition()`throws`UnsupportedOperationException`.
- **Instrumentation**

 This class supports methods to determine whether locks are held or contended. These methods are designed for monitoring system state, not for synchronization control.

Serialization of this class behaves in the same way as built-in locks: a deserialized lock is in the unlocked state, regardless of its state when serialized.

**Sample usages.**Here is a code sketch showing how to perform lock downgrading after updating a cache (exception handling is particularly tricky when handling multiple locks in a non-nested fashion): 

```kotlin
<code>class CachedData {
    Object data;
    boolean cacheValid;
    final ReentrantReadWriteLock rwl = new ReentrantReadWriteLock();
 
    void processCachedData() {
      rwl.readLock().lock();
      if (!cacheValid) {
        // Must release read lock before acquiring write lock
        rwl.readLock().unlock();
        rwl.writeLock().lock();
        try {
          // Recheck state because another thread might have
          // acquired write lock and changed state before we did.
          if (!cacheValid) {
            data = ...;
            cacheValid = true;
          }
          // Downgrade by acquiring read lock before releasing write lock
          rwl.readLock().lock();
        } finally {
          rwl.writeLock().unlock(); // Unlock write, still hold read
        }
      }
 
      try {
        use(data);
      } finally {
        rwl.readLock().unlock();
      }
    }
  }</code>
```
ReentrantReadWriteLocks can be used to improve concurrency in some uses of some kinds of Collections. This is typically worthwhile only when the collections are expected to be large, accessed by more reader threads than writer threads, and entail operations with overhead that outweighs synchronization overhead. For example, here is a class using a TreeMap that is expected to be large and concurrently accessed. 

```kotlin
<code>class RWDictionary {
    private final Map&lt;String, Data&gt; m = new TreeMap&lt;&gt;();
    private final ReentrantReadWriteLock rwl = new ReentrantReadWriteLock();
    private final Lock r = rwl.readLock();
    private final Lock w = rwl.writeLock();
 
    public Data get(String key) {
      r.lock();
      try { return m.get(key); }
      finally { r.unlock(); }
    }
    public List&lt;String&gt; allKeys() {
      r.lock();
      try { return new ArrayList&lt;&gt;(m.keySet()); }
      finally { r.unlock(); }
    }
    public Data put(String key, Data value) {
      w.lock();
      try { return m.put(key, value); }
      finally { w.unlock(); }
    }
    public void clear() {
      w.lock();
      try { m.clear(); }
      finally { w.unlock(); }
    }
  }</code>
```

## Implementation Notes

This lock supports a maximum of 65535 recursive write locks and 65535 read locks. Attempts to exceed these limits result in [Error](https://developer.android.com/reference/kotlin/java/lang/Error.html#) throws from locking methods.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ReadLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.ReadLock) The lock returned by method [ReentrantReadWriteLock.readLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#readLock()). |
| open | [WriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.WriteLock) The lock returned by method [ReentrantReadWriteLock.writeLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#writeLock()). |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ReentrantReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#ReentrantReadWriteLock())`()` Creates a new`ReentrantReadWriteLock`with default (nonfair) ordering properties. |
| [ReentrantReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#ReentrantReadWriteLock(kotlin.Boolean))`(`fair:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new`ReentrantReadWriteLock`with the given fairness policy. |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getQueueLength](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getQueueLength())`()` Returns an estimate of the number of threads waiting to acquire either the read or write lock. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReadHoldCount](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getReadHoldCount())`()` Queries the number of reentrant read holds on this lock by the current thread. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReadLockCount](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getReadLockCount())`()` Queries the number of read locks held for this lock. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWaitQueueLength](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getWaitQueueLength(java.util.concurrent.locks.Condition))`(`condition:` ` [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition)!`)` Returns an estimate of the number of threads waiting on the given condition associated with the write lock. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWriteHoldCount](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getWriteHoldCount())`()` Queries the number of reentrant write holds on this lock by the current thread. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasQueuedThread](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#hasQueuedThread(java.lang.Thread))`(`thread:` ` [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!`)` Queries whether the given thread is waiting to acquire either the read or write lock. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasQueuedThreads](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#hasQueuedThreads())`()` Queries whether any threads are waiting to acquire the read or write lock. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWaiters](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#hasWaiters(java.util.concurrent.locks.Condition))`(`condition:` ` [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition)!`)` Queries whether any threads are waiting on the given condition associated with the write lock. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFair](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#isFair())`()` Returns`true`if this lock has fairness set true. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWriteLocked](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#isWriteLocked())`()` Queries if the write lock is held by any thread. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWriteLockedByCurrentThread](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#isWriteLockedByCurrentThread())`()` Queries if the write lock is held by the current thread. |
| open [ReentrantReadWriteLock.ReadLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.ReadLock)! | [readLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#readLock())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#toString())`()` Returns a string identifying this lock, as well as its lock state. |
| open [ReentrantReadWriteLock.WriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.WriteLock)! | [writeLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#writeLock())`()` <br /> |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)! | [getOwner](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getOwner())`()` Returns the thread that currently owns the write lock, or`null`if not owned. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | [getQueuedReaderThreads](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getQueuedReaderThreads())`()` Returns a collection containing threads that may be waiting to acquire the read lock. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | [getQueuedThreads](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getQueuedThreads())`()` Returns a collection containing threads that may be waiting to acquire either the read or write lock. |
| --- | --- |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | [getQueuedWriterThreads](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getQueuedWriterThreads())`()` Returns a collection containing threads that may be waiting to acquire the write lock. |
| open [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!\>! | [getWaitingThreads](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock#getWaitingThreads(java.util.concurrent.locks.Condition))`(`condition:` ` [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition)!`)` Returns a collection containing those threads that may be waiting on the given condition associated with the write lock. |

## Public constructors

### ReentrantReadWriteLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReentrantReadWriteLock()
```

Creates a new`ReentrantReadWriteLock`with default (nonfair) ordering properties. 

### ReentrantReadWriteLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ReentrantReadWriteLock(fair: Boolean)
```

Creates a new`ReentrantReadWriteLock`with the given fairness policy.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `fair` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if this lock should use a fair ordering policy |

## Public methods

### getQueueLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQueueLength(): Int
```

Returns an estimate of the number of threads waiting to acquire either the read or write lock. The value is only an estimate because the number of threads may change dynamically while this method traverses internal data structures. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the estimated number of threads waiting for this lock |

### getReadHoldCount

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReadHoldCount(): Int
```

Queries the number of reentrant read holds on this lock by the current thread. A reader thread has a hold on a lock for each lock action that is not matched by an unlock action.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of holds on the read lock by the current thread, or zero if the read lock is not held by the current thread |

### getReadLockCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReadLockCount(): Int
```

Queries the number of read locks held for this lock. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of read locks held |

### getWaitQueueLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWaitQueueLength(condition: Condition!): Int
```

Returns an estimate of the number of threads waiting on the given condition associated with the write lock. Note that because timeouts and interrupts may occur at any time, the estimate serves only as an upper bound on the actual number of waiters. This method is designed for use in monitoring of the system state, not for synchronization control.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `condition` | [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition)!:the condition |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the estimated number of waiting threads |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if this lock is not held |
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this lock |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |

### getWriteHoldCount

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWriteHoldCount(): Int
```

Queries the number of reentrant write holds on this lock by the current thread. A writer thread has a hold on a lock for each lock action that is not matched by an unlock action.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of holds on the write lock by the current thread, or zero if the write lock is not held by the current thread |

### hasQueuedThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hasQueuedThread(thread: Thread!): Boolean
```

Queries whether the given thread is waiting to acquire either the read or write lock. Note that because cancellations may occur at any time, a`true`return does not guarantee that this thread will ever acquire a lock. This method is designed primarily for use in monitoring of the system state.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------|
| `thread` | [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!:the thread |

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

Queries whether any threads are waiting to acquire the read or write lock. Note that because cancellations may occur at any time, a`true`return does not guarantee that any other thread will ever acquire a lock. This method is designed primarily for use in monitoring of the system state.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there may be other threads waiting to acquire the lock |

### hasWaiters

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasWaiters(condition: Condition!): Boolean
```

Queries whether any threads are waiting on the given condition associated with the write lock. Note that because timeouts and interrupts may occur at any time, a`true`return does not guarantee that a future`signal`will awaken any threads. This method is designed primarily for use in monitoring of the system state.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `condition` | [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition)!:the condition |

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

### isWriteLocked

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWriteLocked(): Boolean
```

Queries if the write lock is held by any thread. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any thread holds the write lock and`false`otherwise |

### isWriteLockedByCurrentThread

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWriteLockedByCurrentThread(): Boolean
```

Queries if the write lock is held by the current thread.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the current thread holds the write lock and`false`otherwise |

### readLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readLock(): ReentrantReadWriteLock.ReadLock!
```

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [ReentrantReadWriteLock.ReadLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.ReadLock)! | the lock used for reading |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string identifying this lock, as well as its lock state. The state, in brackets, includes the String`"Write locks ="`followed by the number of reentrantly held write locks, and the String`"Read locks ="`followed by the number of held read locks.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string identifying this lock, as well as its lock state |

### writeLock

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeLock(): ReentrantReadWriteLock.WriteLock!
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [ReentrantReadWriteLock.WriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock.WriteLock)! | the lock used for writing |

## Protected methods

### getOwner

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getOwner(): Thread!
```

Returns the thread that currently owns the write lock, or`null`if not owned. When this method is called by a thread that is not the owner, the return value reflects a best-effort approximation of current lock status. For example, the owner may be momentarily`null`even if there are threads trying to acquire the lock but have not yet done so. This method is designed to facilitate construction of subclasses that provide more extensive lock monitoring facilities.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------|
| [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)! | the owner, or`null`if not owned |

### getQueuedReaderThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getQueuedReaderThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire the read lock. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive lock monitoring facilities.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!>! | the collection of threads |

### getQueuedThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getQueuedThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire either the read or write lock. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive monitoring facilities.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!>! | the collection of threads |

### getQueuedWriterThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getQueuedWriterThreads(): MutableCollection<Thread!>!
```

Returns a collection containing threads that may be waiting to acquire the write lock. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive lock monitoring facilities.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!>! | the collection of threads |

### getWaitingThreads

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getWaitingThreads(condition: Condition!): MutableCollection<Thread!>!
```

Returns a collection containing those threads that may be waiting on the given condition associated with the write lock. Because the actual set of threads may change dynamically while constructing this result, the returned collection is only a best-effort estimate. The elements of the returned collection are in no particular order. This method is designed to facilitate construction of subclasses that provide more extensive condition monitoring facilities.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------|
| `condition` | [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition)!:the condition |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [Thread](https://developer.android.com/reference/kotlin/java/lang/Thread.html#)!>! | the collection of threads |

| Exceptions ||
|------------------------------------------|---------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if this lock is not held |
| `java.lang.IllegalArgumentException` | if the given condition is not associated with this lock |
| `java.lang.NullPointerException` | if the condition is null |
| --- | --- |
