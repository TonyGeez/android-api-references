# AtomicLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicLong

```
open class AtomicLong : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.AtomicLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#) |

A`long`value that may be updated atomically. See the [VarHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#) specification for descriptions of the properties of atomic accesses. An`AtomicLong`is used in applications such as atomically incremented sequence numbers, and cannot be used as a replacement for a [java.lang.Long](https://developer.android.com/reference/kotlin/java/lang/Long.html#). However, this class does extend`Number`to allow uniform access by tools and utilities that deal with numerically-based classes.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#AtomicLong())`()` Creates a new AtomicLong with initial value`0`. |
| [AtomicLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#AtomicLong(kotlin.Long))`(`initialValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Creates a new AtomicLong with the given initial value. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [accumulateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#accumulateAndGet(kotlin.Long,%20java.util.function.LongBinaryOperator))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `accumulatorFunction:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the updated value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#addAndGet(kotlin.Long))`(`delta:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#compareAndExchange(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#compareAndExchangeAcquire(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#compareAndExchangeRelease(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#compareAndSet(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [decrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#decrementAndGet())`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#get())`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAcquire())`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndAccumulate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAndAccumulate(kotlin.Long,%20java.util.function.LongBinaryOperator))`(`x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `accumulatorFunction:` ` [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the previous value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndAdd](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAndAdd(kotlin.Long))`(`delta:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndDecrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAndDecrement())`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndIncrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAndIncrement())`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAndSet(kotlin.Long))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndUpdate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getAndUpdate(java.util.function.LongUnaryOperator))`(`updateFunction:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getOpaque())`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)). |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#getPlain())`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [incrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#incrementAndGet())`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#lazySet(kotlin.Long))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#set(kotlin.Long))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#setOpaque(kotlin.Long))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#setPlain(kotlin.Long))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#setRelease(kotlin.Long))`(`newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#toDouble())`()` Returns the current value of this`AtomicLong`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#toFloat())`()` Returns the current value of this`AtomicLong`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#toInt())`()` Returns the current value of this`AtomicLong`as an`int`after a narrowing primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#toLong())`()` Returns the current value of this`AtomicLong`as a`long`, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#toString())`()` Returns the String representation of the current value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [updateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#updateAndGet(java.util.function.LongUnaryOperator))`(`updateFunction:` ` [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSet(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSetAcquire(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSetPlain(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSetRelease(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSetVolatile(kotlin.Long,%20kotlin.Long))`(`expectedValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)). |

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the update value |
| `accumulatorFunction` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!:a side-effect-free function of two arguments |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAndGet(delta: Long): Long
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)).

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

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`addAndGet(-1)`.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): Long
```

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): Long
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the update value |
| `accumulatorFunction` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!:a side-effect-free function of two arguments |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAdd(delta: Long): Long
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`getAndAdd(-1)`.

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndIncrement(): Long
```

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`getAndAdd(1)`.

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: Long): Long
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!:a side-effect-free function |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): Long
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)).

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

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`addAndGet(1)`.

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: Long): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)).

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

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Returns the current value of this`AtomicLong`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the current value of this`AtomicLong`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the current value of this`AtomicLong`as an`int`after a narrowing primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Returns the current value of this`AtomicLong`as a`long`, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). Equivalent to [get()](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#get()).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!:a side-effect-free function |

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

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#compareAndExchange(kotlin.Long,%20kotlin.Long))and [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#compareAndSet(kotlin.Long,%20kotlin.Long))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSetPlain(kotlin.Long,%20kotlin.Long))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLong#weakCompareAndSetPlain(kotlin.Long,%20kotlin.Long)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------|
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
