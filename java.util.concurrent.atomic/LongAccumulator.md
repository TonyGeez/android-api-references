Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongAccumulator

```
open class LongAccumulator : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.LongAccumulator](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#) |

One or more variables that together maintain a running `long` value updated using a supplied function. When updates (method `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#accumulate(kotlin.Long)`) are contended across threads, the set of variables may grow dynamically to reduce contention. Method `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()` (or, equivalently, `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#toLong()`) returns the current value across the variables maintaining updates.

This class is usually preferable to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong` when multiple threads update a common value that is used for purposes such as collecting statistics, not for fine-grained synchronization control. Under low update contention, the two classes have similar characteristics. But under high contention, expected throughput of this class is significantly higher, at the expense of higher space consumption.

The order of accumulation within or across threads is not guaranteed and cannot be depended upon, so this class is only applicable to functions for which the order of accumulation does not matter. The supplied accumulator function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. For predictable results, the accumulator function should be associative and commutative. The function is applied with an existing value (or identity) as one argument, and a given update as the other argument. For example, to maintain a running maximum value, you could supply `Long::max` along with `Long.MIN_VALUE` as the identity.

Class `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder` provides analogs of the functionality of this class for the common special case of maintaining counts and sums. The call `new LongAdder()` is equivalent to `new LongAccumulator((x, y) -> x + y, 0L)`.

This class extends `https://developer.android.com/reference/kotlin/java/lang/Number.html#`, but does *not* define methods such as `equals`, `hashCode` and `compareTo` because instances are expected to be mutated, and so are not useful as collection keys.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#LongAccumulator(java.util.function.LongBinaryOperator,%20kotlin.Long)(accumulatorFunction: https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#!, identity: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Creates a new instance using the given accumulator function and identity element. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#accumulate(kotlin.Long)(x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Updates with the given value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()()` Returns the current value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#getThenReset()()` Equivalent in effect to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()` followed by `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#reset()`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#reset()()` Resets variables maintaining updates to the identity value. |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#toDouble()()` Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()) as a `double` after a widening primitive conversion. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#toFloat()()` Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()) as a `float` after a widening primitive conversion. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#toInt()()` Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()) as an `int` after a narrowing primitive conversion. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#toLong()()` Equivalent to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()`. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#toString()()` {@return the String representation of the current value} |

## Public constructors

### LongAccumulator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LongAccumulator(
    accumulatorFunction: LongBinaryOperator!, 
    identity: Long)
```

Creates a new instance using the given accumulator function and identity element.

| Parameters ||
|---|---|
| `accumulatorFunction` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!: a side-effect-free function of two arguments |
| `identity` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): identity (initial value) for the accumulator function |

## Public methods

### accumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun accumulate(x: Long): Unit
```

Updates with the given value.

| Parameters ||
|---|---|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value |

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(): Long
```

Returns the current value. The returned value is *NOT* an atomic snapshot; invocation in the absence of concurrent updates returns an accurate result, but concurrent updates that occur while the value is being calculated might not be incorporated.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current value |

### getThenReset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getThenReset(): Long
```

Equivalent in effect to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()` followed by `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#reset()`. This method may apply for example during quiescent points between multithreaded computations. If there are updates concurrent with this method, the returned value is *not* guaranteed to be the final value occurring before the reset.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value before reset |

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

Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()) as a `double` after a widening primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html` | the numeric value represented by this object after conversion to type `double`. |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toFloat(): Float
```

Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()) as a `float` after a widening primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | the numeric value represented by this object after conversion to type `float`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toInt(): Int
```

Returns the [current value](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()) as an `int` after a narrowing primitive conversion.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the numeric value represented by this object after conversion to type `int`. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toLong(): Long
```

Equivalent to `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAccumulator#get()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current value |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

{@return the String representation of the current value}

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
