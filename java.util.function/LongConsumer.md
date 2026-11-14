# LongConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongConsumer

```
@FunctionalInterface interface LongConsumer
```

| [java.util.function.LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#) |

| Known Direct Subclasses [LongStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.Builder.html#), [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#) |----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [LongStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/LongStream.Builder.html#) | A mutable builder for a`LongStream`. | | [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#) | A state object for collecting statistics such as count, min, max, sum, and average. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an operation that accepts a single`long`-valued argument and returns no result. This is the primitive type specialization of [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) for`long`. Unlike most other functional interfaces,`LongConsumer`is expected to operate via side-effects.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [accept(long)](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#accept(kotlin.Long)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#accept(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs this operation on the given argument. |
| open [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#andThen(java.util.function.LongConsumer))`(`after:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#)!`)` Returns a composed`LongConsumer`that performs, in sequence, this operation followed by the`after`operation. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(value: Long): Unit
```

Performs this operation on the given argument.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the input argument |

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: LongConsumer!): LongConsumer!
```

Returns a composed`LongConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#)!:the operation to perform after this operation |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#)! | a composed`LongConsumer`that performs in sequence this operation followed by the`after`operation |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`after`is null |
