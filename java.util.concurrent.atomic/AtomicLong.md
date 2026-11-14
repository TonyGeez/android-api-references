# AtomicLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicLong

```
open class AtomicLong : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.AtomicLong](AtomicLong.md) |

A`long`value that may be updated atomically. See the [VarHandle](../java.lang.invoke/VarHandle.md) specification for descriptions of the properties of atomic accesses. An`AtomicLong`is used in applications such as atomically incremented sequence numbers, and cannot be used as a replacement for a [java.lang.Long](../java.lang/Long.md). However, this class does extend`Number`to allow uniform access by tools and utilities that deal with numerically-based classes.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicLong](AtomicLong.md))`()` Creates a new AtomicLong with initial value`0`. |
| [AtomicLong](AtomicLong.md))`(`initialValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new AtomicLong with the given initial value. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [accumulateAndGet](AtomicLong.md))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `accumulatorFunction:` ` [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the updated value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addAndGet](AtomicLong.md))`(`delta:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compareAndExchange](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compareAndExchangeAcquire](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compareAndExchangeRelease](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [decrementAndGet](AtomicLong.md))`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](AtomicLong.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAcquire](AtomicLong.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndAccumulate](AtomicLong.md))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `accumulatorFunction:` ` [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the previous value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndAdd](AtomicLong.md))`(`delta:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndDecrement](AtomicLong.md))`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndIncrement](AtomicLong.md))`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndSet](AtomicLong.md))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndUpdate](AtomicLong.md))`(`updateFunction:` ` [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getOpaque](AtomicLong.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPlain](AtomicLong.md))`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [incrementAndGet](AtomicLong.md))`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](AtomicLong.md))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicLong.md))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](AtomicLong.md))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](AtomicLong.md))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](AtomicLong.md))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](AtomicLong.md))`()` Returns the current value of this`AtomicLong`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](AtomicLong.md))`()` Returns the current value of this`AtomicLong`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](AtomicLong.md))`()` Returns the current value of this`AtomicLong`as an`int`after a narrowing primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](AtomicLong.md))`()` Returns the current value of this`AtomicLong`as a`long`, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AtomicLong.md))`()` Returns the String representation of the current value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [updateAndGet](AtomicLong.md))`(`updateFunction:` ` [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](AtomicLong.md))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)). |

## Public constructors

### AtomicLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicLong()
```

Creates a new AtomicLong with initial value`0`. 

### AtomicLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicLong(initialValue: Long)
```

Creates a new AtomicLong with the given initial value.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------|
| `initialValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the initial value |

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    x: Long, 
    accumulatorFunction: LongBinaryOperator!
): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the update value |
| `accumulatorFunction` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!:a side-effect-free function of two arguments |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAndGet(delta: Long): Long
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `delta` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to add |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(
    expectedValue: Long, 
    newValue: Long
): Long
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(
    expectedValue: Long, 
    newValue: Long
): Long
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(
    expectedValue: Long, 
    newValue: Long
): Long
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful. False return indicates that the actual value was not equal to the expected value. |

### decrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decrementAndGet(): Long
```

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`addAndGet(-1)`.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): Long
```

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): Long
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)).

| Return ||
|------------------------------------------------------------------------------|-----------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    x: Long, 
    accumulatorFunction: LongBinaryOperator!
): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the update value |
| `accumulatorFunction` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!:a side-effect-free function of two arguments |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAdd(delta: Long): Long
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `delta` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to add |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndDecrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndDecrement(): Long
```

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`getAndAdd(-1)`.

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndIncrement(): Long
```

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`getAndAdd(1)`.

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: Long): Long
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(updateFunction: LongUnaryOperator!): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!:a side-effect-free function |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): Long
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)).

| Return ||
|------------------------------------------------------------------------------|-----------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlain(): Long
```

Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`.

| Return ||
|------------------------------------------------------------------------------|-----------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the value |

### incrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun incrementAndGet(): Long
```

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`addAndGet(1)`.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPlain(newValue: Long): Unit
```

Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Returns the current value of this`AtomicLong`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the current value of this`AtomicLong`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the current value of this`AtomicLong`as an`int`after a narrowing primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Returns the current value of this`AtomicLong`as a`long`, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). Equivalent to [get()](AtomicLong.md)).

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the numeric value represented by this object after conversion to type`long`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the current value.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the current value |

### updateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateAndGet(updateFunction: LongUnaryOperator!): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!:a side-effect-free function |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSet(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](AtomicLong.md))and [compareAndSet](AtomicLong.md))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](AtomicLong.md))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](AtomicLong.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetPlain(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetVolatile(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
