# AtomicIntegerArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicIntegerArray

```
open class AtomicIntegerArray : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicIntegerArray](../java/util/concurrent/atomic/AtomicIntegerArray.md) |

An`int`array in which elements may be updated atomically. See the [VarHandle](../java/lang/invoke/VarHandle.md) specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicIntegerArray](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new AtomicIntegerArray of the given length, with all elements initially zero. |
| [AtomicIntegerArray](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`array:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Creates a new AtomicIntegerArray with the same length as, and all elements copied from, the given array. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [accumulateAndGet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](../java/util/function/IntBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the updated value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addAndGet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchange](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeAcquire](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeRelease](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java/lang/invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decrementAndGet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getVolatile](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAcquire](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getAcquire](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAccumulate](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](../java/util/function/IntBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the previous value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAdd](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndDecrement](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndIncrement](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndUpdate](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateFunction:` ` [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpaque](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getOpaque](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPlain](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [incrementAndGet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../java/util/concurrent/atomic/AtomicIntegerArray.md))`()` Returns the length of the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java/lang/invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/concurrent/atomic/AtomicIntegerArray.md))`()` Returns the String representation of the current values of array. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateAndGet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateFunction:` ` [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java/lang/invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](../java/util/concurrent/atomic/AtomicIntegerArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java/lang/invoke/VarHandle.md)). |

## Public constructors

### AtomicIntegerArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicIntegerArray(length: Int)
```

Creates a new AtomicIntegerArray of the given length, with all elements initially zero.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the array |

### AtomicIntegerArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicIntegerArray(array: IntArray!)
```

Creates a new AtomicIntegerArray with the same length as, and all elements copied from, the given array.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------|
| `array` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the array to copy elements from |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if array is null |

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    i: Int, 
    x: Int, 
    accumulatorFunction: IntBinaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index`i`as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](../java/util/function/IntBinaryOperator.md)!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addAndGet(
    i: Int, 
    delta: Int
): Int
```

Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Int
```

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Int
```

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Int
```

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful. False return indicates that the actual value was not equal to the expected value. |

### decrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun decrementAndGet(i: Int): Int
```

Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)).

Equivalent to`addAndGet(i, -1)`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(i: Int): Int
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getVolatile](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(i: Int): Int
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getAcquire](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    i: Int, 
    x: Int, 
    accumulatorFunction: IntBinaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index`i`as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](../java/util/function/IntBinaryOperator.md)!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAdd(
    i: Int, 
    delta: Int
): Int
```

Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndDecrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndDecrement(i: Int): Int
```

Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)).

Equivalent to`getAndAdd(i, -1)`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndIncrement(i: Int): Int
```

Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)).

Equivalent to`getAndAdd(i, 1)`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(
    i: Int, 
    newValue: Int
): Int
```

Atomically sets the element at index`i`to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(
    i: Int, 
    updateFunction: IntUnaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `updateFunction` | [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(i: Int): Int
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getOpaque](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlain(i: Int): Int
```

Returns the current value of the element at index`i`, with memory semantics of reading as if the variable was declared non-`volatile`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the value |

### incrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun incrementAndGet(i: Int): Int
```

Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](../java/lang/invoke/VarHandle.md)).

Equivalent to`addAndGet(i, 1)`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(
    i: Int, 
    newValue: Int
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun length(): Int
```

Returns the length of the array.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the length of the array |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(
    i: Int, 
    newValue: Int
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(
    i: Int, 
    newValue: Int
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPlain(
    i: Int, 
    newValue: Int
): Unit
```

Sets the element at index`i`to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(
    i: Int, 
    newValue: Int
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the current values of array.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the current values of array |

### updateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateAndGet(
    i: Int, 
    updateFunction: IntUnaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `updateFunction` | [IntUnaryOperator](../java/util/function/IntUnaryOperator.md)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSet(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](../java/util/concurrent/atomic/AtomicIntegerArray.md))and [compareAndSet](../java/util/concurrent/atomic/AtomicIntegerArray.md))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](../java/util/concurrent/atomic/AtomicIntegerArray.md))be used instead.*

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](../java/util/concurrent/atomic/AtomicIntegerArray.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetPlain(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetVolatile(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
