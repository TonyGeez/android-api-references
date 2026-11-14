# java.lang.ref

# java.lang.ref

## Interfaces

| [Cleanable](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner.Cleanable) | `Cleanable`represents an object and a cleaning action registered in a`Cleaner`. |

## Classes

| [Cleaner](https://developer.android.com/reference/kotlin/java/lang/ref/Cleaner) | `Cleaner`manages a set of object references and corresponding cleaning actions. |
| [PhantomReference](https://developer.android.com/reference/kotlin/java/lang/ref/PhantomReference) | Phantom reference objects, which are enqueued after the collector determines that their referents may otherwise be reclaimed. |
| [Reference](https://developer.android.com/reference/kotlin/java/lang/ref/Reference) | Abstract base class for reference objects. |
| [ReferenceQueue](https://developer.android.com/reference/kotlin/java/lang/ref/ReferenceQueue) | Reference queues, to which registered reference objects are appended by the garbage collector after the appropriate reachability changes are detected. |
| [SoftReference](https://developer.android.com/reference/kotlin/java/lang/ref/SoftReference) | Soft reference objects, which are cleared at the discretion of the garbage collector in response to memory demand. |
| [WeakReference](https://developer.android.com/reference/kotlin/java/lang/ref/WeakReference) | Weak reference objects, which do not prevent their referents from being made finalizable, finalized, and then reclaimed. |
