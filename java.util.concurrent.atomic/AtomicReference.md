# AtomicReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicReference

```
open class AtomicReference<V : Any!> : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicReference](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#) |

An object reference that may be updated atomically. See the [VarHandle](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#) specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicReference](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#AtomicReference())`()` Creates a new AtomicReference with null initial value. |
| [AtomicReference](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#AtomicReference(java.util.concurrent.atomic.AtomicReference.V))`(`initialValue:` `V`)` Creates a new AtomicReference with the given initial value. |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V | [accumulateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#accumulateAndGet(java.util.concurrent.atomic.AtomicReference.V,%20java.util.function.BinaryOperator))`(`x:` `V`, `accumulatorFunction:` ` [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the updated value. |
| V | [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#compareAndExchange(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)). |
| V | [compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#compareAndExchangeAcquire(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)). |
| --- | --- |
| V | [compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#compareAndExchangeRelease(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#compareAndSet(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)). |
| V | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#get())`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)). |
| --- | --- |
| V | [getAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#getAcquire())`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)). |
| V | [getAndAccumulate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#getAndAccumulate(java.util.concurrent.atomic.AtomicReference.V,%20java.util.function.BinaryOperator))`(`x:` `V`, `accumulatorFunction:` ` [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the previous value. |
| V | [getAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#getAndSet(java.util.concurrent.atomic.AtomicReference.V))`(`newValue:` `V`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)). |
| --- | --- |
| V | [getAndUpdate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#getAndUpdate(java.util.function.UnaryOperator))`(`updateFunction:` ` [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator.html#)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the previous value. |
| V | [getOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#getOpaque())`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)). |
| V | [getPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#getPlain())`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#lazySet(java.util.concurrent.atomic.AtomicReference.V))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#set(java.util.concurrent.atomic.AtomicReference.V))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#setOpaque(java.util.concurrent.atomic.AtomicReference.V))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#setPlain(java.util.concurrent.atomic.AtomicReference.V))`(`newValue:` `V`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#setRelease(java.util.concurrent.atomic.AtomicReference.V))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#toString())`()` Returns the String representation of the current value. |
| --- | --- |
| V | [updateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#updateAndGet(java.util.function.UnaryOperator))`(`updateFunction:` ` [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator.html#)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSet(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSetAcquire(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSetPlain(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSetRelease(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSetVolatile(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)). |
| --- | --- |

## Public constructors

### AtomicReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicReference()
```

Creates a new AtomicReference with null initial value. 

### AtomicReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicReference(initialValue: V)
```

Creates a new AtomicReference with the given initial value.

| Parameters ||
|----------------|---------------------|
| `initialValue` | V:the initial value |

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    x: V, 
    accumulatorFunction: BinaryOperator<V>!
): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | V:the update value |
| `accumulatorFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<V\>!:a side-effect-free function of two arguments |

| Return ||
|---|-------------------|
| V | the updated value |

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(
    expectedValue: V, 
    newValue: V
): V
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchange(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|---|--------------------------------------------------------------------------------|
| V | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(
    expectedValue: V, 
    newValue: V
): V
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeAcquire(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|---|--------------------------------------------------------------------------------|
| V | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(
    expectedValue: V, 
    newValue: V
): V
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndExchangeRelease(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|---|--------------------------------------------------------------------------------|
| V | the*witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(
    expectedValue: V, 
    newValue: V
): Boolean
```

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful. False return indicates that the actual value was not equal to the expected value. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): V
```

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getVolatile(kotlin.Any)).

| Return ||
|---|-------------------|
| V | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): V
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAcquire(kotlin.Any)).

| Return ||
|---|-----------|
| V | the value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    x: V, 
    accumulatorFunction: BinaryOperator<V>!
): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | V:the update value |
| `accumulatorFunction` | [BinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/BinaryOperator.html#)\<V\>!:a side-effect-free function of two arguments |

| Return ||
|---|--------------------|
| V | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: V): V
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getAndSet(kotlin.Any)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

| Return ||
|---|--------------------|
| V | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(updateFunction: UnaryOperator<V>!): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator.html#)\<V\>!:a side-effect-free function |

| Return ||
|---|--------------------|
| V | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): V
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#getOpaque(kotlin.Any)).

| Return ||
|---|-----------|
| V | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlain(): V
```

Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`.

| Return ||
|---|-----------|
| V | the value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(newValue: V): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: V): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setVolatile(kotlin.Any)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: V): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setOpaque(kotlin.Any)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPlain(newValue: V): Unit
```

Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`.

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(newValue: V): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#setRelease(kotlin.Any)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

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
fun updateAndGet(updateFunction: UnaryOperator<V>!): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the current value with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator.html#)\<V\>!:a side-effect-free function |

| Return ||
|---|-------------------|
| V | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSet(
    expectedValue: V, 
    newValue: V
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#compareAndExchange(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))and [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#compareAndSet(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSetPlain(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicReference#weakCompareAndSetPlain(java.util.concurrent.atomic.AtomicReference.V,%20java.util.concurrent.atomic.AtomicReference.V)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: V, 
    newValue: V
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetAcquire(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetPlain(
    expectedValue: V, 
    newValue: V
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetPlain(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(
    expectedValue: V, 
    newValue: V
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSetRelease(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetVolatile(
    expectedValue: V, 
    newValue: V
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#weakCompareAndSet(kotlin.Any)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
