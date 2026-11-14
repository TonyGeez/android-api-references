# Set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Set

```
interface Set<E : Any!> : MutableCollection<E>
```

| [java.util.Set](Set.md) |

A collection that contains no duplicate elements. More formally, sets contain no pair of elements`e1`and`e2`such that`e1.equals(e2)`, and at most one null element. As implied by its name, this interface models the mathematical*set*abstraction.

The`Set`interface places additional stipulations, beyond those inherited from the`Collection`interface, on the contracts of all constructors and on the contracts of the`add`,`equals`and`hashCode`methods. Declarations for other inherited methods are also included here for convenience. (The specifications accompanying these declarations have been tailored to the`Set`interface, but they do not contain any additional stipulations.)

The additional stipulation on constructors is, not surprisingly, that all constructors must create a set that contains no duplicate elements (as defined above).

Note: Great care must be exercised if mutable objects are used as set elements. The behavior of a set is not specified if the value of an object is changed in a manner that affects`equals`comparisons while the object is an element in the set. A special case of this prohibition is that it is not permissible for a set to contain itself as an element.

Some set implementations have restrictions on the elements that they may contain. For example, some implementations prohibit null elements, and some have restrictions on the types of their elements. Attempting to add an ineligible element throws an unchecked exception, typically`NullPointerException`or`ClassCastException`. Attempting to query the presence of an ineligible element may throw an exception, or it may simply return false; some implementations will exhibit the former behavior and some will exhibit the latter. More generally, attempting an operation on an ineligible element whose completion would not result in the insertion of an ineligible element into the set may throw an exception or it may succeed, at the option of the implementation. Such exceptions are marked as "optional" in the specification for this interface.

## Unmodifiable Sets

The [Set.of](Set.md))and [Set.copyOf](Set.md))static factory methods provide a convenient way to create unmodifiable sets. The`Set`instances created by these methods have the following characteristics:

- They are [*unmodifiable*](Collection.md). Elements cannot be added or removed. Calling any mutator method on the Set will always cause`UnsupportedOperationException`to be thrown. However, if the contained elements are themselves mutable, this may cause the Set to behave inconsistently or its contents to appear to change.
- They disallow`null`elements. Attempts to create them with`null`elements result in`NullPointerException`.
- They are serializable if all elements are serializable.
- They reject duplicate elements at creation time. Duplicate elements passed to a static factory method result in`IllegalArgumentException`.
- The iteration order of set elements is unspecified and is subject to change.
- They are [value-based](../java/lang/doc-files/ValueBased.md). Programmers should treat instances that are #equals(java.lang.Object) as interchangeable and should not use them for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. Callers should make no assumptions about the identity of the returned instances. Factories are free to create new instances or reuse existing ones.
- They are serialized as specified on the [Serialized Form](https://developer.android.com//serialized-form.html#java.util.CollSer) page.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](Set.md))`(`element:` `E`)` Adds the specified element to this set if it is not already present (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](Set.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Adds all of the elements in the specified collection to this set if they're not already present (optional operation). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](Set.md))`()` Removes all of the elements from this set (optional operation). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](Set.md))`(`element:` `E?`)` Returns`true`if this set contains the specified element. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](Set.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Returns`true`if this set contains all of the elements of the specified collection. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [copyOf](Set.md))`(`coll:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>`)` Returns an [unmodifiable Set](Set.md) containing the elements of the given Collection. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](Set.md))`()` Returns`true`if this set contains no elements. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](Set.md))`()` Returns an iterator over the elements in this set. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`()` Returns an unmodifiable set containing zero elements. |
| --- | --- |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`)` Returns an unmodifiable set containing one element. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`)` Returns an unmodifiable set containing two elements. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`)` Returns an unmodifiable set containing three elements. |
| --- | --- |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`)` Returns an unmodifiable set containing four elements. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`)` Returns an unmodifiable set containing five elements. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`, `e6:` `E`)` Returns an unmodifiable set containing six elements. |
| --- | --- |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`, `e6:` `E`, `e7:` `E`)` Returns an unmodifiable set containing seven elements. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`, `e6:` `E`, `e7:` `E`, `e8:` `E`)` Returns an unmodifiable set containing eight elements. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`, `e6:` `E`, `e7:` `E`, `e8:` `E`, `e9:` `E`)` Returns an unmodifiable set containing nine elements. |
| --- | --- |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`e1:` `E`, `e2:` `E`, `e3:` `E`, `e4:` `E`, `e5:` `E`, `e6:` `E`, `e7:` `E`, `e8:` `E`, `e9:` `E`, `e10:` `E`)` Returns an unmodifiable set containing ten elements. |
| openstatic [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\<E\> | [of](Set.md))`(`vararg` `elements:` `E`)` Returns an unmodifiable set containing an arbitrary number of elements. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](Set.md))`(`element:` `E?`)` Removes the specified element from this set if it is present (optional operation). |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](Set.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Removes from this set all of its elements that are contained in the specified collection (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](Set.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Retains only the elements in this set that are contained in the specified collection (optional operation). |
| open [Spliterator](Spliterator.md)\<E\> | [spliterator](Set.md))`()` Creates a`Spliterator`over the elements in this set. |
| --- | --- |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](Set.md))`()` Returns an array containing all of the elements in this set. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](Set.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this set; the runtime type of the returned array is that of the specified array. |

| Properties ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](Set.md) Returns the number of elements in this set (its cardinality). |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(element: E): Boolean
```

Adds the specified element to this set if it is not already present (optional operation). More formally, adds the specified element`e`to this set if the set contains no element`e2`such that`Objects.equals(e, e2)`. If this set already contains the element, the call leaves the set unchanged and returns`false`. In combination with the restriction on constructors, this ensures that sets never contain duplicate elements.

The stipulation above does not imply that sets must accept all elements; sets may refuse to add any particular element, including`null`, and throw an exception, as described in the specification for [Collection.add](Collection.md)). Individual set implementations should clearly document any restrictions on the elements that they may contain.

| Parameters ||
|-----|---------------------------------|
| `e` | element to be added to this set |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set did not already contain the specified element |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this set |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this set |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addAll(elements: Collection<E>): Boolean
```

Adds all of the elements in the specified collection to this set if they're not already present (optional operation). If the specified collection is also a set, the`addAll`operation effectively modifies this set so that its value is the*union*of the two sets. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress.

| Parameters ||
|-----|--------------------------------------------------------|
| `c` | collection containing elements to be added to this set |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this set |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this set does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this set |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

**See Also**

- [#add(Object)](Set.md)) 

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clear(): Unit
```

Removes all of the elements from this set (optional operation). The set will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|--------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`method is not supported by this set |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun contains(element: E?): Boolean
```

Returns`true`if this set contains the specified element. More formally, returns`true`if and only if this set contains an element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|----------------------------------------------------|
| `o` | element whose presence in this set is to be tested |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains the specified element |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this set ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements ([optional](Collection.md)) |

### containsAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun containsAll(elements: Collection<E>): Boolean
```

Returns`true`if this set contains all of the elements of the specified collection. If the specified collection is also a set, this method returns`true`if it is a*subset*of this set.

| Parameters ||
|-----|------------------------------------------------------|
| `c` | collection to be checked for containment in this set |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains all of the elements of the specified collection |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this set ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this set does not permit null elements ([optional](Collection.md)), or if the specified collection is null |

**See Also**

- [#contains(Object)](Set.md)) 

### copyOf

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> copyOf(coll: MutableCollection<out E>): MutableSet<E>
```

Returns an [unmodifiable Set](Set.md) containing the elements of the given Collection. The given Collection must not be null, and it must not contain any null elements. If the given Collection contains duplicate elements, an arbitrary element of the duplicates is preserved. If the given Collection is subsequently modified, the returned Set will not reflect such modifications.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<E>` | the`Set`'s element type |
| `coll` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>:a`Collection`from which elements are drawn, must be non-null |

| Return ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the elements of the given`Collection` |

| Exceptions ||
|----------------------------------|----------------------------------------------|
| `java.lang.NullPointerException` | if coll is null, or if it contains any nulls |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isEmpty(): Boolean
```

Returns`true`if this set contains no elements.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this set. The elements are returned in no particular order (unless this set is an instance of some class that provides a guarantee).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this set |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(): MutableSet<E>
```

Returns an unmodifiable set containing zero elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |

| Return ||
|----------------------------------------------------------------------------------------------------------|---------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | an empty`Set` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(e1: E): MutableSet<E>
```

Returns an unmodifiable set containing one element. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the single element |

| Return ||
|----------------------------------------------------------------------------------------------------------|----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified element |

| Exceptions ||
|----------------------------------|-------------------------|
| `java.lang.NullPointerException` | if the element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E
): MutableSet<E>
```

Returns an unmodifiable set containing two elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|--------------------------------|
| `java.lang.IllegalArgumentException` | if the elements are duplicates |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E
): MutableSet<E>
```

Returns an unmodifiable set containing three elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E
): MutableSet<E>
```

Returns an unmodifiable set containing four elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E
): MutableSet<E>
```

Returns an unmodifiable set containing five elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |
| `e5` | E:the fifth element |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E, 
    e6: E
): MutableSet<E>
```

Returns an unmodifiable set containing six elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |
| `e5` | E:the fifth element |
| --- | --- |
| `e6` | E:the sixth element |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E, 
    e6: E, 
    e7: E
): MutableSet<E>
```

Returns an unmodifiable set containing seven elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |
| `e5` | E:the fifth element |
| --- | --- |
| `e6` | E:the sixth element |
| `e7` | E:the seventh element |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E, 
    e6: E, 
    e7: E, 
    e8: E
): MutableSet<E>
```

Returns an unmodifiable set containing eight elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |
| `e5` | E:the fifth element |
| --- | --- |
| `e6` | E:the sixth element |
| `e7` | E:the seventh element |
| `e8` | E:the eighth element |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E, 
    e6: E, 
    e7: E, 
    e8: E, 
    e9: E
): MutableSet<E>
```

Returns an unmodifiable set containing nine elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |
| `e5` | E:the fifth element |
| --- | --- |
| `e6` | E:the sixth element |
| `e7` | E:the seventh element |
| `e8` | E:the eighth element |
| --- | --- |
| `e9` | E:the ninth element |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E, 
    e6: E, 
    e7: E, 
    e8: E, 
    e9: E, 
    e10: E
): MutableSet<E>
```

Returns an unmodifiable set containing ten elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|-------|-------------------------|
| `<E>` | the`Set`'s element type |
| `e1` | E:the first element |
| `e2` | E:the second element |
| --- | --- |
| `e3` | E:the third element |
| `e4` | E:the fourth element |
| `e5` | E:the fifth element |
| --- | --- |
| `e6` | E:the sixth element |
| `e7` | E:the seventh element |
| `e8` | E:the eighth element |
| --- | --- |
| `e9` | E:the ninth element |
| `e10` | E:the tenth element |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
@SafeVarargs open static fun <E : Any!> of(vararg elements: E): MutableSet<E>
```

Returns an unmodifiable set containing an arbitrary number of elements. See [Unmodifiable Sets](Set.md) for details.

| Parameters ||
|------------|-------------------------------------------|
| `<E>` | the`Set`'s element type |
| `elements` | E:the elements to be contained in the set |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)<E> | a`Set`containing the specified elements |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | if there are any duplicate elements |
| `java.lang.NullPointerException` | if an element is`null`or if the array is`null` |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(element: E?): Boolean
```

Removes the specified element from this set if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this set contains such an element. Returns`true`if this set contained the element (or equivalently, if this set changed as a result of the call). (This set will not contain the element once the call returns.)

| Parameters ||
|-----|------------------------------------------------|
| `o` | object to be removed from this set, if present |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contained the specified element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this set ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements ([optional](Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this set |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeAll(elements: Collection<E>): Boolean
```

Removes from this set all of its elements that are contained in the specified collection (optional operation). If the specified collection is also a set, this operation effectively modifies this set so that its value is the*asymmetric set difference*of the two sets.

| Parameters ||
|-----|------------------------------------------------------------|
| `c` | collection containing elements to be removed from this set |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of this set is incompatible with the specified collection ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if this set contains a null element and the specified collection does not permit null elements ([optional](Collection.md)), or if the specified collection is null |
| --- | --- |

**See Also**

- [#remove(Object)](Set.md))
- [#contains(Object)](Set.md)) 

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun retainAll(elements: Collection<E>): Boolean
```

Retains only the elements in this set that are contained in the specified collection (optional operation). In other words, removes from this set all of its elements that are not contained in the specified collection. If the specified collection is also a set, this operation effectively modifies this set so that its value is the*intersection*of the two sets.

| Parameters ||
|-----|-----------------------------------------------------------|
| `c` | collection containing elements to be retained in this set |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`retainAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of this set is incompatible with the specified collection ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if this set contains a null element and the specified collection does not permit null elements ([optional](Collection.md)), or if the specified collection is null |
| --- | --- |

**See Also**

- [#remove(Object)](Set.md)) 

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a`Spliterator`over the elements in this set.

The`Spliterator`reports [Spliterator.DISTINCT](Spliterator.md). Implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------|
| [Spliterator](Spliterator.md)<E> | a`Spliterator`over the elements in this set |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this set. If this set makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order.

The returned array will be "safe" in that no references to it are maintained by this set. (In other words, this method must allocate a new array even if this set is backed by an array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all the elements in this set |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this set; the runtime type of the returned array is that of the specified array. If the set fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this set.

If this set fits in the specified array with room to spare (i.e., the array has more elements than this set), the element in the array immediately following the end of the set is set to`null`. (This is useful in determining the length of this set*only*if the caller knows that this set does not contain any null elements.)

If this set makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order.

Like the [toArray()](Set.md))method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose`x`is a set known to contain only strings. The following code can be used to dump the set into a newly allocated array of`String`: 

```kotlin
String[] y = x.toArray(new String[0]);
```
Note that`toArray(new Object[0])`is identical in function to`toArray()`.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of this set are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing all the elements in this set |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this set |
| `java.lang.NullPointerException` | if the specified array is null |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val size: Int
```

Returns the number of elements in this set (its cardinality). If this set contains more than`Integer.MAX_VALUE`elements, returns`Integer.MAX_VALUE`.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this set (its cardinality) |
