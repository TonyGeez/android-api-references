# AtomicInteger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicInteger

```
open class AtomicInteger : Number, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [kotlin.Number](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-number/index.html) ||
| | ↳ | [java.util.concurrent.atomic.AtomicInteger](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#) |

An`int`value that may be updated atomically. See the [VarHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#) specification for descriptions of the properties of atomic accesses. An`AtomicInteger`is used in applications such as atomically incremented counters, and cannot be used as a replacement for an [java.lang.Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). However, this class does extend`Number`to allow uniform access by tools and utilities that deal with numerically-based classes.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicInteger](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#AtomicInteger())`()` Creates a new AtomicInteger with initial value`0`. |
| [AtomicInteger](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#AtomicInteger(kotlin.Int))`(`initialValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new AtomicInteger with the given initial value. |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [accumulateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#accumulateAndGet(kotlin.Int,%20java.util.function.IntBinaryOperator))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the updated value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#addAndGet(kotlin.Int))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#compareAndExchange(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#compareAndExchangeAcquire(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#compareAndExchangeRelease(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#compareAndSet(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#decrementAndGet())`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#get())`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAcquire())`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAccumulate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAndAccumulate(kotlin.Int,%20java.util.function.IntBinaryOperator))`(`x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the previous value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAdd](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAndAdd(kotlin.Int))`(`delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndDecrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAndDecrement())`()` Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndIncrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAndIncrement())`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAndSet(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndUpdate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getAndUpdate(java.util.function.IntUnaryOperator))`(`updateFunction:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getOpaque())`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#getPlain())`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [incrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#incrementAndGet())`()` Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#lazySet(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#set(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#setOpaque(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#setPlain(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#setRelease(kotlin.Int))`(`newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| open [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | [toDouble](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#toDouble())`()` Returns the current value of this`AtomicInteger`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [toFloat](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#toFloat())`()` Returns the current value of this`AtomicInteger`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [toInt](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#toInt())`()` Returns the current value of this`AtomicInteger`as an`int`, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [toLong](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#toLong())`()` Returns the current value of this`AtomicInteger`as a`long`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#toString())`()` Returns the String representation of the current value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#updateAndGet(java.util.function.IntUnaryOperator))`(`updateFunction:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSet(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSetAcquire(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSetRelease(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSetVolatile(kotlin.Int,%20kotlin.Int))`(`expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)). |

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:a side-effect-free function of two arguments |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAndGet(delta: Int): Int
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)).

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

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)).

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

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`addAndGet(-1)`.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): Int
```

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): Int
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:a side-effect-free function of two arguments |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAdd(delta: Int): Int
```

Atomically adds the given value to the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically decrements the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`getAndAdd(-1)`.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndIncrement(): Int
```

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`getAndAdd(1)`.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: Int): Int
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): Int
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)).

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

Atomically increments the current value, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

Equivalent to`addAndGet(1)`.

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: Int): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)).

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

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### toDouble

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toDouble(): Double
```

Returns the current value of this`AtomicInteger`as a`double`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Double](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-double/index.html) | the numeric value represented by this object after conversion to type`double`. |

### toFloat

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toFloat(): Float
```

Returns the current value of this`AtomicInteger`as a`float`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | the numeric value represented by this object after conversion to type`float`. |

### toInt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toInt(): Int
```

Returns the current value of this`AtomicInteger`as an`int`, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). Equivalent to [get()](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#get()).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the numeric value represented by this object after conversion to type`int`. |

### toLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toLong(): Long
```

Returns the current value of this`AtomicInteger`as a`long`after a widening primitive conversion, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a side-effect-free function |

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

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#compareAndExchange(kotlin.Int,%20kotlin.Int))and [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#compareAndSet(kotlin.Int,%20kotlin.Int))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Int))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicInteger#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Int)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
