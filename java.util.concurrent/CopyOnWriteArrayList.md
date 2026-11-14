Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CopyOnWriteArrayList

```
open class CopyOnWriteArrayList<E : Any!> : Cloneable, MutableList<E>, RandomAccess, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.CopyOnWriteArrayList](CopyOnWriteArrayList.md) |

A thread-safe variant of `https://developer.android.com/reference/kotlin/java/util/ArrayList.html#` in which all mutative operations (`add`, `set`, and so on) are implemented by making a fresh copy of the underlying array.

This is ordinarily too costly, but may be *more* efficient than alternatives when traversal operations vastly outnumber mutations, and is useful when you cannot or don't want to synchronize traversals, yet need to preclude interference among concurrent threads. The "snapshot" style iterator method uses a reference to the state of the array at the point that the iterator was created. This array never changes during the lifetime of the iterator, so interference is impossible and the iterator is guaranteed not to throw `ConcurrentModificationException`. The iterator will not reflect additions, removals, or changes to the list since the iterator was created. Element-changing operations on iterators themselves (`remove`, `set`, and `add`) are not supported. These methods throw `UnsupportedOperationException`.

All elements are permitted, including `null`.

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a `CopyOnWriteArrayList` [*happen-before*](_package.md) actions subsequent to the access or removal of that element from the `CopyOnWriteArrayList` in another thread.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#CopyOnWriteArrayList()()` Creates an empty list. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#CopyOnWriteArrayList(kotlin.Array)(toCopyIn: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<E>)` Creates a list holding a copy of the given array. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#CopyOnWriteArrayList(kotlin.collections.MutableCollection)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out E>)` Creates a list containing the elements of the specified collection, in the order they are returned by the collection's iterator. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#add(java.util.concurrent.CopyOnWriteArrayList.E)(element: E)` Appends the specified element to the end of this list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#add(kotlin.Int,%20java.util.concurrent.CopyOnWriteArrayList.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, element: E)` Inserts the specified element at the specified position in this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addAll(kotlin.Int,%20kotlin.collections.Collection)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Inserts all of the elements in the specified collection into this list, starting at the specified position. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addAllAbsent(kotlin.collections.MutableCollection)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out E>)` Appends all of the elements in the specified collection that are not already contained in this list, to the end of this list, in the order that they are returned by the specified collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addFirst(java.util.concurrent.CopyOnWriteArrayList.E)(e: E)` Adds an element as the first element of this collection (optional operation). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addIfAbsent(java.util.concurrent.CopyOnWriteArrayList.E)(e: E)` Appends the element, if not present. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addLast(java.util.concurrent.CopyOnWriteArrayList.E)(e: E)` Adds an element as the last element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#clear()()` Removes all of the elements from this list. |
| --- | --- |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#clone()()` Returns a shallow copy of this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#contains(java.util.concurrent.CopyOnWriteArrayList.E)(element: E?)` Returns `true` if this list contains the specified element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#containsAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Returns `true` if this list contains all of the elements of the specified collection. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this list for equality. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#forEach(java.util.function.Consumer)(action: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<in E>)` <br /> |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#get(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the element at the specified position in this list. |
| --- | --- |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#getFirst()()` Gets the first element of this collection. |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#getLast()()` Gets the last element of this collection. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#hashCode()()` Returns the hash code value for this list. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#indexOf(java.util.concurrent.CopyOnWriteArrayList.E,%20kotlin.Int)(e: E?, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index of the first occurrence of the specified element in this list, searching forwards from `index`, or returns -1 if the element is not found. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#indexOf(java.util.concurrent.CopyOnWriteArrayList.E)(element: E?)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#isEmpty()()` Returns `true` if this list contains no elements. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#iterator()()` Returns an iterator over the elements in this list in proper sequence. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#lastIndexOf(java.util.concurrent.CopyOnWriteArrayList.E,%20kotlin.Int)(e: E?, index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the index of the last occurrence of the specified element in this list, searching backwards from `index`, or returns -1 if the element is not found. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#lastIndexOf(java.util.concurrent.CopyOnWriteArrayList.E)(element: E?)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| --- | --- |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#listIterator()()` Returns a list iterator over the elements in this list (in proper sequence). |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#listIterator(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#remove(java.util.concurrent.CopyOnWriteArrayList.E)(element: E?)` Removes the first occurrence of the specified element from this list, if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#removeAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Removes from this list all of its elements that are contained in the specified collection. |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#removeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the element at the specified position in this list. |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#removeFirst()()` Removes and returns the first element of this collection (optional operation). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#removeIf(java.util.function.Predicate)(filter: https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<in E>)` <br /> |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#removeLast()()` Removes and returns the last element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#replaceAll(java.util.function.UnaryOperator)(operator: https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator.html#<E>)` Replaces each element of this list with the result of applying the operator to that element (optional operation). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#retainAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Retains only the elements in this list that are contained in the specified collection. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#reversed()()` Returns a reverse-ordered [view](../java/util/concurrent/Collection.md) of this collection. |
| open E | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#set(kotlin.Int,%20java.util.concurrent.CopyOnWriteArrayList.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, element: E)` Replaces the element at the specified position in this list with the specified element. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#sort(java.util.Comparator)(c: https://developer.android.com/reference/kotlin/java/util/Comparator.html#<in E>?)` Sorts this list according to the order induced by the specified `https://developer.android.com/reference/kotlin/java/util/Comparator.html#` (optional operation). |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#spliterator()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this list. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#subList(kotlin.Int,%20kotlin.Int)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, toIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a view of the portion of this list between `fromIndex`, inclusive, and `toIndex`, exclusive. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#toArray()()` Returns an array containing all of the elements in this list in proper sequence (from first to last element). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#toString()()` Returns a string representation of this list. |
| --- | --- |

