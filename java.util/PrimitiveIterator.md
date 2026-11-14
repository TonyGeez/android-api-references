# PrimitiveIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrimitiveIterator

```
interface PrimitiveIterator<T : Any!, T_CONS : Any!> : MutableIterator<T>
```

| [java.util.PrimitiveIterator](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator#) |

| Known Direct Subclasses [PrimitiveIterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfDouble), [PrimitiveIterator.OfInt](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt), [PrimitiveIterator.OfLong](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfLong) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------| | [PrimitiveIterator.OfDouble](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfDouble) | An Iterator specialized for`double`values. | | [PrimitiveIterator.OfInt](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt) | An Iterator specialized for`int`values. | | [PrimitiveIterator.OfLong](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfLong) | An Iterator specialized for`long`values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base type for primitive specializations of`Iterator`. Specialized subtypes are provided for [int](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt), [long](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfLong), and [double](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfDouble) values.

The specialized subtype default implementations of [Iterator.next](https://developer.android.com/reference/kotlin/java/util/Iterator#next())and [Iterator.forEachRemaining(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/util/Iterator#forEachRemaining(java.util.function.Consumer))box primitive values to instances of their corresponding wrapper class. Such boxing may offset any advantages gained when using the primitive specializations. To avoid boxing, the corresponding primitive-based methods should be used. For example, [PrimitiveIterator.OfInt.nextInt()](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt#nextInt())and [PrimitiveIterator.OfInt.forEachRemaining(java.util.function.IntConsumer)](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt#forEachRemaining(java.util.function.IntConsumer))should be used in preference to [PrimitiveIterator.OfInt.next()](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt#next())and [PrimitiveIterator.OfInt.forEachRemaining(java.util.function.Consumer)](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt#forEachRemaining(java.util.function.Consumer)).

Iteration of primitive values using boxing-based methods [next()](https://developer.android.com/reference/kotlin/java/util/Iterator#next())and [forEachRemaining()](https://developer.android.com/reference/kotlin/java/util/Iterator#forEachRemaining(java.util.function.Consumer)), does not affect the order in which the values, transformed to boxed values, are encountered.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OfDouble](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfDouble) An Iterator specialized for`double`values. |
| abstract | [OfInt](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfInt) An Iterator specialized for`int`values. |
| abstract | [OfLong](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator.OfLong) An Iterator specialized for`long`values. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachRemaining](https://developer.android.com/reference/kotlin/java/util/PrimitiveIterator#forEachRemaining(java.util.PrimitiveIterator.T_CONS))`(`action:` `T_CONS`)` Performs the given action for each remaining element until all elements have been processed or the action throws an exception. |

## Public methods

### forEachRemaining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachRemaining(action: T_CONS): Unit
```

Performs the given action for each remaining element until all elements have been processed or the action throws an exception. Actions are performed in the order of iteration, if that order is specified. Exceptions thrown by the action are relayed to the caller.

The behavior of an iterator is unspecified if the action modifies the source of elements in any way (even by calling the [remove](https://developer.android.com/reference/kotlin/java/util/Iterator#remove())method or other mutator methods of`Iterator`subtypes), unless an overriding class has specified a concurrent modification policy.

Subsequent behavior of an iterator is unspecified if the action throws an exception.

| Parameters ||
|----------|----------------------------------------------------|
| `action` | T_CONS:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |
