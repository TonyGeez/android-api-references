# HashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HashSet

```
open class HashSet<E : Any!> : AbstractSet<E>, Cloneable, Serializable, MutableSet<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractSet](AbstractSet.md)\<E\> ||
| | | ↳ | [java.util.HashSet](HashSet.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [LinkedHashSet](LinkedHashSet.md) |-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------| | [LinkedHashSet](LinkedHashSet.md) | Hash table and linked list implementation of the`Set`interface, with well-defined encounter order. | |
| --- | --- | --- | --- | --- | --- | --- |

This class implements the`Set`interface, backed by a hash table (actually a`HashMap`instance). It makes no guarantees as to the iteration order of the set; in particular, it does not guarantee that the order will remain constant over time. This class permits the`null`element.

This class offers constant time performance for the basic operations (`add`,`remove`,`contains`and`size`), assuming the hash function disperses the elements properly among the buckets. Iterating over this set requires time proportional to the sum of the`HashSet`instance's size (the number of elements) plus the "capacity" of the backing`HashMap`instance (the number of buckets). Thus, it's very important not to set the initial capacity too high (or the load factor too low) if iteration performance is important.

**Note that this implementation is not synchronized.** If multiple threads access a hash set concurrently, and at least one of the threads modifies the set, it*must* be synchronized externally. This is typically accomplished by synchronizing on some object that naturally encapsulates the set. If no such object exists, the set should be "wrapped" using the [Collections.synchronizedSet](Collections.md))method. This is best done at creation time, to prevent accidental unsynchronized access to the set: 

```kotlin
Set s = Collections.synchronizedSet(new HashSet(...));
```

The iterators returned by this class's`iterator`method are*fail-fast* : if the set is modified at any time after the iterator is created, in any way except through the iterator's own`remove`method, the Iterator throws a [ConcurrentModificationException](ConcurrentModificationException.md). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HashSet](HashSet.md))`()` Constructs a new, empty set; the backing`HashMap`instance has default initial capacity (16) and load factor (0.75). |
| [HashSet](HashSet.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a new, empty set; the backing`HashMap`instance has the specified initial capacity and default load factor (0.75). |
| [HashSet](HashSet.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `loadFactor:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructs a new, empty set; the backing`HashMap`instance has the specified initial capacity and the specified load factor. |
| [HashSet](HashSet.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>`)` Constructs a new set containing the elements in the specified collection. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](HashSet.md))`(`element:` `E`)` Adds the specified element to this set if it is not already present. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](HashSet.md))`()` Removes all of the elements from this set. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](HashSet.md))`()` Returns a shallow copy of this`HashSet`instance: the elements themselves are not cloned. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](HashSet.md))`(`element:` `E`)` Returns`true`if this set contains the specified element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](HashSet.md))`(`element:` `E`)` Returns`true`if this set contains the specified element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](HashSet.md))`()` Returns`true`if this set contains no elements. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](HashSet.md))`()` Returns an iterator over the elements in this set. |
| openstatic [HashSet](HashSet.md)\<T\> | [newHashSet](HashSet.md))`(`numElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new, empty HashSet suitable for the expected number of elements. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](HashSet.md))`(`element:` `E`)` Removes the specified element from this set if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](HashSet.md))`(`element:` `E`)` Removes the specified element from this set if it is present. |
| open [Spliterator](Spliterator.md)\<E\> | [spliterator](HashSet.md))`()` Creates a* [late-binding](Spliterator.md)* and*fail-fast* [Spliterator](Spliterator.md) over the elements in this set. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](HashSet.md))`()` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](HashSet.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](AbstractCollection.md))`(`element:` `E`)` <br /> Ensures that this collection contains the specified element (optional operation). Returns`true`if this collection changed as a result of the call. (Returns`false`if this collection does not permit duplicates and already contains the specified element.) Collections that support this operation may place limitations on what elements may be added to this collection. In particular, some collections will refuse to add`null`elements, and others will impose restrictions on the type of elements that may be added. Collection classes should clearly specify in their documentation any restrictions on what elements may be added. If a collection refuses to add a particular element for any reason other than that it already contains the element, it*must* throw an exception (rather than returning`false`). This preserves the invariant that a collection always contains the specified element after this call returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](SequencedCollection.md), processing of its elements generally occurs in that order. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](AbstractCollection.md))`()` <br /> Removes all of the elements from this collection (optional operation). The collection will be empty after this method returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||
| From class [AbstractSet](AbstractSet.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AbstractSet.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares the specified object with this set for equality. Returns`true`if the given object is also a set, the two sets have the same size, and every member of the given set is contained in this set. This ensures that the`equals`method works properly across different implementations of the`Set`interface. This implementation first checks if the specified object is this set; if so it returns`true`. Then, it checks if the specified object is a set whose size is identical to the size of this set; if not, it returns false. If so, it returns`containsAll((Collection) o)`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AbstractSet.md))`()` <br /> Returns the hash code value for this set. The hash code of a set is defined to be the sum of the hash codes of the elements in the set, where the hash code of a`null`element is defined to be zero. This ensures that`s1.equals(s2)`implies that`s1.hashCode()==s2.hashCode()`for any two sets`s1`and`s2`, as required by the general contract of [Object.hashCode](../java.lang/Object.md)). This implementation iterates over the set, calling the`hashCode`method on each element in the set, and adding up the results. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](AbstractSet.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes from this set all of its elements that are contained in the specified collection (optional operation). If the specified collection is also a set, this operation effectively modifies this set so that its value is the*asymmetric set difference*of the two sets. This implementation determines which is the smaller of this set and the specified collection, by invoking the`size`method on each. If this set has fewer elements, then the implementation iterates over this set, checking each element returned by the iterator in turn to see if it is contained in the specified collection. If it is so contained, it is removed from this set with the iterator's`remove`method. If the specified collection has fewer elements, then the implementation iterates over the specified collection, removing from this set each element returned by the iterator, using this set's`remove`method. Note that this implementation will throw an`UnsupportedOperationException`if the iterator returned by the`iterator`method does not implement the`remove`method. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](HashSet.md) Returns the number of elements in this set (its cardinality). |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](AbstractCollection.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](AbstractCollection.md) <br /> | ||

