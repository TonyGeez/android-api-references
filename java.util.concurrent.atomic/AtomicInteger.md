# AtomicInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicInteger

```
open class AtomicInteger : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.AtomicInteger](AtomicInteger.md) |

An`int`value that may be updated atomically. See the [VarHandle](../java.lang.invoke/VarHandle.md) specification for descriptions of the properties of atomic accesses. An`AtomicInteger`is used in applications such as atomically incremented counters, and cannot be used as a replacement for an [java.lang.Integer](../java.lang/Integer.md). However, this class does extend`Number`to allow uniform access by tools and utilities that deal with numerically-based classes.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicInteger](AtomicInteger.md))`()` Creates a new AtomicInteger with initial value`0`. |
| [AtomicInteger](AtomicInteger.md))`(`initialValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new AtomicInteger with the given initial value. |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [accumulateAndGet](AtomicInteger.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](../java.util.function/IntBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the updated value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addAndGet](AtomicInteger.md))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchange](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeAcquire](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeRelease](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decrementAndGet](AtomicInteger.md))`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](AtomicInteger.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAcquire](AtomicInteger.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAccumulate](AtomicInteger.md))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](../java.util.function/IntBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the previous value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAdd](AtomicInteger.md))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndDecrement](AtomicInteger.md))`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndIncrement](AtomicInteger.md))`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSet](AtomicInteger.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndUpdate](AtomicInteger.md))`(`updateFunction:` ` [IntUnaryOperator](../java.util.function/IntUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpaque](AtomicInteger.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPlain](AtomicInteger.md))`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [incrementAndGet](AtomicInteger.md))`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](AtomicInteger.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicInteger.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](AtomicInteger.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](AtomicInteger.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](AtomicInteger.md))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](AtomicInteger.md))`()` Returns the current value of this`AtomicInteger`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](AtomicInteger.md))`()` Returns the current value of this`AtomicInteger`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](AtomicInteger.md))`()` Returns the current value of this`AtomicInteger`as an`int`, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](AtomicInteger.md))`()` Returns the current value of this`AtomicInteger`as a`long`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AtomicInteger.md))`()` Returns the String representation of the current value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateAndGet](AtomicInteger.md))`(`updateFunction:` ` [IntUnaryOperator](../java.util.function/IntUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](AtomicInteger.md))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)). |

## Public constructors

### AtomicInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicInteger()
```

Creates a new AtomicInteger with initial value`0`. 

### AtomicInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicInteger(initialValue: Int)
```

Creates a new AtomicInteger with the given initial value.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------|
| `initialValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial value |

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    x: Int, 
    accumulatorFunction: IntBinaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](../java.util.function/IntBinaryOperator.md)!:a side-effect-free function of two arguments |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAndGet(delta: Int): Int
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(
    expectedValue: Int, 
    newValue: Int
): Int
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(
    expectedValue: Int, 
    newValue: Int
): Int
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(
    expectedValue: Int, 
    newValue: Int
): Int
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful. False return indicates that the actual value was not equal to the expected value. |

### decrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decrementAndGet(): Int
```

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`addAndGet(-1)`.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): Int
```

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): Int
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)).

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    x: Int, 
    accumulatorFunction: IntBinaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](../java.util.function/IntBinaryOperator.md)!:a side-effect-free function of two arguments |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAdd(delta: Int): Int
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndDecrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndDecrement(): Int
```

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`getAndAdd(-1)`.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndIncrement(): Int
```

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`getAndAdd(1)`.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: Int): Int
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(updateFunction: IntUnaryOperator!): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [IntUnaryOperator](../java.util.function/IntUnaryOperator.md)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): Int
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)).

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlain(): Int
```

Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`.

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value |

### incrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun incrementAndGet(): Int
```

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](../java.lang.invoke/VarHandle.md)).

Equivalent to`addAndGet(1)`.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPlain(newValue: Int): Unit
```

Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Returns the current value of this`AtomicInteger`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the current value of this`AtomicInteger`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the current value of this`AtomicInteger`as an`int`, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). Equivalent to [get()](AtomicInteger.md)).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Returns the current value of this`AtomicInteger`as a`long`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

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
fun updateAndGet(updateFunction: IntUnaryOperator!): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [IntUnaryOperator](../java.util.function/IntUnaryOperator.md)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSet(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](AtomicInteger.md))and [compareAndSet](AtomicInteger.md))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](AtomicInteger.md))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](AtomicInteger.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetPlain(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetVolatile(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
