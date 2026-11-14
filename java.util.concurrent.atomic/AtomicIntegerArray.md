# AtomicIntegerArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicIntegerArray

```
open class AtomicIntegerArray : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicIntegerArray](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#) |

An`int`array in which elements may be updated atomically. See the [VarHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#) specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicIntegerArray](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#AtomicIntegerArray(kotlin.Int))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new AtomicIntegerArray of the given length, with all elements initially zero. |
| [AtomicIntegerArray](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#AtomicIntegerArray(kotlin.IntArray))`(`array:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Creates a new AtomicIntegerArray with the same length as, and all elements copied from, the given array. |

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [accumulateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#accumulateAndGet(kotlin.Int,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function to the current and given values, returning the updated value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#addAndGet(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#compareAndExchange(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#compareAndExchangeAcquire(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#compareAndExchangeRelease(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#compareAndSet(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#decrementAndGet(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#get(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAcquire(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAccumulate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAndAccumulate(kotlin.Int,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function to the current and given values, returning the previous value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAdd](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAndAdd(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndDecrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAndDecrement(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndIncrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAndIncrement(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAndSet(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the element at index`i`to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndUpdate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getAndUpdate(kotlin.Int,%20java.util.function.IntUnaryOperator))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateFunction:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getOpaque(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#getPlain(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [incrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#incrementAndGet(kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#lazySet(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#length())`()` Returns the length of the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#set(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#setOpaque(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#setPlain(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#setRelease(kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#toString())`()` Returns the String representation of the current values of array. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#updateAndGet(kotlin.Int,%20java.util.function.IntUnaryOperator))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateFunction:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSet(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSetAcquire(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSetRelease(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSetVolatile(kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)). |

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index`i`as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:a side-effect-free function of two arguments |
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

Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)).

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

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)).

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

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)).

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

Atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)).

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

Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

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

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index`i`as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:a side-effect-free function of two arguments |
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

Atomically adds the given value to the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically decrements the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Atomically sets the element at index`i`to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `updateFunction` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(i: Int): Int
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)).

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

Atomically increments the value of the element at index`i`, with memory effects as specified by [VarHandle.getAndAdd](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)).

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

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

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

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)).

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

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)).

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

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the element at index`i`with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `updateFunction` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a side-effect-free function |

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

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#compareAndExchange(kotlin.Int,%20kotlin.Int,%20kotlin.Int))and [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#compareAndSet(kotlin.Int,%20kotlin.Int,%20kotlin.Int))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Int,%20kotlin.Int))be used instead.*

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

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

- [#weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerArray#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    i: Int, 
    expectedValue: Int, 
    newValue: Int
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)).

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

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

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

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)).

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

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)).

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
