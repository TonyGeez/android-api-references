Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentLinkedDeque

```
open class ConcurrentLinkedDeque<E : Any!> : AbstractCollection<E>, Deque<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java.util/AbstractCollection.md)\<E\> ||
| | ↳ | [java.util.concurrent.ConcurrentLinkedDeque](ConcurrentLinkedDeque.md) |

An unbounded concurrent [deque](../java.util/Deque.md) based on linked nodes. Concurrent insertion, removal, and access operations execute safely across multiple threads. A `ConcurrentLinkedDeque` is an appropriate choice when many threads will share access to a common collection. Like most other concurrent collection implementations, this class does not permit the use of `null` elements.

Iterators and spliterators are [*weakly consistent*](_package.md).

Beware that, unlike in most collections, the `size` method is *NOT* a constant-time operation. Because of the asynchronous nature of these deques, determining the current number of elements requires a traversal of the elements, and so may report inaccurate results if this collection is modified during traversal.

Bulk operations that add, remove, or examine multiple elements, such as #addAll, removeIf or forEach, are *not* guaranteed to be performed atomically. For example, a `forEach` traversal concurrent with an `addAll` operation might observe only some of the added elements.

This class and its iterator implement all of the *optional* methods of the `https://developer.android.com/reference/kotlin/java/util/Deque.html#` and `https://developer.android.com/reference/kotlin/java/util/Iterator.html#` interfaces.

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a `ConcurrentLinkedDeque` [*happen-before*](_package.md) actions subsequent to the access or removal of that element from the `ConcurrentLinkedDeque` in another thread.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| ConcurrentLinkedDeque Constructs an empty deque. |
| ConcurrentLinkedDeque Constructs a deque initially containing the elements of the given collection, added in traversal order of the collection's iterator. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | add Inserts the specified element at the tail of this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | addAll Appends all of the elements in the specified collection to the end of this deque, in the order that they are returned by the specified collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addFirst Inserts the specified element at the front of this deque. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addLast Inserts the specified element at the end of this deque. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Removes all of the elements from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Returns `true` if this deque contains the specified element. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | descendingIterator Returns an iterator over the elements in this deque in reverse sequential order. |
| open E | element <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | forEach <br /> |
| --- | --- |
| open E | getFirst <br /> |
| open E | getLast <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isEmpty Returns `true` if this collection contains no elements. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | iterator Returns an iterator over the elements in this deque in proper sequence. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offer Inserts the specified element at the tail of this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offerFirst Inserts the specified element at the front of this deque. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offerLast Inserts the specified element at the end of this deque. |
| open E? | peek Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| open E? | peekFirst Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty. |
| --- | --- |
| open E? | peekLast Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty. |
| open E? | poll Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| open E? | pollFirst Retrieves and removes the first element of this deque, or returns `null` if this deque is empty. |
| --- | --- |
| open E? | pollLast Retrieves and removes the last element of this deque, or returns `null` if this deque is empty. |
| open E | pop <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | push <br /> |
| --- | --- |
| open E | remove <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | remove Removes the first occurrence of the specified element from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeAll <br /> |
| --- | --- |
| open E | removeFirst <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeFirstOccurrence Removes the first occurrence of the specified element from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeIf <br /> |
| --- | --- |
| open E | removeLast <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeLastOccurrence Removes the last occurrence of the specified element from this deque. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | retainAll <br /> |
| --- | --- |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this deque. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | toArray Returns an array containing all of the elements in this deque, in proper sequence (from first to last element). |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | toArray Returns an array containing all of the elements in this deque, in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of this collection. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | containsAll Returns `true` if this collection contains all of the elements in the specified collection. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/Deque.html#` |---|---| | `https://developer.android.com/reference/kotlin/java/util/Deque.html#<E>` | reversed Returns a reverse-ordered [view](../java.util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation. <br /> | ||

| Properties ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque#size:kotlin.Int` Returns the number of elements in this deque. |

## Public constructors

### ConcurrentLinkedDeque

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentLinkedDeque()
```

Constructs an empty deque.

### ConcurrentLinkedDeque

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentLinkedDeque(c: MutableCollection<out E>!)
```

Constructs a deque initially containing the elements of the given collection, added in traversal order of the collection's iterator.

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>!: the collection of elements to initially contain |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

## Public methods

### add

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(element: E): Boolean
```

Inserts the specified element at the tail of this deque. As the deque is unbounded, this method will never throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` or return `false`.

| Parameters ||
|---|---|
| `e` | the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by add) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this collection |

### addAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this deque, in the order that they are returned by the specified collection's iterator. Attempts to `addAll` of a deque to itself result in `IllegalArgumentException`.

| Parameters ||
|---|---|
| `c` | the elements to be inserted into this deque |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this deque changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if the collection is this deque |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this collection |

### addFirst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFirst(e: E): Unit
```

Inserts the specified element at the front of this deque. As the deque is unbounded, this method will never throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### addLast

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addLast(e: E): Unit
```

Inserts the specified element at the end of this deque. As the deque is unbounded, this method will never throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

This method is equivalent to #add.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### clear

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all of the elements from this deque.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this collection |

### contains

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(element: E?): Boolean
```

Returns `true` if this deque contains the specified element. More formally, returns `true` if and only if this deque contains at least one element `e` such that `o.equals(e)`.

| Parameters ||
|---|---|
| `o` | element whose presence in this deque is to be tested |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this deque contains the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### descendingIterator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun descendingIterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in reverse sequential order. The elements will be returned in order from last (tail) to first (head).

The returned iterator is [*weakly consistent*](_package.md).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this deque in reverse order |

### element

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun element(): E
```

| Return ||
|---|---|
| `E` | the head of the queue represented by this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

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

### getFirst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFirst(): E
```

| Return ||
|---|---|
| `E` | the head of this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### getLast

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLast(): E
```

| Return ||
|---|---|
| `E` | the tail of this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### isEmpty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this collection contains no elements.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this collection contains no elements |

### iterator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in proper sequence. The elements will be returned in order from first (head) to last (tail).

The returned iterator is [*weakly consistent*](_package.md).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this deque in proper sequence |

### offer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offer(e: E): Boolean
```

Inserts the specified element at the tail of this deque. As the deque is unbounded, this method will never return `false`.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by offer) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |

### offerFirst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offerFirst(e: E): Boolean
```

Inserts the specified element at the front of this deque. As the deque is unbounded, this method will never return `false`.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by offerFirst) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |

### offerLast

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offerLast(e: E): Boolean
```

Inserts the specified element at the end of this deque. As the deque is unbounded, this method will never return `false`.

This method is equivalent to #add.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by offerLast) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |

### peek

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peek(): E?
```

Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to peekFirst.

| Return ||
|---|---|
| `E?` | the head of the queue represented by this deque, or `null` if this deque is empty |

### peekFirst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekFirst(): E?
```

Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the head of this deque, or `null` if this deque is empty |

### peekLast

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peekLast(): E?
```

Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the tail of this deque, or `null` if this deque is empty |

### poll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun poll(): E?
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to pollFirst.

| Return ||
|---|---|
| `E?` | the first element of this deque, or `null` if this deque is empty |

### pollFirst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollFirst(): E?
```

Retrieves and removes the first element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the head of this deque, or `null` if this deque is empty |

### pollLast

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pollLast(): E?
```

Retrieves and removes the last element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the tail of this deque, or `null` if this deque is empty |

### pop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun pop(): E
```

| Return ||
|---|---|
| `E` | the element at the front of this deque (which is the top of the stack represented by this deque) |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### push

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun push(e: E): Unit
```

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(): E
```

| Return ||
|---|---|
| `E` | the head of the queue represented by this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### remove

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(element: E?): Boolean
```

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element `e` such that `o.equals(e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

This method is equivalent to removeFirstOccurrence.

| Parameters ||
|---|---|
| `o` | element to be removed from this deque, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the deque contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeAll(elements: Collection<E>): Boolean
```

| Parameters ||
|---|---|
| `c` | collection containing elements to be removed from this collection |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this collection changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not support null elements (#) or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `removeAll` operation is not supported by this collection |
| --- | --- |

### removeFirst

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeFirst(): E
```

| Return ||
|---|---|
| `E` | the head of this deque |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this deque is empty |

### removeFirstOccurrence

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeFirstOccurrence(o: Any?): Boolean
```

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element `e` such that `o.equals(e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this deque, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the deque contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null |

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLast(): E
```

| Return ||
|---|---|
| `E` | the tail of this deque |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this deque is empty |

### removeLastOccurrence

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeLastOccurrence(o: Any?): Boolean
```

Removes the last occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the last element `e` such that `o.equals(e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this deque, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the deque contained the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null |

### retainAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun retainAll(elements: Collection<E>): Boolean
```

| Parameters ||
|---|---|
| `c` | collection containing elements to be retained in this collection |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this collection changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not permit null elements (#) or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `retainAll` operation is not supported by this collection |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun spliterator(): Spliterator<E>
```

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this deque.

The returned spliterator is [*weakly consistent*](_package.md).

The `Spliterator` reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#<E>` | a `Spliterator` over the elements in this deque |

### toArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this deque, in proper sequence (from first to last element).

The returned array will be "safe" in that no references to it are maintained by this deque. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | an array containing all of the elements in this deque |

### toArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this deque, in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array. If the deque fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this deque.

If this deque fits in the specified array with room to spare (i.e., the array has more elements than this deque), the element in the array immediately following the end of the deque is set to `null`.

Like the toArray method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose `x` is a deque known to contain only strings. The following code can be used to dump the deque into a newly allocated array of `String`:

```kotlin
<code>String[] y = x.toArray(new String[0]);</code>
```
Note that `toArray(new Object[0])` is identical in function to `toArray()`.

| Parameters ||
|---|---|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array into which the elements of the deque are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | an array containing all of the elements in this deque |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this deque |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by valueOf.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of elements in this deque. If this deque contains more than `Integer.MAX_VALUE` elements, it returns `Integer.MAX_VALUE`.

Beware that, unlike in most collections, this method is *NOT* a constant-time operation. Because of the asynchronous nature of these deques, determining the current number of elements requires traversing them all to count them. Additionally, it is possible for the size to change during execution of this method, in which case the returned result will be inaccurate. Thus, this method is typically not very useful in concurrent applications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this deque |
