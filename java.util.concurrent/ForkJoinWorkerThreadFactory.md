# ForkJoinPool.ForkJoinWorkerThreadFactory

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForkJoinWorkerThreadFactory

```
interface ForkJoinWorkerThreadFactory
```

| [java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory#) |

Factory for creating new [ForkJoinWorkerThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread) s. A`ForkJoinWorkerThreadFactory`must be defined and used for`ForkJoinWorkerThread`subclasses that extend base functionality or initialize threads with different contexts.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ForkJoinWorkerThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread)! | [newThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory#newThread(java.util.concurrent.ForkJoinPool))`(`pool:` ` [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool)!`)` Returns a new worker thread operating in the given pool. |

## Public methods

### newThread

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newThread(pool: ForkJoinPool!): ForkJoinWorkerThread!
```

Returns a new worker thread operating in the given pool. Returning null or throwing an exception may result in tasks never being executed. If this method throws an exception, it is relayed to the caller of the method (for example`execute`) causing attempted thread creation. If this method returns null or throws an exception, it is not retried until the next attempted creation (for example another call to`execute`).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `pool` | [ForkJoinPool](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinPool)!:the pool this thread works in |

| Return ||
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ForkJoinWorkerThread](https://developer.android.com/reference/kotlin/java/util/concurrent/ForkJoinWorkerThread)! | the new worker thread, or`null`if the request to create a thread is rejected |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the pool is null |
