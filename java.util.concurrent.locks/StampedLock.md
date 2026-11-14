# StampedLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StampedLock

```
open class StampedLock : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.locks.StampedLock](../java/util/concurrent/locks/StampedLock.md) |

A capability-based lock with three modes for controlling read/write access. The state of a StampedLock consists of a version and mode. Lock acquisition methods return a stamp that represents and controls access with respect to a lock state; "try" versions of these methods may instead return the special value zero to represent failure to acquire access. Lock release and conversion methods require stamps as arguments, and fail if they do not match the state of the lock. The three modes are:

- **Writing.** Method [writeLock](../java/util/concurrent/locks/StampedLock.md))possibly blocks waiting for exclusive access, returning a stamp that can be used in method [unlockWrite](../java/util/concurrent/locks/StampedLock.md))to release the lock. Untimed and timed versions of`tryWriteLock`are also provided. When the lock is held in write mode, no read locks may be obtained, and all optimistic read validations will fail.
- **Reading.** Method [readLock](../java/util/concurrent/locks/StampedLock.md))possibly blocks waiting for non-exclusive access, returning a stamp that can be used in method [unlockRead](../java/util/concurrent/locks/StampedLock.md))to release the lock. Untimed and timed versions of`tryReadLock`are also provided.
- **Optimistic Reading.** Method [tryOptimisticRead](../java/util/concurrent/locks/StampedLock.md))returns a non-zero stamp only if the lock is not currently held in write mode. Method [validate](../java/util/concurrent/locks/StampedLock.md))returns true if the lock has not been acquired in write mode since obtaining a given stamp, in which case all actions prior to the most recent write lock release happen-before actions following the call to`tryOptimisticRead`. This mode can be thought of as an extremely weak version of a read-lock, that can be broken by a writer at any time. The use of optimistic read mode for short read-only code segments often reduces contention and improves throughput. However, its use is inherently fragile. Optimistic read sections should only read fields and hold them in local variables for later use after validation. Fields read while in optimistic read mode may be wildly inconsistent, so usage applies only when you are familiar enough with data representations to check consistency and/or repeatedly invoke method`validate()`. For example, such steps are typically required when first reading an object or array reference, and then accessing one of its fields, elements or methods.

<br />

This class also supports methods that conditionally provide conversions across the three modes. For example, method [tryConvertToWriteLock](../java/util/concurrent/locks/StampedLock.md))attempts to "upgrade" a mode, returning a valid write stamp if (1) already in writing mode (2) in reading mode and there are no other readers or (3) in optimistic read mode and the lock is available. The forms of these methods are designed to help reduce some of the code bloat that otherwise occurs in retry-based designs.

StampedLocks are designed for use as internal utilities in the development of thread-safe components. Their use relies on knowledge of the internal properties of the data, objects, and methods they are protecting. They are not reentrant, so locked bodies should not call other unknown methods that may try to re-acquire locks (although you may pass a stamp to other methods that can use or convert it). The use of read lock modes relies on the associated code sections being side-effect-free. Unvalidated optimistic read sections cannot call methods that are not known to tolerate potential inconsistencies. Stamps use finite representations, and are not cryptographically secure (i.e., a valid stamp may be guessable). Stamp values may recycle after (no sooner than) one year of continuous operation. A stamp held without use or validation for longer than this period may fail to validate correctly. StampedLocks are serializable, but always deserialize into initial unlocked state, so they are not useful for remote locking.

Like [Semaphore](../java/util/concurrent/Semaphore.md), but unlike most [Lock](../java/util/concurrent/locks/Lock.md) implementations, StampedLocks have no notion of ownership. Locks acquired in one thread can be released or converted in another.

The scheduling policy of StampedLock does not consistently prefer readers over writers or vice versa. All "try" methods are best-effort and do not necessarily conform to any scheduling or fairness policy. A zero return from any "try" method for acquiring or converting locks does not carry any information about the state of the lock; a subsequent invocation may succeed.

Because it supports coordinated usage across multiple lock modes, this class does not directly implement the [Lock](../java/util/concurrent/locks/Lock.md) or [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md) interfaces. However, a StampedLock may be viewed [asReadLock()](../java/util/concurrent/locks/StampedLock.md)), [asWriteLock()](../java/util/concurrent/locks/StampedLock.md)), or [asReadWriteLock()](../java/util/concurrent/locks/StampedLock.md))in applications requiring only the associated set of functionality.

**Memory Synchronization.** Methods with the effect of successfully locking in any mode have the same memory synchronization effects as a*Lock* action, as described in Chapter 17 of The Java Language Specification. Methods successfully unlocking in write mode have the same memory synchronization effects as an*Unlock*action. In optimistic read usages, actions prior to the most recent write mode unlock action are guaranteed to happen-before those following a tryOptimisticRead only if a later validate returns true; otherwise there is no guarantee that the reads between tryOptimisticRead and validate obtain a consistent snapshot.

**Sample Usage.**The following illustrates some usage idioms in a class that maintains simple two-dimensional points. The sample code illustrates some try/catch conventions even though they are not strictly needed here because no exceptions can occur in their bodies. 

```kotlin
<code>class Point {
    private double x, y;
    private final StampedLock sl = new StampedLock();
 
    // an exclusively locked method
    void move(double deltaX, double deltaY) {
      long stamp = sl.writeLock();
      try {
        x += deltaX;
        y += deltaY;
      } finally {
        sl.unlockWrite(stamp);
      }
    }
 
    // a read-only method
    // upgrade from optimistic read to read lock
    double distanceFromOrigin() {
      long stamp = sl.tryOptimisticRead();
      try {
        retryHoldingLock: for (;; stamp = sl.readLock()) {
          if (stamp == 0L)
            continue retryHoldingLock;
          // possibly racy reads
          double currentX = x;
          double currentY = y;
          if (!sl.validate(stamp))
            continue retryHoldingLock;
          return Math.hypot(currentX, currentY);
        }
      } finally {
        if (StampedLock.isReadLockStamp(stamp))
          sl.unlockRead(stamp);
      }
    }
 
    // upgrade from optimistic read to write lock
    void moveIfAtOrigin(double newX, double newY) {
      long stamp = sl.tryOptimisticRead();
      try {
        retryHoldingLock: for (;; stamp = sl.writeLock()) {
          if (stamp == 0L)
            continue retryHoldingLock;
          // possibly racy reads
          double currentX = x;
          double currentY = y;
          if (!sl.validate(stamp))
            continue retryHoldingLock;
          if (currentX != 0.0 || currentY != 0.0)
            break;
          stamp = sl.tryConvertToWriteLock(stamp);
          if (stamp == 0L)
            continue retryHoldingLock;
          // exclusive access
          x = newX;
          y = newY;
          return;
        }
      } finally {
        if (StampedLock.isWriteLockStamp(stamp))
          sl.unlockWrite(stamp);
      }
    }
 
    // upgrade read lock to write lock
    void moveIfAtOrigin2(double newX, double newY) {
      long stamp = sl.readLock();
      try {
        while (x == 0.0 &amp;&amp; y == 0.0) {
          long ws = sl.tryConvertToWriteLock(stamp);
          if (ws != 0L) {
            stamp = ws;
            x = newX;
            y = newY;
            break;
          }
          else {
            sl.unlockRead(stamp);
            stamp = sl.writeLock();
          }
        }
      } finally {
        sl.unlock(stamp);
      }
    }
  }</code>
