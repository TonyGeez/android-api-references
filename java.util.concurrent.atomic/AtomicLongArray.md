Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicLongArray

```
open class AtomicLongArray : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicLongArray](AtomicLongArray.md) |

A `long` array in which elements may be updated atomically. See the `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#` specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|---|---|
| AtomicLongArray Creates a new AtomicLongArray of the given length, with all elements initially zero. |
| AtomicLongArray Creates a new AtomicLongArray with the same length as, and all elements copied from, the given array. |

| Public methods ||
|---|---|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | accumulateAndGet Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function to the current and given values, returning the updated value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | addAndGet Atomically adds the given value to the element at index `i`, with memory effects as specified by getAndAdd. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | compareAndExchange Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by compareAndExchange. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | compareAndExchangeAcquire Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by compareAndExchangeAcquire. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | compareAndExchangeRelease Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by compareAndExchangeRelease. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | compareAndSet Atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by compareAndSet. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | decrementAndGet Atomically decrements the value of the element at index `i`, with memory effects as specified by getAndAdd. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | get Returns the current value of the element at index `i`, with memory effects as specified by getVolatile. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAcquire Returns the current value of the element at index `i`, with memory effects as specified by getAcquire. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAndAccumulate Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function to the current and given values, returning the previous value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAndAdd Atomically adds the given value to the element at index `i`, with memory effects as specified by getAndAdd. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAndDecrement Atomically decrements the value of the element at index `i`, with memory effects as specified by getAndAdd. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAndIncrement Atomically increments the value of the element at index `i`, with memory effects as specified by getAndAdd. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAndSet Atomically sets the element at index `i` to `newValue` and returns the old value, with memory effects as specified by getAndSet. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getAndUpdate Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getOpaque Returns the current value of the element at index `i`, with memory effects as specified by getOpaque. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | getPlain Returns the current value of the element at index `i`, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | incrementAndGet Atomically increments the value of the element at index `i`, with memory effects as specified by getAndAdd. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | lazySet Sets the element at index `i` to `newValue`, with memory effects as specified by setRelease. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | length Returns the length of the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | set Sets the element at index `i` to `newValue`, with memory effects as specified by setVolatile. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOpaque Sets the element at index `i` to `newValue`, with memory effects as specified by setOpaque. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlain Sets the element at index `i` to `newValue`, with memory semantics of setting as if the variable was declared non-`volatile` and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRelease Sets the element at index `i` to `newValue`, with memory effects as specified by setRelease. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString {@return the String representation of the current values of array} |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | updateAndGet Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | weakCompareAndSet Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetPlain. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | weakCompareAndSetAcquire Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetAcquire. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | weakCompareAndSetPlain Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetPlain. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | weakCompareAndSetRelease Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetRelease. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | weakCompareAndSetVolatile Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSet. |

## Public constructors

### AtomicLongArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AtomicLongArray(length: Int)
```

Creates a new AtomicLongArray of the given length, with all elements initially zero.

| Parameters ||
|---|---|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the length of the array |

### AtomicLongArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
AtomicLongArray(array: LongArray!)
```

Creates a new AtomicLongArray with the same length as, and all elements copied from, the given array.

| Parameters ||
|---|---|
| `array` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!: the array to copy elements from |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if array is null |

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun accumulateAndGet(
    i: Int, 
    x: Long, 
    accumulatorFunction: LongBinaryOperator!
): Long
```

Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index `i` as its first argument, and the given update as the second argument.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the update value |
| `accumulatorFunction` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!: a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAndGet(
    i: Int, 
    delta: Long
): Long
```

