# LongSummaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongSummaryStatistics

```
open class LongSummaryStatistics : IntConsumer, LongConsumer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#) |

A state object for collecting statistics such as count, min, max, sum, and average.

This class is designed to work with (though does not require) [streams](https://developer.android.com/reference/kotlin/java/util/stream/package-summary). For example, you can compute summary statistics on a stream of longs with: 

```kotlin
<code>LongSummaryStatistics stats = longStream.collect(LongSummaryStatistics::new,
                                                   LongSummaryStatistics::accept,
                                                   LongSummaryStatistics::combine);
  </code>
```

`LongSummaryStatistics`can be used as a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/Stream#collect(java.util.stream.Collector))target for a [stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream). For example: 

```kotlin
<code>LongSummaryStatistics stats = people.stream()
                                      .collect(Collectors.summarizingLong(Person::getAge));
 </code>
```
This computes, in a single pass, the count of people, as well as the minimum, maximum, sum, and average of their ages.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#LongSummaryStatistics())`()` Constructs an empty instance with zero count, zero sum,`Long.MAX_VALUE`min,`Long.MIN_VALUE`max and zero average. |
| [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#LongSummaryStatistics(kotlin.Long,%20kotlin.Long,%20kotlin.Long,%20kotlin.Long))`(`count:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `min:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `max:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `sum:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a non-empty instance with the specified`count`,`min`,`max`, and`sum`. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#accept(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Records a new`int`value into the summary information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#accept(kotlin.Long))`(`value:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Records a new`long`value into the summary information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [combine](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#combine(java.util.LongSummaryStatistics))`(`other:` ` [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#)!`)` Combines the state of another`LongSummaryStatistics`into this one. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAverage](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#getAverage())`()` Returns the arithmetic mean of values recorded, or zero if no values have been recorded. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCount](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#getCount())`()` Returns the count of values recorded. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMax](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#getMax())`()` Returns the maximum value recorded, or`Long.MIN_VALUE`if no values have been recorded |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getMin](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#getMin())`()` Returns the minimum value recorded, or`Long.MAX_VALUE`if no values have been recorded. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSum](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#getSum())`()` Returns the sum of values recorded, or zero if no values have been recorded. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#toString())`()` Returns a non-empty string representation of this object suitable for debugging. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer) |-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#andThen(java.util.function.IntConsumer))`(`after:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)!`)` <br /> Returns a composed`IntConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed. <br /> | ||
| From class [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer) |-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer#andThen(java.util.function.LongConsumer))`(`after:` ` [LongConsumer](https://developer.android.com/reference/kotlin/java/util/function/LongConsumer)!`)` <br /> Returns a composed`LongConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed. <br /> | ||

## Public constructors

### LongSummaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LongSummaryStatistics()
```

Constructs an empty instance with zero count, zero sum,`Long.MAX_VALUE`min,`Long.MIN_VALUE`max and zero average. 

### LongSummaryStatistics

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LongSummaryStatistics(
    count: Long, 
    min: Long, 
    max: Long, 
    sum: Long)
```

Constructs a non-empty instance with the specified`count`,`min`,`max`, and`sum`.

If`count`is zero then the remaining arguments are ignored and an empty instance is constructed.

If the arguments are inconsistent then an`IllegalArgumentException`is thrown. The necessary consistent argument conditions are:

- `count >= 0`
- `min <= max`

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------|
| `count` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the count of values |
| `min` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the minimum value |
| `max` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum value |
| --- | --- |
| `sum` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the sum of all values |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if the arguments are inconsistent |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun accept(value: Int): Unit
```

Records a new`int`value into the summary information.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input value |

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun accept(value: Long): Unit
```

Records a new`long`value into the summary information.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------|
| `value` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the input value |

### combine

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun combine(other: LongSummaryStatistics!): Unit
```

Combines the state of another`LongSummaryStatistics`into this one.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [LongSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/LongSummaryStatistics#)!:another`LongSummaryStatistics` |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`other`is null |

### getAverage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAverage(): Double
```

Returns the arithmetic mean of values recorded, or zero if no values have been recorded.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | The arithmetic mean of values, or zero if none |

### getCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCount(): Long
```

Returns the count of values recorded.

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the count of values |

### getMax

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMax(): Long
```

Returns the maximum value recorded, or`Long.MIN_VALUE`if no values have been recorded

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the maximum value, or`Long.MIN_VALUE`if none |

### getMin

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMin(): Long
```

Returns the minimum value recorded, or`Long.MAX_VALUE`if no values have been recorded.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the minimum value, or`Long.MAX_VALUE`if none |

### getSum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSum(): Long
```

Returns the sum of values recorded, or zero if no values have been recorded.

| Return ||
|------------------------------------------------------------------------------|------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum of values, or zero if none |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a non-empty string representation of this object suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
