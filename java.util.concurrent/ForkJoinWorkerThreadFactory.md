# ForkJoinPool.ForkJoinWorkerThreadFactory

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ForkJoinWorkerThreadFactory

```
interface ForkJoinWorkerThreadFactory
```

| [java.util.concurrent.ForkJoinPool.ForkJoinWorkerThreadFactory](../java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory.md) |

Factory for creating new [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md) s. A`ForkJoinWorkerThreadFactory`must be defined and used for`ForkJoinWorkerThread`subclasses that extend base functionality or initialize threads with different contexts.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md)! | [newThread](../java/util/concurrent/ForkJoinPool.ForkJoinWorkerThreadFactory.md))`(`pool:` ` [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md)!`)` Returns a new worker thread operating in the given pool. |

## Public methods

### newThread

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun newThread(pool: ForkJoinPool!): ForkJoinWorkerThread!
```

Returns a new worker thread operating in the given pool. Returning null or throwing an exception may result in tasks never being executed. If this method throws an exception, it is relayed to the caller of the method (for example`execute`) causing attempted thread creation. If this method returns null or throws an exception, it is not retried until the next attempted creation (for example another call to`execute`).

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------|
| `pool` | [ForkJoinPool](../java/util/concurrent/ForkJoinPool.md)!:the pool this thread works in |

| Return ||
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [ForkJoinWorkerThread](../java/util/concurrent/ForkJoinWorkerThread.md)! | the new worker thread, or`null`if the request to create a thread is rejected |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if the pool is null |
