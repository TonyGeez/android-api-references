# NavigableSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NavigableSet

```
interface NavigableSet<E : Any!> : SortedSet<E>
```

| [java.util.NavigableSet](../java/util/NavigableSet.md) |

| Known Direct Subclasses [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md), [TreeSet](../java/util/TreeSet.md) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ConcurrentSkipListSet](../java/util/concurrent/ConcurrentSkipListSet.md) | A scalable concurrent [NavigableSet](../java/util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](../java/util/concurrent/ConcurrentSkipListMap.md). | | [TreeSet](../java/util/TreeSet.md) | A [NavigableSet](../java/util/NavigableSet.md) implementation based on a [TreeMap](../java/util/TreeMap.md). | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A [SortedSet](../java/util/SortedSet.md) extended with navigation methods reporting closest matches for given search targets. Methods [lower](../java/util/NavigableSet.md)), [floor](../java/util/NavigableSet.md)), [ceiling](../java/util/NavigableSet.md)), and [higher](../java/util/NavigableSet.md))return elements respectively less than, less than or equal, greater than or equal, and greater than a given element, returning`null`if there is no such element.

A`NavigableSet`may be accessed and traversed in either ascending or descending order. The [descendingSet](../java/util/NavigableSet.md))method returns a view of the set with the senses of all relational and directional methods inverted. The performance of ascending operations and views is likely to be faster than that of descending ones. This interface additionally defines methods [pollFirst](../java/util/NavigableSet.md))and [pollLast](../java/util/NavigableSet.md))that return and remove the lowest and highest element, if one exists, else returning`null`. Methods [subSet(E, boolean, E, boolean)](../java/util/NavigableSet.md)), [headSet(E, boolean)](../java/util/NavigableSet.md)), and [tailSet(E, boolean)](../java/util/NavigableSet.md))differ from the like-named`SortedSet`methods in accepting additional arguments describing whether lower and upper bounds are inclusive versus exclusive. Subsets of any`NavigableSet`must implement the`NavigableSet`interface.

The return values of navigation methods may be ambiguous in implementations that permit`null`elements. However, even in this case the result can be disambiguated by checking`contains(null)`. To avoid such issues, implementations of this interface are encouraged to*not* permit insertion of`null`elements. (Note that sorted sets of [Comparable](../java/lang/Comparable.md) elements intrinsically do not permit`null`.)

