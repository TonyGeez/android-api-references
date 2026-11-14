# TreeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TreeSet

```
open class TreeSet<E : Any!> : AbstractSet<E>, Cloneable, NavigableSet<E>, Serializable, MutableSet<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java/util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractSet](../java/util/AbstractSet.md)\<E\> ||
| | | ↳ | [java.util.TreeSet](../java/util/TreeSet.md) |
| --- | --- | --- | --- |

A [NavigableSet](../java/util/NavigableSet.md) implementation based on a [TreeMap](../java/util/TreeMap.md). The elements are ordered using their [ordering](../java/lang/Comparable.md), or by a [Comparator](../java/util/Comparator.md) provided at set creation time, depending on which constructor is used.

This implementation provides guaranteed log(n) time cost for the basic operations (`add`,`remove`and`contains`).

Note that the ordering maintained by a set (whether or not an explicit comparator is provided) must be*consistent with equals* if it is to correctly implement the`Set`interface. (See`Comparable`or`Comparator`for a precise definition of*consistent with equals* .) This is so because the`Set`interface is defined in terms of the`equals`operation, but a`TreeSet`instance performs all element comparisons using its`compareTo`(or`compare`) method, so two elements that are deemed equal by this method are, from the standpoint of the set, equal. The behavior of a set*is* well-defined even if its ordering is inconsistent with equals; it just fails to obey the general contract of the`Set`interface.

**Note that this implementation is not synchronized.** If multiple threads access a tree set concurrently, and at least one of the threads modifies the set, it*must* be synchronized externally. This is typically accomplished by synchronizing on some object that naturally encapsulates the set. If no such object exists, the set should be "wrapped" using the [Collections.synchronizedSortedSet](../java/util/Collections.md))method. This is best done at creation time, to prevent accidental unsynchronized access to the set: 

```kotlin
SortedSet s = Collections.synchronizedSortedSet(new TreeSet(...));
```

The iterators returned by this class's`iterator`method are*fail-fast* : if the set is modified at any time after the iterator is created, in any way except through the iterator's own`remove`method, the iterator will throw a [ConcurrentModificationException](../java/util/ConcurrentModificationException.md). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

The #addFirst and #addLast methods of this class throw`UnsupportedOperationException`. The encounter order of elements is determined by the comparison method; therefore, explicit positioning is not supported.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TreeSet](../java/util/TreeSet.md))`()` Constructs a new, empty tree set, sorted according to the natural ordering of its elements. |
| [TreeSet](../java/util/TreeSet.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Constructs a new tree set containing the elements in the specified collection, sorted according to the*natural ordering*of its elements. |
| [TreeSet](../java/util/TreeSet.md))`(`comparator:` ` [Comparator](../java/util/Comparator.md)<in` `E>!`)` Constructs a new, empty tree set, sorted according to the specified comparator. |
| [TreeSet](../java/util/TreeSet.md))`(`s:` ` [SortedSet](../java/util/SortedSet.md)<E>!`)` Constructs a new tree set containing the same elements and using the same ordering as the specified sorted set. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java/util/TreeSet.md))`(`element:` `E`)` Adds the specified element to this set if it is not already present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java/util/TreeSet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Adds all of the elements in the specified collection to this set. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/TreeSet.md))`(`e:` `E`)` Throws`UnsupportedOperationException`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/TreeSet.md))`(`e:` `E`)` Throws`UnsupportedOperationException`. |
| openE | [ceiling](../java/util/TreeSet.md))`(`e:` `E`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/TreeSet.md))`()` Removes all of the elements from this set. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/TreeSet.md))`()` Returns a shallow copy of this`TreeSet`instance. |
| open [Comparator](../java/util/Comparator.md)\<inE\>! | [comparator](../java/util/TreeSet.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/TreeSet.md))`(`element:` `E`)` Returns`true`if this set contains the specified element. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/TreeSet.md))`(`element:` `E`)` Returns`true`if this set contains the specified element. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\>! | [descendingIterator](../java/util/TreeSet.md))`()` Returns an iterator over the elements in this set in descending order. |
| open [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [descendingSet](../java/util/TreeSet.md))`()` <br /> |
| --- | --- |
| openE | [first](../java/util/TreeSet.md))`()` <br /> |
| openE | [floor](../java/util/TreeSet.md))`(`e:` `E`)` <br /> |
| open [SortedSet](../java/util/SortedSet.md)\<E\>! | [headSet](../java/util/TreeSet.md))`(`toElement:` `E`)` <br /> |
| --- | --- |
| open [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [headSet](../java/util/TreeSet.md))`(`toElement:` `E`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| openE | [higher](../java/util/TreeSet.md))`(`e:` `E`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/TreeSet.md))`()` Returns`true`if this set contains no elements. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](../java/util/TreeSet.md))`()` Returns an iterator over the elements in this set in ascending order. |
| openE | [last](../java/util/TreeSet.md))`()` <br /> |
| openE | [lower](../java/util/TreeSet.md))`(`e:` `E`)` <br /> |
| --- | --- |
| openE | [pollFirst](../java/util/TreeSet.md))`()` <br /> |
| openE | [pollLast](../java/util/TreeSet.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/TreeSet.md))`(`element:` `E`)` Removes the specified element from this set if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/TreeSet.md))`(`element:` `E`)` Removes the specified element from this set if it is present. |
| open [Spliterator](../java/util/Spliterator.md)\<E\> | [spliterator](../java/util/TreeSet.md))`()` Creates a* [late-binding](../java/util/Spliterator.md)* and*fail-fast* [Spliterator](../java/util/Spliterator.md) over the elements in this set. |
| open [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [subSet](../java/util/TreeSet.md))`(`fromElement:` `E`, `fromInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `toElement:` `E`, `toInclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |
| open [SortedSet](../java/util/SortedSet.md)\<E\>! | [subSet](../java/util/TreeSet.md))`(`fromElement:` `E`, `toElement:` `E`)` <br /> |
| open [SortedSet](../java/util/SortedSet.md)\<E\>! | [tailSet](../java/util/TreeSet.md))`(`fromElement:` `E`)` <br /> |
| open [NavigableSet](../java/util/NavigableSet.md)\<E\>! | [tailSet](../java/util/TreeSet.md))`(`fromElement:` `E`, `inclusive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](../java/util/AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java/util/AbstractCollection.md))`(`element:` `E`)` <br /> Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.) Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added. If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](../java/util/SequencedCollection.md), processing of its elements generally occurs in that order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/AbstractCollection.md))`()` <br /> Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](../java/util/AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java/util/AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java/lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java/util/AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java/lang/String.md)). <br /> | ||
| From class [SortedSet](../java/util/SortedSet.md) |--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/SortedSet.md))`(`e:` `E`)` <br /> Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/SortedSet.md))`(`e:` `E`)` <br /> Throws`UnsupportedOperationException`. The encounter order induced by this set's comparison method determines the position of elements, so explicit positioning is not supported. <br /> | | [Comparator](../java/util/Comparator.md)<in` `E>! | [comparator](../java/util/SortedSet.md))`()` <br /> Returns the comparator used to order the elements in this set, or`null`if this set uses the [natural ordering](../java/lang/Comparable.md) of its elements. <br /> | | E | [first](../java/util/SortedSet.md))`()` <br /> Returns the first (lowest) element currently in this set. <br /> | | E | [getFirst](../java/util/SortedSet.md))`()` <br /> Gets the first element of this collection. <br /> | | E | [getLast](../java/util/SortedSet.md))`()` <br /> Gets the last element of this collection. <br /> | | E | [last](../java/util/SortedSet.md))`()` <br /> Returns the last (highest) element currently in this set. <br /> | | [Spliterator](../java/util/Spliterator.md)<E> | [spliterator](../java/util/SortedSet.md))`()` <br /> Creates a`Spliterator`over the elements in this sorted set. The`Spliterator`reports [Spliterator.DISTINCT](../java/util/Spliterator.md), [Spliterator.SORTED](../java/util/Spliterator.md) and [Spliterator.ORDERED](../java/util/Spliterator.md). Implementations should document the reporting of additional characteristic values. The spliterator's comparator (see [java.util.Spliterator#getComparator()](../java/util/Spliterator.md))) must be`null`if the sorted set's comparator (see [comparator()](../java/util/SortedSet.md))) is`null`. Otherwise, the spliterator's comparator must be the same as or impose the same total ordering as the sorted set's comparator. <br /> | ||
| From class [AbstractSet](../java/util/AbstractSet.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/AbstractSet.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares the specified object with this set for equality. Returns`true`if the given object is also a set, the two sets have the same size, and every member of the given set is contained in this set. This ensures that the`equals`method works properly across different implementations of the`Set`interface. This implementation first checks if the specified object is this set; if so it returns`true`. Then, it checks if the specified object is a set whose size is identical to the size of this set; if not, it returns false. If so, it returns`containsAll((Collection) o)`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/AbstractSet.md))`()` <br /> Returns the hash code value for this set. The hash code of a set is defined to be the sum of the hash codes of the elements in the set, where the hash code of a`null`element is defined to be zero. This ensures that`s1.equals(s2)`implies that`s1.hashCode()==s2.hashCode()`for any two sets`s1`and`s2`, as required by the general contract of [Object.hashCode](../java/lang/Object.md)). This implementation iterates over the set, calling the`hashCode`method on each element in the set, and adding up the results. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../java/util/AbstractSet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes from this set all of its elements that are contained in the specified collection (optional operation). If the specified collection is also a set, this operation effectively modifies this set so that its value is the*asymmetric set difference*of the two sets. This implementation determines which is the smaller of this set and the specified collection, by invoking the`size`method on each. If this set has fewer elements, then the implementation iterates over this set, checking each element returned by the iterator in turn to see if it is contained in the specified collection. If it is so contained, it is removed from this set with the iterator's`remove`method. If the specified collection has fewer elements, then the implementation iterates over the specified collection, removing from this set each element returned by the iterator, using this set's`remove`method. Note that this implementation will throw an`UnsupportedOperationException`if the iterator returned by the`iterator`method does not implement the`remove`method. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class [NavigableSet](../java/util/NavigableSet.md) |-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [removeFirst](../java/util/NavigableSet.md))`()` <br /> Removes and returns the first element of this collection (optional operation). <br /> | | E | [removeLast](../java/util/NavigableSet.md))`()` <br /> Removes and returns the last element of this collection (optional operation). <br /> | | [NavigableSet](../java/util/NavigableSet.md)<E>! | [reversed](../java/util/NavigableSet.md))`()` <br /> Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation. This method is equivalent to [descendingSet](../java/util/NavigableSet.md)). <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/TreeSet.md) Returns the number of elements in this set (its cardinality). |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](../java/util/AbstractCollection.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/AbstractCollection.md) <br /> | ||

## Public constructors

### TreeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TreeSet()
```

Constructs a new, empty tree set, sorted according to the natural ordering of its elements. All elements inserted into the set must implement the [Comparable](../java/lang/Comparable.md) interface. Furthermore, all such elements must be*mutually comparable* :`e1.compareTo(e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the set. If the user attempts to add an element to the set that violates this constraint (for example, the user attempts to add a string element to a set whose elements are integers), the`add`call will throw a`ClassCastException`. 

### TreeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TreeSet(c: MutableCollection<out E>!)
```

Constructs a new tree set containing the elements in the specified collection, sorted according to the*natural ordering* of its elements. All elements inserted into the set must implement the [Comparable](../java/lang/Comparable.md) interface. Furthermore, all such elements must be*mutually comparable* :`e1.compareTo(e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the set.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:collection whose elements will comprise the new set |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the elements in`c`are not [Comparable](../java/lang/Comparable.md), or are not mutually comparable |
| `java.lang.NullPointerException` | if the specified collection is null |

### TreeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TreeSet(comparator: Comparator<in E>!)
```

Constructs a new, empty tree set, sorted according to the specified comparator. All elements inserted into the set must be*mutually comparable* by the specified comparator:`comparator.compare(e1, e2)`must not throw a`ClassCastException`for any elements`e1`and`e2`in the set. If the user attempts to add an element to the set that violates this constraint, the`add`call will throw a`ClassCastException`.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](../java/util/Comparator.md)\<inE\>!:the comparator that will be used to order this set. If`null`, the [ordering](../java/lang/Comparable.md) of the elements will be used. |

### TreeSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TreeSet(s: SortedSet<E>!)
```

Constructs a new tree set containing the same elements and using the same ordering as the specified sorted set.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [SortedSet](../java/util/SortedSet.md)\<E\>!:sorted set whose elements will comprise the new set |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the specified sorted set is null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Adds the specified element to this set if it is not already present. More formally, adds the specified element`e`to this set if the set contains no element`e2`such that`Objects.equals(e, e2)`. If this set already contains the element, the call leaves the set unchanged and returns`false`.

| Parameters ||
|-----|---------------------------------|
| `e` | element to be added to this set |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set did not already contain the specified element |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the specified object cannot be compared with the elements currently in this set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the element prevents it from being added to this collection |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Adds all of the elements in the specified collection to this set.

| Parameters ||
|-----|--------------------------------------------------------|
| `c` | collection containing elements to be added to this set |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set changed as a result of the call |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the elements provided cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified collection is null or if any element is null and this set uses natural ordering, or its comparator does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this collection |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

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
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this set. The set will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a shallow copy of this`TreeSet`instance. (The elements themselves are not cloned.)

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this set |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### comparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun comparator(): Comparator<in E>!
```

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Comparator](../java/util/Comparator.md)<in` `E>! | the comparator used to order the elements in this set, or`null`if this set uses the natural ordering of its elements |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E): Boolean
```

Returns`true`if this set contains the specified element. More formally, returns`true`if and only if this set contains an element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|--------------------------------------------------|
| `o` | object to be checked for containment in this set |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains the specified element |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified object cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E): Boolean
```

Returns`true`if this set contains the specified element. More formally, returns`true`if and only if this set contains an element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|--------------------------------------------------|
| `o` | object to be checked for containment in this set |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains the specified element |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified object cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |

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

| Return ||
|-------------------------------------------------------------------------------------------|----------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a reverse order view of this set |

### first

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |

### headSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun headSet(toElement: E): SortedSet<E>!
```

| Parameters ||
|-------------|-------------------------------------------------|
| `toElement` | E:high endpoint (exclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements are strictly less than`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null and this set uses natural ordering, or its comparator does not permit null elements |
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
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are less than (or equal to, if`inclusive`is true)`toElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`toElement`is not compatible with this set's comparator (or, if the set has no comparator, if`toElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`toElement`is null and this set uses natural ordering, or its comparator does not permit null elements |
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
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this set contains no elements.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this set in ascending order.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this set in ascending order |

### last

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with the elements currently in the set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E): Boolean
```

Removes the specified element from this set if it is present. More formally, removes an element`e`such that`Objects.equals(o, e)`, if this set contains such an element. Returns`true`if this set contained the element (or equivalently, if this set changed as a result of the call). (This set will not contain the element once the call returns.)

| Parameters ||
|-----|------------------------------------------------|
| `o` | object to be removed from this set, if present |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contained the specified element |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified object cannot be compared with the elements currently in this set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E): Boolean
```

