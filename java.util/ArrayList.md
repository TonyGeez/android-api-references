# ArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayList

```
open class ArrayList<E : Any!> : AbstractList<E>, Cloneable, RandomAccess, Serializable, MutableList<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java/util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractList](../java/util/AbstractList.md)\<E\> ||
| | | ↳ | [java.util.ArrayList](../java/util/ArrayList.md) |
| --- | --- | --- | --- |

Resizable-array implementation of the`List`interface. Implements all optional list operations, and permits all elements, including`null`. In addition to implementing the`List`interface, this class provides methods to manipulate the size of the array that is used internally to store the list. (This class is roughly equivalent to`Vector`, except that it is unsynchronized.)

The`size`,`isEmpty`,`get`,`set`,`iterator`, and`listIterator`operations run in constant time. The`add`operation runs in*amortized constant time* , that is, adding n elements requires O(n) time. All of the other operations run in linear time (roughly speaking). The constant factor is low compared to that for the`LinkedList`implementation.

Each`ArrayList`instance has a*capacity*. The capacity is the size of the array used to store the elements in the list. It is always at least as large as the list size. As elements are added to an ArrayList, its capacity grows automatically. The details of the growth policy are not specified beyond the fact that adding an element has constant amortized time cost.

An application can increase the capacity of an`ArrayList`instance before adding a large number of elements using the`ensureCapacity`operation. This may reduce the amount of incremental reallocation.

**Note that this implementation is not synchronized.** If multiple threads access an`ArrayList`instance concurrently, and at least one of the threads modifies the list structurally, it*must* be synchronized externally. (A structural modification is any operation that adds or deletes one or more elements, or explicitly resizes the backing array; merely setting the value of an element is not a structural modification.) This is typically accomplished by synchronizing on some object that naturally encapsulates the list. If no such object exists, the list should be "wrapped" using the [Collections.synchronizedList](../java/util/Collections.md))method. This is best done at creation time, to prevent accidental unsynchronized access to the list: 

```kotlin
List list = Collections.synchronizedList(new ArrayList(...));
```

The iterators returned by this class's #iterator() and [listIterator](../java/util/ArrayList.md))methods are*fail-fast* : if the list is structurally modified at any time after the iterator is created, in any way except through the iterator's own [remove](../java/util/ListIterator.md))or [add](../java/util/ListIterator.md))methods, the iterator will throw a [ConcurrentModificationException](../java/util/ConcurrentModificationException.md). Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw`ConcurrentModificationException`on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness:*the fail-fast behavior of iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ArrayList](../java/util/ArrayList.md))`()` Constructs an empty list with an initial capacity of ten. |
| [ArrayList](../java/util/ArrayList.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs an empty list with the specified initial capacity. |
| [ArrayList](../java/util/ArrayList.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>`)` Constructs a list containing the elements of the specified collection, in the order they are returned by the collection's iterator. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java/util/ArrayList.md))`(`element:` `E`)` Appends the specified element to the end of this list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](../java/util/ArrayList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Inserts the specified element at the specified position in this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java/util/ArrayList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Inserts all of the elements in the specified collection into this list, starting at the specified position. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java/util/ArrayList.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's Iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](../java/util/ArrayList.md))`(`element:` `E`)` Adds an element as the first element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](../java/util/ArrayList.md))`(`element:` `E`)` Adds an element as the last element of this collection (optional operation). |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../java/util/ArrayList.md))`()` Removes all of the elements from this list. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [clone](../java/util/ArrayList.md))`()` Returns a shallow copy of this`ArrayList`instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/ArrayList.md))`(`element:` `E`)` Returns`true`if this list contains the specified element. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/ArrayList.md))`(`element:` `E`)` Returns`true`if this list contains the specified element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [ensureCapacity](../java/util/ArrayList.md))`(`minCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Increases the capacity of this`ArrayList`instance, if necessary, to ensure that it can hold at least the number of elements specified by the minimum capacity argument. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/util/ArrayList.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares the specified object with this list for equality. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](../java/util/ArrayList.md))`(`action:` ` [Consumer](../java/util/function/Consumer.md)<in` `E>`)` <br /> |
| openE | [get](../java/util/ArrayList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the element at the specified position in this list. |
| openE | [getFirst](../java/util/ArrayList.md))`()` Gets the first element of this collection. |
| --- | --- |
| openE | [getLast](../java/util/ArrayList.md))`()` Gets the last element of this collection. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/util/ArrayList.md))`()` Returns the hash code value for this list. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../java/util/ArrayList.md))`(`element:` `E`)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](../java/util/ArrayList.md))`(`element:` `E`)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/ArrayList.md))`()` Returns`true`if this list contains no elements. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](../java/util/ArrayList.md))`()` Returns an iterator over the elements in this list in proper sequence. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](../java/util/ArrayList.md))`(`element:` `E`)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](../java/util/ArrayList.md))`(`element:` `E`)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](../java/util/ArrayList.md))`()` Returns a list iterator over the elements in this list (in proper sequence). |
| --- | --- |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](../java/util/ArrayList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/ArrayList.md))`(`element:` `E`)` Removes the first occurrence of the specified element from this list, if it is present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/ArrayList.md))`(`element:` `E`)` Removes the first occurrence of the specified element from this list, if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../java/util/ArrayList.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Removes from this list all of its elements that are contained in the specified collection. |
| openE | [removeAt](../java/util/ArrayList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes the element at the specified position in this list. |
| openE | [removeFirst](../java/util/ArrayList.md))`()` Removes and returns the first element of this collection (optional operation). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](../java/util/ArrayList.md))`(`filter:` ` [Predicate](../java/util/function/Predicate.md)<in` `E>`)` <br /> |
| openE | [removeLast](../java/util/ArrayList.md))`()` Removes and returns the last element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [replaceAll](../java/util/ArrayList.md))`(`operator:` ` [UnaryOperator](../java/util/function/UnaryOperator.md)<E>`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java/util/ArrayList.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Retains only the elements in this list that are contained in the specified collection. |
| openE | [set](../java/util/ArrayList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Replaces the element at the specified position in this list with the specified element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sort](../java/util/ArrayList.md))`(`c:` ` [Comparator](../java/util/Comparator.md)<in` `E>?`)` <br /> |
| --- | --- |
| open [Spliterator](../java/util/Spliterator.md)\<E\> | [spliterator](../java/util/ArrayList.md))`()` Creates a* [late-binding](../java/util/Spliterator.md)* and*fail-fast* [Spliterator](../java/util/Spliterator.md) over the elements in this list. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | [subList](../java/util/ArrayList.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a view of the portion of this list between the specified`fromIndex`, inclusive, and`toIndex`, exclusive. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](../java/util/ArrayList.md))`()` Returns an array containing all of the elements in this list in proper sequence (from first to last element). |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](../java/util/ArrayList.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [trimToSize](../java/util/ArrayList.md))`()` Trims the capacity of this`ArrayList`instance to be the list's current size. |

| Protected methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeRange](../java/util/ArrayList.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes from this list all of the elements whose index is between`fromIndex`, inclusive, and`toIndex`, exclusive. |

| Inherited functions ||
|---|---|
| From class [AbstractCollection](../java/util/AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](../java/util/SequencedCollection.md), processing of its elements generally occurs in that order. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java/util/AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java/util/AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java/util/AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java/util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java/util/AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java/lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java/util/AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/util/AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java/lang/String.md)). <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/ArrayList.md) Returns the number of elements in this list. |

| Inherited properties ||
|---|---|
| From class [AbstractList](../java/util/AbstractList.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [modCount](../java/util/AbstractList.md) <br /> The number of times this list has been*structurally modified*. Structural modifications are those that change the size of the list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results. This field is used by the iterator and list iterator implementation returned by the`iterator`and`listIterator`methods. If the value of this field changes unexpectedly, the iterator (or list iterator) will throw a`ConcurrentModificationException`in response to the`next`,`remove`,`previous`,`set`or`add`operations. This provides*fail-fast*behavior, rather than non-deterministic behavior in the face of concurrent modification during iteration. **Use of this field by subclasses is optional.** If a subclass wishes to provide fail-fast iterators (and list iterators), then it merely has to increment this field in its`add(int, E)`and`remove(int)`methods (and any other methods that it overrides that result in structural modifications to the list). A single call to`add(int, E)`or`remove(int)`must add no more than one to this field, or the iterators (and list iterators) will throw bogus`ConcurrentModificationExceptions`. If an implementation does not wish to provide fail-fast iterators, this field may be ignored. <br /> | ||
| From class [AbstractCollection](../java/util/AbstractCollection.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java/util/AbstractCollection.md) <br /> | ||

## Public constructors

### ArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayList()
```

Constructs an empty list with an initial capacity of ten. 

### ArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayList(initialCapacity: Int)
```

Constructs an empty list with the specified initial capacity.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity of the list |

| Exceptions ||
|--------------------------------------|-----------------------------------------------|
| `java.lang.IllegalArgumentException` | if the specified initial capacity is negative |

### ArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ArrayList(c: MutableCollection<out E>)
```

Constructs a list containing the elements of the specified collection, in the order they are returned by the collection's iterator.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>:the collection whose elements are to be placed into this list |

| Exceptions ||
|----------------------------------|-------------------------------------|
| `java.lang.NullPointerException` | if the specified collection is null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Appends the specified element to the end of this list.

| Parameters ||
|-----|-------------------------------------|
| `e` | element to be appended to this list |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](../java/util/Collection.md))) |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this list |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(
    index: Int, 
    element: E
): Unit
```

Inserts the specified element at the specified position in this list. Shifts the element currently at that position (if any) and any subsequent elements to the right (adds one to their indices).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which the specified element is to be inserted |
| `element` | E:element to be inserted |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(
    index: Int, 
    elements: Collection<E>
): Boolean
```

Inserts all of the elements in the specified collection into this list, starting at the specified position. Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in the list in the order that they are returned by the specified collection's iterator.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which to insert the first element from the specified collection |
| `c` | collection containing elements to be added to this list |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's Iterator. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this list, and this list is nonempty.)

| Parameters ||
|-----|---------------------------------------------------------|
| `c` | collection containing elements to be added to this list |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |

### addFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addFirst(element: E): Unit
```

Adds an element as the first element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the first element in encounter order.

| Parameters ||
|-----|-------------------------|
| `e` | the element to be added |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### addLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun addLast(element: E): Unit
```

Adds an element as the last element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the last element in encounter order.

| Parameters ||
|-----|--------------------------|
| `e` | the element to be added. |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this list. The list will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this list |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any
```

Returns a shallow copy of this`ArrayList`instance. (The elements themselves are not copied.)

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a clone of this`ArrayList`instance |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E): Boolean
```

Returns`true`if this list contains the specified element. More formally, returns`true`if and only if this list contains at least one element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|-----------------------------------------------------|
| `o` | element whose presence in this list is to be tested |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list contains the specified element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E): Boolean
```

Returns`true`if this list contains the specified element. More formally, returns`true`if and only if this list contains at least one element`e`such that`Objects.equals(o, e)`.

| Parameters ||
|-----|-----------------------------------------------------|
| `o` | element whose presence in this list is to be tested |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list contains the specified element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### ensureCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun ensureCapacity(minCapacity: Int): Unit
```

Increases the capacity of this`ArrayList`instance, if necessary, to ensure that it can hold at least the number of elements specified by the minimum capacity argument.

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------|
| `minCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the desired minimum capacity |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this list for equality. Returns`true`if and only if the specified object is also a list, both lists have the same size, and all corresponding pairs of elements in the two lists are*equal* . (Two elements`e1`and`e2`are*equal* if`(e1==null ? e2==null : e1.equals(e2))`.) In other words, two lists are defined to be equal if they contain the same elements in the same order.

| Parameters ||
|-------|-------------------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | the object to be compared for equality with this list |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the specified object is equal to this list |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: Consumer<in E>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java/util/function/Consumer.md)\<inE\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(index: Int): E
```

Returns the element at the specified position in this list.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to return |

| Return ||
|---|----------------------------------------------------|
| E | the element at the specified position in this list |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

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

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns the hash code value for this list.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the hash code value for this list |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun indexOf(element: E): Int
```

Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun indexOf(element: E): Int
```

Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this list contains no elements.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this list in proper sequence.

The returned iterator is [*fail-fast*](../java/util/ArrayList.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this list in proper sequence |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastIndexOf(element: E): Int
```

Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun lastIndexOf(element: E): Int
```

Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|-----|-----------------------|
| `o` | element to search for |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun listIterator(): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence).

The returned list iterator is [*fail-fast*](../java/util/ArrayList.md).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence) |

**See Also**

- [#listIterator(int)](../java/util/ArrayList.md)) 

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. The specified index indicates the first element that would be returned by an initial call to [next](../java/util/ListIterator.md)). An initial call to [previous](../java/util/ListIterator.md))would return the element with the specified index minus one.

The returned list iterator is [*fail-fast*](../java/util/ArrayList.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the first element to be returned from the list iterator (by a call to [next](../java/util/ListIterator.md))) |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E): Boolean
```

Removes the first occurrence of the specified element from this list, if it is present. If the list does not contain the element, it is unchanged. More formally, removes the element with the lowest index`i`such that`Objects.equals(o, get(i))`(if such an element exists). Returns`true`if this list contained the specified element (or equivalently, if this list changed as a result of the call).

| Parameters ||
|-----|--------------------------------------------------|
| `o` | element to be removed from this list, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list contained the specified element |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| --- | --- |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E): Boolean
```

Removes the first occurrence of the specified element from this list, if it is present. If the list does not contain the element, it is unchanged. More formally, removes the element with the lowest index`i`such that`Objects.equals(o, get(i))`(if such an element exists). Returns`true`if this list contained the specified element (or equivalently, if this list changed as a result of the call).

| Parameters ||
|-----|--------------------------------------------------|
| `o` | element to be removed from this list, if present |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list contained the specified element |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

Removes from this list all of its elements that are contained in the specified collection.

| Parameters ||
|-----|-------------------------------------------------------------|
| `c` | collection containing elements to be removed from this list |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list changed as a result of the call |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of this list is incompatible with the specified collection ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if this list contains a null element and the specified collection does not permit null elements ([optional](../java/util/Collection.md)), or if the specified collection is null |
| --- | --- |

**See Also**

- [java.util.Collection#contains(Object)](../java/util/Collection.md)) 

### removeAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAt(index: Int): E
```

Removes the element at the specified position in this list. Shifts any subsequent elements to the left (subtracts one from their indices).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the element to be removed |

| Return ||
|---|--------------------------------------------|
| E | the element that was removed from the list |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

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

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](../java/util/function/Predicate.md)\<inE\>:a predicate which returns`true`for elements to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements were removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if elements cannot be removed from this collection. Implementations may throw this exception if a matching element cannot be removed or if, in general, removal is not supported. |

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

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun replaceAll(operator: UnaryOperator<E>): Unit
```

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `operator` | [UnaryOperator](../java/util/function/UnaryOperator.md)\<E\>:the operator to apply to each element |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if this list is unmodifiable. Implementations may throw this exception if an element cannot be replaced or if, in general, modification is not supported |
| `java.lang.NullPointerException` | if the specified operator is null or if the operator result is a null value and this list does not permit null elements ([optional](../java/util/Collection.md)) |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainAll(elements: Collection<E>): Boolean
```

Retains only the elements in this list that are contained in the specified collection. In other words, removes from this list all of its elements that are not contained in the specified collection.

| Parameters ||
|-----|------------------------------------------------------------|
| `c` | collection containing elements to be retained in this list |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list changed as a result of the call |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`retainAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of this list is incompatible with the specified collection ([optional](../java/util/Collection.md)) |
| `java.lang.NullPointerException` | if this list contains a null element and the specified collection does not permit null elements ([optional](../java/util/Collection.md)), or if the specified collection is null |
| --- | --- |

**See Also**

- [java.util.Collection#contains(Object)](../java/util/Collection.md)) 

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    index: Int, 
    element: E
): E
```

Replaces the element at the specified position in this list with the specified element.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to replace |
| `element` | E:element to be stored at the specified position |

| Return ||
|---|--------------------------------------------------|
| E | the element previously at the specified position |

| Exceptions ||
|-------------------------------------------|-------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`set`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### sort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sort(c: Comparator<in E>?): Unit
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [Comparator](../java/util/Comparator.md)\<inE\>?:the`Comparator`used to compare list elements. A`null`value indicates that the elements' [natural ordering](../java/lang/Comparable.md) should be used |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the list contains elements that are not*mutually comparable*using the specified comparator |
| `java.lang.UnsupportedOperationException` | if the list's list-iterator does not support the`set`operation |
| `java.lang.IllegalArgumentException` | ([optional](../java/util/Collection.md)) if the comparator is found to violate the [Comparator](../java/util/Comparator.md) contract |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](../java/util/Spliterator.md)* and*fail-fast* [Spliterator](../java/util/Spliterator.md) over the elements in this list.

The`Spliterator`reports [Spliterator.SIZED](../java/util/Spliterator.md), [Spliterator.SUBSIZED](../java/util/Spliterator.md), and [Spliterator.ORDERED](../java/util/Spliterator.md). Overriding implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|----------------------------------------------|
| [Spliterator](../java/util/Spliterator.md)<E> | a`Spliterator`over the elements in this list |

### subList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subList(
    fromIndex: Int, 
    toIndex: Int
): MutableList<E>
```

Returns a view of the portion of this list between the specified`fromIndex`, inclusive, and`toIndex`, exclusive. (If`fromIndex``toIndex`are equal, the returned list is empty.) The returned list is backed by this list, so non-structural changes in the returned list are reflected in this list, and vice-versa. The returned list supports all of the optional list operations.

This method eliminates the need for explicit range operations (of the sort that commonly exist for arrays). Any operation that expects a list can be used as a range operation by passing a subList view instead of a whole list. For example, the following idiom removes a range of elements from a list: 

```kotlin
list.subList(from, to).clear();
  
```
Similar idioms may be constructed for [indexOf(java.lang.Object)](../java/util/ArrayList.md))and [lastIndexOf(java.lang.Object)](../java/util/ArrayList.md)), and all of the algorithms in the [Collections](../java/util/Collections.md) class can be applied to a subList.

The semantics of the list returned by this method become undefined if the backing list (i.e., this list) is*structurally modified*in any way other than via the returned list. (Structural modifications are those that change the size of this list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):low endpoint (inclusive) of the subList |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):high endpoint (exclusive) of the subList |

| Return ||
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<E> | a view of the specified range within this list |

| Exceptions ||
|---------------------------------------|-------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if an endpoint index value is out of range`(fromIndex < 0 || toIndex > size)` |
| `java.lang.IllegalArgumentException` | if the endpoint indices are out of order`(fromIndex > toIndex)` |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element).

The returned array will be "safe" in that no references to it are maintained by this list. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all of the elements in this list in proper sequence |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the list fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this list.

If the list fits in the specified array with room to spare (i.e., the array has more elements than the list), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of the list*only*if the caller knows that the list does not contain any null elements.)

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of the list are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing the elements of the list |

| Exceptions ||
|----------------------------------|-----------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this list |
| `java.lang.NullPointerException` | if the specified array is null |

### trimToSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun trimToSize(): Unit
```

Trims the capacity of this`ArrayList`instance to be the list's current size. An application can use this operation to minimize the storage of an`ArrayList`instance.

## Protected methods

### removeRange

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun removeRange(
    fromIndex: Int, 
    toIndex: Int
): Unit
```

Removes from this list all of the elements whose index is between`fromIndex`, inclusive, and`toIndex`, exclusive. Shifts any succeeding elements to the left (reduces their index). This call shortens the list by`(toIndex - fromIndex)`elements. (If`toIndex==fromIndex`, this operation has no effect.)

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of first element to be removed |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index after last element to be removed |

| Exceptions ||
|---------------------------------------|------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if`fromIndex`or`toIndex`is out of range (`fromIndex < 0 || toIndex > size() || toIndex < fromIndex`) |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of elements in this list.

| Return ||
|----------------------------------------------------------------------------|-------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this list |
