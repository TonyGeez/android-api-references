# java.lang.ref

# java.lang.ref

## Interfaces

| [Cleanable](../java/lang/ref/Cleaner.Cleanable.md) | `Cleanable`represents an object and a cleaning action registered in a`Cleaner`. |
| --- | --- |

## Classes

| [Cleaner](../java/lang/ref/Cleaner.md) | `Cleaner`manages a set of object references and corresponding cleaning actions. |
| --- | --- |
| [PhantomReference](../java/lang/ref/PhantomReference.md) | Phantom reference objects, which are enqueued after the collector determines that their referents may otherwise be reclaimed. |
| [Reference](../java/lang/ref/Reference.md) | Abstract base class for reference objects. |
| [ReferenceQueue](../java/lang/ref/ReferenceQueue.md) | Reference queues, to which registered reference objects are appended by the garbage collector after the appropriate reachability changes are detected. |
| --- | --- |
| [SoftReference](../java/lang/ref/SoftReference.md) | Soft reference objects, which are cleared at the discretion of the garbage collector in response to memory demand. |
| [WeakReference](../java/lang/ref/WeakReference.md) | Weak reference objects, which do not prevent their referents from being made finalizable, finalized, and then reclaimed. |