| Properties ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#size:kotlin.Int` Returns the number of elements in this list. |

## Public constructors

### CopyOnWriteArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CopyOnWriteArrayList()
```

Creates an empty list.

### CopyOnWriteArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CopyOnWriteArrayList(toCopyIn: Array<E>)
```

Creates a list holding a copy of the given array.

| Parameters ||
|---|---|
| `toCopyIn` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<E\>: the array (a copy of this array is used as the internal array) |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified array is null |

### CopyOnWriteArrayList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CopyOnWriteArrayList(c: MutableCollection<out E>)
```

Creates a list containing the elements of the specified collection, in the order they are returned by the collection's iterator.

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>: the collection of initially held elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified collection is null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(element: E): Boolean
```

Appends the specified element to the end of this list.

| Parameters ||
|---|---|
| `e` | element to be appended to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Collection.html#add(java.util.Collection.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this list |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this list |

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
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index at which the specified element is to be inserted |
| `element` | E: element to be inserted |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| --- | --- | --- | --- |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this list |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(
    index: Int, 
    elements: Collection<E>
): Boolean
```

Inserts all of the elements in the specified collection into this list, starting at the specified position. Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in this list in the order that they are returned by the specified collection's iterator.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index at which to insert the first element from the specified collection |
| `c` | collection containing elements to be added to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| --- | --- | --- | --- |
| `java.lang.NullPointerException` | if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this list |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#add(kotlin.Int,%20java.util.concurrent.CopyOnWriteArrayList.E)`

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator.

| Parameters ||
|---|---|
| `c` | collection containing elements to be added to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this list |

**See Also**

### addAllAbsent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAllAbsent(c: MutableCollection<out E>): Int
```

Appends all of the elements in the specified collection that are not already contained in this list, to the end of this list, in the order that they are returned by the specified collection's iterator.

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>: collection containing elements to be added to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements added |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified collection is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/concurrent/CopyOnWriteArrayList#addIfAbsent(java.util.concurrent.CopyOnWriteArrayList.E)`

### addFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFirst(e: E): Unit
```

Adds an element as the first element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the first element in encounter order.

| Parameters ||
|---|---|
| `e` | E: the element to be added |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### addIfAbsent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addIfAbsent(e: E): Boolean
```