Removes the specified element from this set if it is present. More formally, removes an element`e`such that`Objects.equals(o, e)`, if this set contains such an element. Returns`true`if this set contained the element (or equivalently, if this set changed as a result of the call). (This set will not contain the element once the call returns.)

| Parameters ||
|-----|------------------------------------------------|
| `o` | object to be removed from this set, if present |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this set contained the specified element |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified object cannot be compared with the elements currently in this set |
| `java.lang.NullPointerException` | if the specified element is null and this set uses natural ordering, or its comparator does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](../java/util/Spliterator.md)* and*fail-fast* [Spliterator](../java/util/Spliterator.md) over the elements in this set.

The`Spliterator`reports [Spliterator.SIZED](../java/util/Spliterator.md), [Spliterator.DISTINCT](../java/util/Spliterator.md), [Spliterator.SORTED](../java/util/Spliterator.md), and [Spliterator.ORDERED](../java/util/Spliterator.md). Overriding implementations should document the reporting of additional characteristic values.

The spliterator's comparator (see [java.util.Spliterator#getComparator()](../java/util/Spliterator.md))) is`null`if the tree set's comparator (see [comparator()](../java/util/TreeSet.md))) is`null`. Otherwise, the spliterator's comparator is the same as or imposes the same total ordering as the tree set's comparator.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------|
| [Spliterator](../java/util/Spliterator.md)<E> | a`Spliterator`over the elements in this set |

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
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a view of the portion of this set whose elements range from`fromElement`, inclusive, to`toElement`, exclusive |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`and`toElement`cannot be compared to one another using this set's comparator (or, if the set has no comparator, using natural ordering). Implementations may, but are not required to, throw this exception if`fromElement`or`toElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null and this set uses natural ordering, or its comparator does not permit null elements |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range. |
| --- | --- |

### subSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subSet(
    fromElement: E, 
    toElement: E
): SortedSet<E>!
```

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
| `java.lang.NullPointerException` | if`fromElement`or`toElement`is null and this set uses natural ordering, or its comparator does not permit null elements |
| `java.lang.IllegalArgumentException` | if`fromElement`is greater than`toElement`; or if this set itself has a restricted range, and`fromElement`or`toElement`lies outside the bounds of the range |
| --- | --- |

### tailSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tailSet(fromElement: E): SortedSet<E>!
```

| Parameters ||
|---------------|------------------------------------------------|
| `fromElement` | E:low endpoint (inclusive) of the returned set |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [SortedSet](../java/util/SortedSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null and this set uses natural ordering, or its comparator does not permit null elements |
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
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [NavigableSet](../java/util/NavigableSet.md)<E>! | a view of the portion of this set whose elements are greater than or equal to`fromElement` |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if`fromElement`is not compatible with this set's comparator (or, if the set has no comparator, if`fromElement`does not implement [Comparable](../java/lang/Comparable.md)). Implementations may, but are not required to, throw this exception if`fromElement`cannot be compared to elements currently in the set. |
| `java.lang.NullPointerException` | if`fromElement`is null and this set uses natural ordering, or its comparator does not permit null elements |
| `java.lang.IllegalArgumentException` | if this set itself has a restricted range, and`fromElement`lies outside the bounds of the range |
| --- | --- |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of elements in this set (its cardinality).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this set (its cardinality) |
