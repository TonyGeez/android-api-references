# IntConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntConsumer

```
@FunctionalInterface interface IntConsumer
```

| [java.util.function.IntConsumer](IntConsumer.md) |

| Known Direct Subclasses [IntStream.Builder](../java/util/stream/IntStream.Builder.md), [IntSummaryStatistics](../java.util/IntSummaryStatistics.md), [LongSummaryStatistics](../java.util/LongSummaryStatistics.md) |---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [IntStream.Builder](../java/util/stream/IntStream.Builder.md) | A mutable builder for an`IntStream`. | | [IntSummaryStatistics](../java.util/IntSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. | | [LongSummaryStatistics](../java.util/LongSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an operation that accepts a single`int`-valued argument and returns no result. This is the primitive type specialization of [Consumer](Consumer.md) for`int`. Unlike most other functional interfaces,`IntConsumer`is expected to operate via side-effects.

This is a [functional interface](_package.md) whose functional method is [accept(int)](IntConsumer.md)).

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](IntConsumer.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Performs this operation on the given argument. |
| open [IntConsumer](IntConsumer.md)! | [andThen](IntConsumer.md))`(`after:` ` [IntConsumer](IntConsumer.md)!`)` Returns a composed`IntConsumer`that performs, in sequence, this operation followed by the`after`operation. |

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
| `after` | [IntConsumer](IntConsumer.md)!:the operation to perform after this operation |

| Return ||
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [IntConsumer](IntConsumer.md)! | a composed`IntConsumer`that performs in sequence this operation followed by the`after`operation |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`after`is null |
