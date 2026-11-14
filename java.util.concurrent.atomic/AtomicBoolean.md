# AtomicBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicBoolean

```
open class AtomicBoolean : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicBoolean](AtomicBoolean.md) |

A`boolean`value that may be updated atomically. See the [VarHandle](../java.lang.invoke/VarHandle.md) specification for descriptions of the properties of atomic accesses. An`AtomicBoolean`is used in applications such as atomically updated flags, and cannot be used as a replacement for a [java.lang.Boolean](../java.lang/Boolean.md).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicBoolean](AtomicBoolean.md))`()` Creates a new`AtomicBoolean`with initial value`false`. |
| [AtomicBoolean](AtomicBoolean.md))`(`initialValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new`AtomicBoolean`with the given initial value. |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndExchange](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndExchangeAcquire](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndExchangeRelease](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [get](AtomicBoolean.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAcquire](AtomicBoolean.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAndSet](AtomicBoolean.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getOpaque](AtomicBoolean.md))`()` Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getPlain](AtomicBoolean.md))`()` Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](AtomicBoolean.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicBoolean.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOpaque](AtomicBoolean.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlain](AtomicBoolean.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRelease](AtomicBoolean.md))`(`newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)). |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AtomicBoolean.md))`()` Returns the String representation of the current value. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetAcquire](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetPlain](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetRelease](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSetVolatile](AtomicBoolean.md))`(`expectedValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `newValue:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)). |

## Public constructors

### AtomicBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicBoolean()
```

Creates a new`AtomicBoolean`with initial value`false`. 

### AtomicBoolean

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AtomicBoolean(initialValue: Boolean)
```

Creates a new`AtomicBoolean`with the given initial value.

| Parameters ||
|----------------|------------------------------------------------------------------------------------------------------|
| `initialValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the initial value |

## Public methods

### compareAndExchange

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchange(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchange](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeAcquire(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeAcquire](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndExchangeRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndExchangeRelease(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Atomically sets the value to`newValue`if the current value, referred to as the*witness value* ,`== expectedValue`, with memory effects as specified by [VarHandle.compareAndExchangeRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the*witness value*, which will be the same as the expected value if successful |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun compareAndSet(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.compareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful. False return indicates that the actual value was not equal to the expected value. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun get(): Boolean
```

Returns the current value, with memory effects as specified by [VarHandle.getVolatile](../java.lang.invoke/VarHandle.md)).

| Return ||
|------------------------------------------------------------------------------------|-------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the current value |

### getAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAcquire(): Boolean
```

Returns the current value, with memory effects as specified by [VarHandle.getAcquire](../java.lang.invoke/VarHandle.md)).

| Return ||
|------------------------------------------------------------------------------------|-----------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndSet(newValue: Boolean): Boolean
```

Atomically sets the value to`newValue`and returns the old value, with memory effects as specified by [VarHandle.getAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the previous value |

### getOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOpaque(): Boolean
```

Returns the current value, with memory effects as specified by [VarHandle.getOpaque](../java.lang.invoke/VarHandle.md)).

| Return ||
|------------------------------------------------------------------------------------|-----------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value |

### getPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlain(): Boolean
```

Returns the current value, with memory semantics of reading as if the variable was declared non-`volatile`.

| Return ||
|------------------------------------------------------------------------------------|-----------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | the value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun lazySet(newValue: Boolean): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun set(newValue: Boolean): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setVolatile](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

### setOpaque

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOpaque(newValue: Boolean): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setOpaque](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

### setPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPlain(newValue: Boolean): Unit
```

Sets the value to`newValue`, with memory semantics of setting as if the variable was declared non-`volatile`and non-`final`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

### setRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRelease(newValue: Boolean): Unit
```

Sets the value to`newValue`, with memory effects as specified by [VarHandle.setRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------|
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Returns the String representation of the current value.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the String representation of the current value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun weakCompareAndSet(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

**Deprecated:** *This method has plain memory effects but the method name implies volatile memory effects (see methods such as [compareAndExchange](AtomicBoolean.md))and [compareAndSet](AtomicBoolean.md))). To avoid confusion over plain or volatile memory effects it is recommended that the method [weakCompareAndSetPlain](AtomicBoolean.md))be used instead.*

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

**See Also**

- [#weakCompareAndSetPlain](AtomicBoolean.md)) 

### weakCompareAndSetAcquire

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetAcquire(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetAcquire](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetPlain

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun weakCompareAndSetPlain(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetPlain](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetRelease

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetRelease(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSetRelease](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### weakCompareAndSetVolatile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun weakCompareAndSetVolatile(
    expectedValue: Boolean, 
    newValue: Boolean
): Boolean
```

Possibly atomically sets the value to`newValue`if the current value`== expectedValue`, with memory effects as specified by [VarHandle.weakCompareAndSet](../java.lang.invoke/VarHandle.md)).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------|
| `expectedValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the expected value |
| `newValue` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
