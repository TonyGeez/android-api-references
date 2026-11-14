Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicLongArray

```
open class AtomicLongArray : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicLongArray](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#) |

A `long` array in which elements may be updated atomically. See the `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#` specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#AtomicLongArray(kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new AtomicLongArray of the given length, with all elements initially zero. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#AtomicLongArray(kotlin.LongArray)(array: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html!)` Creates a new AtomicLongArray with the same length as, and all elements copied from, the given array. |

| Public methods ||
|---|---|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#accumulateAndGet(kotlin.Int,%20kotlin.Long,%20java.util.function.LongBinaryOperator)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, accumulatorFunction: https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#!)` Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function to the current and given values, returning the updated value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#addAndGet(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, delta: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically adds the given value to the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#compareAndExchange(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)`. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#compareAndExchangeAcquire(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#compareAndExchangeRelease(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#compareAndSet(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#decrementAndGet(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically decrements the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#get(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the current value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAcquire(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the current value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)`. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAndAccumulate(kotlin.Int,%20kotlin.Long,%20java.util.function.LongBinaryOperator)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, x: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, accumulatorFunction: https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#!)` Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function to the current and given values, returning the previous value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAndAdd(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, delta: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically adds the given value to the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAndDecrement(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically decrements the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAndIncrement(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically increments the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAndSet(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Atomically sets the element at index `i` to `newValue` and returns the old value, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getAndUpdate(kotlin.Int,%20java.util.function.LongUnaryOperator)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, updateFunction: https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#!)` Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function, returning the previous value. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getOpaque(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the current value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#getPlain(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the current value of the element at index `i`, with memory semantics of reading as if the variable was declared non-`volatile`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#incrementAndGet(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Atomically increments the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#lazySet(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#length()()` Returns the length of the array. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#set(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#setOpaque(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#setPlain(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the element at index `i` to `newValue`, with memory semantics of setting as if the variable was declared non-`volatile` and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#setRelease(kotlin.Int,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)`. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#toString()()` {@return the String representation of the current values of array} |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#updateAndGet(kotlin.Int,%20java.util.function.LongUnaryOperator)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, updateFunction: https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#!)` Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSet(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSetAcquire(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSetRelease(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)`. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSetVolatile(kotlin.Int,%20kotlin.Long,%20kotlin.Long)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, expectedValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, newValue: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)`. |

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

Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index `i` as its first argument, and the given update as the second argument.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the update value |
| `accumulatorFunction` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!: a side-effect-free function of two arguments |
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

Atomically adds the given value to the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`.

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

Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)`.

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

Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)`.

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

Atomically sets the element at index `i` to `newValue` if the element's current value, referred to as the *witness value* , `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)`.

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

Atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`.

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

Atomically decrements the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`.

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

Returns the current value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)`.

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

Returns the current value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)`.

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

Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value of the element at index `i` as its first argument, and the given update as the second argument.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the update value |
| `accumulatorFunction` | [LongBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongBinaryOperator.html#)!: a side-effect-free function of two arguments |
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

Atomically adds the given value to the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`.

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

Atomically decrements the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`.

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

Atomically increments the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`.

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

Atomically sets the element at index `i` to `newValue` and returns the old value, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)`.

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

Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `updateFunction` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!: a side-effect-free function |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOpaque(i: Int): Long
```

Returns the current value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)`.

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

Atomically increments the value of the element at index `i`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndAdd(kotlin.Any)`.

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

Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)`.

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

Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)`.

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

Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)`.

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

Sets the element at index `i` to `newValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)`.

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

Atomically updates (with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)`) the element at index `i` with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `updateFunction` | [LongUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/LongUnaryOperator.html#)!: a side-effect-free function |

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

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#compareAndExchange(kotlin.Int,%20kotlin.Long,%20kotlin.Long)` and `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#compareAndSet(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`). To avoid confusion over plain or volatile memory effects it is recommended that the method `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Long,%20kotlin.Long)` be used instead.*

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)`.

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

- `https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicLongArray#weakCompareAndSetPlain(kotlin.Int,%20kotlin.Long,%20kotlin.Long)`

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun weakCompareAndSetAcquire(
    i: Int, 
    expectedValue: Long, 
    newValue: Long
): Boolean
```

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)`.

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

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)`.

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

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)`.

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

Possibly atomically sets the element at index `i` to `newValue` if the element's current value `== expectedValue`, with memory effects as specified by `https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)`.

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index |
| `expectedValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the expected value |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new value |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful |
