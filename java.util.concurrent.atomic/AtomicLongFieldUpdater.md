# AtomicLongFieldUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicLongFieldUpdater

```
abstract class AtomicLongFieldUpdater<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicLongFieldUpdater](AtomicLongFieldUpdater.md) |

A reflection-based utility that enables atomic updates to designated`volatile long`fields of designated classes. This class is designed for use in atomic data structures in which several fields of the same node are independently subject to atomic updates.

Note that the guarantees of the`compareAndSet`method in this class are weaker than in other atomic classes. Because this class cannot ensure that all uses of the field are appropriate for purposes of atomic access, it can guarantee atomicity only with respect to other invocations of`compareAndSet`and`set`on the same updater.

Object arguments for parameters of type`T`that are not instances of the class passed to [newUpdater](AtomicLongFieldUpdater.md))will result in a [ClassCastException](../java.lang/ClassCastException.md) being thrown.

## Summary

| Protected constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicLongFieldUpdater](AtomicLongFieldUpdater.md))`()` Protected do-nothing constructor for use by subclasses. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [accumulateAndGet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `accumulatorFunction:` ` [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the updated value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [addAndGet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `delta:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically adds the given value to the current value of the field of the given object managed by this updater. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `expect:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `update:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [decrementAndGet](AtomicLongFieldUpdater.md))`(`obj:` `T`)` Atomically decrements by one the current value of the field of the given object managed by this updater. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [get](AtomicLongFieldUpdater.md))`(`obj:` `T`)` Returns the current value held in the field of the given object managed by this updater. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndAccumulate](AtomicLongFieldUpdater.md))`(`obj:` `T`, `x:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `accumulatorFunction:` ` [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the previous value. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndAdd](AtomicLongFieldUpdater.md))`(`obj:` `T`, `delta:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically adds the given value to the current value of the field of the given object managed by this updater. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndDecrement](AtomicLongFieldUpdater.md))`(`obj:` `T`)` Atomically decrements by one the current value of the field of the given object managed by this updater. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndIncrement](AtomicLongFieldUpdater.md))`(`obj:` `T`)` Atomically increments by one the current value of the field of the given object managed by this updater. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndSet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the field of the given object managed by this updater to the given value and returns the old value. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getAndUpdate](AtomicLongFieldUpdater.md))`(`obj:` `T`, `updateFunction:` ` [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the previous value. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [incrementAndGet](AtomicLongFieldUpdater.md))`(`obj:` `T`)` Atomically increments by one the current value of the field of the given object managed by this updater. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Eventually sets the field of the given object managed by this updater to the given updated value. |
| openstatic [AtomicLongFieldUpdater](AtomicLongFieldUpdater.md)\<U\>! | [newUpdater](AtomicLongFieldUpdater.md))`(`tclass:` ` [Class](../java.lang/Class.md)<U>!`, `fieldName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates and returns an updater for objects with the given field. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicLongFieldUpdater.md))`(`obj:` `T`, `newValue:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Sets the field of the given object managed by this updater to the given updated value. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [updateAndGet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `updateFunction:` ` [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the updated value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicLongFieldUpdater.md))`(`obj:` `T`, `expect:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `update:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. |

## Protected constructors

### AtomicLongFieldUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AtomicLongFieldUpdater()
```

Protected do-nothing constructor for use by subclasses.

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    obj: T, 
    x: Long, 
    accumulatorFunction: LongBinaryOperator!
): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the update value |
| `accumulatorFunction` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAndGet(
    obj: T, 
    delta: Long
): Long
```

Atomically adds the given value to the current value of the field of the given object managed by this updater.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `delta` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to add |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compareAndSet(
    obj: T, 
    expect: Long, 
    update: Long
): Boolean
```

Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. This method is guaranteed to be atomic with respect to other calls to`compareAndSet`and`set`, but not necessarily with respect to other changes in the field.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to conditionally set |
| `expect` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `update` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### decrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun decrementAndGet(obj: T): Long
```

Atomically decrements by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(obj: T): Long
```

Returns the current value held in the field of the given object managed by this updater.

| Parameters ||
|-------|--------------------------------|
| `obj` | T:An object whose field to get |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the current value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    obj: T, 
    x: Long, 
    accumulatorFunction: LongBinaryOperator!
): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `x` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the update value |
| `accumulatorFunction` | [LongBinaryOperator](../java.util.function/LongBinaryOperator.md)!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndAdd(
    obj: T, 
    delta: Long
): Long
```

Atomically adds the given value to the current value of the field of the given object managed by this updater.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `delta` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the value to add |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndDecrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndDecrement(obj: T): Long
```

Atomically decrements by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndIncrement(obj: T): Long
```

Atomically increments by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndSet(
    obj: T, 
    newValue: Long
): Long
```

Atomically sets the field of the given object managed by this updater to the given value and returns the old value.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(
    obj: T, 
    updateFunction: LongUnaryOperator!
): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `updateFunction` | [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!:a side-effect-free function |

| Return ||
|------------------------------------------------------------------------------|--------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the previous value |

### incrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun incrementAndGet(obj: T): Long
```

Atomically increments by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lazySet(
    obj: T, 
    newValue: Long
): Unit
```

Eventually sets the field of the given object managed by this updater to the given updated value.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to set |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### newUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <U : Any!> newUpdater(
    tclass: Class<U>!, 
    fieldName: String!
): AtomicLongFieldUpdater<U>!
```

Creates and returns an updater for objects with the given field. The Class argument is needed to check that reflective types and generic types match.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------|
| `tclass` | [Class](../java.lang/Class.md)\<U\>!:the class of the objects holding the field |
| `fieldName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the field to be updated |
| `<U>` | the type of instances of tclass |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|-------------|
| [AtomicLongFieldUpdater](AtomicLongFieldUpdater.md)<U>! | the updater |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the field is not a volatile long type |
| `java.lang.RuntimeException` | with a nested reflection-based exception if the class does not hold field or is the wrong type, or the field is inaccessible to the caller according to Java language access control |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun set(
    obj: T, 
    newValue: Long
): Unit
```

Sets the field of the given object managed by this updater to the given updated value. This operation is guaranteed to act as a volatile store with respect to subsequent invocations of`compareAndSet`.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to set |
| `newValue` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |

### updateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateAndGet(
    obj: T, 
    updateFunction: LongUnaryOperator!
): Long
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `updateFunction` | [LongUnaryOperator](../java.util.function/LongUnaryOperator.md)!:a side-effect-free function |

| Return ||
|------------------------------------------------------------------------------|-------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun weakCompareAndSet(
    obj: T, 
    expect: Long, 
    update: Long
): Boolean
```

Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. This method is guaranteed to be atomic with respect to other calls to`compareAndSet`and`set`, but not necessarily with respect to other changes in the field.

This operation may fail spuriously and does not provide ordering guarantees, so is only rarely an appropriate alternative to`compareAndSet`.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to conditionally set |
| `expect` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the expected value |
| `update` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
