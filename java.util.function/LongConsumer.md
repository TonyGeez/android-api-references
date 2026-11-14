# LongConsumer

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongConsumer

```
@FunctionalInterface interface LongConsumer
```

| [java.util.function.LongConsumer](LongConsumer.md) |

| Known Direct Subclasses [LongStream.Builder](../java/util/stream/LongStream.Builder.md), [LongSummaryStatistics](../java.util/LongSummaryStatistics.md) |----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------| | [LongStream.Builder](../java/util/stream/LongStream.Builder.md) | A mutable builder for a`LongStream`. | | [LongSummaryStatistics](../java.util/LongSummaryStatistics.md) | A state object for collecting statistics such as count, min, max, sum, and average. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents an operation that accepts a single`long`-valued argument and returns no result. This is the primitive type specialization of [Consumer](Consumer.md) for`long`. Unlike most other functional interfaces,`LongConsumer`is expected to operate via side-effects.

This is a [functional interface](_package.md) whose functional method is [accept(long)](LongConsumer.md)).

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](LongConsumer.md))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Performs this operation on the given argument. |
| open [LongConsumer](LongConsumer.md)! | [andThen](LongConsumer.md))`(`after:` ` [LongConsumer](LongConsumer.md)!`)` Returns a composed`LongConsumer`that performs, in sequence, this operation followed by the`after`operation. |

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
| `after` | [LongConsumer](LongConsumer.md)!:the operation to perform after this operation |

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [LongConsumer](LongConsumer.md)! | a composed`LongConsumer`that performs in sequence this operation followed by the`after`operation |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`after`is null |
