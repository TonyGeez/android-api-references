# java.util.concurrent.locks

# java.util.concurrent.locks

## Interfaces

| [Condition](Condition.md) | `Condition`factors out the`Object`monitor methods ([wait](../java.lang/Object.md)), [notify](../java.lang/Object.md))and [notifyAll](../java.lang/Object.md))) into distinct objects to give the effect of having multiple wait-sets per object, by combining them with the use of arbitrary [Lock](Lock.md) implementations. |
| --- | --- |
| [Lock](Lock.md) | `Lock`implementations provide more extensive locking operations than can be obtained using`synchronized`methods and statements. |
| [ReadWriteLock](ReadWriteLock.md) | A`ReadWriteLock`maintains a pair of associated [locks](Lock.md), one for read-only operations and one for writing. |

## Classes

| [AbstractOwnableSynchronizer](AbstractOwnableSynchronizer.md) | A synchronizer that may be exclusively owned by a thread. |
| --- | --- |
| [AbstractQueuedLongSynchronizer](AbstractQueuedLongSynchronizer.md) | A version of [AbstractQueuedSynchronizer](AbstractQueuedSynchronizer.md) in which synchronization state is maintained as a`long`. |
| [AbstractQueuedSynchronizer](AbstractQueuedSynchronizer.md) | Provides a framework for implementing blocking locks and related synchronizers (semaphores, events, etc) that rely on first-in-first-out (FIFO) wait queues. |
| [LockSupport](LockSupport.md) | Basic thread blocking primitives for creating locks and other synchronization classes. |
| --- | --- |
| [ReentrantLock](ReentrantLock.md) | A reentrant mutual exclusion [Lock](Lock.md) with the same basic behavior and semantics as the implicit monitor lock accessed using`synchronized`methods and statements, but with extended capabilities. |
| [ReentrantReadWriteLock](ReentrantReadWriteLock.md) | An implementation of [ReadWriteLock](ReadWriteLock.md) supporting similar semantics to [ReentrantLock](ReentrantLock.md). |
| [StampedLock](StampedLock.md) | A capability-based lock with three modes for controlling read/write access. |
| --- | --- |
