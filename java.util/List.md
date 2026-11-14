Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# List

```
interface List<E : Any!> : MutableCollection<E>, SequencedCollection<E>
```

| [java.util.List](https://developer.android.com/reference/kotlin/java/util/List#) |

An ordered collection, where the user has precise control over where in the list each element is inserted. The user can access elements by their integer index (position in the list), and search for elements in the list.

Unlike sets, lists typically allow duplicate elements. More formally, lists typically allow pairs of elements `e1` and `e2` such that `e1.equals(e2)`, and they typically allow multiple null elements if they allow null elements at all. It is not inconceivable that someone might wish to implement a list that prohibits duplicates, by throwing runtime exceptions when the user attempts to insert them, but we expect this usage to be rare.

The `List` interface places additional stipulations, beyond those specified in the `Collection` interface, on the contracts of the `iterator`, `add`, `remove`, `equals`, and `hashCode` methods. Declarations for other inherited methods are also included here for convenience.

The `List` interface provides four methods for positional (indexed) access to list elements. Lists (like Java arrays) are zero based. Note that these operations may execute in time proportional to the index value for some implementations (the `LinkedList` class, for example). Thus, iterating over the elements in a list is typically preferable to indexing through it if the caller does not know the implementation.

The `List` interface provides a special iterator, called a `ListIterator`, that allows element insertion and replacement, and bidirectional access in addition to the normal operations that the `Iterator` interface provides. A method is provided to obtain a list iterator that starts at a specified position in the list.

The `List` interface provides two methods to search for a specified object. From a performance standpoint, these methods should be used with caution. In many implementations they will perform costly linear searches.

The `List` interface provides two methods to efficiently insert and remove multiple elements at an arbitrary point in the list.

Note: While it is permissible for lists to contain themselves as elements, extreme caution is advised: the `equals` and `hashCode` methods are no longer well defined on such a list.

Some list implementations have restrictions on the elements that they may contain. For example, some implementations prohibit null elements, and some have restrictions on the types of their elements. Attempting to add an ineligible element throws an unchecked exception, typically `NullPointerException` or `ClassCastException`. Attempting to query the presence of an ineligible element may throw an exception, or it may simply return false; some implementations will exhibit the former behavior and some will exhibit the latter. More generally, attempting an operation on an ineligible element whose completion would not result in the insertion of an ineligible element into the list may throw an exception or it may succeed, at the option of the implementation. Such exceptions are marked as "optional" in the specification for this interface.

## Unmodifiable Lists

The `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E)` and `https://developer.android.com/reference/kotlin/java/util/List#copyOf(kotlin.collections.MutableCollection)` static factory methods provide a convenient way to create unmodifiable lists. The `List` instances created by these methods have the following characteristics:

- They are [*unmodifiable*](https://developer.android.com/reference/kotlin/java/util/Collection#unmodifiable). Elements cannot be added, removed, or replaced. Calling any mutator method on the List will always cause `UnsupportedOperationException` to be thrown. However, if the contained elements are themselves mutable, this may cause the List's contents to appear to change.
- They disallow `null` elements. Attempts to create them with `null` elements result in `NullPointerException`.
- They are serializable if all elements are serializable.
- The order of elements in the list is the same as the order of the provided arguments, or of the elements in the provided array.
- The lists and their `https://developer.android.com/reference/kotlin/java/util/List#subList(kotlin.Int,%20kotlin.Int)` views implement the `https://developer.android.com/reference/kotlin/java/util/RandomAccess` interface.
- They are [value-based](https://developer.android.com/reference/kotlin/java/lang/doc-files/ValueBased.html). Programmers should treat instances that are #equals(java.lang.Object) as interchangeable and should not use them for synchronization, or unpredictable behavior may occur. For example, in a future release, synchronization may fail. Callers should make no assumptions about the identity of the returned instances. Factories are free to create new instances or reuse existing ones.
- They are serialized as specified on the [Serialized Form](https://developer.android.com//serialized-form.html#java.util.CollSer) page.

## Summary

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#add(java.util.List.E)(element: E)` Appends the specified element to the end of this list (optional operation). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#add(kotlin.Int,%20java.util.List.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, element: E)` Inserts the specified element at the specified position in this list (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#addAll(kotlin.Int,%20kotlin.collections.MutableCollection)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out E>)` Inserts all of the elements in the specified collection into this list at the specified position (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#addAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#addFirst(java.util.List.E)(e: E)` Adds an element as the first element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#addLast(java.util.List.E)(e: E)` Adds an element as the last element of this collection (optional operation). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#clear()()` Removes all of the elements from this list (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#contains(java.util.List.E)(element: E?)` Returns `true` if this list contains the specified element. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#containsAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Returns `true` if this list contains all of the elements of the specified collection. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#copyOf(kotlin.collections.MutableCollection)(coll: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out E>)` Returns an [unmodifiable List](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) containing the elements of the given Collection, in its iteration order. |
| abstract E | `https://developer.android.com/reference/kotlin/java/util/List#get(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the element at the specified position in this list. |
| open E | `https://developer.android.com/reference/kotlin/java/util/List#getFirst()()` Gets the first element of this collection. |
| open E | `https://developer.android.com/reference/kotlin/java/util/List#getLast()()` Gets the last element of this collection. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#indexOf(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#isEmpty()()` Returns `true` if this list contains no elements. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#iterator()()` Returns an iterator over the elements in this list in proper sequence. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#lastIndexOf(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| abstract [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#listIterator()()` Returns a list iterator over the elements in this list (in proper sequence). |
| abstract [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#listIterator(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of()()` Returns an unmodifiable list containing zero elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E)(e1: E)` Returns an unmodifiable list containing one element. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E)` Returns an unmodifiable list containing two elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E)` Returns an unmodifiable list containing three elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E)` Returns an unmodifiable list containing four elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E, e5: E)` Returns an unmodifiable list containing five elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E, e5: E, e6: E)` Returns an unmodifiable list containing six elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E, e5: E, e6: E, e7: E)` Returns an unmodifiable list containing seven elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E, e5: E, e6: E, e7: E, e8: E)` Returns an unmodifiable list containing eight elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E, e5: E, e6: E, e7: E, e8: E, e9: E)` Returns an unmodifiable list containing nine elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E,%20java.util.List.of.E)(e1: E, e2: E, e3: E, e4: E, e5: E, e6: E, e7: E, e8: E, e9: E, e10: E)` Returns an unmodifiable list containing ten elements. |
| open static [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#of(java.util.List.of.E)(vararg elements: E)` Returns an unmodifiable list containing an arbitrary number of elements. |
| abstract E | `https://developer.android.com/reference/kotlin/java/util/List#remove(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the element at the specified position in this list (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#remove(java.util.List.E)(element: E?)` Removes the first occurrence of the specified element from this list, if it is present (optional operation). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#removeAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Removes from this list all of its elements that are contained in the specified collection (optional operation). |
| open E | `https://developer.android.com/reference/kotlin/java/util/List#removeFirst()()` Removes and returns the first element of this collection (optional operation). |
| open E | `https://developer.android.com/reference/kotlin/java/util/List#removeLast()()` Removes and returns the last element of this collection (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#replaceAll(java.util.function.UnaryOperator)(operator: https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator<E>)` Replaces each element of this list with the result of applying the operator to that element. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#retainAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Retains only the elements in this list that are contained in the specified collection (optional operation). |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#reversed()()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. |
| abstract E | `https://developer.android.com/reference/kotlin/java/util/List#set(kotlin.Int,%20java.util.List.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, element: E)` Replaces the element at the specified position in this list with the specified element (optional operation). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#sort(java.util.Comparator)(c: https://developer.android.com/reference/kotlin/java/util/Comparator<in E>?)` Sorts this list according to the order induced by the specified `https://developer.android.com/reference/kotlin/java/util/Comparator`. |
| open [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#spliterator()()` Creates a `https://developer.android.com/reference/kotlin/java/util/Spliterator` over the elements in this list. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/List#subList(kotlin.Int,%20kotlin.Int)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, toIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a view of the portion of this list between the specified `fromIndex`, inclusive, and `toIndex`, exclusive. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/List#toArray()()` Returns an array containing all of the elements in this list in proper sequence (from first to last element). |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | `https://developer.android.com/reference/kotlin/java/util/List#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. |

| Properties ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/List#size:kotlin.Int` Returns the number of elements in this list. |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun add(element: E): Boolean
```

Appends the specified element to the end of this list (optional operation).

Lists that support this operation may place limitations on what elements may be added to this list. In particular, some lists will refuse to add null elements, and others will impose restrictions on the type of elements that may be added. List classes should clearly specify in their documentation any restrictions on what elements may be added.

| Parameters ||
|---|---|
| `e` | element to be appended to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Collection#add(java.util.Collection.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this list |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to insertion restrictions |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this list |

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun add(
    index: Int, 
    element: E
): Unit
```

Inserts the specified element at the specified position in this list (optional operation). Shifts the element currently at that position (if any) and any subsequent elements to the right (adds one to their indices).

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index at which the specified element is to be inserted |
| `element` | E: element to be inserted |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this list |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addAll(
    index: Int, 
    c: MutableCollection<out E>
): Boolean
```

Inserts all of the elements in the specified collection into this list at the specified position (optional operation). Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in this list in the order that they are returned by the specified collection's iterator. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (Note that this will occur if the specified collection is this list, and it's nonempty.)

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index at which to insert the first element from the specified collection |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>: collection containing elements to be added to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this list |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this list |
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this list does not permit null elements, or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this list |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (Note that this will occur if the specified collection is this list, and it's nonempty.)

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
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this list does not permit null elements, or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this list |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/List#add(java.util.List.E)`

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
abstract fun clear(): Unit
```

Removes all of the elements from this list (optional operation). The list will be empty after this call returns.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this list |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun contains(element: E?): Boolean
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
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### containsAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun containsAll(elements: Collection<E>): Boolean
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
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)), or if the specified collection is null |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/List#contains(java.util.List.E)`

### copyOf

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> copyOf(coll: MutableCollection<out E>): MutableList<E>
```

Returns an [unmodifiable List](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) containing the elements of the given Collection, in its iteration order. The given Collection must not be null, and it must not contain any null elements. If the given Collection is subsequently modified, the returned List will not reflect such modifications.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `coll` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>: a `Collection` from which elements are drawn, must be non-null |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the elements of the given `Collection` |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if coll is null, or if it contains any nulls |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun get(index: Int): E
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

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun indexOf(o: Any?): Int
```

Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index `i` such that `Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isEmpty(): Boolean
```

Returns `true` if this list contains no elements.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this list in proper sequence.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this list in proper sequence |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun lastIndexOf(o: Any?): Int
```

Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index `i` such that `Objects.equals(o, get(i))`, or -1 if there is no such index.

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to search for |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun listIterator(): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html<E>` | a list iterator over the elements in this list (in proper sequence) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list. The specified index indicates the first element that would be returned by an initial call to `https://developer.android.com/reference/kotlin/java/util/ListIterator#next()`. An initial call to `https://developer.android.com/reference/kotlin/java/util/ListIterator#previous()` would return the element with the specified index minus one.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the first element to be returned from the list iterator (by a call to `https://developer.android.com/reference/kotlin/java/util/ListIterator#next()`) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html<E>` | a list iterator over the elements in this list (in proper sequence), starting at the specified position in the list |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> of(): MutableList<E>
```

Returns an unmodifiable list containing zero elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | an empty `List` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> of(e1: E): MutableList<E>
```

Returns an unmodifiable list containing one element. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the single element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified element |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the element is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E
): MutableList<E>
```

Returns an unmodifiable list containing two elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E
): MutableList<E>
```

Returns an unmodifiable list containing three elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E
): MutableList<E>
```

Returns an unmodifiable list containing four elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun <E : Any!> of(
    e1: E, 
    e2: E, 
    e3: E, 
    e4: E, 
    e5: E
): MutableList<E>
```

Returns an unmodifiable list containing five elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |
| `e5` | E: the fifth element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

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
): MutableList<E>
```

Returns an unmodifiable list containing six elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |
| `e5` | E: the fifth element |
| `e6` | E: the sixth element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

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
): MutableList<E>
```

Returns an unmodifiable list containing seven elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |
| `e5` | E: the fifth element |
| `e6` | E: the sixth element |
| `e7` | E: the seventh element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

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
): MutableList<E>
```

Returns an unmodifiable list containing eight elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |
| `e5` | E: the fifth element |
| `e6` | E: the sixth element |
| `e7` | E: the seventh element |
| `e8` | E: the eighth element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

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
): MutableList<E>
```

Returns an unmodifiable list containing nine elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |
| `e5` | E: the fifth element |
| `e6` | E: the sixth element |
| `e7` | E: the seventh element |
| `e8` | E: the eighth element |
| `e9` | E: the ninth element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

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
): MutableList<E>
```

Returns an unmodifiable list containing ten elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `e1` | E: the first element |
| `e2` | E: the second element |
| `e3` | E: the third element |
| `e4` | E: the fourth element |
| `e5` | E: the fifth element |
| `e6` | E: the sixth element |
| `e7` | E: the seventh element |
| `e8` | E: the eighth element |
| `e9` | E: the ninth element |
| `e10` | E: the tenth element |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` |

### of

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
@SafeVarargs open static fun <E : Any!> of(vararg elements: E): MutableList<E>
```

Returns an unmodifiable list containing an arbitrary number of elements. See [Unmodifiable Lists](https://developer.android.com/reference/kotlin/java/util/List#unmodifiable) for details.

| Parameters ||
|---|---|
| `<E>` | the `List`'s element type |
| `elements` | E: the elements to be contained in the list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a `List` containing the specified elements |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if an element is `null` or if the array is `null` |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(index: Int): E
```

Removes the element at the specified position in this list (optional operation). Shifts any subsequent elements to the left (subtracts one from their indices). Returns the element that was removed from the list.

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

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(element: E?): Boolean
```

Removes the first occurrence of the specified element from this list, if it is present (optional operation). If this list does not contain the element, it is unchanged. More formally, removes the element with the lowest index `i` such that `Objects.equals(o, get(i))` (if such an element exists). Returns `true` if this list contained the specified element (or equivalently, if this list changed as a result of the call).

| Parameters ||
|---|---|
| `o` | element to be removed from this list, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this list |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeAll(elements: Collection<E>): Boolean
```

Removes from this list all of its elements that are contained in the specified collection (optional operation).

| Parameters ||
|---|---|
| `c` | collection containing elements to be removed from this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this list is incompatible with the specified collection ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if this list contains a null element and the specified collection does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)), or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `removeAll` operation is not supported by this list |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/List#remove(java.util.List.E)`
- `https://developer.android.com/reference/kotlin/java/util/List#contains(java.util.List.E)`

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

Replaces each element of this list with the result of applying the operator to that element. Errors or runtime exceptions thrown by the operator are relayed to the caller.

| Parameters ||
|---|---|
| `operator` | [UnaryOperator](https://developer.android.com/reference/kotlin/java/util/function/UnaryOperator)\<E\>: the operator to apply to each element |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified operator is null or if the operator result is a null value and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.UnsupportedOperationException` | if this list is unmodifiable. Implementations may throw this exception if an element cannot be replaced or if, in general, modification is not supported |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun retainAll(elements: Collection<E>): Boolean
```

Retains only the elements in this list that are contained in the specified collection (optional operation). In other words, removes from this list all of its elements that are not contained in the specified collection.

| Parameters ||
|---|---|
| `c` | collection containing elements to be retained in this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this list is incompatible with the specified collection ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if this list contains a null element and the specified collection does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)), or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `retainAll` operation is not supported by this list |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/List#remove(java.util.List.E)`
- `https://developer.android.com/reference/kotlin/java/util/List#contains(java.util.List.E)`

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reversed(): MutableList<E>
```

Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | a reverse-ordered view of this collection, as a `List` |

### set

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun set(
    index: Int, 
    element: E
): E
```

Replaces the element at the specified position in this list with the specified element (optional operation).

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
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `set` operation is not supported by this list |

### sort

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun sort(c: Comparator<in E>?): Unit
```

Sorts this list according to the order induced by the specified `https://developer.android.com/reference/kotlin/java/util/Comparator`.

All elements in this list must be *mutually comparable* using the specified comparator (that is, `c.compare(e1, e2)` must not throw a `ClassCastException` for any elements `e1` and `e2` in the list).

If the specified comparator is `null` then all elements in this list must implement the `https://developer.android.com/reference/kotlin/java/lang/Comparable.html#` interface and the elements' [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) should be used.

This list must be modifiable, but need not be resizable.

For apps running on and targeting Android versions greater than Nougat (API level `> 25`), `https://developer.android.com/reference/kotlin/java/util/Collections#sort(kotlin.collections.MutableList)` delegates to this method. Such apps must not call `https://developer.android.com/reference/kotlin/java/util/Collections#sort(kotlin.collections.MutableList)` from this method. Instead, prefer not overriding this method at all. If you must override it, consider this implementation:

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
| `c` | [Comparator](https://developer.android.com/reference/kotlin/java/util/Comparator)\<in E\>?: the `Comparator` used to compare list elements. A `null` value indicates that the elements' [natural ordering](https://developer.android.com/reference/kotlin/java/lang/Comparable.html#) should be used |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the list contains elements that are not *mutually comparable* using the specified comparator |
| `java.lang.IllegalArgumentException` | ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) if the comparator is found to violate the `https://developer.android.com/reference/kotlin/java/util/Comparator` contract |
| `java.lang.UnsupportedOperationException` | if the list's list-iterator does not support the `set` operation |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun spliterator(): Spliterator<E>
```

Creates a `https://developer.android.com/reference/kotlin/java/util/Spliterator` over the elements in this list.

The `Spliterator` reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`. Implementations should document the reporting of additional characteristic values.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator<E>` | a `Spliterator` over the elements in this list |

### subList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun subList(
    fromIndex: Int, 
    toIndex: Int
): MutableList<E>
```

Returns a view of the portion of this list between the specified `fromIndex`, inclusive, and `toIndex`, exclusive. (If `fromIndex``toIndex` are equal, the returned list is empty.) The returned list is backed by this list, so non-structural changes in the returned list are reflected in this list, and vice-versa. The returned list supports all of the optional list operations supported by this list.

This method eliminates the need for explicit range operations (of the sort that commonly exist for arrays). Any operation that expects a list can be used as a range operation by passing a subList view instead of a whole list. For example, the following idiom removes a range of elements from a list:

```kotlin
<code>list.subList(from, to).clear();
  </code>
```
Similar idioms may be constructed for `indexOf` and `lastIndexOf`, and all of the algorithms in the `Collections` class can be applied to a subList.

The semantics of the list returned by this method become undefined if the backing list (i.e., this list) is *structurally modified* in any way other than via the returned list. (Structural modifications are those that change the size of this list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.)

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
abstract fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element).

The returned array will be "safe" in that no references to it are maintained by this list. (In other words, this method must allocate a new array even if this list is backed by an array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | an array containing all of the elements in this list in proper sequence |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/Arrays#asList(java.util.Arrays.asList.T)`

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the list fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this list.

If the list fits in the specified array with room to spare (i.e., the array has more elements than the list), the element in the array immediately following the end of the list is set to `null`. (This is useful in determining the length of the list *only* if the caller knows that the list does not contain any null elements.)

Like the `https://developer.android.com/reference/kotlin/java/util/List#toArray()` method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose `x` is a list known to contain only strings. The following code can be used to dump the list into a newly allocated array of `String`:

```kotlin
<code>String[] y = x.toArray(new String[0]);
  </code>
```
Note that `toArray(new Object[0])` is identical in function to `toArray()`.

| Parameters ||
|---|---|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array into which the elements of this list are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | an array containing the elements of this list |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this list |
| `java.lang.NullPointerException` | if the specified array is null |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract val size: Int
```

Returns the number of elements in this list. If this list contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this list |
