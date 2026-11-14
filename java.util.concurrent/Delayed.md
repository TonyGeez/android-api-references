# Delayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Delayed

```
interface Delayed : Comparable<Delayed!>
```

| [java.util.concurrent.Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed#) |

| Known Direct Subclasses [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture) | A delayed result-bearing action that can be cancelled. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture) |------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RunnableScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/RunnableScheduledFuture) | A [ScheduledFuture](https://developer.android.com/reference/kotlin/java/util/concurrent/ScheduledFuture) that is [Runnable](https://developer.android.com/reference/kotlin/java/lang/Runnable.html#). | |
| --- | --- | --- | --- | --- | --- | --- |

A mix-in style interface for marking objects that should be acted upon after a given delay.

An implementation of this interface must define a `compareTo` method that provides an ordering consistent with its `getDelay` method.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDelay](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed#getDelay(java.util.concurrent.TimeUnit))`(`unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Returns the remaining delay associated with this object, in the given time unit. |

## Public methods

### getDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDelay(unit: TimeUnit!): Long
```

Returns the remaining delay associated with this object, in the given time unit.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: the time unit |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the remaining delay; zero or negative values indicate that the delay has already elapsed |
