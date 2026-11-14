# LongAdder

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LongAdder

```
open class LongAdder : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.LongAdder](LongAdder.md) |

One or more variables that together maintain an initially zero`long`sum. When updates (method [add](LongAdder.md))) are contended across threads, the set of variables may grow dynamically to reduce contention. Method [sum](LongAdder.md))(or, equivalently, [longValue](LongAdder.md))) returns the current total combined across the variables maintaining the sum.

This class is usually preferable to [AtomicLong](AtomicLong.md) when multiple threads update a common sum that is used for purposes such as collecting statistics, not for fine-grained synchronization control. Under low update contention, the two classes have similar characteristics. But under high contention, expected throughput of this class is significantly higher, at the expense of higher space consumption.

LongAdders can be used with a to maintain a scalable frequency map (a form of histogram or multiset). For example, to add a count to a`ConcurrentHashMap<String,LongAdder> freqs`, initializing if not already present, you can use`freqs.computeIfAbsent(key, k -> new LongAdder()).increment();`

This class extends [Number](../java.lang/Number.md), but does*not* define methods such as`equals`,`hashCode`and`compareTo`because instances are expected to be mutated, and so are not useful as collection keys.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LongAdder](LongAdder.md))`()` Creates a new adder with initial sum of zero. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](LongAdder.md))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Adds the given value. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [decrement](LongAdder.md))`()` Equivalent to`add(-1)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [increment](LongAdder.md))`()` Equivalent to`add(1)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [reset](LongAdder.md))`()` Resets variables maintaining the sum to zero. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sum](LongAdder.md))`()` Returns the current sum. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [sumThenReset](LongAdder.md))`()` Equivalent in effect to [sum](LongAdder.md))followed by [reset](LongAdder.md)). |
| --- | --- |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](LongAdder.md))`()` Returns the [sum](LongAdder.md))as a`double`after a widening primitive conversion. |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](LongAdder.md))`()` Returns the [sum](LongAdder.md))as a`float`after a widening primitive conversion. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](LongAdder.md))`()` Returns the [sum](LongAdder.md))as an`int`after a narrowing primitive conversion. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](LongAdder.md))`()` Equivalent to [sum](LongAdder.md)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LongAdder.md))`()` Returns the String representation of the [sum](LongAdder.md)). |

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

Equivalent in effect to [sum](LongAdder.md))followed by [reset](LongAdder.md)). This method may apply for example during quiescent points between multithreaded computations. If there are updates concurrent with this method, the returned value is*not*guaranteed to be the final value occurring before the reset.

| Return ||
|------------------------------------------------------------------------------|---------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum |

### toDouble

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Returns the [sum](LongAdder.md))as a`double`after a widening primitive conversion.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the [sum](LongAdder.md))as a`float`after a widening primitive conversion.

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the [sum](LongAdder.md))as an`int`after a narrowing primitive conversion.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Equivalent to [sum](LongAdder.md)).

| Return ||
|------------------------------------------------------------------------------|---------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the sum |

### toString

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the [sum](LongAdder.md)).

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the [sum](LongAdder.md)) |
