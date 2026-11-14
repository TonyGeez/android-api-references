# LinkedHashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkedHashSet

```
open class LinkedHashSet<E : Any!> : HashSet<E>, Cloneable, SequencedSet<E>, Serializable, MutableSet<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java/util/AbstractCollection.md)\<E\> ||||
| | ↳ | [java.util.AbstractSet](../java/util/AbstractSet.md)\<E\> |||
| | | ↳ | [java.util.HashSet](../java/util/HashSet.md)\<E\> ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.LinkedHashSet](../java/util/LinkedHashSet.md) |

Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. This implementation differs from`HashSet`in that it maintains a doubly-linked list running through all of its entries. This linked list defines the encounter order (iteration order), which is the order in which elements were inserted into the set (*insertion-order* ). The least recently inserted element (the eldest) is first, and the youngest element is last. Note that encounter order is*not* affected if an element is*re-inserted* into the set with the`add`method. (An element`e`is reinserted into a set`s`if`s.add(e)`is invoked when`s.contains(e)`would return`true`immediately prior to the invocation.) The reverse-ordered view of this set is in the opposite order, with the youngest element appearing first and the eldest element appearing last. The encounter order of elements already in the set can be changed by using the [addFirst](../java/util/LinkedHashSet.md))and [addLast](../java/util/LinkedHashSet.md))methods.

This implementation spares its clients from the unspecified, generally chaotic ordering provided by [HashSet](../java/util/HashSet.md), without incurring the increased cost associated with [TreeSet](../java/util/TreeSet.md). It can be used to produce a copy of a set that has the same order as the original, regardless of the original set's implementation: 

```kotlin
<code>void foo(Set&lt;String&gt; s) {
          Set&lt;String&gt; copy = new LinkedHashSet&lt;&gt;(s);
          ...
      }
  </code>
