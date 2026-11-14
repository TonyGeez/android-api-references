# java.util.concurrent.locks

# java.util.concurrent.locks

## Interfaces

| [Condition](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Condition) | `Condition`factors out the`Object`monitor methods ([wait](https://developer.android.com/reference/kotlin/java/lang/Object.html#wait()), [notify](https://developer.android.com/reference/kotlin/java/lang/Object.html#notify())and [notifyAll](https://developer.android.com/reference/kotlin/java/lang/Object.html#notifyAll())) into distinct objects to give the effect of having multiple wait-sets per object, by combining them with the use of arbitrary [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) implementations. |
| --- | --- |
| [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) | `Lock`implementations provide more extensive locking operations than can be obtained using`synchronized`methods and statements. |
| [ReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReadWriteLock) | A`ReadWriteLock`maintains a pair of associated [locks](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock), one for read-only operations and one for writing. |

## Classes

| [AbstractOwnableSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractOwnableSynchronizer) | A synchronizer that may be exclusively owned by a thread. |
| --- | --- |
| [AbstractQueuedLongSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedLongSynchronizer) | A version of [AbstractQueuedSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer) in which synchronization state is maintained as a`long`. |
| [AbstractQueuedSynchronizer](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/AbstractQueuedSynchronizer) | Provides a framework for implementing blocking locks and related synchronizers (semaphores, events, etc) that rely on first-in-first-out (FIFO) wait queues. |
| [LockSupport](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/LockSupport) | Basic thread blocking primitives for creating locks and other synchronization classes. |
| --- | --- |
| [ReentrantLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantLock) | A reentrant mutual exclusion [Lock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/Lock) with the same basic behavior and semantics as the implicit monitor lock accessed using`synchronized`methods and statements, but with extended capabilities. |
| [ReentrantReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantReadWriteLock) | An implementation of [ReadWriteLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReadWriteLock) supporting similar semantics to [ReentrantLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/ReentrantLock). |
| [StampedLock](https://developer.android.com/reference/kotlin/java/util/concurrent/locks/StampedLock) | A capability-based lock with three modes for controlling read/write access. |
| --- | --- |