Atomically adds the given value to the element at index `i`, with memory effects as specified by getAndAdd.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `delta` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the updated value |

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareAndExchange(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Long
```

Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by compareAndExchange.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the *witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareAndExchangeAcquire(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Long
```

Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by compareAndExchangeAcquire.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the *witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareAndExchangeRelease(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Long
```

Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by compareAndExchangeRelease.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the *witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareAndSet(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by compareAndSet.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful. False return indicates that the actual value was not equal to the expected value. |

### decrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun decrementAndGet(i: Int): Long
```

Atomically decrements the value of the element at index `i`, with memory effects as specified by getAndAdd.

Equivalent to `addAndGet(i, -1)`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun get(i: Int): Long
```

Returns the current value of the element at index `i`, with memory effects as specified by getVolatile.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAcquire(i: Int): Long
```

Returns the current value of the element at index `i`, with memory effects as specified by getAcquire.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAndAccumulate(
    i: Int, 
    x: Long, 
    accumulatorFunction: LongBinaryOperator!
): Long
```

Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index `i` as its first argument, and the given update as the second argument.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the update value |
| `accumulatorFunction` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!: a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAndAdd(
    i: Int, 
    delta: Long
): Long
```

Atomically adds the given value to the element at index `i`, with memory effects as specified by getAndAdd.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `delta` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the value to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getAndDecrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAndDecrement(i: Int): Long
```

Atomically decrements the value of the element at index `i`, with memory effects as specified by getAndAdd.

Equivalent to `getAndAdd(i, -1)`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAndIncrement(i: Int): Long
```

Atomically increments the value of the element at index `i`, with memory effects as specified by getAndAdd.

Equivalent to `getAndAdd(i, 1)`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAndSet(
    i: Int, 
    newValue: Long
): Long
```

Atomically sets the element at index `i` to `newValue` and returns the old value, with memory effects as specified by getAndSet.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAndUpdate(
    i: Int, 
    updateFunction: LongUnaryOperator!
): Long
```

Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `updateFunction` | [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!: a side-effect-free function |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOpaque(i: Int): Long
```

Returns the current value of the element at index `i`, with memory effects as specified by getOpaque.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getPlain(i: Int): Long
```

Returns the current value of the element at index `i`, with memory semantics of reading as if the variable was declared non-`volatile`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value |

### incrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun incrementAndGet(i: Int): Long
```

Atomically increments the value of the element at index `i`, with memory effects as specified by getAndAdd.

Equivalent to `addAndGet(i, 1)`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun lazySet(
    i: Int, 
    newValue: Long
): Unit
```

Sets the element at index `i` to `newValue`, with memory effects as specified by setRelease.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

### length

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun length(): Int
```

Returns the length of the array.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the length of the array |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun set(
    i: Int, 
    newValue: Long
): Unit
```

Sets the element at index `i` to `newValue`, with memory effects as specified by setVolatile.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setOpaque(
    i: Int, 
    newValue: Long
): Unit
```

Sets the element at index `i` to `newValue`, with memory effects as specified by setOpaque.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPlain(
    i: Int, 
    newValue: Long
): Unit
```

Sets the element at index `i` to `newValue`, with memory semantics of setting as if the variable was declared non-`volatile` and non-`final`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRelease(
    i: Int, 
    newValue: Long
): Unit
```

Sets the element at index `i` to `newValue`, with memory effects as specified by setRelease.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

{@return the String representation of the current values of array}

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### updateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun updateAndGet(
    i: Int, 
    updateFunction: LongUnaryOperator!
): Long
```

Atomically updates (with memory effects as specified by compareAndSet) the element at index `i` with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `updateFunction` | [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!: a side-effect-free function |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun weakCompareAndSet(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as compareAndExchange and compareAndSet). To avoid confusion over plain or volatile memory effects it is recommended that the method weakCompareAndSetPlain be used instead.*

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetPlain.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful |

**See Also**

- weakCompareAndSetPlain

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun weakCompareAndSetAcquire(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetAcquire.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun weakCompareAndSetPlain(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetPlain.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun weakCompareAndSetRelease(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSetRelease.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun weakCompareAndSetVolatile(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by weakCompareAndSet.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful |
