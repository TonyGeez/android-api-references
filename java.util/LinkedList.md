Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkedList

```
open class LinkedList<E : Any!> : AbstractSequentialList<E>, Cloneable, Deque<E>, Serializable, MutableList<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection)\<E\> ||||
| | ↳ | [java.util.AbstractList](https://developer.android.com/reference/kotlin/java/util/AbstractList)\<E\> |||
| | | ↳ | [java.util.AbstractSequentialList](https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList)\<E\> ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [java.util.LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList#) |

Doubly-linked list implementation of the `List` and `Deque` interfaces. Implements all optional list operations, and permits all elements (including `null`).

All of the operations perform as could be expected for a doubly-linked list. Operations that index into the list will traverse the list from the beginning or the end, whichever is closer to the specified index.

**Note that this implementation is not synchronized.** If multiple threads access a linked list concurrently, and at least one of the threads modifies the list structurally, it *must* be synchronized externally. (A structural modification is any operation that adds or deletes one or more elements; merely setting the value of an element is not a structural modification.) This is typically accomplished by synchronizing on some object that naturally encapsulates the list. If no such object exists, the list should be "wrapped" using the `https://developer.android.com/reference/kotlin/java/util/Collections#synchronizedList(kotlin.collections.MutableList)` method. This is best done at creation time, to prevent accidental unsynchronized access to the list:

```kotlin
List list = Collections.synchronizedList(new LinkedList(...));
```

The iterators returned by this class's `iterator` and `listIterator` methods are *fail-fast* : if the list is structurally modified at any time after the iterator is created, in any way except through the Iterator's own `remove` or `add` methods, the iterator will throw a `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException`. Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

Note that the fail-fast behavior of an iterator cannot be guaranteed as it is, generally speaking, impossible to make any hard guarantees in the presence of unsynchronized concurrent modification. Fail-fast iterators throw `ConcurrentModificationException` on a best-effort basis. Therefore, it would be wrong to write a program that depended on this exception for its correctness: *the fail-fast behavior of iterators should be used only to detect bugs.*

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/LinkedList#LinkedList()()` Constructs an empty list. |
| `https://developer.android.com/reference/kotlin/java/util/LinkedList#LinkedList(kotlin.collections.MutableCollection)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out E>)` Constructs a list containing the elements of the specified collection, in the order they are returned by the collection's iterator. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#add(java.util.LinkedList.E)(element: E)` Appends the specified element to the end of this list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#add(kotlin.Int,%20java.util.LinkedList.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, element: E)` Inserts the specified element at the specified position in this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#addAll(kotlin.Int,%20kotlin.collections.Collection)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Inserts all of the elements in the specified collection into this list, starting at the specified position. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#addAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#addFirst(java.util.LinkedList.E)(e: E)` Inserts the specified element at the beginning of this list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#addLast(java.util.LinkedList.E)(e: E)` Appends the specified element to the end of this list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#clear()()` Removes all of the elements from this list. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#clone()()` Returns a shallow copy of this `LinkedList`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#contains(java.util.LinkedList.E)(element: E)` Returns `true` if this list contains the specified element. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#contains(java.util.LinkedList.E)(element: E)` Returns `true` if this list contains the specified element. |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/LinkedList#descendingIterator()()` <br /> |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#element()()` Retrieves, but does not remove, the head (first element) of this list. |
| --- | --- |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#get(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the element at the specified position in this list. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#getFirst()()` Returns the first element in this list. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#getLast()()` Returns the last element in this list. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#indexOf(java.util.LinkedList.E)(element: E)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#indexOf(java.util.LinkedList.E)(element: E)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#lastIndexOf(java.util.LinkedList.E)(element: E)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#lastIndexOf(java.util.LinkedList.E)(element: E)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. |
| open [MutableListIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/LinkedList#listIterator(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a list-iterator of the elements in this list (in proper sequence), starting at the specified position in the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#offer(java.util.LinkedList.E)(e: E)` Adds the specified element as the tail (last element) of this list. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#offerFirst(java.util.LinkedList.E)(e: E)` Inserts the specified element at the front of this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#offerLast(java.util.LinkedList.E)(e: E)` Inserts the specified element at the end of this list. |
| open E? | `https://developer.android.com/reference/kotlin/java/util/LinkedList#peek()()` Retrieves, but does not remove, the head (first element) of this list. |
| --- | --- |
| open E? | `https://developer.android.com/reference/kotlin/java/util/LinkedList#peekFirst()()` Retrieves, but does not remove, the first element of this list, or returns `null` if this list is empty. |
| open E? | `https://developer.android.com/reference/kotlin/java/util/LinkedList#peekLast()()` Retrieves, but does not remove, the last element of this list, or returns `null` if this list is empty. |
| open E? | `https://developer.android.com/reference/kotlin/java/util/LinkedList#poll()()` Retrieves and removes the head (first element) of this list. |
| --- | --- |
| open E? | `https://developer.android.com/reference/kotlin/java/util/LinkedList#pollFirst()()` Retrieves and removes the first element of this list, or returns `null` if this list is empty. |
| open E? | `https://developer.android.com/reference/kotlin/java/util/LinkedList#pollLast()()` Retrieves and removes the last element of this list, or returns `null` if this list is empty. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#pop()()` Pops an element from the stack represented by this list. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#push(java.util.LinkedList.E)(e: E)` Pushes an element onto the stack represented by this list. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#remove()()` Retrieves and removes the head (first element) of this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#remove(java.util.LinkedList.E)(element: E)` Removes the first occurrence of the specified element from this list, if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#remove(java.util.LinkedList.E)(element: E)` Removes the first occurrence of the specified element from this list, if it is present. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#removeAt(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes the element at the specified position in this list. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#removeFirst()()` Removes and returns the first element from this list. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#removeFirstOccurrence(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Removes the first occurrence of the specified element in this list (when traversing the list from head to tail). |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#removeLast()()` Removes and returns the last element from this list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#removeLastOccurrence(kotlin.Any)(o: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Removes the last occurrence of the specified element in this list (when traversing the list from head to tail). |
| --- | --- |
| open [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList#)\<E\> | `https://developer.android.com/reference/kotlin/java/util/LinkedList#reversed()()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. |
| open E | `https://developer.android.com/reference/kotlin/java/util/LinkedList#set(kotlin.Int,%20java.util.LinkedList.E)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, element: E)` Replaces the element at the specified position in this list with the specified element. |
| open [Spliterator](https://developer.android.com/reference/kotlin/java/util/Spliterator)\<E\> | `https://developer.android.com/reference/kotlin/java/util/LinkedList#spliterator()()` Creates a * [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator#binding)* and *fail-fast* `https://developer.android.com/reference/kotlin/java/util/Spliterator` over the elements in this list. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/LinkedList#toArray()()` Returns an array containing all of the elements in this list in proper sequence (from first to last element). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | `https://developer.android.com/reference/kotlin/java/util/LinkedList#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractList` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#add(java.util.AbstractList.E)(element: E)` Appends the specified element to the end of this list (optional operation). Lists that support this operation may place limitations on what elements may be added to this list. In particular, some lists will refuse to add null elements, and others will impose restrictions on the type of elements that may be added. List classes should clearly specify in their documentation any restrictions on what elements may be added. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#clear()()` Removes all of the elements from this list (optional operation). The list will be empty after this call returns. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Compares the specified object with this list for equality. Returns `true` if and only if the specified object is also a list, both lists have the same size, and all corresponding pairs of elements in the two lists are *equal* . (Two elements `e1` and `e2` are *equal* if `(e1==null ? e2==null : e1.equals(e2))`.) In other words, two lists are defined to be equal if they contain the same elements in the same order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#hashCode()()` Returns the hash code value for this list. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#indexOf(java.util.AbstractList.E)(element: E?)` Returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the lowest index `i` such that `Objects.equals(o, get(i))`, or -1 if there is no such index. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#lastIndexOf(java.util.AbstractList.E)(element: E?)` Returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element. More formally, returns the highest index `i` such that `Objects.equals(o, get(i))`, or -1 if there is no such index. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html<E>` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#listIterator()()` Returns a list iterator over the elements in this list (in proper sequence). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#removeRange(kotlin.Int,%20kotlin.Int)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, toIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Removes from this list all of the elements whose index is between `fromIndex`, inclusive, and `toIndex`, exclusive. Shifts any succeeding elements to the left (reduces their index). This call shortens the list by `(toIndex - fromIndex)` elements. (If `toIndex==fromIndex`, this operation has no effect.) This method is called by the `clear` operation on this list and its subLists. Overriding this method to take advantage of the internals of the list implementation can *substantially* improve the performance of the `clear` operation on this list and its subLists. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<E>` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#subList(kotlin.Int,%20kotlin.Int)(fromIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, toIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a view of the portion of this list between the specified `fromIndex`, inclusive, and `toIndex`, exclusive. (If `fromIndex``toIndex` are equal, the returned list is empty.) The returned list is backed by this list, so non-structural changes in the returned list are reflected in this list, and vice-versa. The returned list supports all of the optional list operations supported by this list. This method eliminates the need for explicit range operations (of the sort that commonly exist for arrays). Any operation that expects a list can be used as a range operation by passing a subList view instead of a whole list. For example, the following idiom removes a range of elements from a list: ```kotlin <code>list.subList(from, to).clear(); </code> ``` Similar idioms may be constructed for `indexOf` and `lastIndexOf`, and all of the algorithms in the `Collections` class can be applied to a subList. The semantics of the list returned by this method become undefined if the backing list (i.e., this list) is *structurally modified* in any way other than via the returned list. (Structural modifications are those that change the size of this list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results.) <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#addAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Adds all of the elements in the specified collection to this collection (optional operation). The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (This implies that the behavior of this call is undefined if the specified collection is this collection, and this collection is nonempty.) If the specified collection has a defined [encounter order](https://developer.android.com/reference/kotlin/java/util/SequencedCollection#encounter), processing of its elements generally occurs in that order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#contains(java.util.AbstractCollection.E)(element: E?)` Returns `true` if this collection contains the specified element. More formally, returns `true` if and only if this collection contains at least one element `e` such that `Objects.equals(o, e)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#containsAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Returns `true` if this collection contains all of the elements in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#isEmpty()()` Returns `true` if this collection contains no elements. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#remove(java.util.AbstractCollection.E)(element: E?)` Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element `e` such that `Objects.equals(o, e)`, if this collection contains one or more such elements. Returns `true` if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#removeAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#retainAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray()()` Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType()) is `Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to `null`. (This is useful in determining the length of this collection *only* if the caller knows that this collection does not contain any `null` elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#toString()()` Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | `https://developer.android.com/reference/kotlin/java/util/AbstractSequentialList#iterator()()` Returns an iterator over the elements in this list (in proper sequence). This implementation merely returns a list iterator over the list. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/LinkedList#size:kotlin.Int` Returns the number of elements in this list. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractList` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractList#modCount:kotlin.Int` The number of times this list has been *structurally modified*. Structural modifications are those that change the size of the list, or otherwise perturb it in such a fashion that iterations in progress may yield incorrect results. This field is used by the iterator and list iterator implementation returned by the `iterator` and `listIterator` methods. If the value of this field changes unexpectedly, the iterator (or list iterator) will throw a `ConcurrentModificationException` in response to the `next`, `remove`, `previous`, `set` or `add` operations. This provides *fail-fast* behavior, rather than non-deterministic behavior in the face of concurrent modification during iteration. **Use of this field by subclasses is optional.** If a subclass wishes to provide fail-fast iterators (and list iterators), then it merely has to increment this field in its `add(int, E)` and `remove(int)` methods (and any other methods that it overrides that result in structural modifications to the list). A single call to `add(int, E)` or `remove(int)` must add no more than one to this field, or the iterators (and list iterators) will throw bogus `ConcurrentModificationExceptions`. If an implementation does not wish to provide fail-fast iterators, this field may be ignored. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection#size:kotlin.Int` Returns the number of elements in this collection. If this collection contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`. <br /> | ||

## Public constructors

### LinkedList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LinkedList()
```

Constructs an empty list.

### LinkedList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
LinkedList(c: MutableCollection<out E>)
```

Constructs a list containing the elements of the specified collection, in the order they are returned by the collection's iterator.

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>: the collection whose elements are to be placed into this list |

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

This method is equivalent to #addLast.

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
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
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

Inserts all of the elements in the specified collection into this list, starting at the specified position. Shifts the element currently at that position (if any) and any subsequent elements to the right (increases their indices). The new elements will appear in the list in the order that they are returned by the specified collection's iterator.

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

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection's iterator. The behavior of this operation is undefined if the specified collection is modified while the operation is in progress. (Note that this will occur if the specified collection is this list, and it's nonempty.)

| Parameters ||
|---|---|
| `c` | collection containing elements to be added to this list |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this list changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this list |

### addFirst

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFirst(e: E): Unit
```

Inserts the specified element at the beginning of this list.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### addLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLast(e: E): Unit
```

Appends the specified element to the end of this list.

This method is equivalent to #add.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

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

Returns a shallow copy of this `LinkedList`. (The elements themselves are not cloned.)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html` | a shallow copy of this `LinkedList` instance |

| Exceptions ||
|---|---|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the `Cloneable` interface. Subclasses that override the `clone` method can also throw this exception to indicate that an instance cannot be cloned. |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(element: E): Boolean
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
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(element: E): Boolean
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
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### descendingIterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descendingIterator(): MutableIterator<E>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this deque in reverse sequence |

### element

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun element(): E
```

Retrieves, but does not remove, the head (first element) of this list.

| Return ||
|---|---|
| `E` | the head of this list |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this list is empty |

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFirst(): E
```

Returns the first element in this list.

| Return ||
|---|---|
| `E` | the first element in this list |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this list is empty |

### getLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLast(): E
```

Returns the last element in this list.

| Return ||
|---|---|
| `E` | the last element in this list |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this list is empty |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOf(element: E): Int
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
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### indexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun indexOf(element: E): Int
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
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastIndexOf(element: E): Int
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
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### lastIndexOf

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun lastIndexOf(element: E): Int
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
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this list ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null and this list does not permit null elements ([optional](https://developer.android.com/reference/kotlin/java/util/Collection#optional-restrictions)) |

### listIterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun listIterator(index: Int): MutableListIterator<E>
```

Returns a list-iterator of the elements in this list (in proper sequence), starting at the specified position in the list. Obeys the general contract of `List.listIterator(int)`.

The list-iterator is *fail-fast* : if the list is structurally modified at any time after the Iterator is created, in any way except through the list-iterator's own `remove` or `add` methods, the list-iterator will throw a `ConcurrentModificationException`. Thus, in the face of concurrent modification, the iterator fails quickly and cleanly, rather than risking arbitrary, non-deterministic behavior at an undetermined time in the future.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the first element to be returned from the list-iterator (by a call to `next`) |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list-iterator/index.html<E>` | a ListIterator of the elements in this list (in proper sequence), starting at the specified position in the list |

| Exceptions ||
|---|---|
| `java.lang.IndexOutOfBoundsException` | if the index is out of range (`index < 0 || index > size()`) |

**See Also**

- `https://developer.android.com/reference/kotlin/java/util/List#listIterator(kotlin.Int)`

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offer(e: E): Boolean
```

Adds the specified element as the tail (last element) of this list.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| --- | --- |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offerFirst(e: E): Boolean
```

Inserts the specified element at the front of this list.

| Parameters ||
|---|---|
| `e` | E: the element to insert |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Deque#offerFirst(java.util.Deque.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| --- | --- |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offerLast(e: E): Boolean
```

Inserts the specified element at the end of this list.

| Parameters ||
|---|---|
| `e` | E: the element to insert |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Deque#offerLast(java.util.Deque.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| --- | --- |

### peek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peek(): E?
```

Retrieves, but does not remove, the head (first element) of this list.

| Return ||
|---|---|
| `E?` | the head of this list, or `null` if this list is empty |

### peekFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekFirst(): E?
```

Retrieves, but does not remove, the first element of this list, or returns `null` if this list is empty.

| Return ||
|---|---|
| `E?` | the first element of this list, or `null` if this list is empty |

### peekLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekLast(): E?
```

Retrieves, but does not remove, the last element of this list, or returns `null` if this list is empty.

| Return ||
|---|---|
| `E?` | the last element of this list, or `null` if this list is empty |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun poll(): E?
```

Retrieves and removes the head (first element) of this list.

| Return ||
|---|---|
| `E?` | the head of this list, or `null` if this list is empty |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollFirst(): E?
```

Retrieves and removes the first element of this list, or returns `null` if this list is empty.

| Return ||
|---|---|
| `E?` | the first element of this list, or `null` if this list is empty |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollLast(): E?
```

Retrieves and removes the last element of this list, or returns `null` if this list is empty.

| Return ||
|---|---|
| `E?` | the last element of this list, or `null` if this list is empty |

### pop

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pop(): E
```

Pops an element from the stack represented by this list. In other words, removes and returns the first element of this list.

This method is equivalent to #removeFirst().

| Return ||
|---|---|
| `E` | the element at the front of this list (which is the top of the stack represented by this list) |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this list is empty |

### push

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun push(e: E): Unit
```

Pushes an element onto the stack represented by this list. In other words, inserts the element at the front of this list.

This method is equivalent to #addFirst.

| Parameters ||
|---|---|
| `e` | E: the element to push |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(): E
```

Retrieves and removes the head (first element) of this list.

| Return ||
|---|---|
| `E` | the head of this list |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this list is empty |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(element: E): Boolean
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
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this list |
| --- | --- |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(element: E): Boolean
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
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this list |
| --- | --- |

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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeFirst(): E
```

Removes and returns the first element from this list.

| Return ||
|---|---|
| `E` | the first element from this list |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this list is empty |

### removeFirstOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeFirstOccurrence(o: Any?): Boolean
```

Removes the first occurrence of the specified element in this list (when traversing the list from head to tail). If the list does not contain the element, it is unchanged.

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this list, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the list contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### removeLast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLast(): E
```

Removes and returns the last element from this list.

| Return ||
|---|---|
| `E` | the last element from this list |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this list is empty |

### removeLastOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLastOccurrence(o: Any?): Boolean
```

Removes the last occurrence of the specified element in this list (when traversing the list from head to tail). If the list does not contain the element, it is unchanged.

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this list, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the list contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reversed(): LinkedList<E>
```

Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection#view) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

Modifications to the reversed view are permitted and will be propagated to this list. In addition, modifications to this list will be visible in the reversed view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/LinkedList#<E>` | a reverse-ordered view of this collection, as a `List` |

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

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun spliterator(): Spliterator<E>
```

Creates a * [late-binding](https://developer.android.com/reference/kotlin/java/util/Spliterator#binding)* and *fail-fast* `https://developer.android.com/reference/kotlin/java/util/Spliterator` over the elements in this list.

The `Spliterator` reports `https://developer.android.com/reference/kotlin/java/util/Spliterator#SIZED:kotlin.Int` and `https://developer.android.com/reference/kotlin/java/util/Spliterator#ORDERED:kotlin.Int`. Overriding implementations should document the reporting of additional characteristic values.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator<E>` | a `Spliterator` over the elements in this list |

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
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | an array containing all of the elements in this list in proper sequence |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the list fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this list.

If the list fits in the specified array with room to spare (i.e., the array has more elements than the list), the element in the array immediately following the end of the list is set to `null`. (This is useful in determining the length of the list *only* if the caller knows that the list does not contain any null elements.)

Like the `https://developer.android.com/reference/kotlin/java/util/LinkedList#toArray()` method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose `x` is a list known to contain only strings. The following code can be used to dump the list into a newly allocated array of `String`:

```kotlin
String[] y = x.toArray(new String[0]);
```
Note that `toArray(new Object[0])` is identical in function to `toArray()`.

| Parameters ||
|---|---|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array into which the elements of the list are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | an array containing the elements of the list |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this list |
| `java.lang.NullPointerException` | if the specified array is null |

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
