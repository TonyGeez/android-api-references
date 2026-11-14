# DoubleConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleConsumer

```
@FunctionalInterface interface DoubleConsumer
```

| [java.util.function.DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#) |

| Known Direct Subclasses [DoubleStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.Builder.html#), [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics.html#) |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [DoubleStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/DoubleStream.Builder.html#) | A mutable builder for a`DoubleStream`. | | [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics.html#) | A state object for collecting statistics such as count, min, max, sum, and average. | |

Represents an operation that accepts a single`double`-valued argument and returns no result. This is the primitive type specialization of [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) for`double`. Unlike most other functional interfaces,`DoubleConsumer`is expected to operate via side-effects.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [accept(double)](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#accept(kotlin.Double)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#accept(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Performs this operation on the given argument. |
| open [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#andThen(java.util.function.DoubleConsumer))`(`after:` ` [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#)!`)` Returns a composed`DoubleConsumer`that performs, in sequence, this operation followed by the`after`operation. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(value: Double): Unit
```

Performs this operation on the given argument.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the input argument |

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: DoubleConsumer!): DoubleConsumer!
```

Returns a composed`DoubleConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#)!:the operation to perform after this operation |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#)! | a composed`DoubleConsumer`that performs in sequence this operation followed by the`after`operation |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`after`is null |
