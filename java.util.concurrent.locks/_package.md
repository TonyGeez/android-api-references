# java.util.concurrent.locks

# java.util.concurrent.locks

## Interfaces

| [Condition](../java/util/concurrent/locks/Condition.md) | `Condition`factors out the`Object`monitor methods ([wait](../java/lang/Object.md)), [notify](../java/lang/Object.md))and [notifyAll](../java/lang/Object.md))) into distinct objects to give the effect of having multiple wait-sets per object, by combining them with the use of arbitrary [Lock](../java/util/concurrent/locks/Lock.md) implementations. |
| --- | --- |
| [Lock](../java/util/concurrent/locks/Lock.md) | `Lock`implementations provide more extensive locking operations than can be obtained using`synchronized`methods and statements. |
| [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md) | A`ReadWriteLock`maintains a pair of associated [locks](../java/util/concurrent/locks/Lock.md), one for read-only operations and one for writing. |

## Classes

| [AbstractOwnableSynchronizer](../java/util/concurrent/locks/AbstractOwnableSynchronizer.md) | A synchronizer that may be exclusively owned by a thread. |
| --- | --- |
| [AbstractQueuedLongSynchronizer](../java/util/concurrent/locks/AbstractQueuedLongSynchronizer.md) | A version of [AbstractQueuedSynchronizer](../java/util/concurrent/locks/AbstractQueuedSynchronizer.md) in which synchronization state is maintained as a`long`. |
| [AbstractQueuedSynchronizer](../java/util/concurrent/locks/AbstractQueuedSynchronizer.md) | Provides a framework for implementing blocking locks and related synchronizers (semaphores, events, etc) that rely on first-in-first-out (FIFO) wait queues. |
| [LockSupport](../java/util/concurrent/locks/LockSupport.md) | Basic thread blocking primitives for creating locks and other synchronization classes. |
| --- | --- |
| [ReentrantLock](../java/util/concurrent/locks/ReentrantLock.md) | A reentrant mutual exclusion [Lock](../java/util/concurrent/locks/Lock.md) with the same basic behavior and semantics as the implicit monitor lock accessed using`synchronized`methods and statements, but with extended capabilities. |
| [ReentrantReadWriteLock](../java/util/concurrent/locks/ReentrantReadWriteLock.md) | An implementation of [ReadWriteLock](../java/util/concurrent/locks/ReadWriteLock.md) supporting similar semantics to [ReentrantLock](../java/util/concurrent/locks/ReentrantLock.md). |
| [StampedLock](../java/util/concurrent/locks/StampedLock.md) | A capability-based lock with three modes for controlling read/write access. |
| --- | --- |
