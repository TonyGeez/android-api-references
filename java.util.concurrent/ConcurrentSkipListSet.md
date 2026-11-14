# ConcurrentSkipListSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentSkipListSet

```
open class ConcurrentSkipListSet<E : Any!> : AbstractSet<E>, Cloneable, NavigableSet<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java.util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractSet](../java.util/AbstractSet.md)\<E\> ||
| | | ↳ | [java.util.concurrent.ConcurrentSkipListSet](ConcurrentSkipListSet.md) |
| --- | --- | --- | --- |

A scalable concurrent [NavigableSet](../java.util/NavigableSet.md) implementation based on a [ConcurrentSkipListMap](ConcurrentSkipListMap.md). The elements of the set are kept sorted according to their [natural ordering](../java.lang/Comparable.md), or by a [Comparator](../java.util/Comparator.md) provided at set creation time, depending on which constructor is used.

This implementation provides expected average*log(n)* time cost for the`contains`,`add`, and`remove`operations and their variants. Insertion, removal, and access operations safely execute concurrently by multiple threads.

Iterators and spliterators are [*weakly consistent*](_package.md).

Ascending ordered views and their iterators are faster than descending ones.

Beware that, unlike in most collections, the`size`method is*not*a constant-time operation. Because of the asynchronous nature of these sets, determining the current number of elements requires a traversal of the elements, and so may report inaccurate results if this collection is modified during traversal.

Bulk operations that add, remove, or examine multiple elements, such as #addAll, [removeIf](../java.util/Collection.md))or [forEach](../java.lang/Iterable.md)), are*not* guaranteed to be performed atomically. For example, a`forEach`traversal concurrent with an`addAll`operation might observe only some of the added elements.

This class and its iterators implement all of the*optional* methods of the [Set](../java.util/Set.md) and [Iterator](../java.util/Iterator.md) interfaces. Like most other concurrent collection implementations, this class does not permit the use of`null`elements, because`null`arguments and return values cannot be reliably distinguished from the absence of elements.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ConcurrentSkipListSet](ConcurrentSkipListSet.md))`()` Constructs a new, empty set that orders its elements according to their [natural ordering](../java.lang/Comparable.md). |
| [ConcurrentSkipListSet](ConcurrentSkipListSet.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Constructs a new set containing the elements in the specified collection, that orders its elements according to their [natural ordering](../java.lang/Comparable.md). |
| [ConcurrentSkipListSet](ConcurrentSkipListSet.md))`(`comparator:` ` [Comparator](../java.util/Comparator.md)<in` `E>!`)` Constructs a new, empty set that orders its elements according to the specified comparator. |
| [ConcurrentSkipListSet](ConcurrentSkipListSet.md))`(`s:` ` [SortedSet](../java.util/SortedSet.md)<E>!`)` Constructs a new set containing the same elements and using the same ordering as the specified sorted set. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](ConcurrentSkipListSet.md))`(`element:` `E`)` Adds the specified element to this set if it is not already present. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](ConcurrentSkipListSet.md))`(`e:` `E`)` Throws`UnsupportedOperationException`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](ConcurrentSkipListSet.md))`(`e:` `E`)` Throws`UnsupportedOperationException`. |
| --- | --- |
| openE | [ceiling](ConcurrentSkipListSet.md))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](ConcurrentSkipListSet.md))`()` Removes all of the elements from this set. |
| open [ConcurrentSkipListSet](ConcurrentSkipListSet.md)\<E\> | [clone](ConcurrentSkipListSet.md))`()` Returns a shallow copy of this`ConcurrentSkipListSet`instance. |
| --- | --- |
| open [Comparator](../java.util/Comparator.md)\<inE\>! | [comparator](ConcurrentSkipListSet.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](ConcurrentSkipListSet.md))`(`element:` `E?`)` Returns`true`if this set contains the specified element. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\>! | [descendingIterator](ConcurrentSkipListSet.md))`()` Returns an iterator over the elements in this set in descending order. |
| --- | --- |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [descendingSet](ConcurrentSkipListSet.md))`()` Returns a reverse order view of the elements contained in this set. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](ConcurrentSkipListSet.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this set for equality. |
| openE | [first](ConcurrentSkipListSet.md))`()` <br /> |
| --- | --- |
| openE | [floor](ConcurrentSkipListSet.md))`(`e:` `E`)` <br /> |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [headSet](ConcurrentSkipListSet.md))`(`toElement:` `E`)` <br /> |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [headSet](ConcurrentSkipListSet.md))`(`toElement:` `E`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| openE | [higher](ConcurrentSkipListSet.md))`(`e:` `E`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](ConcurrentSkipListSet.md))`()` Returns`true`if this set contains no elements. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](ConcurrentSkipListSet.md))`()` Returns an iterator over the elements in this set in ascending order. |
| --- | --- |
| openE | [last](ConcurrentSkipListSet.md))`()` <br /> |
| openE | [lower](ConcurrentSkipListSet.md))`(`e:` `E`)` <br /> |
| openE | [pollFirst](ConcurrentSkipListSet.md))`()` <br /> |
| --- | --- |
| openE | [pollLast](ConcurrentSkipListSet.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](ConcurrentSkipListSet.md))`(`element:` `E?`)` Removes the specified element from this set if it is present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](ConcurrentSkipListSet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Removes from this set all of its elements that are contained in the specified collection. |
| --- | --- |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | [spliterator](ConcurrentSkipListSet.md))`()` Returns a [Spliterator](../java.util/Spliterator.md) over the elements in this set. |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [subSet](ConcurrentSkipListSet.md))`(`fromElement:` `E`, `fromInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `toElement:` `E`, `toInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [subSet](ConcurrentSkipListSet.md))`(`fromElement:` `E`, `toElement:` `E`)` <br /> |
| --- | --- |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [tailSet](ConcurrentSkipListSet.md))`(`fromElement:` `E`)` <br /> |
| open [NavigableSet](../java.util/NavigableSet.md)\<E\>! | [tailSet](ConcurrentSkipListSet.md))`(`fromElement:` `E`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](../java.util/AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java.util/AbstractCollection.md))`(`element:` `E`)` <br /> Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.) Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added. If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](../java.util/SequencedCollection.md), processing of its elements generally occurs in that order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java.util/AbstractCollection.md))`()` <br /> Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java.util/AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java.util/AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](../java.util/AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java.util/AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java.util/AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java.util/AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||
| From class [SortedSet](../java.util/SortedSet.md) |--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java.util/SortedSet.md))`(`e:` `E`)` <br /> Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java.util/SortedSet.md))`(`e:` `E`)` <br /> Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported. <br /> | | [Comparator](../java.util/Comparator.md)<in` `E>! | [comparator](../java.util/SortedSet.md))`()` <br /> Returns the comparator used to order the elements in this set, or`null`if this set uses the [natural ordering](../java.lang/Comparable.md) of its elements. <br /> | | E | [first](../java.util/SortedSet.md))`()` <br /> Returns the first (lowest) element currently in this set. <br /> | | E | [getFirst](../java.util/SortedSet.md))`()` <br /> Gets the first element of this collection. <br /> | | E | [getLast](../java.util/SortedSet.md))`()` <br /> Gets the last element of this collection. <br /> | | E | [last](../java.util/SortedSet.md))`()` <br /> Returns the last (highest) element currently in this set. <br /> | | [Spliterator](../java.util/Spliterator.md)<E> | [spliterator](../java.util/SortedSet.md))`()` <br /> Creates a`Spliterator`over the elements in this sorted set. The`Spliterator`reports [Spliterator.DISTINCT](../java.util/Spliterator.md), [Spliterator.SORTED](../java.util/Spliterator.md) and [Spliterator.ORDERED](../java.util/Spliterator.md). Implementations should document the reporting of additional characteristic values. The spliterator's comparator (see [java.util.Spliterator#getComparator()](../java.util/Spliterator.md))) must be`null`if the sorted set's comparator (see [comparator()](../java.util/SortedSet.md))) is`null`. Otherwise, the spliterator's comparator must be the same as or impose the same total ordering as the sorted set's comparator. <br /> | ||
| From class [AbstractSet](../java.util/AbstractSet.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java.util/AbstractSet.md))`()` <br /> Returns the hash code value for this set. The hash code of a set is defined to be the sum of the hash codes of the elements in the set, where the hash code of a`null`element is defined to be zero. This ensures that`s1.equals(s2)`implies that`s1.hashCode()==s2.hashCode()`for any two sets`s1`and`s2`, as required by the general contract of [Object.hashCode](../java.lang/Object.md)). This implementation iterates over the set, calling the`hashCode`method on each element in the set, and adding up the results. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |
| From class [NavigableSet](../java.util/NavigableSet.md) |-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [removeFirst](../java.util/NavigableSet.md))`()` <br /> Removes and returns the first element of this collection (optional operation). <br /> | | E | [removeLast](../java.util/NavigableSet.md))`()` <br /> Removes and returns the last element of this collection (optional operation). <br /> | | [NavigableSet](../java.util/NavigableSet.md)<E>! | [reversed](../java.util/NavigableSet.md))`()` <br /> Returns a reverse-ordered [view](../java.util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation. This method is equivalent to [descendingSet](../java.util/NavigableSet.md)). <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](ConcurrentSkipListSet.md) Returns the number of elements in this set. |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](../java.util/AbstractCollection.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java.util/AbstractCollection.md) <br /> | ||

## Public constructors

### ConcurrentSkipListSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentSkipListSet()
```

Constructs a new, empty set that orders its elements according to their [natural ordering](../java.lang/Comparable.md). 

### ConcurrentSkipListSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentSkipListSet(c: MutableCollection<out E>!)
```

Constructs a new set containing the elements in the specified collection, that orders its elements according to their [natural ordering](../java.lang/Comparable.md).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:The elements that will comprise the new set |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the elements in`c`are not [Comparable](../java.lang/Comparable.md), or are not mutually comparable |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

### ConcurrentSkipListSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentSkipListSet(comparator: Comparator<in E>!)
```

Constructs a new, empty set that orders its elements according to the specified comparator.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java.util/Comparator.md)\<inE\>!:the comparator that will be used to order this set. If`null`, the [ordering](../java.lang/Comparable.md) of the elements will be used. |

### ConcurrentSkipListSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ConcurrentSkipListSet(s: SortedSet<E>!)
```

Constructs a new set containing the same elements and using the same ordering as the specified sorted set.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [SortedSet](../java.util/SortedSet.md)\<E\>!:sorted set whose elements will comprise the new set |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified sorted set or any of its elements are null |

## Public methods

### add

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Adds the specified element to this set if it is not already present. More formally, adds the specified element`e`to this set if the set contains no element`e2`such that`e.equals(e2)`. If this set already contains the element, the call leaves the set unchanged and returns`false`.

| Parameters ||
|-----|---------------------------------|
| `e` | element to be added to this set |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set did not already contain the specified element |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if`e`cannot be compared with the elements currently in this set |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the element prevents it from being added to this collection |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

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

### ceiling

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ceiling(e: E): E
```

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------------------|
| E | the least element greater than or equal to`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null |

### clear

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this set.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### clone

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): ConcurrentSkipListSet<E>
```

