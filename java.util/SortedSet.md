# SortedSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SortedSet

```
interface SortedSet<E : Any!> : SequencedSet<E>, MutableSet<E>
```

| [java.util.SortedSet](../java/util/SortedSet.md) |

| Known Direct Subclasses [NavigableSet](../java/util/NavigableSet.md) |---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [NavigableSet](../java/util/NavigableSet.md) | A [SortedSet](../java/util/SortedSet.md) extended with navigation methods reporting closest matches for given search targets. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md), [TreeSet](../java/util/TreeSet.md) |--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md) | A scalable concurrent [NavigableSet](../java/util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md). | | [TreeSet](../java/util/TreeSet.md) | A [NavigableSet](../java/util/NavigableSet.md) implementation based on a [TreeMap](../java/util/TreeMap.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A [Set](../java/util/Set.md) that further provides a*total ordering* on its elements. The elements are ordered using their [ordering](../java/lang/Comparable.md), or by a [Comparator](../java/util/Comparator.md) typically provided at sorted set creation time. The set's iterator will traverse the set in ascending element order. Several additional operations are provided to take advantage of the ordering. (This interface is the set analogue of [SortedMap](../java/util/SortedMap.md).)

All elements inserted into a sorted set must implement the`Comparable`interface (or be accepted by the specified comparator). Furthermore, all such elements must be*mutually comparable* :`e1.compareTo(e2)`(or`comparator.compare(e1, e2)`) must not throw a`ClassCastException`for any elements`e1`and`e2`in the sorted set. Attempts to violate this restriction will cause the offending method or constructor invocation to throw a`ClassCastException`.

Note that the ordering maintained by a sorted set (whether or not an explicit comparator is provided) must be*consistent with equals* if the sorted set is to correctly implement the`Set`interface. (See the`Comparable`interface or`Comparator`interface for a precise definition of*consistent with equals* .) This is so because the`Set`interface is defined in terms of the`equals`operation, but a sorted set performs all element comparisons using its`compareTo`(or`compare`) method, so two elements that are deemed equal by this method are, from the standpoint of the sorted set, equal. The behavior of a sorted set*is* well-defined even if its ordering is inconsistent with equals; it just fails to obey the general contract of the`Set`interface.

All general-purpose sorted set implementation classes should provide four "standard" constructors: 1) A void (no arguments) constructor, which creates an empty sorted set sorted according to the natural ordering of its elements. 2) A constructor with a single argument of type`Comparator`, which creates an empty sorted set sorted according to the specified comparator. 3) A constructor with a single argument of type`Collection`, which creates a new sorted set with the same elements as its argument, sorted according to the natural ordering of the elements. 4) A constructor with a single argument of type`SortedSet`, which creates a new sorted set with the same elements and the same ordering as the input sorted set. There is no way to enforce this recommendation, as interfaces cannot contain constructors.

Note: several methods return subsets with restricted ranges. Such ranges are*half-open* , that is, they include their low endpoint but not their high endpoint (where applicable). If you need a*closed range* (which includes both endpoints), and the element type allows for calculation of the successor of a given value, merely request the subrange from`lowEndpoint`to`successor(highEndpoint)`. For example, suppose that`s`is a sorted set of strings. The following idiom obtains a view containing all of the strings in`s`from`low`to`high`, inclusive: 

```kotlin
SortedSet<String> sub = s.subSet(low, high+"\0");
```
A similar technique can be used to generate an*open range* (which contains neither endpoint). The following idiom obtains a view containing all of the Strings in`s`from`low`to`high`, exclusive: 

```kotlin
SortedSet<String> sub = s.subSet(low+"\0", high);
```

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/SortedSet.md))`(`e:` `E`)` Throws`UnsupportedOperationException`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/SortedSet.md))`(`e:` `E`)` Throws`UnsupportedOperationException`. |
| abstract [Comparator](../java/util/Comparator.md)\<inE\>! | [comparator](../java/util/SortedSet.md))`()` Returns the comparator used to order the elements in this set, or`null`if this set uses the [natural ordering](../java/lang/Comparable.md) of its elements. |
| --- | --- |
| abstractE | [first](../java/util/SortedSet.md))`()` Returns the first (lowest) element currently in this set. |
| openE | [getFirst](../java/util/SortedSet.md))`()` Gets the first element of this collection. |
| openE | [getLast](../java/util/SortedSet.md))`()` Gets the last element of this collection. |
| --- | --- |
| abstract [SortedSet](../java/util/SortedSet.md)\<E\>! | [headSet](../java/util/SortedSet.md))`(`toElement:` `E`)` Returns a view of the portion of this set whose elements are strictly less than`toElement`. |
| abstractE | [last](../java/util/SortedSet.md))`()` Returns the last (highest) element currently in this set. |
| openE | [removeFirst](../java/util/SortedSet.md))`()` Removes and returns the first element of this collection (optional operation). |
| --- | --- |
| openE | [removeLast](../java/util/SortedSet.md))`()` Removes and returns the last element of this collection (optional operation). |
| open [SortedSet](../java/util/SortedSet.md)\<E\>! | [reversed](../java/util/SortedSet.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. |
| open [Spliterator](../java/util/Spliterator.md)\<E\> | [spliterator](../java/util/SortedSet.md))`()` Creates a`Spliterator`over the elements in this sorted set. |
| --- | --- |
| abstract [SortedSet](../java/util/SortedSet.md)\<E\>! | [subSet](../java/util/SortedSet.md))`(`fromElement:` `E`, `toElement:` `E`)` Returns a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive. |
| abstract [SortedSet](../java/util/SortedSet.md)\<E\>! | [tailSet](../java/util/SortedSet.md))`(`fromElement:` `E`)` Returns a view of the portion of this set whose elements are greater than or equal to`fromElement`. |

## Public methods

### addFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFirst(e: E): Unit
```

Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported.

| Parameters ||
|-----|---------------------------|
| `e` | E:the element to be added |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | always |

### addLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLast(e: E): Unit
```

Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported.

| Parameters ||
|-----|----------------------------|
| `e` | E:the element to be added. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | always |

### comparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun comparator(): Comparator<in E>!
```

Returns the comparator used to order the elements in this set, or`null`if this set uses the [natural ordering](../java/lang/Comparable.md) of its elements.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Comparator](../java/util/Comparator.md)<in` `E>! | the comparator used to order the elements in this set, or`null`if this set uses the natural ordering of its elements |

### first

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun first(): E
```

Returns the first (lowest) element currently in this set.

| Return ||
|---|--------------------------------------------------|
| E | the first (lowest) element currently in this set |

| Exceptions ||
|------------------------------------|----------------------|
| `java.util.NoSuchElementException` | if this set is empty |

### getFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFirst(): E
```

Gets the first element of this collection.

| Return ||
|---|-----------------------|
| E | the retrieved element |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |

### getLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLast(): E
```

Gets the last element of this collection.

| Return ||
|---|-----------------------|
| E | the retrieved element |

| Exceptions ||
|------------------------------------|-----------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |

### headSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun headSet(toElement: E): SortedSet<E>!
```

Returns a view of the portion of this set whose elements are strictly less than`toElement`. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

| Parameters ||
|-------------|-------------------------------------------------|
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements are strictly less than`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`toElement`lies outside the bounds of the range |
| --- | --- |

### last

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun last(): E
```

Returns the last (highest) element currently in this set.

| Return ||
|---|--------------------------------------------------|
| E | the last (highest) element currently in this set |

| Exceptions ||
|------------------------------------|----------------------|
| `java.util.NoSuchElementException` | if this set is empty |

### removeFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeFirst(): E
```

Removes and returns the first element of this collection (optional operation).

| Return ||
|---|---------------------|
| E | the removed element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### removeLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeLast(): E
```

Removes and returns the last element of this collection (optional operation).

| Return ||
|---|---------------------|
| E | the removed element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if this collection is empty |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun reversed(): SortedSet<E>!
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a reverse-ordered view of this collection, as a`SortedSet` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a`Spliterator`over the elements in this sorted set.

The`Spliterator`reports [Spliterator.DISTINCT](../java/util/Spliterator.md), [Spliterator.SORTED](../java/util/Spliterator.md) and [Spliterator.ORDERED](../java/util/Spliterator.md). Implementations should document the reporting of additional characteristic values.

The spliterator's comparator (see [java.util.Spliterator#getComparator()](../java/util/Spliterator.md))) must be`null`if the sorted set's comparator (see [comparator()](../java/util/SortedSet.md))) is`null`. Otherwise, the spliterator's comparator must be the same as or impose the same total ordering as the sorted set's comparator.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------------|
| [Spliterator](../java/util/Spliterator.md)<E> | a`Spliterator`over the elements in this sorted set |

### subSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subSet(
    fromElement: E, 
    toElement: E
): SortedSet<E>!
```

Returns a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive. (If`fromElement`and`toElement`are equal, the returned set is empty.) The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

| Parameters ||
|---------------|-------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`and`toElement`cannot be compared to one another using this set's comparator (or, if the set has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromElement`or`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range |
| --- | --- |

### tailSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tailSet(fromElement: E): SortedSet<E>!
```

Returns a view of the portion of this set whose elements are greater than or equal to`fromElement`. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

| Parameters ||
|---------------|------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |

| Return ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`fromElement`lies outside the bounds of the range |
| --- | --- |