```

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StampedLock](../java/util/concurrent/locks/StampedLock.md))`()` Creates a new lock, initially in unlocked state. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Lock](../java/util/concurrent/locks/Lock.md)! | [asReadLock](../java/util/concurrent/locks/StampedLock.md))`()` Returns a plain [Lock](../java/util/concurrent/locks/Lock.md) view of this StampedLock in which the [Lock.lock](../java/util/concurrent/locks/Lock.md))method is mapped to [readLock](../java/util/concurrent/locks/StampedLock.md)), and similarly for other methods. |
| open [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md)! | [asReadWriteLock](../java/util/concurrent/locks/StampedLock.md))`()` Returns a [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md) view of this StampedLock in which the [ReadWriteLock.readLock()](../java/util/concurrent/locks/ReadWriteLock.md))method is mapped to [asReadLock()](../java/util/concurrent/locks/StampedLock.md)), and [ReadWriteLock.writeLock()](../java/util/concurrent/locks/ReadWriteLock.md))to [asWriteLock()](../java/util/concurrent/locks/StampedLock.md)). |
| open [Lock](../java/util/concurrent/locks/Lock.md)! | [asWriteLock](../java/util/concurrent/locks/StampedLock.md))`()` Returns a plain [Lock](../java/util/concurrent/locks/Lock.md) view of this StampedLock in which the [Lock.lock](../java/util/concurrent/locks/Lock.md))method is mapped to [writeLock](../java/util/concurrent/locks/StampedLock.md)), and similarly for other methods. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getReadLockCount](../java/util/concurrent/locks/StampedLock.md))`()` Queries the number of read locks held for this lock. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLockStamp](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Tells whether a stamp represents holding a lock. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOptimisticReadStamp](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Tells whether a stamp represents a successful optimistic read. |
| --- | --- |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadLockStamp](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Tells whether a stamp represents holding a lock non-exclusively. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReadLocked](../java/util/concurrent/locks/StampedLock.md))`()` Returns`true`if the lock is currently held non-exclusively. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWriteLockStamp](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Tells whether a stamp represents holding a lock exclusively. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWriteLocked](../java/util/concurrent/locks/StampedLock.md))`()` Returns`true`if the lock is currently held exclusively. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [readLock](../java/util/concurrent/locks/StampedLock.md))`()` Non-exclusively acquires the lock, blocking if necessary until available. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [readLockInterruptibly](../java/util/concurrent/locks/StampedLock.md))`()` Non-exclusively acquires the lock, blocking if necessary until available or the current thread is interrupted. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/concurrent/locks/StampedLock.md))`()` Returns a string identifying this lock, as well as its lock state. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryConvertToOptimisticRead](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If the lock state matches the given stamp then, atomically, if the stamp represents holding a lock, releases it and returns an observation stamp. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryConvertToReadLock](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If the lock state matches the given stamp, atomically performs one of the following actions. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryConvertToWriteLock](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If the lock state matches the given stamp, atomically performs one of the following actions. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryOptimisticRead](../java/util/concurrent/locks/StampedLock.md))`()` Returns a stamp that can later be validated, or zero if exclusively locked. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryReadLock](../java/util/concurrent/locks/StampedLock.md))`()` Non-exclusively acquires the lock if it is immediately available. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryReadLock](../java/util/concurrent/locks/StampedLock.md))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Non-exclusively acquires the lock if it is available within the given time and the current thread has not been interrupted. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryUnlockRead](../java/util/concurrent/locks/StampedLock.md))`()` Releases one hold of the read lock if it is held, without requiring a stamp value. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryUnlockWrite](../java/util/concurrent/locks/StampedLock.md))`()` Releases the write lock if it is held, without requiring a stamp value. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryWriteLock](../java/util/concurrent/locks/StampedLock.md))`()` Exclusively acquires the lock if it is immediately available. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [tryWriteLock](../java/util/concurrent/locks/StampedLock.md))`(`time:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Exclusively acquires the lock if it is available within the given time and the current thread has not been interrupted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlock](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If the lock state matches the given stamp, releases the corresponding mode of the lock. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockRead](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If the lock state matches the given stamp, releases the non-exclusive lock. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unlockWrite](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` If the lock state matches the given stamp, releases the exclusive lock. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [validate](../java/util/concurrent/locks/StampedLock.md))`(`stamp:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Returns true if the lock has not been exclusively acquired since issuance of the given stamp. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [writeLock](../java/util/concurrent/locks/StampedLock.md))`()` Exclusively acquires the lock, blocking if necessary until available. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [writeLockInterruptibly](../java/util/concurrent/locks/StampedLock.md))`()` Exclusively acquires the lock, blocking if necessary until available or the current thread is interrupted. |

## Public constructors

### StampedLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StampedLock()
```

Creates a new lock, initially in unlocked state.

## Public methods

### asReadLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun asReadLock(): Lock!
```

Returns a plain [Lock](../java/util/concurrent/locks/Lock.md) view of this StampedLock in which the [Lock.lock](../java/util/concurrent/locks/Lock.md))method is mapped to [readLock](../java/util/concurrent/locks/StampedLock.md)), and similarly for other methods. The returned Lock does not support a [Condition](../java/util/concurrent/locks/Condition.md); method [Lock.newCondition()](../java/util/concurrent/locks/Lock.md))throws`UnsupportedOperationException`.

| Return ||
|-----------------------------------------------------------------------------------------|----------|
| [Lock](../java/util/concurrent/locks/Lock.md)! | the lock |

### asReadWriteLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun asReadWriteLock(): ReadWriteLock!
```

Returns a [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md) view of this StampedLock in which the [ReadWriteLock.readLock()](../java/util/concurrent/locks/ReadWriteLock.md))method is mapped to [asReadLock()](../java/util/concurrent/locks/StampedLock.md)), and [ReadWriteLock.writeLock()](../java/util/concurrent/locks/ReadWriteLock.md))to [asWriteLock()](../java/util/concurrent/locks/StampedLock.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------------|----------|
| [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md)! | the lock |

### asWriteLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun asWriteLock(): Lock!
```

Returns a plain [Lock](../java/util/concurrent/locks/Lock.md) view of this StampedLock in which the [Lock.lock](../java/util/concurrent/locks/Lock.md))method is mapped to [writeLock](../java/util/concurrent/locks/StampedLock.md)), and similarly for other methods. The returned Lock does not support a [Condition](../java/util/concurrent/locks/Condition.md); method [Lock.newCondition()](../java/util/concurrent/locks/Lock.md))throws`UnsupportedOperationException`.

| Return ||
|-----------------------------------------------------------------------------------------|----------|
| [Lock](../java/util/concurrent/locks/Lock.md)! | the lock |

### getReadLockCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getReadLockCount(): Int
```

Queries the number of read locks held for this lock. This method is designed for use in monitoring system state, not for synchronization control.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of read locks held |

### isLockStamp

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isLockStamp(stamp: Long): Boolean
```

Tells whether a stamp represents holding a lock. This method may be useful in conjunction with [tryConvertToReadLock](../java/util/concurrent/locks/StampedLock.md))and [tryConvertToWriteLock](../java/util/concurrent/locks/StampedLock.md)), for example: 

```kotlin
<code>long stamp = sl.tryOptimisticRead();
  try {
    ...
    stamp = sl.tryConvertToReadLock(stamp);
    ...
    stamp = sl.tryConvertToWriteLock(stamp);
    ...
  } finally {
    if (StampedLock.isLockStamp(stamp))
      sl.unlock(stamp);
  }</code>
```

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a previous StampedLock operation |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the stamp was returned by a successful read-lock or write-lock operation |

### isOptimisticReadStamp

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isOptimisticReadStamp(stamp: Long): Boolean
```

Tells whether a stamp represents a successful optimistic read.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a previous StampedLock operation |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the stamp was returned by a successful optimistic read operation, that is, a non-zero return from [tryOptimisticRead()](../java/util/concurrent/locks/StampedLock.md))or [tryConvertToOptimisticRead(long)](../java/util/concurrent/locks/StampedLock.md)) |

### isReadLockStamp

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isReadLockStamp(stamp: Long): Boolean
```

Tells whether a stamp represents holding a lock non-exclusively. This method may be useful in conjunction with [tryConvertToReadLock](../java/util/concurrent/locks/StampedLock.md)), for example: 

```kotlin
<code>long stamp = sl.tryOptimisticRead();
  try {
    ...
    stamp = sl.tryConvertToReadLock(stamp);
    ...
  } finally {
    if (StampedLock.isReadLockStamp(stamp))
      sl.unlockRead(stamp);
  }</code>
```

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a previous StampedLock operation |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the stamp was returned by a successful read-lock operation |

### isReadLocked

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReadLocked(): Boolean
```

Returns`true`if the lock is currently held non-exclusively.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the lock is currently held non-exclusively |

### isWriteLockStamp

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isWriteLockStamp(stamp: Long): Boolean
```

Tells whether a stamp represents holding a lock exclusively. This method may be useful in conjunction with [tryConvertToWriteLock](../java/util/concurrent/locks/StampedLock.md)), for example: 

```kotlin
<code>long stamp = sl.tryOptimisticRead();
  try {
    ...
    stamp = sl.tryConvertToWriteLock(stamp);
    ...
  } finally {
    if (StampedLock.isWriteLockStamp(stamp))
      sl.unlockWrite(stamp);
  }</code>
```

<br />

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a previous StampedLock operation |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the stamp was returned by a successful write-lock operation |

### isWriteLocked

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isWriteLocked(): Boolean
```

Returns`true`if the lock is currently held exclusively.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the lock is currently held exclusively |

### readLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readLock(): Long
```

Non-exclusively acquires the lock, blocking if necessary until available.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a read stamp that can be used to unlock or convert mode |

### readLockInterruptibly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun readLockInterruptibly(): Long
```

Non-exclusively acquires the lock, blocking if necessary until available or the current thread is interrupted. Behavior under interruption matches that specified for method [Lock.lockInterruptibly()](../java/util/concurrent/locks/Lock.md)).

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a read stamp that can be used to unlock or convert mode |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted before acquiring the lock |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a string identifying this lock, as well as its lock state. The state, in brackets, includes the String`"Unlocked"`or the String`"Write-locked"`or the String`"Read-locks:"`followed by the current number of read-locks held.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string identifying this lock, as well as its lock state |

### tryConvertToOptimisticRead

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryConvertToOptimisticRead(stamp: Long): Long
```

If the lock state matches the given stamp then, atomically, if the stamp represents holding a lock, releases it and returns an observation stamp. Or, if an optimistic read, returns it if validated. This method returns zero in all other cases, and so may be useful as a form of "tryUnlock".

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp |

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a valid optimistic read stamp, or zero on failure |

### tryConvertToReadLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryConvertToReadLock(stamp: Long): Long
```

If the lock state matches the given stamp, atomically performs one of the following actions. If the stamp represents holding a write lock, releases it and obtains a read lock. Or, if a read lock, returns it. Or, if an optimistic read, acquires a read lock and returns a read stamp only if immediately available. This method returns zero in all other cases.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a valid read stamp, or zero on failure |

### tryConvertToWriteLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryConvertToWriteLock(stamp: Long): Long
```

If the lock state matches the given stamp, atomically performs one of the following actions. If the stamp represents holding a write lock, returns it. Or, if a read lock, if the write lock is available, releases the read lock and returns a write stamp. Or, if an optimistic read, returns a write stamp only if immediately available. This method returns zero in all other cases.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a valid write stamp, or zero on failure |

### tryOptimisticRead

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryOptimisticRead(): Long
```

Returns a stamp that can later be validated, or zero if exclusively locked.

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a valid optimistic read stamp, or zero if exclusively locked |

### tryReadLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryReadLock(): Long
```

Non-exclusively acquires the lock if it is immediately available.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a read stamp that can be used to unlock or convert mode, or zero if the lock is not available |

### tryReadLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryReadLock(
    time: Long, 
    unit: TimeUnit!
): Long
```

Non-exclusively acquires the lock if it is available within the given time and the current thread has not been interrupted. Behavior under timeout and interruption matches that specified for method [Lock.tryLock(long,TimeUnit)](../java/util/concurrent/locks/Lock.md)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait for the lock |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the`time`argument |

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a read stamp that can be used to unlock or convert mode, or zero if the lock is not available |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted before acquiring the lock |

### tryUnlockRead

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryUnlockRead(): Boolean
```

Releases one hold of the read lock if it is held, without requiring a stamp value. This method may be useful for recovery after errors.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the read lock was held, else false |

### tryUnlockWrite

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryUnlockWrite(): Boolean
```

Releases the write lock if it is held, without requiring a stamp value. This method may be useful for recovery after errors.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the lock was held, else false |

### tryWriteLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryWriteLock(): Long
```

Exclusively acquires the lock if it is immediately available.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a write stamp that can be used to unlock or convert mode, or zero if the lock is not available |

### tryWriteLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryWriteLock(
    time: Long, 
    unit: TimeUnit!
): Long
```

Exclusively acquires the lock if it is available within the given time and the current thread has not been interrupted. Behavior under timeout and interruption matches that specified for method [Lock.tryLock(long,TimeUnit)](../java/util/concurrent/locks/Lock.md)).

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `time` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait for the lock |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the`time`argument |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a write stamp that can be used to unlock or convert mode, or zero if the lock is not available |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted before acquiring the lock |

### unlock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlock(stamp: Long): Unit
```

If the lock state matches the given stamp, releases the corresponding mode of the lock.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a lock operation |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if the stamp does not match the current state of this lock |

### unlockRead

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlockRead(stamp: Long): Unit
```

If the lock state matches the given stamp, releases the non-exclusive lock.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a read-lock operation |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if the stamp does not match the current state of this lock |

### unlockWrite

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlockWrite(stamp: Long): Unit
```

If the lock state matches the given stamp, releases the exclusive lock.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp returned by a write-lock operation |

| Exceptions ||
|------------------------------------------|------------------------------------------------------------|
| `java.lang.IllegalMonitorStateException` | if the stamp does not match the current state of this lock |

### validate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun validate(stamp: Long): Boolean
```

Returns true if the lock has not been exclusively acquired since issuance of the given stamp. Always returns false if the stamp is zero. Always returns true if the stamp represents a currently held lock. Invoking this method with a value not obtained from [tryOptimisticRead](../java/util/concurrent/locks/StampedLock.md))or a locking method for this lock has no defined effect or result.

| Parameters ||
|---------|--------------------------------------------------------------------------------------|
| `stamp` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a stamp |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the lock has not been exclusively acquired since issuance of the given stamp; else false |

### writeLock

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeLock(): Long
```

Exclusively acquires the lock, blocking if necessary until available.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a write stamp that can be used to unlock or convert mode |

### writeLockInterruptibly

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeLockInterruptibly(): Long
```

Exclusively acquires the lock, blocking if necessary until available or the current thread is interrupted. Behavior under interruption matches that specified for method [Lock.lockInterruptibly()](../java/util/concurrent/locks/Lock.md)).

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a write stamp that can be used to unlock or convert mode |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------|
| `java.lang.InterruptedException` | if the current thread is interrupted before acquiring the lock |
