# AtomicReference

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicReference

```
open class AtomicReference<V : Any!> : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicReference](AtomicReference.md) |

An object reference that may be updated atomically. See the [VarHandle](../java.lang.invoke/VarHandle.md) specification for descriptions of the properties of atomic accesses.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicReference](AtomicReference.md))`()` Creates a new AtomicReference with null initial value. |
| [AtomicReference](AtomicReference.md))`(`initialValue:` `V`)` Creates a new AtomicReference with the given initial value. |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V | [accumulateAndGet](AtomicReference.md))`(`x:` `V`, `accumulatorFunction:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the updated value. |
| V | [compareAndExchange](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)). |
| V | [compareAndExchangeAcquire](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| V | [compareAndExchangeRelease](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)). |
| V | [get](AtomicReference.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| V | [getAcquire](AtomicReference.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)). |
| V | [getAndAccumulate](AtomicReference.md))`(`x:` `V`, `accumulatorFunction:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the previous value. |
| V | [getAndSet](AtomicReference.md))`(`newValue:` `V`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| V | [getAndUpdate](AtomicReference.md))`(`updateFunction:` ` [UnaryOperator](../java.util.function/UnaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the previous value. |
| V | [getOpaque](AtomicReference.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)). |
| V | [getPlain](AtomicReference.md))`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](AtomicReference.md))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicReference.md))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](AtomicReference.md))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](AtomicReference.md))`(`newValue:` `V`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](AtomicReference.md))`(`newValue:` `V`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AtomicReference.md))`()` Returns the String representation of the current value. |
| --- | --- |
| V | [updateAndGet](AtomicReference.md))`(`updateFunction:` ` [UnaryOperator](../java.util.function/UnaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the updated value. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](AtomicReference.md))`(`expectedValue:` `V`, `newValue:` `V`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)). |
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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | V:the update value |
| `accumulatorFunction` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<V\>!:a side-effect-free function of two arguments |

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)).

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

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)).

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

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)).

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

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|---|-------------------|
| V | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): V
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | V:the update value |
| `accumulatorFunction` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<V\>!:a side-effect-free function of two arguments |

| Return ||
|---|--------------------|
| V | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: V): V
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<V\>!:a side-effect-free function |

| Return ||
|---|--------------------|
| V | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): V
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)).

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

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: V): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|-----------------|
| `newValue` | V:the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: V): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)).

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

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

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

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the current value with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `updateFunction` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<V\>!:a side-effect-free function |

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

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](AtomicReference.md))and [compareAndSet](AtomicReference.md))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](AtomicReference.md))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](AtomicReference.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: V, 
    newValue: V
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)).

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

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|----------------------|
| `expectedValue` | V:the expected value |
| `newValue` | V:the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
