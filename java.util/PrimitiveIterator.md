# PrimitiveIterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PrimitiveIterator

```
interface PrimitiveIterator<T : Any!, T_CONS : Any!> : MutableIterator<T>
```

| [java.util.PrimitiveIterator](PrimitiveIterator.md) |

| Known Direct Subclasses [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md), [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md), [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md) |-------------------------------------------------------------------------------------------------------------------|--------------------------------------------| | [PrimitiveIterator.OfDouble](../java/util/PrimitiveIterator.OfDouble.md) | An Iterator specialized for`double`values. | | [PrimitiveIterator.OfInt](../java/util/PrimitiveIterator.OfInt.md) | An Iterator specialized for`int`values. | | [PrimitiveIterator.OfLong](../java/util/PrimitiveIterator.OfLong.md) | An Iterator specialized for`long`values. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A base type for primitive specializations of`Iterator`. Specialized subtypes are provided for [int](../java/util/PrimitiveIterator.OfInt.md), [long](../java/util/PrimitiveIterator.OfLong.md), and [double](../java/util/PrimitiveIterator.OfDouble.md) values.

The specialized subtype default implementations of [Iterator.next](Iterator.md))and [Iterator.forEachRemaining(java.util.function.Consumer)](Iterator.md))box primitive values to instances of their corresponding wrapper class. Such boxing may offset any advantages gained when using the primitive specializations. To avoid boxing, the corresponding primitive-based methods should be used. For example, [PrimitiveIterator.OfInt.nextInt()](../java/util/PrimitiveIterator.OfInt.md))and [PrimitiveIterator.OfInt.forEachRemaining(java.util.function.IntConsumer)](../java/util/PrimitiveIterator.OfInt.md))should be used in preference to [PrimitiveIterator.OfInt.next()](../java/util/PrimitiveIterator.OfInt.md))and [PrimitiveIterator.OfInt.forEachRemaining(java.util.function.Consumer)](../java/util/PrimitiveIterator.OfInt.md)).

Iteration of primitive values using boxing-based methods [next()](Iterator.md))and [forEachRemaining()](Iterator.md)), does not affect the order in which the values, transformed to boxed values, are encountered.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OfDouble](../java/util/PrimitiveIterator.OfDouble.md) An Iterator specialized for`double`values. |
| abstract | [OfInt](../java/util/PrimitiveIterator.OfInt.md) An Iterator specialized for`int`values. |
| abstract | [OfLong](../java/util/PrimitiveIterator.OfLong.md) An Iterator specialized for`long`values. |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachRemaining](PrimitiveIterator.md))`(`action:` `T_CONS`)` Performs the given action for each remaining element until all elements have been processed or the action throws an exception. |

## Public methods

### forEachRemaining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun forEachRemaining(action: T_CONS): Unit
```

Performs the given action for each remaining element until all elements have been processed or the action throws an exception. Actions are performed in the order of iteration, if that order is specified. Exceptions thrown by the action are relayed to the caller.

The behavior of an iterator is unspecified if the action modifies the source of elements in any way (even by calling the [remove](Iterator.md))method or other mutator methods of`Iterator`subtypes), unless an overriding class has specified a concurrent modification policy.

Subsequent behavior of an iterator is unspecified if the action throws an exception.

| Parameters ||
|----------|----------------------------------------------------|
| `action` | T_CONS:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |
