# IntSummaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IntSummaryStatistics

```
open class IntSummaryStatistics : IntConsumer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.util.IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#) |

A state object for collecting statistics such as count, min, max, sum, and average.

This class is designed to work with (though does not require) [streams](https://developer.android.com/reference/kotlin/java/util/stream/package-summary). For example, you can compute summary statistics on a stream of ints with: 

```kotlin
<code>IntSummaryStatistics stats = intStream.collect(IntSummaryStatistics::new,
                                                 IntSummaryStatistics::accept,
                                                 IntSummaryStatistics::combine);
  </code>
```

`IntSummaryStatistics`can be used as a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/Stream#collect(java.util.stream.Collector))target for a [stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream). For example: 

```kotlin
<code>IntSummaryStatistics stats = people.stream()
                                     .collect(Collectors.summarizingInt(Person::getDependents));
 </code>
```
This computes, in a single pass, the count of people, as well as the minimum, maximum, sum, and average of their number of dependents.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#IntSummaryStatistics())`()` Constructs an empty instance with zero count, zero sum,`Integer.MAX_VALUE`min,`Integer.MIN_VALUE`max and zero average. |
| [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#IntSummaryStatistics(kotlin.Long,%20kotlin.Int,%20kotlin.Int,%20kotlin.Long))`(`count:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `min:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `max:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sum:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a non-empty instance with the specified`count`,`min`,`max`, and`sum`. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#accept(kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Records a new value into the summary information |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [combine](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#combine(java.util.IntSummaryStatistics))`(`other:` ` [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#)!`)` Combines the state of another`IntSummaryStatistics`into this one. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAverage](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#getAverage())`()` Returns the arithmetic mean of values recorded, or zero if no values have been recorded. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCount](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#getCount())`()` Returns the count of values recorded. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMax](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#getMax())`()` Returns the maximum value recorded, or`Integer.MIN_VALUE`if no values have been recorded. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMin](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#getMin())`()` Returns the minimum value recorded, or`Integer.MAX_VALUE`if no values have been recorded. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSum](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#getSum())`()` Returns the sum of values recorded, or zero if no values have been recorded. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#toString())`()` Returns a non-empty string representation of this object suitable for debugging. |

| Inherited functions ||
|---|---|
| From class [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer) |-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer#andThen(java.util.function.IntConsumer))`(`after:` ` [IntConsumer](https://developer.android.com/reference/kotlin/java/util/function/IntConsumer)!`)` <br /> Returns a composed`IntConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed. <br /> | ||

## Public constructors

### IntSummaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IntSummaryStatistics()
```

Constructs an empty instance with zero count, zero sum,`Integer.MAX_VALUE`min,`Integer.MIN_VALUE`max and zero average. 

### IntSummaryStatistics

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
IntSummaryStatistics(
    count: Long, 
    min: Int, 
    max: Int, 
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
| `min` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the minimum value |
| `max` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum value |
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

Records a new value into the summary information

| Parameters ||
|---------|--------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the input value |

### combine

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun combine(other: IntSummaryStatistics!): Unit
```

Combines the state of another`IntSummaryStatistics`into this one.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [IntSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/IntSummaryStatistics#)!:another`IntSummaryStatistics` |

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
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the arithmetic mean of values, or zero if none |

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
fun getMax(): Int
```

Returns the maximum value recorded, or`Integer.MIN_VALUE`if no values have been recorded.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum value, or`Integer.MIN_VALUE`if none |

### getMin

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMin(): Int
```

Returns the minimum value recorded, or`Integer.MAX_VALUE`if no values have been recorded.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the minimum value, or`Integer.MAX_VALUE`if none |

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
