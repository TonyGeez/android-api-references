# IntConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntConsumer

```
@FunctionalInterface interface IntConsumer
```

| [java.util.function.IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#) |

| Known Direct Subclasses [IntStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.Builder.html#), [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics.html#), [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [IntStream.Builder](https://developer.android.com/reference/kotlin/java/util/stream/IntStream.Builder.html#) | A mutable builder for an`IntStream`. | | [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics.html#) | A state object for collecting statistics such as count, min, max, sum, and average. | | [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics.html#) | A state object for collecting statistics such as count, min, max, sum, and average. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an operation that accepts a single`int`-valued argument and returns no result. This is the primitive type specialization of [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer) for`int`. Unlike most other functional interfaces,`IntConsumer`is expected to operate via side-effects.

This is a [functional interface](https://developer.android.com/reference/kotlin/java/util/function/package-summary) whose functional method is [accept(int)](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#accept(kotlin.Int)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#accept(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs this operation on the given argument. |
| open [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#andThen(java.util.function.IntConsumer))`(`after:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#)!`)` Returns a composed`IntConsumer`that performs, in sequence, this operation followed by the`after`operation. |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun accept(value: Int): Unit
```

Performs this operation on the given argument.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input argument |

### andThen

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun andThen(after: IntConsumer!): IntConsumer!
```

Returns a composed`IntConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `after` | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#)!:the operation to perform after this operation |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#)! | a composed`IntConsumer`that performs in sequence this operation followed by the`after`operation |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`after`is null |
