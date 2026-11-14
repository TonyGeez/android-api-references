# DoubleSummaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleSummaryStatistics

```
open class DoubleSummaryStatistics : DoubleConsumer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#) |

A state object for collecting statistics such as count, min, max, sum, and average.

This class is designed to work with (though does not require) [streams](https://developer.android.com/reference/kotlin/java/util/stream/package-summary). For example, you can compute summary statistics on a stream of doubles with: 

```kotlin
<code>DoubleSummaryStatistics stats = doubleStream.collect(DoubleSummaryStatistics::new,
                                                       DoubleSummaryStatistics::accept,
                                                       DoubleSummaryStatistics::combine);
  </code>
```

`DoubleSummaryStatistics`can be used as a [reduction](https://developer.android.com/reference/kotlin/java/util/stream/Stream#collect(java.util.stream.Collector))target for a [stream](https://developer.android.com/reference/kotlin/java/util/stream/Stream). For example: 

```kotlin
<code>DoubleSummaryStatistics stats = people.stream()
      .collect(Collectors.summarizingDouble(Person::getWeight));
 </code>
```
This computes, in a single pass, the count of people, as well as the minimum, maximum, sum, and average of their weights.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#DoubleSummaryStatistics())`()` Constructs an empty instance with zero count, zero sum,`Double.POSITIVE_INFINITY`min,`Double.NEGATIVE_INFINITY`max and zero average. |
| [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#DoubleSummaryStatistics(kotlin.Long,%20kotlin.Double,%20kotlin.Double,%20kotlin.Double))`(`count:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `min:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `max:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`, `sum:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Constructs a non-empty instance with the specified`count`,`min`,`max`, and`sum`. |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [accept](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#accept(kotlin.Double))`(`value:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Records another value into the summary information. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [combine](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#combine(java.util.DoubleSummaryStatistics))`(`other:` ` [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#)!`)` Combines the state of another`DoubleSummaryStatistics`into this one. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getAverage](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#getAverage())`()` Returns the arithmetic mean of values recorded, or zero if no values have been recorded. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getCount](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#getCount())`()` Return the count of values recorded. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getMax](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#getMax())`()` Returns the maximum recorded value,`Double.NaN`if any recorded value was NaN or`Double.NEGATIVE_INFINITY`if no values were recorded. |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getMin](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#getMin())`()` Returns the minimum recorded value,`Double.NaN`if any recorded value was NaN or`Double.POSITIVE_INFINITY`if no values were recorded. |
| --- | --- |
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [getSum](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#getSum())`()` Returns the sum of values recorded, or zero if no values have been recorded. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#toString())`()` Returns a non-empty string representation of this object suitable for debugging. |

| Inherited functions ||
|---|---|
| From class [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer) |-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer)! | [andThen](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer#andThen(java.util.function.DoubleConsumer))`(`after:` ` [DoubleConsumer](https://developer.android.com/reference/kotlin/java/util/function/DoubleConsumer)!`)` <br /> Returns a composed`DoubleConsumer`that performs, in sequence, this operation followed by the`after`operation. If performing either operation throws an exception, it is relayed to the caller of the composed operation. If performing this operation throws an exception, the`after`operation will not be performed. <br /> | ||

## Public constructors

### DoubleSummaryStatistics

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DoubleSummaryStatistics()
```

Constructs an empty instance with zero count, zero sum,`Double.POSITIVE_INFINITY`min,`Double.NEGATIVE_INFINITY`max and zero average. 

### DoubleSummaryStatistics

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DoubleSummaryStatistics(
    count: Long, 
    min: Double, 
    max: Double, 
    sum: Double)
```

Constructs a non-empty instance with the specified`count`,`min`,`max`, and`sum`.

If`count`is zero then the remaining arguments are ignored and an empty instance is constructed.

If the arguments are inconsistent then an`IllegalArgumentException`is thrown. The necessary consistent argument conditions are:

- `count >= 0`
- `(min <= max && !isNaN(sum)) || (isNaN(min) && isNaN(max) && isNaN(sum))`
| --- | --- | --- |

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `count` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the count of values |
| `min` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the minimum value |
| `max` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the maximum value |
| --- | --- |
| `sum` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the sum of all values |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if the arguments are inconsistent |

## Public methods

### accept

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun accept(value: Double): Unit
```

Records another value into the summary information.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------|
| `value` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the input value |

### combine

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun combine(other: DoubleSummaryStatistics!): Unit
```

Combines the state of another`DoubleSummaryStatistics`into this one.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `other` | [DoubleSummaryStatistics](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#)!:another`DoubleSummaryStatistics` |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if`other`is null |

### getAverage

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAverage(): Double
```

Returns the arithmetic mean of values recorded, or zero if no values have been recorded.

The computed average can vary numerically and have the special case behavior as computing the sum; see [getSum](https://developer.android.com/reference/kotlin/java/util/DoubleSummaryStatistics#getSum())for details.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the arithmetic mean of values, or zero if none |

### getCount

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCount(): Long
```

Return the count of values recorded.

| Return ||
|------------------------------------------------------------------------------|---------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the count of values |

### getMax

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMax(): Double
```

Returns the maximum recorded value,`Double.NaN`if any recorded value was NaN or`Double.NEGATIVE_INFINITY`if no values were recorded. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the maximum recorded value,`Double.NaN`if any recorded value was NaN or`Double.NEGATIVE_INFINITY`if no values were recorded |

### getMin

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMin(): Double
```

Returns the minimum recorded value,`Double.NaN`if any recorded value was NaN or`Double.POSITIVE_INFINITY`if no values were recorded. Unlike the numerical comparison operators, this method considers negative zero to be strictly smaller than positive zero.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the minimum recorded value,`Double.NaN`if any recorded value was NaN or`Double.POSITIVE_INFINITY`if no values were recorded |

### getSum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSum(): Double
```

Returns the sum of values recorded, or zero if no values have been recorded.

The value of a floating-point sum is a function both of the input values as well as the order of addition operations. The order of addition operations of this method is intentionally not defined to allow for implementation flexibility to improve the speed and accuracy of the computed result. In particular, this method may be implemented using compensated summation or other technique to reduce the error bound in the numerical sum compared to a simple summation of`double`values. Because of the unspecified order of operations and the possibility of using differing summation schemes, the output of this method may vary on the same input values.

Various conditions can result in a non-finite sum being computed. This can occur even if the all the recorded values being summed are finite. If any recorded value is non-finite, the sum will be non-finite:

- If any recorded value is a NaN, then the final sum will be NaN.
- If the recorded values contain one or more infinities, the sum will be infinite or NaN.
 - If the recorded values contain infinities of opposite sign, the sum will be NaN.
 - If the recorded values contain infinities of one sign and an intermediate sum overflows to an infinity of the opposite sign, the sum may be NaN.

It is possible for intermediate sums of finite values to overflow into opposite-signed infinities; if that occurs, the final sum will be NaN even if the recorded values are all finite. If all the recorded values are zero, the sign of zero is*not* guaranteed to be preserved in the final sum.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum of values, or zero if none |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns a non-empty string representation of this object suitable for debugging. The exact presentation format is unspecified and may vary between implementations and versions.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |
