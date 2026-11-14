# AtomicIntegerFieldUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicIntegerFieldUpdater

```
abstract class AtomicIntegerFieldUpdater<T : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicIntegerFieldUpdater](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#) |

A reflection-based utility that enables atomic updates to designated`volatile int`fields of designated classes. This class is designed for use in atomic data structures in which several fields of the same node are independently subject to atomic updates.

Note that the guarantees of the`compareAndSet`method in this class are weaker than in other atomic classes. Because this class cannot ensure that all uses of the field are appropriate for purposes of atomic access, it can guarantee atomicity only with respect to other invocations of`compareAndSet`and`set`on the same updater.

Object arguments for parameters of type`T`that are not instances of the class passed to [newUpdater](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#newUpdater(java.lang.Class,%20kotlin.String))will result in a [ClassCastException](https://developer.android.com/reference/kotlin/java/lang/ClassCastException.html#) being thrown.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicIntegerFieldUpdater](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#AtomicIntegerFieldUpdater())`()` Protected do-nothing constructor for use by subclasses. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [accumulateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#accumulateAndGet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`obj:` `T`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the updated value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [addAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#addAndGet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int))`(`obj:` `T`, `delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the current value of the field of the given object managed by this updater. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#compareAndSet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int,%20kotlin.Int))`(`obj:` `T`, `expect:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `update:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [decrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#decrementAndGet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T))`(`obj:` `T`)` Atomically decrements by one the current value of the field of the given object managed by this updater. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#get(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T))`(`obj:` `T`)` Returns the current value held in the field of the given object managed by this updater. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAccumulate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#getAndAccumulate(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int,%20java.util.function.IntBinaryOperator))`(`obj:` `T`, `x:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `accumulatorFunction:` ` [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the previous value. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndAdd](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#getAndAdd(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int))`(`obj:` `T`, `delta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically adds the given value to the current value of the field of the given object managed by this updater. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndDecrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#getAndDecrement(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T))`(`obj:` `T`)` Atomically decrements by one the current value of the field of the given object managed by this updater. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndIncrement](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#getAndIncrement(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T))`(`obj:` `T`)` Atomically increments by one the current value of the field of the given object managed by this updater. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#getAndSet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int))`(`obj:` `T`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the field of the given object managed by this updater to the given value and returns the old value. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAndUpdate](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#getAndUpdate(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20java.util.function.IntUnaryOperator))`(`obj:` `T`, `updateFunction:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function, returning the previous value. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [incrementAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#incrementAndGet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T))`(`obj:` `T`)` Atomically increments by one the current value of the field of the given object managed by this updater. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#lazySet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int))`(`obj:` `T`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Eventually sets the field of the given object managed by this updater to the given updated value. |
| openstatic [AtomicIntegerFieldUpdater](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#)\<U\>! | [newUpdater](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#newUpdater(java.lang.Class,%20kotlin.String))`(`tclass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<U>!`, `fieldName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates and returns an updater for objects with the given field. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#set(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int))`(`obj:` `T`, `newValue:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the field of the given object managed by this updater to the given updated value. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [updateAndGet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#updateAndGet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20java.util.function.IntUnaryOperator))`(`obj:` `T`, `updateFunction:` ` [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function, returning the updated value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#weakCompareAndSet(java.util.concurrent.atomic.AtomicIntegerFieldUpdater.T,%20kotlin.Int,%20kotlin.Int))`(`obj:` `T`, `expect:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `update:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. |

## Protected constructors

### AtomicIntegerFieldUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AtomicIntegerFieldUpdater()
```

Protected do-nothing constructor for use by subclasses.

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    obj: T, 
    x: Int, 
    accumulatorFunction: IntBinaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### addAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAndGet(
    obj: T, 
    delta: Int
): Int
```

Atomically adds the given value to the current value of the field of the given object managed by this updater.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compareAndSet(
    obj: T, 
    expect: Int, 
    update: Int
): Boolean
```

Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. This method is guaranteed to be atomic with respect to other calls to`compareAndSet`and`set`, but not necessarily with respect to other changes in the field.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to conditionally set |
| `expect` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `update` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### decrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun decrementAndGet(obj: T): Int
```

Atomically decrements by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(obj: T): Int
```

Returns the current value held in the field of the given object managed by this updater.

| Parameters ||
|-------|--------------------------------|
| `obj` | T:An object whose field to get |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the current value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    obj: T, 
    x: Int, 
    accumulatorFunction: IntBinaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `x` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the update value |
| `accumulatorFunction` | [IntBinaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntBinaryOperator.html#)!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndAdd

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndAdd(
    obj: T, 
    delta: Int
): Int
```

Atomically adds the given value to the current value of the field of the given object managed by this updater.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `delta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the value to add |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndDecrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndDecrement(obj: T): Int
```

Atomically decrements by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndIncrement

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndIncrement(obj: T): Int
```

Atomically increments by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndSet(
    obj: T, 
    newValue: Int
): Int
```

Atomically sets the field of the given object managed by this updater to the given value and returns the old value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(
    obj: T, 
    updateFunction: IntUnaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `updateFunction` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the previous value |

### incrementAndGet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun incrementAndGet(obj: T): Int
```

Atomically increments by one the current value of the field of the given object managed by this updater.

| Parameters ||
|-------|----------------------------------------|
| `obj` | T:An object whose field to get and set |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lazySet(
    obj: T, 
    newValue: Int
): Unit
```

Eventually sets the field of the given object managed by this updater to the given updated value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to set |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### newUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <U : Any!> newUpdater(
    tclass: Class<U>!, 
    fieldName: String!
): AtomicIntegerFieldUpdater<U>!
```

Creates and returns an updater for objects with the given field. The Class argument is needed to check that reflective types and generic types match.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------|
| `tclass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<U\>!:the class of the objects holding the field |
| `fieldName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the field to be updated |
| `<U>` | the type of instances of tclass |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [AtomicIntegerFieldUpdater](https://developer.android.com/reference/kotlin/java/util/concurrent/atomic/AtomicIntegerFieldUpdater#)<U>! | the updater |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the field is not a volatile integer type |
| `java.lang.RuntimeException` | with a nested reflection-based exception if the class does not hold field or is the wrong type, or the field is inaccessible to the caller according to Java language access control |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun set(
    obj: T, 
    newValue: Int
): Unit
```

Sets the field of the given object managed by this updater to the given updated value. This operation is guaranteed to act as a volatile store with respect to subsequent invocations of`compareAndSet`.

| Parameters ||
|------------|------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to set |
| `newValue` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |

### updateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateAndGet(
    obj: T, 
    updateFunction: IntUnaryOperator!
): Int
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](https://developer.android.com/reference/kotlin/java/lang/invoke/VarHandle.html#compareAndSet(kotlin.Any))) the field of the given object managed by this updater with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `updateFunction` | [IntUnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/IntUnaryOperator.html#)!:a side-effect-free function |

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun weakCompareAndSet(
    obj: T, 
    expect: Int, 
    update: Int
): Boolean
```

Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. This method is guaranteed to be atomic with respect to other calls to`compareAndSet`and`set`, but not necessarily with respect to other changes in the field.

This operation may fail spuriously and does not provide ordering guarantees, so is only rarely an appropriate alternative to`compareAndSet`.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to conditionally set |
| `expect` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected value |
| `update` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
