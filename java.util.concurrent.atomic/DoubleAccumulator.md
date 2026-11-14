Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DoubleAccumulator

```
open class DoubleAccumulator : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.DoubleAccumulator](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#) |

One or more variables that together maintain a running `double` value updated using a supplied function. When updates (method `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#accumulate(kotlin.Double)`) are contended across threads, the set of variables may grow dynamically to reduce contention. Method `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()` (or, equivalently, `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#toDouble()`) returns the current value across the variables maintaining updates.

This class is usually preferable to alternatives when multiple threads update a common value that is used for purposes such as summary statistics that are frequently updated but less frequently read.

The supplied accumulator function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. For predictable results, the accumulator function should be commutative and associative within the floating point tolerance required in usage contexts. The function is applied with an existing value (or identity) as one argument, and a given update as the other argument. For example, to maintain a running maximum value, you could supply `Double::max` along with `Double.NEGATIVE_INFINITY` as the identity. The order of accumulation within or across threads is not guaranteed. Thus, this class may not be applicable if numerical stability is required, especially when combining values of substantially different orders of magnitude.

Class `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAdder` provides analogs of the functionality of this class for the common special case of maintaining sums. The call `new DoubleAdder()` is equivalent to `new DoubleAccumulator((x, y) -> x + y, 0.0)`.

This class extends `https://developer.android.com/reference/kotlin/java/lang/Number.html#`, but does *not* define methods such as `equals`, `hashCode` and `compareTo` because instances are expected to be mutated, and so are not useful as collection keys.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#DoubleAccumulator(java.util.function.DoubleBinaryOperator,%20kotlin.Double)(accumulatorFunction: https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#!, identity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Creates a new instance using the given accumulator function and identity element. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#accumulate(kotlin.Double)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html)` Updates with the given value. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()()` Returns the current value. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#getThenReset()()` Equivalent in effect to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()` followed by `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#reset()`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#reset()()` Resets variables maintaining updates to the identity value. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#toDouble()()` Equivalent to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()`. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#toFloat()()` Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()) as a `float` after a narrowing primitive conversion. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#toInt()()` Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()) as an `int` after a narrowing primitive conversion. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#toLong()()` Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()) as a `long` after a narrowing primitive conversion. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#toString()()` {@return the String representation of the current value} |
| --- | --- |

## Public constructors

### DoubleAccumulator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DoubleAccumulator(
    accumulatorFunction: DoubleBinaryOperator!, 
    identity: Double)
```

Creates a new instance using the given accumulator function and identity element.

| Parameters ||
|---|---|
| `accumulatorFunction` | [DoubleBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/DoubleBinaryOperator.html#)!: a side-effect-free function of two arguments |
| `identity` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): identity (initial value) for the accumulator function |

## Public methods

### accumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun accumulate(x: Double): Unit
```

Updates with the given value.

| Parameters ||
|---|---|
| `x` | [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html): the value |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(): Double
```

Returns the current value. The returned value is *NOT* an atomic snapshot; invocation in the absence of concurrent updates returns an accurate result, but concurrent updates that occur while the value is being calculated might not be incorporated.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the current value |

### getThenReset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getThenReset(): Double
```

Equivalent in effect to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()` followed by `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#reset()`. This method may apply for example during quiescent points between multithreaded computations. If there are updates concurrent with this method, the returned value is *not* guaranteed to be the final value occurring before the reset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the value before reset |

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reset(): Unit
```

Resets variables maintaining updates to the identity value. This method may be a useful alternative to creating a new updater, but is only effective if there are no concurrent updates. Because this method is intrinsically racy, it should only be used when it is known that no threads are concurrently updating.

### toDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toDouble(): Double
```

Equivalent to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the current value |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toFloat(): Float
```

Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()) as a `float` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the numeric value represented by this object after conversion to type `float`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toInt(): Int
```

Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()) as an `int` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the numeric value represented by this object after conversion to type `int`. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toLong(): Long
```

Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/DoubleAccumulator#get()) as a `long` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the numeric value represented by this object after conversion to type `long`. |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

{@return the String representation of the current value}

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
