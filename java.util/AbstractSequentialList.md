# AbstractSequentialList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AbstractSequentialList

```
abstract class AbstractSequentialList<E : Any!> : AbstractList<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractList](AbstractList.md)\<E\> ||
| | | ↳ | [java.util.AbstractSequentialList](AbstractSequentialList.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [LinkedList](LinkedList.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------| | [LinkedList](LinkedList.md) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | |
| --- | --- | --- | --- | --- | --- | --- |

This class provides a skeletal implementation of the`List`interface to minimize the effort required to implement this interface backed by a "sequential access" data store (such as a linked list). For random access data (such as an array),`AbstractList`should be used in preference to this class.

This class is the opposite of the`AbstractList`class in the sense that it implements the "random access" methods (`get(int index)`,`set(int index, E element)`,`add(int index, E element)`and`remove(int index)`) on top of the list's list iterator, instead of the other way around.

To implement a list the programmer needs only to extend this class and provide implementations for the`listIterator`and`size`methods. For an unmodifiable list, the programmer need only implement the list iterator's`hasNext`,`next`,`hasPrevious`,`previous`and`index`methods.

For a modifiable list the programmer should additionally implement the list iterator's`set`method. For a variable-size list the programmer should additionally implement the list iterator's`remove`and`add`methods.

The programmer should generally provide a void (no argument) and collection constructor, as per the recommendation in the`Collection`interface specification.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Protected constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AbstractSequentialList](AbstractSequentialList.md))`()` Sole constructor. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](AbstractSequentialList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Inserts the specified element at the specified position in this list (optional operation). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](AbstractSequentialList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Inserts all of the elements in the specified collection into this list at the specified position (optional operation). |
| openE | [get](AbstractSequentialList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the element at the specified position in this list. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](AbstractSequentialList.md))`()` Returns an iterator over the elements in this list (in proper sequence). |
| abstract [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | [listIterator](AbstractSequentialList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a list iterator over the elements in this list (in proper sequence). |
| openE | [removeAt](AbstractSequentialList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes the element at the specified position in this list (optional operation). |
| --- | --- |
| openE | [set](AbstractSequentialList.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `element:` `E`)` Replaces the element at the specified position in this list with the specified element (optional operation). |

| Inherited functions ||
|---|---|
| From class [AbstractList](AbstractList.md) |-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](AbstractList.md))`(`element:` `E`)` <br /> Appends the specified element to the end of this list (optional operation). Lists that support this operation may place limitations on what elements may be added to this list. In particular, some lists will refuse to add null elements, and others will impose restrictions on the type of elements that may be added. List classes should clearly specify in their documentation any restrictions on what elements may be added. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](AbstractList.md))`()` <br /> Removes all of the elements from this list (optional operation). The list will be empty after this call returns. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](AbstractList.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> Compares the specified object with this list for equality. Returns`true`if and only if the specified object is also a list, both lists have the same size, and all corresponding pairs of elements in the two lists are*equal* . (Two elements`e1`and`e2`are*equal* if`(e1==null ? e2==null : e1.equals(e2))`.) In other words, two lists are defined to be equal if they contain the same elements in the same order. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](AbstractList.md))`()` <br /> Returns the hash code value for this list. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [indexOf](AbstractList.md))`(`element:` `E?`)` <br /> Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lastIndexOf](AbstractList.md))`(`element:` `E?`)` <br /> Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index`i`such that`Objects.equals(o, get(i))`, or -1 if there is no such index. <br /> | | [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | [listIterator](AbstractList.md))`()` <br /> Returns a list iterator over the elements in this list (in proper sequence). <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeRange](AbstractList.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Removes from this list all of the elements whose index is between`fromIndex`, inclusive, and`toIndex`, exclusive. Shifts any succeeding elements to the left (reduces their index). This call shortens the list by`(toIndex - fromIndex)`elements. (If`toIndex==fromIndex`, this operation has no effect.) This method is called by the`clear`operation on this list and its subLists. Overriding this method to take advantage of the internals of the list implementation can*substantially* improve the performance of the`clear`operation on this list and its subLists. <br /> | | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<E> | [subList](AbstractList.md))`(`fromIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `toIndex:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Returns a view of the portion of this list between the specified`fromIndex`, inclusive, and`toIndex`, exclusive. (If`fromIndex``toIndex`are equal, the returned list is empty.) The returned list is backed by this list, so non-structural changes in the returned list are reflected in this list, and vice-versa. The returned list supports all of the optional list operations supported by this list. This method eliminates the need for explicit range operations (of the sort that commonly exist for arrays). Any operation that expects a list can be used as a range operation by passing a subList view instead of a whole list. For example, the following idiom removes a range of elements from a list: ```kotlin <code>list.subList(from, to).clear(); </code> ``` Similar idioms may be constructed for`indexOf`and`lastIndexOf`, and all of the algorithms in the`Collections`class can be applied to a subList. The semantics of the list returned by this method become undefined if the backing list (i.e., this list) is*structurally modified*in any way other than via the returned list. (Structural modifications are those that change the size of this list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.) <br /> | ||
| From class [AbstractCollection](AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](SequencedCollection.md), processing of its elements generally occurs in that order. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||

| Inherited properties ||
|---|---|
| From class [AbstractList](AbstractList.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [modCount](AbstractList.md) <br /> The number of times this list has been*structurally modified*. Structural modifications are those that change the size of the list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results. This field is used by the iterator and list iterator implementation returned by the`iterator`and`listIterator`methods. If the value of this field changes unexpectedly, the iterator (or list iterator) will throw a`ConcurrentModificationException`in response to the`next`,`remove`,`previous`,`set`or`add`operations. This provides*fail-fast*behavior, rather than non-deterministic behavior in the face of concurrent modification during iteration. **Use of this field by subclasses is optional.** If a subclass wishes to provide fail-fast iterators (and list iterators), then it merely has to increment this field in its`add(int, E)`and`remove(int)`methods (and any other methods that it overrides that result in structural modifications to the list). A single call to`add(int, E)`or`remove(int)`must add no more than one to this field, or the iterators (and list iterators) will throw bogus`ConcurrentModificationExceptions`. If an implementation does not wish to provide fail-fast iterators, this field may be ignored. <br /> | ||
| From class [AbstractCollection](AbstractCollection.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](AbstractCollection.md) <br /> | ||

## Protected constructors

### AbstractSequentialList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected AbstractSequentialList()
```

Sole constructor. (For invocation by subclass constructors, typically implicit.)

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(
    index: Int, 
    element: E
): Unit
```

Inserts the specified element at the specified position in this list (optional operation). Shifts the element currently at that position (if any) and any subsequent elements to the right (adds one to their indices).

This implementation first gets a list iterator pointing to the indexed element (with`listIterator(index)`). Then, it inserts the specified element with`ListIterator.add`.

Note that this implementation will throw an`UnsupportedOperationException`if the list iterator does not implement the`add`operation.

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

Inserts all of the elements in the specified collection into this list at the specified position (optional operation). Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in this list in the order that they are returned by the specified collection's iterator. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (Note that this will occur if the specified collection is this list, and it's nonempty.)

This implementation gets an iterator over the specified collection and a list iterator over this list pointing to the indexed element (with`listIterator(index)`). Then, it iterates over the specified collection, inserting the elements obtained from the iterator into this list, one at a time, using`ListIterator.add`followed by`ListIterator.next`(to skip over the added element).

Note that this implementation will throw an`UnsupportedOperationException`if the list iterator returned by the`listIterator`method does not implement the`add`operation.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index at which to insert the first element from the specified collection |
| `c` | collection containing elements to be added to this list |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this list changed as a result of the call |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`addAll`operation is not supported by this list |
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this list does not permit null elements, or if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(index: Int): E
```

Returns the element at the specified position in this list.

This implementation first gets a list iterator pointing to the indexed element (with`listIterator(index)`). Then, it gets the element using`ListIterator.next`and returns it.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the element to return |

| Return ||
|---|----------------------------------------------------|
| E | the element at the specified position in this list |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this list (in proper sequence).

This implementation merely returns a list iterator over the list.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this list (in proper sequence) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of first element to be returned from the list iterator (by a call to the`next`method) |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)<E> | a list iterator over the elements in this list (in proper sequence) |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### removeAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAt(index: Int): E
```

Removes the element at the specified position in this list (optional operation). Shifts any subsequent elements to the left (subtracts one from their indices). Returns the element that was removed from the list.

This implementation first gets a list iterator pointing to the indexed element (with`listIterator(index)`). Then, it removes the element with`ListIterator.remove`.

Note that this implementation will throw an`UnsupportedOperationException`if the list iterator does not implement the`remove`operation.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the element to be removed |

| Return ||
|---|--------------------------------------------------|
| E | the element previously at the specified position |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun set(
    index: Int, 
    element: E
): E
```

Replaces the element at the specified position in this list with the specified element (optional operation).

This implementation first gets a list iterator pointing to the indexed element (with`listIterator(index)`). Then, it gets the current element using`ListIterator.next`and replaces it with`ListIterator.set`.

Note that this implementation will throw an`UnsupportedOperationException`if the list iterator does not implement the`set`operation.

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
