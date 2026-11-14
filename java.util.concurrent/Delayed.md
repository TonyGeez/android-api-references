# Delayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Delayed

```
interface Delayed : Comparable<Delayed!>
```

| [java.util.concurrent.Delayed](../java/util/concurrent/Delayed.md) |

| Known Direct Subclasses [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md) | A delayed result-bearing action that can be cancelled. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RunnableScheduledFuture](../java/util/concurrent/RunnableScheduledFuture.md) |------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RunnableScheduledFuture](../java/util/concurrent/RunnableScheduledFuture.md) | A [ScheduledFuture](../java/util/concurrent/ScheduledFuture.md) that is [Runnable](../java/lang/Runnable.md). | |
| --- | --- | --- | --- | --- | --- | --- |

A mix-in style interface for marking objects that should be acted upon after a given delay.

An implementation of this interface must define a `compareTo` method that provides an ordering consistent with its `getDelay` method.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDelay](../java/util/concurrent/Delayed.md))`(`unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Returns the remaining delay associated with this object, in the given time unit. |

## Public methods

### getDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDelay(unit: TimeUnit!): Long
```

Returns the remaining delay associated with this object, in the given time unit.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: the time unit |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the remaining delay; zero or negative values indicate that the delay has already elapsed |
