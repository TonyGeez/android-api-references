# LongAdder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongAdder

```
open class LongAdder : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.LongAdder](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#) |

One or more variables that together maintain an initially zero`long`sum. When updates (method [add](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#add(kotlin.Long))) are contended across threads, the set of variables may grow dynamically to reduce contention. Method [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())(or, equivalently, [longValue](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#toLong())) returns the current total combined across the variables maintaining the sum.

This class is usually preferable to [AtomicLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong) when multiple threads update a common sum that is used for purposes such as collecting statistics, not for fine-grained synchronization control. Under low update contention, the two classes have similar characteristics. But under high contention, expected throughput of this class is significantly higher, at the expense of higher space consumption.

LongAdders can be used with a to maintain a scalable frequency map (a form of histogram or multiset). For example, to add a count to a`ConcurrentHashMap<String,LongAdder> freqs`, initializing if not already present, you can use`freqs.computeIfAbsent(key, k -> new LongAdder()).increment();`

This class extends [Number](https://developer.android.com/reference/kotlin/java/lang/Number.html#), but does*not* define methods such as`equals`,`hashCode`and`compareTo`because instances are expected to be mutated, and so are not useful as collection keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LongAdder](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#LongAdder())`()` Creates a new adder with initial sum of zero. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#add(kotlin.Long))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Adds the given value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [decrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#decrement())`()` Equivalent to`add(-1)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [increment](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#increment())`()` Equivalent to`add(1)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#reset())`()` Resets variables maintaining the sum to zero. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())`()` Returns the current sum. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sumThenReset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sumThenReset())`()` Equivalent in effect to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())followed by [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#reset()). |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#toDouble())`()` Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())as a`double`after a widening primitive conversion. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#toFloat())`()` Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())as a`float`after a widening primitive conversion. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#toInt())`()` Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())as an`int`after a narrowing primitive conversion. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#toLong())`()` Equivalent to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum()). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#toString())`()` Returns the String representation of the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum()). |

## Public constructors

### LongAdder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LongAdder()
```

Creates a new adder with initial sum of zero.

## Public methods

### add

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(x: Long): Unit
```

Adds the given value.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to add |

### decrement

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun decrement(): Unit
```

Equivalent to`add(-1)`. 

### increment

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun increment(): Unit
```

Equivalent to`add(1)`. 

### reset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reset(): Unit
```

Resets variables maintaining the sum to zero. This method may be a useful alternative to creating a new adder, but is only effective if there are no concurrent updates. Because this method is intrinsically racy, it should only be used when it is known that no threads are concurrently updating. 

### sum

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sum(): Long
```

Returns the current sum. The returned value is*NOT*an atomic snapshot; invocation in the absence of concurrent updates returns an accurate result, but concurrent updates that occur while the sum is being calculated might not be incorporated.

| Return ||
|------------------------------------------------------------------------------|---------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum |

### sumThenReset

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sumThenReset(): Long
```

Equivalent in effect to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())followed by [reset](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#reset()). This method may apply for example during quiescent points between multithreaded computations. If there are updates concurrent with this method, the returned value is*not*guaranteed to be the final value occurring before the reset.

| Return ||
|------------------------------------------------------------------------------|---------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum |

### toDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())as a`double`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())as a`float`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum())as an`int`after a narrowing primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Equivalent to [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum()).

| Return ||
|------------------------------------------------------------------------------|---------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum()).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the [sum](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/LongAdder#sum()) |
