# Iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Iterator

```
interface Iterator<E : Any!>
```

| [java.util.Iterator](Iterator.md) |

An iterator over a collection.`Iterator`takes the place of [Enumeration](Enumeration.md) in the Java Collections Framework. Iterators differ from enumerations in two ways:

- Iterators allow the caller to remove elements from the underlying collection during the iteration with well-defined semantics.
- Method names have been improved.

<br />

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEachRemaining](Iterator.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `E>`)` Performs the given action for each remaining element until all elements have been processed or the action throws an exception. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasNext](Iterator.md))`()` Returns`true`if the iteration has more elements. |
| abstractE | [next](Iterator.md))`()` Returns the next element in the iteration. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](Iterator.md))`()` Removes from the underlying collection the last element returned by this iterator (optional operation). |

## Public methods

### forEachRemaining

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEachRemaining(action: Consumer<in E>): Unit
```

Performs the given action for each remaining element until all elements have been processed or the action throws an exception. Actions are performed in the order of iteration, if that order is specified. Exceptions thrown by the action are relayed to the caller.

The behavior of an iterator is unspecified if the action modifies the collection in any way (even by calling the [remove](Iterator.md))method or other mutator methods of`Iterator`subtypes), unless an overriding class has specified a concurrent modification policy.

Subsequent behavior of an iterator is unspecified if the action throws an exception.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inE\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### hasNext

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasNext(): Boolean
```

Returns`true`if the iteration has more elements. (In other words, returns`true`if [next](Iterator.md))would return an element rather than throwing an exception.)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the iteration has more elements |

### next

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun next(): E
```

Returns the next element in the iteration.

| Return ||
|---|-----------------------------------|
| E | the next element in the iteration |

| Exceptions ||
|------------------------------------|---------------------------------------|
| `java.util.NoSuchElementException` | if the iteration has no more elements |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): Unit
```

Removes from the underlying collection the last element returned by this iterator (optional operation). This method can be called only once per call to [next](Iterator.md)).

The behavior of an iterator is unspecified if the underlying collection is modified while the iteration is in progress in any way other than by calling this method, unless an overriding class has specified a concurrent modification policy.

The behavior of an iterator is unspecified if this method is called after a call to the [forEachRemaining](Iterator.md))method.

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this iterator |
| `java.lang.IllegalStateException` | if the`next`method has not yet been called, or the`remove`method has already been called after the last call to the`next`method |