## Public constructors

### HashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HashSet()
```

Constructs a new, empty set; the backing`HashMap`instance has default initial capacity (16) and load factor (0.75). 

### HashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HashSet(initialCapacity: Int)
```

Constructs a new, empty set; the backing`HashMap`instance has the specified initial capacity and default load factor (0.75).

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the hash table |

| Exceptions ||
|--------------------------------------|-------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero |

### HashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HashSet(
    initialCapacity: Int, 
    loadFactor: Float)
```

Constructs a new, empty set; the backing`HashMap`instance has the specified initial capacity and the specified load factor.

| Parameters ||
|-------------------|-----------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the hash map |
| `loadFactor` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the load factor of the hash map |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the initial capacity is less than zero, or if the load factor is nonpositive |

### HashSet

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HashSet(c: MutableCollection<out E>)
```

Constructs a new set containing the elements in the specified collection. The`HashMap`is created with default load factor (0.75) and an initial capacity sufficient to contain the elements in the specified collection.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>:the collection whose elements are to be placed into this set |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the specified collection is null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Adds the specified element to this set if it is not already present. More formally, adds the specified element`e`to this set if this set contains no element`e2`such that`Objects.equals(e, e2)`. If this set already contains the element, the call leaves the set unchanged and returns`false`.

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

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this set. The set will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|--------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`method is not supported by this set |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a shallow copy of this`HashSet`instance: the elements themselves are not cloned.

| Return ||
|----------------------------------------------------------------------------|----------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a shallow copy of this set |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E): Boolean
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

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E): Boolean
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

Returns an iterator over the elements in this set. The elements are returned in no particular order.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an Iterator over the elements in this set |

**See Also**

- [java.util.ConcurrentModificationException](ConcurrentModificationException.md) 

### newHashSet

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun <T : Any!> newHashSet(numElements: Int): HashSet<T>
```

Creates a new, empty HashSet suitable for the expected number of elements. The returned set uses the default load factor of 0.75, and its initial capacity is generally large enough so that the expected number of elements can be added without resizing the set.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------|
| `numElements` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the expected number of elements |
| `<T>` | the type of elements maintained by the new set |

| Return ||
|---------------------------------------------------------------------------------|-----------------------|
| [HashSet](HashSet.md)<T> | the newly created set |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if numElements is negative |

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
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the set contained the specified element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this set ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements ([optional](Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this set |
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
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the set contained the specified element |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this set ([optional](Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this set does not permit null elements ([optional](Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this set |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](Spliterator.md)* and*fail-fast* [Spliterator](Spliterator.md) over the elements in this set.

The`Spliterator`reports [Spliterator.SIZED](Spliterator.md) and [Spliterator.DISTINCT](Spliterator.md). Overriding implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------|
| [Spliterator](Spliterator.md)<E> | a`Spliterator`over the elements in this set |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all the elements in this set |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

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
open val size: Int
```

Returns the number of elements in this set (its cardinality).

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this set (its cardinality) |