```
This technique is particularly useful if a module takes a set on input, copies it, and later returns results whose order is determined by that of the copy. (Clients generally appreciate having things returned in the same order they were presented.)

This class provides all of the optional [Set](../java/util/Set.md) and [SequencedSet](../java/util/SequencedSet.md) operations, and it permits null elements. Like`HashSet`, it provides constant-time performance for the basic operations (`add`,`contains`and`remove`), assuming the hash function disperses elements properly among the buckets. Performance is likely to be just slightly below that of`HashSet`, due to the added expense of maintaining the linked list, with one exception: Iteration over a`LinkedHashSet`requires time proportional to the*size* of the set, regardless of its capacity. Iteration over a`HashSet`is likely to be more expensive, requiring time proportional to its*capacity*.

A linked hash set has two parameters that affect its performance:*initial capacity* and*load factor* . They are defined precisely as for`HashSet`. Note, however, that the penalty for choosing an excessively high value for initial capacity is less severe for this class than for`HashSet`, as iteration times for this class are unaffected by capacity.

**Note that this implementation is not synchronized.** If multiple threads access a linked hash set concurrently, and at least one of the threads modifies the set, it*must* be synchronized externally. This is typically accomplished by synchronizing on some object that naturally encapsulates the set. If no such object exists, the set should be "wrapped" using the [Collections.synchronizedSet](../java/util/Collections.md))method. This is best done at creation time, to prevent accidental unsynchronized access to the set: 

```kotlin
Set s = Collections.synchronizedSet(new LinkedHashSet(...));
```

The iterators returned by this class's`iterator`method are*fail-fast* : if the set is modified at any time after the iterator is created, in any way except through the iterator's own`remove`method, the iterator will throw a [ConcurrentModificationException](../java/util/ConcurrentModificationException.md). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkedHashSet](../java/util/LinkedHashSet.md))`()` Constructs a new, empty linked hash set with the default initial capacity (16) and load factor (0.75). |
| [LinkedHashSet](../java/util/LinkedHashSet.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new, empty linked hash set with the specified initial capacity and the default load factor (0.75). |
| [LinkedHashSet](../java/util/LinkedHashSet.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loadFactor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a new, empty linked hash set with the specified initial capacity and load factor. |
| [LinkedHashSet](../java/util/LinkedHashSet.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Constructs a new linked hash set with the same elements as the specified collection. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/LinkedHashSet.md))`(`e:` `E`)` Adds an element as the first element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/LinkedHashSet.md))`(`e:` `E`)` Adds an element as the last element of this collection (optional operation). |
| openE | [getFirst](../java/util/LinkedHashSet.md))`()` Gets the first element of this collection. |
| --- | --- |
| openE | [getLast](../java/util/LinkedHashSet.md))`()` Gets the last element of this collection. |
| openstatic [LinkedHashSet](../java/util/LinkedHashSet.md)\<T\>! | [newLinkedHashSet](../java/util/LinkedHashSet.md))`(`numElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new, empty LinkedHashSet suitable for the expected number of elements. |
| openE | [removeFirst](../java/util/LinkedHashSet.md))`()` Removes and returns the first element of this collection (optional operation). |
| --- | --- |
| openE | [removeLast](../java/util/LinkedHashSet.md))`()` Removes and returns the last element of this collection (optional operation). |
| open [SequencedSet](../java/util/SequencedSet.md)\<E\>! | [reversed](../java/util/LinkedHashSet.md))`()` Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. |
| open [Spliterator](../java/util/Spliterator.md)\<E\> | [spliterator](../java/util/LinkedHashSet.md))`()` Creates a* [late-binding](../java/util/Spliterator.md)* and*fail-fast* `Spliterator`over the elements in this set. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [HashSet](../java/util/HashSet.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java/util/HashSet.md))`(`element:` `E`)` <br /> Adds the specified element to this set if it is not already present. More formally, adds the specified element`e`to this set if this set contains no element`e2`such that`Objects.equals(e, e2)`. If this set already contains the element, the call leaves the set unchanged and returns`false`. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/HashSet.md))`()` <br /> Removes all of the elements from this set. The set will be empty after this call returns. <br /> | | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/HashSet.md))`()` <br /> Returns a shallow copy of this`HashSet`instance: the elements themselves are not cloned. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/HashSet.md))`(`element:` `E`)` <br /> Returns`true`if this set contains the specified element. More formally, returns`true`if and only if this set contains an element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/HashSet.md))`()` <br /> Returns`true`if this set contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](../java/util/HashSet.md))`()` <br /> Returns an iterator over the elements in this set. The elements are returned in no particular order. <br /> | | [HashSet](../java/util/HashSet.md)<T> | [newHashSet](../java/util/HashSet.md))`(`numElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Creates a new, empty HashSet suitable for the expected number of elements. The returned set uses the default load factor of 0.75, and its initial capacity is generally large enough so that the expected number of elements can be added without resizing the set. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/HashSet.md))`(`element:` `E`)` <br /> Removes the specified element from this set if it is present. More formally, removes an element`e`such that`Objects.equals(o, e)`, if this set contains such an element. Returns`true`if this set contained the element (or equivalently, if this set changed as a result of the call). (This set will not contain the element once the call returns.) <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java/util/HashSet.md))`()` <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java/util/HashSet.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> | ||
| From class [AbstractCollection](../java/util/AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java/util/AbstractCollection.md))`(`element:` `E`)` <br /> Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.) Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added. If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](../java/util/SequencedCollection.md), processing of its elements generally occurs in that order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/AbstractCollection.md))`()` <br /> Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](../java/util/AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java/util/AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java/lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java/util/AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java/lang/String.md)). <br /> | ||
| From class [AbstractSet](../java/util/AbstractSet.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/AbstractSet.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares the specified object with this set for equality. Returns`true`if the given object is also a set, the two sets have the same size, and every member of the given set is contained in this set. This ensures that the`equals`method works properly across different implementations of the`Set`interface. This implementation first checks if the specified object is this set; if so it returns`true`. Then, it checks if the specified object is a set whose size is identical to the size of this set; if not, it returns false. If so, it returns`containsAll((Collection) o)`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/AbstractSet.md))`()` <br /> Returns the hash code value for this set. The hash code of a set is defined to be the sum of the hash codes of the elements in the set, where the hash code of a`null`element is defined to be zero. This ensures that`s1.equals(s2)`implies that`s1.hashCode()==s2.hashCode()`for any two sets`s1`and`s2`, as required by the general contract of [Object.hashCode](../java/lang/Object.md)). This implementation iterates over the set, calling the`hashCode`method on each element in the set, and adding up the results. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../java/util/AbstractSet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes from this set all of its elements that are contained in the specified collection (optional operation). If the specified collection is also a set, this operation effectively modifies this set so that its value is the*asymmetric set difference*of the two sets. This implementation determines which is the smaller of this set and the specified collection, by invoking the`size`method on each. If this set has fewer elements, then the implementation iterates over this set, checking each element returned by the iterator in turn to see if it is contained in the specified collection. If it is so contained, it is removed from this set with the iterator's`remove`method. If the specified collection has fewer elements, then the implementation iterates over the specified collection, removing from this set each element returned by the iterator, using this set's`remove`method. Note that this implementation will throw an`UnsupportedOperationException`if the iterator returned by the`iterator`method does not implement the`remove`method. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Inherited properties ||
|---|---|
| From class [HashSet](../java/util/HashSet.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/HashSet.md) <br /> Returns the number of elements in this set (its cardinality). <br /> | ||
| From class [AbstractCollection](../java/util/AbstractCollection.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/AbstractCollection.md) <br /> | ||

## Public constructors

### LinkedHashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedHashSet()
```

Constructs a new, empty linked hash set with the default initial capacity (16) and load factor (0.75). 

### LinkedHashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedHashSet(initialCapacity: Int)
```

Constructs a new, empty linked hash set with the specified initial capacity and the default load factor (0.75).

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the LinkedHashSet |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero |

### LinkedHashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedHashSet(
    initialCapacity: Int, 
    loadFactor: Float)
```

Constructs a new, empty linked hash set with the specified initial capacity and load factor.

| Parameters ||
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the linked hash set |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the load factor of the linked hash set |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero, or if the load factor is nonpositive |

### LinkedHashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedHashSet(c: MutableCollection<out E>!)
```

Constructs a new linked hash set with the same elements as the specified collection. The linked hash set is created with an initial capacity sufficient to hold the elements in the specified collection and the default load factor (0.75).

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:the collection whose elements are to be placed into this set |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the specified collection is null |

## Public methods

### addFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFirst(e: E): Unit
```

Adds an element as the first element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the first element in encounter order.

If this set already contains the element, it is relocated if necessary so that it is first in encounter order.

| Parameters ||
|-----|---------------------------|
| `e` | E:the element to be added |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### addLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLast(e: E): Unit
```

Adds an element as the last element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the last element in encounter order.

If this set already contains the element, it is relocated if necessary so that it is last in encounter order.

| Parameters ||
|-----|----------------------------|
| `e` | E:the element to be added. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

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

### newLinkedHashSet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> newLinkedHashSet(numElements: Int): LinkedHashSet<T>!
```

Creates a new, empty LinkedHashSet suitable for the expected number of elements. The returned set uses the default load factor of 0.75, and its initial capacity is generally large enough so that the expected number of elements can be added without resizing the set.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------|
| `numElements` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected number of elements |
| `<T>` | the type of elements maintained by the new set |

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------|
| [LinkedHashSet](../java/util/LinkedHashSet.md)<T>! | the newly created set |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if numElements is negative |

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
open fun reversed(): SequencedSet<E>!
```

Returns a reverse-ordered [view](../java/util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

Modifications to the reversed view are permitted and will be propagated to this set. In addition, modifications to this set will be visible in the reversed view.

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [SequencedSet](../java/util/SequencedSet.md)<E>! | a reverse-ordered view of this collection, as a`SequencedSet` |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](../java/util/Spliterator.md)* and*fail-fast* `Spliterator`over the elements in this set.

The`Spliterator`reports [Spliterator.SIZED](../java/util/Spliterator.md), [Spliterator.DISTINCT](../java/util/Spliterator.md), and`ORDERED`. Implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------|
| [Spliterator](../java/util/Spliterator.md)<E> | a`Spliterator`over the elements in this set |
