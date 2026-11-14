# ForkJoinPool.ManagedBlocker

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ManagedBlocker

```
interface ManagedBlocker
```

| [java.util.concurrent.ForkJoinPool.ManagedBlocker](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md) |

Interface for extending managed parallelism for tasks running in [ForkJoinPool](ForkJoinPool.md) s.

A`ManagedBlocker`provides two methods. Method [isReleasable](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md))must return`true`if blocking is not necessary. Method [block](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md))blocks the current thread if necessary (perhaps internally invoking`isReleasable`before actually blocking). These actions are performed by any thread invoking [java.util.concurrent.ForkJoinPool#managedBlock(java.util.concurrent.ForkJoinPool.ManagedBlocker)](ForkJoinPool.md)). The unusual methods in this API accommodate synchronizers that may, but don't usually, block for long periods. Similarly, they allow more efficient internal handling of cases in which additional workers may be, but usually are not, needed to ensure sufficient parallelism. Toward this end, implementations of method`isReleasable`must be amenable to repeated invocation. Neither method is invoked after a prior invocation of`isReleasable`or`block`returns`true`.

For example, here is a ManagedBlocker based on a ReentrantLock: 

```kotlin
<code>class ManagedLocker implements ManagedBlocker {
    final ReentrantLock lock;
    boolean hasLock = false;
    ManagedLocker(ReentrantLock lock) { this.lock = lock; }
    public boolean block() {
      if (!hasLock)
        lock.lock();
      return true;
    }
    public boolean isReleasable() {
      return hasLock || (hasLock = lock.tryLock());
    }
  }</code>
```

Here is a class that possibly blocks waiting for an item on a given queue: 

```kotlin
<code>class QueueTaker&lt;E&gt; implements ManagedBlocker {
    final BlockingQueue&lt;E&gt; queue;
    volatile E item = null;
    QueueTaker(BlockingQueue&lt;E&gt; q) { this.queue = q; }
    public boolean block() throws InterruptedException {
      if (item == null)
        item = queue.take();
      return true;
    }
    public boolean isReleasable() {
      return item != null || (item = queue.poll()) != null;
    }
    public E getItem() { // call after pool.managedBlock completes
      return item;
    }
  }</code>
```

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [block](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md))`()` Possibly blocks the current thread, for example waiting for a lock or condition. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReleasable](../java/util/concurrent/ForkJoinPool.ManagedBlocker.md))`()` Returns`true`if blocking is unnecessary. |

## Public methods

### block

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun block(): Boolean
```

Possibly blocks the current thread, for example waiting for a lock or condition.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if no additional blocking is necessary (i.e., if isReleasable would return true) |

| Exceptions ||
|----------------------------------|---------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting (the method is not required to do so, but is allowed to) |

### isReleasable

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isReleasable(): Boolean
```

Returns`true`if blocking is unnecessary.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if blocking is unnecessary |