Returns a shallow copy of this`ConcurrentSkipListSet`instance. (The elements themselves are not cloned.)

| Return ||
|------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [ConcurrentSkipListSet](ConcurrentSkipListSet.md)<E> | a shallow copy of this set |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### comparator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun comparator(): Comparator<in E>!
```

| Return ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Comparator](../java.util/Comparator.md)<in` `E>! | the comparator used to order the elements in this set, or`null`if this set uses the natural ordering of its elements |

### contains

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E?): Boolean
```

Returns`true`if this set contains the specified element. More formally, returns`true`if and only if this set contains an element`e`such that`o.equals(e)`.

| Parameters ||
|-----|--------------------------------------------------|
| `o` | object to be checked for containment in this set |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains the specified element |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in this set |
| `java.lang.NullPointerException` | if the specified element is null |

### descendingIterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun descendingIterator(): MutableIterator<E>!
```

Returns an iterator over the elements in this set in descending order.

| Return ||
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E>! | an iterator over the elements in this set in descending order |

### descendingSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun descendingSet(): NavigableSet<E>!
```

Returns a reverse order view of the elements contained in this set. The descending set is backed by this set, so changes to the set are reflected in the descending set, and vice-versa.

The returned set has an ordering equivalent to [Collections.reverseOrder](../java.util/Collections.md))`(comparator())`. The expression`s.descendingSet().descendingSet()`returns a view of`s`essentially equivalent to`s`.

| Return ||
|-------------------------------------------------------------------------------------------------|----------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a reverse order view of this set |

### equals

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this set for equality. Returns`true`if the specified object is also a set, the two sets have the same size, and every member of the specified set is contained in this set (or equivalently, every member of this set is contained in the specified set). This definition ensures that the equals method works properly across different implementations of the set interface.

| Parameters ||
|-------|------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the object to be compared for equality with this set |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this set |

### first

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun first(): E
```

| Return ||
|---|--------------------------------------------------|
| E | the first (lowest) element currently in this set |

| Exceptions ||
|------------------------------------|----------------------|
| `java.util.NoSuchElementException` | if this set is empty |

### floor

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun floor(e: E): E
```

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------------------|
| E | the greatest element less than or equal to`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null |

### headSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun headSet(toElement: E): NavigableSet<E>!
```

| Parameters ||
|-------------|-------------------------------------------------|
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are strictly less than`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`toElement`lies outside the bounds of the range |
| --- | --- |

### headSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun headSet(
    toElement: E, 
    inclusive: Boolean
): NavigableSet<E>!
```

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `toElement` | E:high endpoint of the returned set |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the high endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are less than (or equal to, if`inclusive`is true)`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`toElement`lies outside the bounds of the range |
| --- | --- |

### higher

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun higher(e: E): E
```

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------|
| E | the least element greater than`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null |

### isEmpty

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this set contains no elements.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains no elements |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this set in ascending order.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this set in ascending order |

### last

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun last(): E
```

| Return ||
|---|--------------------------------------------------|
| E | the last (highest) element currently in this set |

| Exceptions ||
|------------------------------------|----------------------|
| `java.util.NoSuchElementException` | if this set is empty |

### lower

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lower(e: E): E
```

| Parameters ||
|-----|----------------------|
| `e` | E:the value to match |

| Return ||
|---|------------------------------------------------------------------------|
| E | the greatest element less than`e`, or`null`if there is no such element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollFirst(): E
```

| Return ||
|---|-------------------------------------------------|
| E | the first element, or`null`if this set is empty |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pollLast(): E
```

| Return ||
|---|------------------------------------------------|
| E | the last element, or`null`if this set is empty |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes the specified element from this set if it is present. More formally, removes an element`e`such that`o.equals(e)`, if this set contains such an element. Returns`true`if this set contained the element (or equivalently, if this set changed as a result of the call). (This set will not contain the element once the call returns.)

| Parameters ||
|-----|------------------------------------------------|
| `o` | object to be removed from this set, if present |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contained the specified element |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------|
| `java.lang.ClassCastException` | if`o`cannot be compared with the elements currently in this set |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

Removes from this set all of its elements that are contained in the specified collection. If the specified collection is also a set, this operation effectively modifies this set so that its value is the*asymmetric set difference*of the two sets.

| Parameters ||
|-----|------------------------------------------------------------|
| `c` | collection containing elements to be removed from this set |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`operation is not supported by this set |
| `java.lang.ClassCastException` | if the class of an element of this set is incompatible with the specified collection ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Returns a [Spliterator](../java.util/Spliterator.md) over the elements in this set.

The`Spliterator`reports [Spliterator.CONCURRENT](../java.util/Spliterator.md), [Spliterator.NONNULL](../java.util/Spliterator.md), [Spliterator.DISTINCT](../java.util/Spliterator.md), [Spliterator.SORTED](../java.util/Spliterator.md) and [Spliterator.ORDERED](../java.util/Spliterator.md), with an encounter order that is ascending order. Overriding implementations should document the reporting of additional characteristic values.

The [spliterator's comparator](../java.util/Spliterator.md))is`null`if the [set's comparator](ConcurrentSkipListSet.md))is`null`. Otherwise, the spliterator's comparator is the same as or imposes the same total ordering as the set's comparator.

| Return ||
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| [Spliterator](../java.util/Spliterator.md)<E> | a`Spliterator`over the elements in this set |

### subSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subSet(
    fromElement: E, 
    fromInclusive: Boolean, 
    toElement: E, 
    toInclusive: Boolean
): NavigableSet<E>!
```

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromElement` | E:low endpoint of the returned set |
| `fromInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the low endpoint is to be included in the returned view |
| `toElement` | E:high endpoint of the returned set |
| --- | --- |
| `toInclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the high endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`and`toElement`cannot be compared to one another using this set's comparator (or, if the set has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromElement`or`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range. |
| --- | --- |

### subSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subSet(
    fromElement: E, 
    toElement: E
): NavigableSet<E>!
```

| Parameters ||
|---------------|-------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`and`toElement`cannot be compared to one another using this set's comparator (or, if the set has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromElement`or`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range |
| --- | --- |

### tailSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tailSet(fromElement: E): NavigableSet<E>!
```

| Parameters ||
|---------------|------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`fromElement`lies outside the bounds of the range |
| --- | --- |

### tailSet

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tailSet(
    fromElement: E, 
    inclusive: Boolean
): NavigableSet<E>!
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `fromElement` | E:low endpoint of the returned set |
| `inclusive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the low endpoint is to be included in the returned view |

| Return ||
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [NavigableSet](../java.util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java.lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`fromElement`lies outside the bounds of the range |
| --- | --- |

## Properties

### size

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of elements in this set. If this set contains more than`Integer.MAX_VALUE`elements, it returns`Integer.MAX_VALUE`.

Beware that, unlike in most collections, this method is*NOT*a constant-time operation. Because of the asynchronous nature of these sets, determining the current number of elements requires traversing them all to count them. Additionally, it is possible for the size to change during execution of this method, in which case the returned result will be inaccurate. Thus, this method is typically not very useful in concurrent applications.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this set |
