# DoubleAdder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleAdder

```
open class DoubleAdder : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.DoubleAdder](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#) |

One or more variables that together maintain an initially zero`double`sum. When updates (method [add](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#add(kotlin.Double))) are contended across threads, the set of variables may grow dynamically to reduce contention. Method [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())(or, equivalently [doubleValue](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#toDouble())) returns the current total combined across the variables maintaining the sum. The order of accumulation within or across threads is not guaranteed. Thus, this class may not be applicable if numerical stability is required, especially when combining values of substantially different orders of magnitude.

This class is usually preferable to alternatives when multiple threads update a common value that is used for purposes such as summary statistics that are frequently updated but less frequently read.

This class extends [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#), but does*not* define methods such as`equals`,`hashCode`and`compareTo`because instances are expected to be mutated, and so are not useful as collection keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DoubleAdder](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#DoubleAdder())`()` Creates a new adder with initial sum of zero. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#add(kotlin.Double))`(`x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Adds the given value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#reset())`()` Resets variables maintaining the sum to zero. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())`()` Returns the current sum. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sumThenReset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sumThenReset())`()` Equivalent in effect to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())followed by [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#reset()). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#toDouble())`()` Equivalent to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum()). |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#toFloat())`()` Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())as a`float`after a narrowing primitive conversion. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#toInt())`()` Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())as an`int`after a narrowing primitive conversion. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#toLong())`()` Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())as a`long`after a narrowing primitive conversion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#toString())`()` Returns the String representation of the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum()). |
| --- | --- |

## Public constructors

### DoubleAdder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DoubleAdder()
```

Creates a new adder with initial sum of zero.

## Public methods

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(x: Double): Unit
```

Adds the given value.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html):the value to add |

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets variables maintaining the sum to zero. This method may be a useful alternative to creating a new adder, but is only effective if there are no concurrent updates. Because this method is intrinsically racy, it should only be used when it is known that no threads are concurrently updating. 

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sum(): Double
```

Returns the current sum. The returned value is*NOT*an atomic snapshot; invocation in the absence of concurrent updates returns an accurate result, but concurrent updates that occur while the sum is being calculated might not be incorporated. Also, because floating-point arithmetic is not strictly associative, the returned result need not be identical to the value that would be obtained in a sequential series of updates to a single variable.

| Return ||
|----------------------------------------------------------------------------------|---------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum |

### sumThenReset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sumThenReset(): Double
```

Equivalent in effect to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())followed by [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#reset()). This method may apply for example during quiescent points between multithreaded computations. If there are updates concurrent with this method, the returned value is*not*guaranteed to be the final value occurring before the reset.

| Return ||
|----------------------------------------------------------------------------------|---------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum |

### toDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Equivalent to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum()).

| Return ||
|----------------------------------------------------------------------------------|---------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())as a`float`after a narrowing primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())as an`int`after a narrowing primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum())as a`long`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum()).

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder#sum()) |
