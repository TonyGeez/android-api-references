# AtomicReferenceArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicReferenceArray

```
open class AtomicReferenceArray<E : Any!> : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicReferenceArray](../java/util/concurrent/atomic/AtomicReferenceArray.md) |

An array of object references in which elements may be updated atomically. See the [VarHandle](../java/lang/invoke/VarHandle.md) specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicReferenceArray](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`array:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<E>!`)` Creates a new AtomicReferenceArray with the same length as, and all elements copied from, the given array. |
| [AtomicReferenceArray](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`length:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new AtomicReferenceArray of the given length, with all elements initially null. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| E | [accumulateAndGet](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` `E`, `accumulatorFunction:` ` [BinaryOperator](../java/util/function/BinaryOperator.md)<E>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the updated value. |
| E | [compareAndExchange](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java/lang/invoke/VarHandle.md)). |
| E | [compareAndExchangeAcquire](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| E | [compareAndExchangeRelease](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java/lang/invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java/lang/invoke/VarHandle.md)). |
| E | [get](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getVolatile](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| E | [getAcquire](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getAcquire](../java/lang/invoke/VarHandle.md)). |
| E | [getAndAccumulate](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `x:` `E`, `accumulatorFunction:` ` [BinaryOperator](../java/util/function/BinaryOperator.md)<E>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the previous value. |
| E | [getAndSet](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` `E`)` Atomically sets the element at index`i`to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| E | [getAndUpdate](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateFunction:` ` [UnaryOperator](../java/util/function/UnaryOperator.md)<E>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the previous value. |
| E | [getOpaque](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getOpaque](../java/lang/invoke/VarHandle.md)). |
| E | [getPlain](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the current value of the element at index`i`, with memory semantics of reading as if the variable was declared non-`volatile`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` `E`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [length](../java/util/concurrent/atomic/AtomicReferenceArray.md))`()` Returns the length of the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` `E`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` `E`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java/lang/invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` `E`)` Sets the element at index`i`to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newValue:` `E`)` Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/concurrent/atomic/AtomicReferenceArray.md))`()` Returns the String representation of the current values of array. |
| E | [updateAndGet](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `updateFunction:` ` [UnaryOperator](../java/util/function/UnaryOperator.md)<E>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java/lang/invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java/lang/invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](../java/util/concurrent/atomic/AtomicReferenceArray.md))`(`i:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `expectedValue:` `E`, `newValue:` `E`)` Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java/lang/invoke/VarHandle.md)). |

## Public constructors

### AtomicReferenceArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicReferenceArray(array: Array<E>!)
```

Creates a new AtomicReferenceArray with the same length as, and all elements copied from, the given array.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------|
| `array` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<E\>!:the array to copy elements from |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if array is null |

### AtomicReferenceArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicReferenceArray(length: Int)
```

Creates a new AtomicReferenceArray of the given length, with all elements initially null.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the length of the array |

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    i: Int, 
    x: E, 
    accumulatorFunction: BinaryOperator<E>!
): E
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index`i`as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `x` | E:the update value |
| `accumulatorFunction` | [BinaryOperator](../java/util/function/BinaryOperator.md)\<E\>!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|---|-------------------|
| E | the updated value |

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(
    i: Int, 
    expectedValue: E, 
    newValue: E
): E
```

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|---|--------------------------------------------------------------------------------|
| E | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(
    i: Int, 
    expectedValue: E, 
    newValue: E
): E
```

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|---|--------------------------------------------------------------------------------|
| E | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(
    i: Int, 
    expectedValue: E, 
    newValue: E
): E
```

Atomically sets the element at index`i`to`newValue`if the element's current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|---|--------------------------------------------------------------------------------|
| E | the*witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(
    i: Int, 
    expectedValue: E, 
    newValue: E
): Boolean
```

Atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful. False return indicates that the actual value was not equal to the expected value. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(i: Int): E
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getVolatile](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|---|-------------------|
| E | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(i: Int): E
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getAcquire](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|---|-----------|
| E | the value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    i: Int, 
    x: E, 
    accumulatorFunction: BinaryOperator<E>!
): E
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index`i`as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `x` | E:the update value |
| `accumulatorFunction` | [BinaryOperator](../java/util/function/BinaryOperator.md)\<E\>!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|---|--------------------|
| E | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(
    i: Int, 
    newValue: E
): E
```

Atomically sets the element at index`i`to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | E:the new value |

| Return ||
|---|--------------------|
| E | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(
    i: Int, 
    updateFunction: UnaryOperator<E>!
): E
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `updateFunction` | [UnaryOperator](../java/util/function/UnaryOperator.md)\<E\>!:a side-effect-free function |

| Return ||
|---|--------------------|
| E | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(i: Int): E
```

Returns the current value of the element at index`i`, with memory effects as specified by [VarHandle.getOpaque](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|---|-----------|
| E | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlain(i: Int): E
```

Returns the current value of the element at index`i`, with memory semantics of reading as if the variable was declared non-`volatile`.

| Parameters ||
|-----|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |

| Return ||
|---|-----------|
| E | the value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(
    i: Int, 
    newValue: E
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | E:the new value |

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
    newValue: E
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | E:the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(
    i: Int, 
    newValue: E
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | E:the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPlain(
    i: Int, 
    newValue: E
): Unit
```

Sets the element at index`i`to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | E:the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(
    i: Int, 
    newValue: E
): Unit
```

Sets the element at index`i`to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `newValue` | E:the new value |

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
    updateFunction: UnaryOperator<E>!
): E
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java/lang/invoke/VarHandle.md))) the element at index`i`with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `updateFunction` | [UnaryOperator](../java/util/function/UnaryOperator.md)\<E\>!:a side-effect-free function |

| Return ||
|---|-------------------|
| E | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSet(
    i: Int, 
    expectedValue: E, 
    newValue: E
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](../java/util/concurrent/atomic/AtomicReferenceArray.md))and [compareAndSet](../java/util/concurrent/atomic/AtomicReferenceArray.md))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](../java/util/concurrent/atomic/AtomicReferenceArray.md))be used instead.*

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](../java/util/concurrent/atomic/AtomicReferenceArray.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    i: Int, 
    expectedValue: E, 
    newValue: E
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetPlain(
    i: Int, 
    expectedValue: E, 
    newValue: E
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(
    i: Int, 
    expectedValue: E, 
    newValue: E
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetVolatile(
    i: Int, 
    expectedValue: E, 
    newValue: E
): Boolean
```

Possibly atomically sets the element at index`i`to`newValue`if the element's current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java/lang/invoke/VarHandle.md)).

| Parameters ||
|-----------------|--------------------------------------------------------------------------------------|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index |
| `expectedValue` | E:the expected value |
| `newValue` | E:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