Methods [subSet(E, E)](../java/util/NavigableSet.md)), [headSet(E)](../java/util/NavigableSet.md)), and [tailSet(E)](../java/util/NavigableSet.md))are specified to return`SortedSet`to allow existing implementations of`SortedSet`to be compatibly retrofitted to implement`NavigableSet`, but extensions and implementations of this interface are encouraged to override these methods to return`NavigableSet`.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractE | [ceiling](../java/util/NavigableSet.md))`(`e:` `E`)` Returns the least element in this set greater than or equal to the given element, or`null`if there is no such element. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\>! | [descendingIterator](../java/util/NavigableSet.md))`()` Returns an iterator over the elements in this set, in descending order. |
| abstract [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [descendingSet](../java/util/NavigableSet.md))`()` Returns a reverse order view of the elements contained in this set. |
| --- | --- |
| abstractE | [floor](../java/util/NavigableSet.md))`(`e:` `E`)` Returns the greatest element in this set less than or equal to the given element, or`null`if there is no such element. |
| abstract [SortedSet](../java/util/SortedSet.md)\<E\>! | [headSet](../java/util/NavigableSet.md))`(`toElement:` `E`)` Returns a view of the portion of this set whose elements are strictly less than`toElement`. |
| abstract [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [headSet](../java/util/NavigableSet.md))`(`toElement:` `E`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a view of the portion of this set whose elements are less than (or equal to, if`inclusive`is true)`toElement`. |
| --- | --- |
| abstractE | [higher](../java/util/NavigableSet.md))`(`e:` `E`)` Returns the least element in this set strictly greater than the given element, or`null`if there is no such element. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](../java/util/NavigableSet.md))`()` Returns an iterator over the elements in this set, in ascending order. |
| abstractE | [lower](../java/util/NavigableSet.md))`(`e:` `E`)` Returns the greatest element in this set strictly less than the given element, or`null`if there is no such element. |
| --- | --- |
| abstractE | [pollFirst](../java/util/NavigableSet.md))`()` Retrieves and removes the first (lowest) element, or returns`null`if this set is empty. |
| abstractE | [pollLast](../java/util/NavigableSet.md))`()` Retrieves and removes the last (highest) element, or returns`null`if this set is empty. |
| openE | [removeFirst](../java/util/NavigableSet.md))`()` Removes and returns the first element of this collection (optional operation). |
| --- | --- |
| openE | [removeLast](../java/util/NavigableSet.md))`()` Removes and returns the last element of this collection (optional operation). |
| open [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [reversed](../java/util/NavigableSet.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. |
| abstract [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [subSet](../java/util/NavigableSet.md))`(`fromElement:` `E`, `fromInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `toElement:` `E`, `toInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a view of the portion of this set whose elements range from`fromElement`to`toElement`. |
| --- | --- |
| abstract [SortedSet](../java/util/SortedSet.md)\<E\>! | [subSet](../java/util/NavigableSet.md))`(`fromElement:` `E`, `toElement:` `E`)` Returns a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive. |
| abstract [SortedSet](../java/util/SortedSet.md)\<E\>! | [tailSet](../java/util/NavigableSet.md))`(`fromElement:` `E`)` Returns a view of the portion of this set whose elements are greater than or equal to`fromElement`. |
| abstract [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [tailSet](../java/util/NavigableSet.md))`(`fromElement:` `E`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Returns a view of the portion of this set whose elements are greater than (or equal to, if`inclusive`is true)`fromElement`. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [SortedSet](../java/util/SortedSet.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/SortedSet.md))`(`e:` `E`)` <br /> Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/SortedSet.md))`(`e:` `E`)` <br /> Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported. <br /> | | [Comparator](../java/util/Comparator.md)<in` `E>! | [comparator](../java/util/SortedSet.md))`()` <br /> Returns the comparator used to order the elements in this set, or`null`if this set uses the [natural ordering](../java/lang/Comparable.md) of its elements. <br /> | | E | [first](../java/util/SortedSet.md))`()` <br /> Returns the first (lowest) element currently in this set. <br /> | | E | [getFirst](../java/util/SortedSet.md))`()` <br /> Gets the first element of this collection. <br /> | | E | [getLast](../java/util/SortedSet.md))`()` <br /> Gets the last element of this collection. <br /> | | E | [last](../java/util/SortedSet.md))`()` <br /> Returns the last (highest) element currently in this set. <br /> | | [Spliterator](../java/util/Spliterator.md)<E> | [spliterator](../java/util/SortedSet.md))`()` <br /> Creates a`Spliterator`over the elements in this sorted set. The`Spliterator`reports [Spliterator.DISTINCT](../java/util/Spliterator.md), [Spliterator.SORTED](../java/util/Spliterator.md) and [Spliterator.ORDERED](../java/util/Spliterator.md). Implementations should document the reporting of additional characteristic values. The spliterator's comparator (see [java.util.Spliterator#getComparator()](../java/util/Spliterator.md))) must be`null`if the sorted set's comparator (see [comparator()](../java/util/SortedSet.md))) is`null`. Otherwise, the spliterator's comparator must be the same as or impose the same total ordering as the sorted set's comparator. <br /> | ||

## Public methods

### ceiling

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun ceiling(e: E): E
```

Returns the least element in this set greater than or equal to the given element, or`null`if there is no such element.

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------------------|
| E | the least element greater than or equal to`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements |

### descendingIterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descendingIterator(): MutableIterator<E>!
```

Returns an iterator over the elements in this set, in descending order. Equivalent in effect to`descendingSet().iterator()`.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E>! | an iterator over the elements in this set, in descending order |

### descendingSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun descendingSet(): NavigableSet<E>!
```

Returns a reverse order view of the elements contained in this set. The descending set is backed by this set, so changes to the set are reflected in the descending set, and vice-versa. If either set is modified while an iteration over either set is in progress (except through the iterator's own`remove`operation), the results of the iteration are undefined.

The returned set has an ordering equivalent to [Collections.reverseOrder](../java/util/Collections.md))`(comparator())`. The expression`s.descendingSet().descendingSet()`returns a view of`s`essentially equivalent to`s`.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a reverse order view of this set |

### floor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun floor(e: E): E
```

Returns the greatest element in this set less than or equal to the given element, or`null`if there is no such element.

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------------------|
| E | the greatest element less than or equal to`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements |

### headSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun headSet(toElement: E): SortedSet<E>!
```

Returns a view of the portion of this set whose elements are strictly less than`toElement`. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

Equivalent to`headSet(toElement, false)`.

| Parameters ||
|-------------|-------------------------------------------------|
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements are strictly less than`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`toElement`lies outside the bounds of the range |
| --- | --- |

### headSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun headSet(
    toElement: E, 
    inclusive: Boolean
): NavigableSet<E>!
```

Returns a view of the portion of this set whose elements are less than (or equal to, if`inclusive`is true)`toElement`. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toElement` | E:high endpoint of the returned set |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the high endpoint is to be included in the returned view |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are less than (or equal to, if`inclusive`is true)`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`toElement`lies outside the bounds of the range |
| --- | --- |

### higher

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun higher(e: E): E
```

Returns the least element in this set strictly greater than the given element, or`null`if there is no such element.

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------|
| E | the least element greater than`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this set, in ascending order.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this set, in ascending order |

### lower

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun lower(e: E): E
```

Returns the greatest element in this set strictly less than the given element, or`null`if there is no such element.

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------|
| E | the greatest element less than`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pollFirst(): E
```

Retrieves and removes the first (lowest) element, or returns`null`if this set is empty.

| Return ||
|---|-------------------------------------------------|
| E | the first element, or`null`if this set is empty |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pollLast(): E
```

Retrieves and removes the last (highest) element, or returns`null`if this set is empty.

| Return ||
|---|------------------------------------------------|
| E | the last element, or`null`if this set is empty |

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
open fun reversed(): NavigableSet<E>!
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

This method is equivalent to [descendingSet](../java/util/NavigableSet.md)).

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a reverse-ordered view of this collection, as a`NavigableSet` |

### subSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subSet(
    fromElement: E, 
    fromInclusive: Boolean, 
    toElement: E, 
    toInclusive: Boolean
): NavigableSet<E>!
```

Returns a view of the portion of this set whose elements range from`fromElement`to`toElement`. If`fromElement`and`toElement`are equal, the returned set is empty unless`fromInclusive`and`toInclusive`are both true. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromElement` | E:low endpoint of the returned set |
| `fromInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the low endpoint is to be included in the returned view |
| `toElement` | E:high endpoint of the returned set |
| --- | --- |
| `toInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the high endpoint is to be included in the returned view |

| Return ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`and`toElement`cannot be compared to one another using this set's comparator (or, if the set has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromElement`or`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range. |
| --- | --- |

### subSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subSet(
    fromElement: E, 
    toElement: E
): SortedSet<E>!
```

Returns a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive. (If`fromElement`and`toElement`are equal, the returned set is empty.) The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

Equivalent to`subSet(fromElement, true, toElement, false)`.

| Parameters ||
|---------------|-------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`and`toElement`cannot be compared to one another using this set's comparator (or, if the set has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromElement`or`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range |
| --- | --- |

### tailSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tailSet(fromElement: E): SortedSet<E>!
```

Returns a view of the portion of this set whose elements are greater than or equal to`fromElement`. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

Equivalent to`tailSet(fromElement, true)`.

| Parameters ||
|---------------|------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`fromElement`lies outside the bounds of the range |
| --- | --- |

### tailSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun tailSet(
    fromElement: E, 
    inclusive: Boolean
): NavigableSet<E>!
```

Returns a view of the portion of this set whose elements are greater than (or equal to, if`inclusive`is true)`fromElement`. The returned set is backed by this set, so changes in the returned set are reflected in this set, and vice-versa. The returned set supports all optional set operations that this set supports.

The returned set will throw an`IllegalArgumentException`on an attempt to insert an element outside its range.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromElement` | E:low endpoint of the returned set |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the low endpoint is to be included in the returned view |

| Return ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null and this set does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`fromElement`lies outside the bounds of the range |
| --- | --- |
