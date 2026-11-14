# AtomicReferenceFieldUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AtomicReferenceFieldUpdater

```
abstract class AtomicReferenceFieldUpdater<T : Any!, V : Any!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.atomic.AtomicReferenceFieldUpdater](AtomicReferenceFieldUpdater.md) |

A reflection-based utility that enables atomic updates to designated`volatile`reference fields of designated classes. This class is designed for use in atomic data structures in which several reference fields of the same node are independently subject to atomic updates. For example, a tree node might be declared as 

```kotlin
<code>class Node {
    private volatile Node left, right;
 
    private static final AtomicReferenceFieldUpdater&lt;Node, Node&gt; leftUpdater =
      AtomicReferenceFieldUpdater.newUpdater(Node.class, Node.class, "left");
    private static final AtomicReferenceFieldUpdater&lt;Node, Node&gt; rightUpdater =
      AtomicReferenceFieldUpdater.newUpdater(Node.class, Node.class, "right");
 
    Node getLeft() { return left; }
    boolean compareAndSetLeft(Node expect, Node update) {
      return leftUpdater.compareAndSet(this, expect, update);
    }
    // ... and so on
  }</code>
```

<br />

Note that the guarantees of the`compareAndSet`method in this class are weaker than in other atomic classes. Because this class cannot ensure that all uses of the field are appropriate for purposes of atomic access, it can guarantee atomicity only with respect to other invocations of`compareAndSet`and`set`on the same updater.

Object arguments for parameters of type`T`that are not instances of the class passed to [newUpdater](AtomicReferenceFieldUpdater.md))will result in a [ClassCastException](../java.lang/ClassCastException.md) being thrown.

## Summary

| Protected constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AtomicReferenceFieldUpdater](AtomicReferenceFieldUpdater.md))`()` Protected do-nothing constructor for use by subclasses. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| V | [accumulateAndGet](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `x:` `V`, `accumulatorFunction:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the updated value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [compareAndSet](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `expect:` `V`, `update:` `V`)` Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. |
| abstractV | [get](AtomicReferenceFieldUpdater.md))`(`obj:` `T`)` Returns the current value held in the field of the given object managed by this updater. |
| --- | --- |
| V | [getAndAccumulate](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `x:` `V`, `accumulatorFunction:` ` [BinaryOperator](../java.util.function/BinaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the previous value. |
| openV | [getAndSet](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `newValue:` `V`)` Atomically sets the field of the given object managed by this updater to the given value and returns the old value. |
| V | [getAndUpdate](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `updateFunction:` ` [UnaryOperator](../java.util.function/UnaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the previous value. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [lazySet](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `newValue:` `V`)` Eventually sets the field of the given object managed by this updater to the given updated value. |
| openstatic [AtomicReferenceFieldUpdater](AtomicReferenceFieldUpdater.md)\<U,W\>! | [newUpdater](AtomicReferenceFieldUpdater.md))`(`tclass:` ` [Class](../java.lang/Class.md)<U>!`, `vclass:` ` [Class](../java.lang/Class.md)<W>!`, `fieldName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates and returns an updater for objects with the given field. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [set](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `newValue:` `V`)` Sets the field of the given object managed by this updater to the given updated value. |
| --- | --- |
| V | [updateAndGet](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `updateFunction:` ` [UnaryOperator](../java.util.function/UnaryOperator.md)<V>!`)` Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the updated value. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [weakCompareAndSet](AtomicReferenceFieldUpdater.md))`(`obj:` `T`, `expect:` `V`, `update:` `V`)` Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. |

## Protected constructors

### AtomicReferenceFieldUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AtomicReferenceFieldUpdater()
```

Protected do-nothing constructor for use by subclasses.

## Public methods

### accumulateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun accumulateAndGet(
    obj: T, 
    x: V, 
    accumulatorFunction: BinaryOperator<V>!
): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `x` | V:the update value |
| `accumulatorFunction` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<V\>!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|---|-------------------|
| V | the updated value |

### compareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun compareAndSet(
    obj: T, 
    expect: V, 
    update: V
): Boolean
```

Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. This method is guaranteed to be atomic with respect to other calls to`compareAndSet`and`set`, but not necessarily with respect to other changes in the field.

| Parameters ||
|----------|----------------------------------------------|
| `obj` | T:An object whose field to conditionally set |
| `expect` | V:the expected value |
| `update` | V:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(obj: T): V
```

Returns the current value held in the field of the given object managed by this updater.

| Parameters ||
|-------|--------------------------------|
| `obj` | T:An object whose field to get |

| Return ||
|---|-------------------|
| V | the current value |

### getAndAccumulate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndAccumulate(
    obj: T, 
    x: V, 
    accumulatorFunction: BinaryOperator<V>!
): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function to the current and given values, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads. The function is applied with the current value as its first argument, and the given update as the second argument.

| Parameters ||
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `x` | V:the update value |
| `accumulatorFunction` | [BinaryOperator](../java.util.function/BinaryOperator.md)\<V\>!:a side-effect-free function of two arguments |
| --- | --- |

| Return ||
|---|--------------------|
| V | the previous value |

### getAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAndSet(
    obj: T, 
    newValue: V
): V
```

Atomically sets the field of the given object managed by this updater to the given value and returns the old value.

| Parameters ||
|------------|----------------------------------------|
| `obj` | T:An object whose field to get and set |
| `newValue` | V:the new value |

| Return ||
|---|--------------------|
| V | the previous value |

### getAndUpdate

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAndUpdate(
    obj: T, 
    updateFunction: UnaryOperator<V>!
): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the previous value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `updateFunction` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<V\>!:a side-effect-free function |

| Return ||
|---|--------------------|
| V | the previous value |

### lazySet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lazySet(
    obj: T, 
    newValue: V
): Unit
```

Eventually sets the field of the given object managed by this updater to the given updated value.

| Parameters ||
|------------|--------------------------------|
| `obj` | T:An object whose field to set |
| `newValue` | V:the new value |

### newUpdater

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <U : Any!, W : Any!> newUpdater(
    tclass: Class<U>!, 
    vclass: Class<W>!, 
    fieldName: String!
): AtomicReferenceFieldUpdater<U, W>!
```

Creates and returns an updater for objects with the given field. The Class arguments are needed to check that reflective types and generic types match.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------|
| `tclass` | [Class](../java.lang/Class.md)\<U\>!:the class of the objects holding the field |
| `vclass` | [Class](../java.lang/Class.md)\<W\>!:the class of the field |
| `fieldName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the name of the field to be updated |
| --- | --- |
| `<U>` | the type of instances of tclass |
| `<W>` | the type of instances of vclass |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [AtomicReferenceFieldUpdater](AtomicReferenceFieldUpdater.md)<U,` `W>! | the updater |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the field is of the wrong type |
| `java.lang.IllegalArgumentException` | if the field is not volatile |
| `java.lang.RuntimeException` | with a nested reflection-based exception if the class does not hold field or is the wrong type, or the field is inaccessible to the caller according to Java language access control |
| --- | --- |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun set(
    obj: T, 
    newValue: V
): Unit
```

Sets the field of the given object managed by this updater to the given updated value. This operation is guaranteed to act as a volatile store with respect to subsequent invocations of`compareAndSet`.

| Parameters ||
|------------|--------------------------------|
| `obj` | T:An object whose field to set |
| `newValue` | V:the new value |

### updateAndGet

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun updateAndGet(
    obj: T, 
    updateFunction: UnaryOperator<V>!
): V
```

Atomically updates (with memory effects as specified by [java.lang.invoke.VarHandle#compareAndSet](../java.lang.invoke/VarHandle.md))) the field of the given object managed by this updater with the results of applying the given function, returning the updated value. The function should be side-effect-free, since it may be re-applied when attempted updates fail due to contention among threads.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `obj` | T:An object whose field to get and set |
| `updateFunction` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<V\>!:a side-effect-free function |

| Return ||
|---|-------------------|
| V | the updated value |

### weakCompareAndSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun weakCompareAndSet(
    obj: T, 
    expect: V, 
    update: V
): Boolean
```

Atomically sets the field of the given object managed by this updater to the given updated value if the current value`==`the expected value. This method is guaranteed to be atomic with respect to other calls to`compareAndSet`and`set`, but not necessarily with respect to other changes in the field.

This operation may fail spuriously and does not provide ordering guarantees, so is only rarely an appropriate alternative to`compareAndSet`.

| Parameters ||
|----------|----------------------------------------------|
| `obj` | T:An object whose field to conditionally set |
| `expect` | V:the expected value |
| `update` | V:the new value |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful |
