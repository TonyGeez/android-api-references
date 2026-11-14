# Delayed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Delayed

```
interface Delayed : Comparable<Delayed!>
```

| [java.util.concurrent.Delayed](Delayed.md) |

| Known Direct Subclasses [ScheduledFuture](ScheduledFuture.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------| | [ScheduledFuture](ScheduledFuture.md) | A delayed result-bearing action that can be cancelled. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [RunnableScheduledFuture](RunnableScheduledFuture.md) |------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RunnableScheduledFuture](RunnableScheduledFuture.md) | A [ScheduledFuture](ScheduledFuture.md) that is [Runnable](../java.lang/Runnable.md). | |
| --- | --- | --- | --- | --- | --- | --- |

A mix-in style interface for marking objects that should be acted upon after a given delay.

An implementation of this interface must define a `compareTo` method that provides an ordering consistent with its `getDelay` method.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getDelay](Delayed.md))`(`unit:` ` [TimeUnit](TimeUnit.md)!`)` Returns the remaining delay associated with this object, in the given time unit. |

## Public methods

### getDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDelay(unit: TimeUnit!): Long
```

Returns the remaining delay associated with this object, in the given time unit.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------|
| `unit` | [TimeUnit](TimeUnit.md)!: the time unit |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the remaining delay; zero or negative values indicate that the delay has already elapsed |
