# DoubleConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleConsumer

```
@FunctionalInterface interface DoubleConsumer
```

| [java.util.function.DoubleConsumer](../java/util/function/DoubleConsumer.md) |

| Known Direct Subclasses [DoubleStream.Builder](../java/util/stream/DoubleStream.Builder.md), [DoubleSummaryStatistics](../java/util/DoubleSummaryStatistics.md) |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [DoubleStream.Builder](../java/util/stream/DoubleStream.Builder.md) | A mutable builder for a`DoubleStream`. | | [DoubleSummaryStatistics](../java/util/DoubleSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an operation that accepts a single`double`-valued argument and returns no result. This is the primitive type specialization of [Consumer](../java/util/function/Consumer.md) for`double`. Unlike most other functional interfaces,`DoubleConsumer`is expected to operate via side-effects.

This is a [functional interface](../java/util/function/_package.md) whose functional method is [accept(double)](../java/util/function/DoubleConsumer.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](../java/util/function/DoubleConsumer.md))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Performs this operation on the given argument. |
| open [DoubleConsumer](../java/util/function/DoubleConsumer.md)! | [andThen](../java/util/function/DoubleConsumer.md))`(`after:` ` [DoubleConsumer](../java/util/function/DoubleConsumer.md)!`)` Returns a composed`DoubleConsumer`that performs, in sequence, this operation followed by the`after`operation. |

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
| `after` | [DoubleConsumer](../java/util/function/DoubleConsumer.md)!:the operation to perform after this operation |

| Return ||
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [DoubleConsumer](../java/util/function/DoubleConsumer.md)! | a composed`DoubleConsumer`that performs in sequence this operation followed by the`after`operation |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`after`is null |
