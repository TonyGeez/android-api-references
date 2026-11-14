# java.lang.ref

# java.lang.ref

## Interfaces

| [Cleanable](../java/lang/ref/Cleaner.Cleanable.md) | `Cleanable`represents an object and a cleaning action registered in a`Cleaner`. |
| --- | --- |

## Classes

| [Cleaner](Cleaner.md) | `Cleaner`manages a set of object references and corresponding cleaning actions. |
| --- | --- |
| [PhantomReference](PhantomReference.md) | Phantom reference objects, which are enqueued after the collector determines that their referents may otherwise be reclaimed. |
| [Reference](Reference.md) | Abstract base class for reference objects. |
| [ReferenceQueue](ReferenceQueue.md) | Reference queues, to which registered reference objects are appended by the garbage collector after the appropriate reachability changes are detected. |
| --- | --- |
| [SoftReference](SoftReference.md) | Soft reference objects, which are cleared at the discretion of the garbage collector in response to memory demand. |
| [WeakReference](WeakReference.md) | Weak reference objects, which do not prevent their referents from being made finalizable, finalized, and then reclaimed. |
