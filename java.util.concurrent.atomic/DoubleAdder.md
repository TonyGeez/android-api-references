# DoubleAdder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleAdder

```
open class DoubleAdder : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.DoubleAdder](DoubleAdder.md) |

One or more variables that together maintain an initially zero`double`sum. When updates (method [add](DoubleAdder.md))) are contended across threads, the set of variables may grow dynamically to reduce contention. Method [sum](DoubleAdder.md))(or, equivalently [doubleValue](DoubleAdder.md))) returns the current total combined across the variables maintaining the sum. The order of accumulation within or across threads is not guaranteed. Thus, this class may not be applicable if numerical stability is required, especially when combining values of substantially different orders of magnitude.

This class is usually preferable to alternatives when multiple threads update a common value that is used for purposes such as summary statistics that are frequently updated but less frequently read.

This class extends [Number](../java.lang/Number.md), but does*not* define methods such as`equals`,`hashCode`and`compareTo`because instances are expected to be mutated, and so are not useful as collection keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DoubleAdder](DoubleAdder.md))`()` Creates a new adder with initial sum of zero. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](DoubleAdder.md))`(`x:` ` [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)`)` Adds the given value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](DoubleAdder.md))`()` Resets variables maintaining the sum to zero. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sum](DoubleAdder.md))`()` Returns the current sum. |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [sumThenReset](DoubleAdder.md))`()` Equivalent in effect to [sum](DoubleAdder.md))followed by [reset](DoubleAdder.md)). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](DoubleAdder.md))`()` Equivalent to [sum](DoubleAdder.md)). |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](DoubleAdder.md))`()` Returns the [sum](DoubleAdder.md))as a`float`after a narrowing primitive conversion. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](DoubleAdder.md))`()` Returns the [sum](DoubleAdder.md))as an`int`after a narrowing primitive conversion. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](DoubleAdder.md))`()` Returns the [sum](DoubleAdder.md))as a`long`after a narrowing primitive conversion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](DoubleAdder.md))`()` Returns the String representation of the [sum](DoubleAdder.md)). |
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

Equivalent in effect to [sum](DoubleAdder.md))followed by [reset](DoubleAdder.md)). This method may apply for example during quiescent points between multithreaded computations. If there are updates concurrent with this method, the returned value is*not*guaranteed to be the final value occurring before the reset.

| Return ||
|----------------------------------------------------------------------------------|---------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum |

### toDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Equivalent to [sum](DoubleAdder.md)).

| Return ||
|----------------------------------------------------------------------------------|---------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the sum |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the [sum](DoubleAdder.md))as a`float`after a narrowing primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the [sum](DoubleAdder.md))as an`int`after a narrowing primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Returns the [sum](DoubleAdder.md))as a`long`after a narrowing primitive conversion.

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the [sum](DoubleAdder.md)).

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the [sum](DoubleAdder.md)) |