Appends the element, if not present.

| Parameters ||
|---|---|
| `e` | E: element to be added to this list, if absent |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the element was added |

### addLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLast(e: E): Unit
```

Adds an element as the last element of this collection (optional operation). After this operation completes normally, the given element will be a member of this collection, and it will be the last element in encounter order.

| Parameters ||
|---|---|
| `e` | E: the element to be added. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all of the elements from this list. The list will be empty after this call returns.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this list |

### clone

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clone(): Any
```

Returns a shallow copy of this list. (The elements themselves are not copied.)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a clone of this list |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(element: E?): Boolean
```

Returns `true` if this list contains the specified element. More formally, returns `true` if and only if this list contains at least one element `e` such that `Objects.equals(o, e)`.

| Parameters ||
|---|---|
| `o` | element whose presence in this list is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list contains the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/concurrent/Collection.md)) |

### containsAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun containsAll(elements: Collection<E>): Boolean
```

Returns `true` if this list contains all of the elements of the specified collection.

| Parameters ||
|---|---|
| `c` | collection to be checked for containment in this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list contains all of the elements of the specified collection |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this list ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.NullPointerException` | if the specified collection is null |

**See Also**

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
```

Compares the specified object with this list for equality. Returns `true` if the specified object is the same object as this object, or if it is also a `https://developer.android.com/reference/kotlin/java/util/List.html#` and the sequence of elements returned by an java.util.List#iterator() over the specified list is the same as the sequence returned by an iterator over this list. The two sequences are considered to be the same if they have the same length and corresponding elements at the same position in the sequence are *equal* . Two elements `e1` and `e2` are considered *equal* if `Objects.equals(e1, e2)`.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | the object to be compared for equality with this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the specified object is equal to this list |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: Consumer<in E>): Unit
```

| Parameters ||
|---|---|
| `action` | [Consumer](../java.util.function/Consumer.md)\<in E\>: The action to be performed for each element |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun get(index: Int): E
```

Returns the element at the specified position in this list.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the element to return |

| Return ||
|---|---|
| `E` | the element at the specified position in this list |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |

### getFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFirst(): E
```

Gets the first element of this collection.

| Return ||
|---|---|
| `E` | the retrieved element |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this collection is empty |

### getLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLast(): E
```

Gets the last element of this collection.

| Return ||
|---|---|
| `E` | the retrieved element |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this collection is empty |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns the hash code value for this list.

This implementation uses the definition in java.util.List#hashCode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the hash code value for this list |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOf(
    e: E?, 
    index: Int
): Int
```

Returns the index of the first occurrence of the specified element in this list, searching forwards from `index`, or returns -1 if the element is not found. More formally, returns the lowest index `i` such that `i >= index && Objects.equals(get(i), e)`, or -1 if there is no such index.

| Parameters ||
|---|---|
| `e` | E?: element to search for |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index to start searching from |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the element in this list at position `index` or later in the list; `-1` if the element is not found. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the specified index is negative |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOf(element: E?): Int
```

Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index `i` such that `Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|---|---|
| `o` | element to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/concurrent/Collection.md)) |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this list contains no elements.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this list in proper sequence.

The returned iterator provides a snapshot of the state of the list when the iterator was constructed. No synchronization is needed while traversing the iterator. The iterator does *NOT* support the `remove` method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this list in proper sequence |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastIndexOf(
    e: E?, 
    index: Int
): Int
```

Returns the index of the last occurrence of the specified element in this list, searching backwards from `index`, or returns -1 if the element is not found. More formally, returns the highest index `i` such that `i <= index && Objects.equals(get(i), e)`, or -1 if there is no such index.

| Parameters ||
|---|---|
| `e` | E?: element to search for |
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index to start searching backwards from |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the element at position less than or equal to `index` in this list; -1 if the element is not found. |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the specified index is greater than or equal to the current size of this list |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastIndexOf(element: E?): Int
```

Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index `i` such that `Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|---|---|
| `o` | element to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/concurrent/Collection.md)) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listIterator(): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence).

The returned iterator provides a snapshot of the state of the list when the iterator was constructed. No synchronization is needed while traversing the iterator. The iterator does *NOT* support the `remove`, `set` or `add` methods.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html<E>` | a list iterator over the elements in this list (in proper sequence) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. The specified index indicates the first element that would be returned by an initial call to `https://developer.android.com/reference/kotlin/java/util/ListIterator.html#next()`. An initial call to `https://developer.android.com/reference/kotlin/java/util/ListIterator.html#previous()` would return the element with the specified index minus one.

The returned iterator provides a snapshot of the state of the list when the iterator was constructed. No synchronization is needed while traversing the iterator. The iterator does *NOT* support the `remove`, `set` or `add` methods.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the first element to be returned from the list iterator (by a call to `https://developer.android.com/reference/kotlin/java/util/ListIterator.html#next()`) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html<E>` | a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(element: E?): Boolean
```

Removes the first occurrence of the specified element from this list, if it is present. If this list does not contain the element, it is unchanged. More formally, removes the element with the lowest index `i` such that `Objects.equals(o, get(i))` (if such an element exists). Returns `true` if this list contained the specified element (or equivalently, if this list changed as a result of the call).

| Parameters ||
|---|---|
| `o` | element to be removed from this list, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this list |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAll(elements: Collection<E>): Boolean
```

Removes from this list all of its elements that are contained in the specified collection. This is a particularly expensive operation in this class because of the need for an internal temporary array.

| Parameters ||
|---|---|
| `c` | collection containing elements to be removed from this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this list is incompatible with the specified collection ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if this list contains a null element and the specified collection does not permit null elements ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)), or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `removeAll` operation is not supported by this list |
| --- | --- |

**See Also**

### removeAt

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAt(index: Int): E
```

Removes the element at the specified position in this list. Shifts any subsequent elements to the left (subtracts one from their indices). Returns the element that was removed from the list.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the index of the element to be removed |

| Return ||
|---|---|
| `E` | the element previously at the specified position |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this list |

### removeFirst

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeFirst(): E
```

Removes and returns the first element of this collection (optional operation).

| Return ||
|---|---|
| `E` | the removed element |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this collection is empty |

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

| Parameters ||
|---|---|
| `filter` | [Predicate](../java.util.function/Predicate.md)\<in E\>: a predicate which returns `true` for elements to be removed |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if any elements were removed |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if the `removeIf` operation is not supported by this collection |

### removeLast

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLast(): E
```

Removes and returns the last element of this collection (optional operation).

| Return ||
|---|---|
| `E` | the removed element |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this collection is empty |

### replaceAll

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun replaceAll(operator: UnaryOperator<E>): Unit
```

Replaces each element of this list with the result of applying the operator to that element (optional operation). Errors or runtime exceptions thrown by the operator are relayed to the caller.

| Parameters ||
|---|---|
| `operator` | [UnaryOperator](../java.util.function/UnaryOperator.md)\<E\>: the operator to apply to each element |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified operator is null or if the operator result is a null value and this list does not permit null elements ([optional](../java/util/concurrent/Collection.md)) |
| `java.lang.UnsupportedOperationException` | if the `replaceAll` operation is not supported by this list |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun retainAll(elements: Collection<E>): Boolean
```

Retains only the elements in this list that are contained in the specified collection. In other words, removes from this list all of its elements that are not contained in the specified collection.

| Parameters ||
|---|---|
| `c` | collection containing elements to be retained in this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this list is incompatible with the specified collection ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if this list contains a null element and the specified collection does not permit null elements ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)), or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `retainAll` operation is not supported by this list |
| --- | --- |

**See Also**

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reversed(): MutableList<E>
```

Returns a reverse-ordered [view](../java/util/concurrent/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

Modifications to the reversed view are permitted and will be propagated to this list. In addition, modifications to this list will be visible in the reversed view. Sublists and iterators of the reversed view have the same restrictions as those of this list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a reverse-ordered view of this collection, as a `List` |

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
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the element to replace |
| `element` | E: element to be stored at the specified position |

| Return ||
|---|---|
| `E` | the element previously at the specified position |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index >= size()`) |
| --- | --- | --- | --- |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `set` operation is not supported by this list |

### sort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sort(c: Comparator<in E>?): Unit
```

Sorts this list according to the order induced by the specified `https://developer.android.com/reference/kotlin/java/util/Comparator.html#` (optional operation). The sort is *stable*: this method must not reorder equal elements.

All elements in this list must be *mutually comparable* using the specified comparator (that is, `c.compare(e1, e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the list).

If the specified comparator is `null` then all elements in this list must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface and the elements' [natural ordering](../java.lang/Comparable.md) should be used.

This list must be modifiable, but need not be resizable.

For apps running on and targeting Android versions greater than Nougat (API level `> 25`), `https://developer.android.com/reference/kotlin/java/util/Collections.html#sort(kotlin.collections.MutableList)` delegates to this method. Such apps must not call `https://developer.android.com/reference/kotlin/java/util/Collections.html#sort(kotlin.collections.MutableList)` from this method. Instead, prefer not overriding this method at all. If you must override it, consider this implementation:

```kotlin
@Override
  public void sort(Comparator<? super E> c) {
    Object[] elements = toArray();
    Arrays.sort(elements, c);
    ListIterator<E> iterator = (ListIterator<Object>) listIterator();
    for (Object element : elements) {
      iterator.next();
      iterator.set((E) element);
    }
  }
  
```

| Parameters ||
|---|---|
| `c` | [Comparator](../java.util/Comparator.md)\<in E\>?: the `Comparator` used to compare list elements. A `null` value indicates that the elements' [natural ordering](../java.lang/Comparable.md) should be used |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the list contains elements that are not *mutually comparable* using the specified comparator |
| `java.lang.IllegalArgumentException` | ([optional](../java/util/concurrent/Collection.md)) if the comparator is found to violate the `https://developer.android.com/reference/kotlin/java/util/Comparator.html#` contract |
| `java.lang.UnsupportedOperationException` | if the `sort` operation is not supported by this list |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun spliterator(): Spliterator<E>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this list.

The `Spliterator` reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#IMMUTABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#SIZED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#SUBSIZED:kotlin.Int`.

The spliterator provides a snapshot of the state of the list when the spliterator was constructed. No synchronization is needed while operating on the spliterator.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#<E>` | a `Spliterator` over the elements in this list |

### subList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun subList(
    fromIndex: Int, 
    toIndex: Int
): MutableList<E>
```

Returns a view of the portion of this list between `fromIndex`, inclusive, and `toIndex`, exclusive. The returned list is backed by this list, so changes in the returned list are reflected in this list.

The semantics of the list returned by this method become undefined if the backing list (i.e., this list) is modified in any way other than via the returned list.

| Parameters ||
|---|---|
| `fromIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): low endpoint (inclusive) of the subList |
| `toIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): high endpoint (exclusive) of the subList |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a view of the specified range within this list |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | for an illegal endpoint index value (`fromIndex < 0 || toIndex > size || fromIndex > toIndex`) |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element).

The returned array will be "safe" in that no references to it are maintained by this list. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | an array containing all the elements in this list |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the list fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this list.

If this list fits in the specified array with room to spare (i.e., the array has more elements than this list), the element in the array immediately following the end of the list is set to `null`. (This is useful in determining the length of this list *only* if the caller knows that this list does not contain any null elements.)

Like the #toArray() method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose `x` is a list known to contain only strings. The following code can be used to dump the list into a newly allocated array of `String`:

```kotlin
<code>String[] y = x.toArray(new String[0]);</code>
```
Note that `toArray(new Object[0])` is identical in function to `toArray()`.

| Parameters ||
|---|---|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array into which the elements of the list are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | an array containing all the elements in this list |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this list |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of this list. The string representation consists of the string representations of the list's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of this list |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of elements in this list.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this list |
