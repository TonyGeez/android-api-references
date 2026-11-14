Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConcurrentLinkedQueue

```
open class ConcurrentLinkedQueue<E : Any!> : AbstractQueue<E>, Queue<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java/util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractQueue](../java/util/AbstractQueue.md)\<E\> ||
| | | ↳ | [java.util.concurrent.ConcurrentLinkedQueue](../java/util/concurrent/ConcurrentLinkedQueue.md) |
| --- | --- | --- | --- |

An unbounded thread-safe [queue](../java/util/Queue.md) based on linked nodes. This queue orders elements FIFO (first-in-first-out). The *head* of the queue is that element that has been on the queue the longest time. The *tail* of the queue is that element that has been on the queue the shortest time. New elements are inserted at the tail of the queue, and the queue retrieval operations obtain elements at the head of the queue. A `ConcurrentLinkedQueue` is an appropriate choice when many threads will share access to a common collection. Like most other concurrent collection implementations, this class does not permit the use of `null` elements.

This implementation employs an efficient *non-blocking* algorithm based on one described in [Simple, Fast, and Practical Non-Blocking and Blocking Concurrent Queue Algorithms](http://www.cs.rochester.edu/~scott/papers/1996_PODC_queues.pdf) by Maged M. Michael and Michael L. Scott.

Iterators are *weakly consistent* , returning elements reflecting the state of the queue at some point at or since the creation of the iterator. They do *not* throw `https://developer.android.com/reference/kotlin/java/util/ConcurrentModificationException.html#`, and may proceed concurrently with other operations. Elements contained in the queue since the creation of the iterator will be returned exactly once.

Beware that, unlike in most collections, the `size` method is *NOT* a constant-time operation. Because of the asynchronous nature of these queues, determining the current number of elements requires a traversal of the elements, and so may report inaccurate results if this collection is modified during traversal.

Bulk operations that add, remove, or examine multiple elements, such as #addAll, `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#removeIf(java.util.function.Predicate)` or `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#forEach(java.util.function.Consumer)`, are *not* guaranteed to be performed atomically. For example, a `forEach` traversal concurrent with an `addAll` operation might observe only some of the added elements.

This class and its iterator implement all of the *optional* methods of the `https://developer.android.com/reference/kotlin/java/util/Queue.html#` and `https://developer.android.com/reference/kotlin/java/util/Iterator.html#` interfaces.

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a `ConcurrentLinkedQueue` [*happen-before*](../java/util/concurrent/_package.md) actions subsequent to the access or removal of that element from the `ConcurrentLinkedQueue` in another thread.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#ConcurrentLinkedQueue()()` Creates a `ConcurrentLinkedQueue` that is initially empty. |
| `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#ConcurrentLinkedQueue(kotlin.collections.MutableCollection)(c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html<out E>!)` Creates a `ConcurrentLinkedQueue` initially containing the elements of the given collection, added in traversal order of the collection's iterator. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#add(java.util.concurrent.ConcurrentLinkedQueue.E)(element: E)` Inserts the specified element at the tail of this queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#addAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Appends all of the elements in the specified collection to the end of this queue, in the order that they are returned by the specified collection's iterator. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#clear()()` Removes all of the elements from this queue. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#contains(java.util.concurrent.ConcurrentLinkedQueue.E)(element: E?)` Returns `true` if this queue contains the specified element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#forEach(java.util.function.Consumer)(action: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<in E>)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#isEmpty()()` Returns `true` if this queue contains no elements. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#iterator()()` Returns an iterator over the elements in this queue in proper sequence. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#offer(java.util.concurrent.ConcurrentLinkedQueue.E)(e: E)` Inserts the specified element at the tail of this queue. |
| open E? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#peek()()` Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty. |
| --- | --- |
| open E? | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#poll()()` Retrieves and removes the head of this queue, or returns `null` if this queue is empty. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#remove(java.util.concurrent.ConcurrentLinkedQueue.E)(element: E?)` Removes a single instance of the specified element from this queue, if it is present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#removeAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#removeIf(java.util.function.Predicate)(filter: https://developer.android.com/reference/kotlin/java/util/function/Predicate.html#<in E>)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#retainAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` <br /> |
| open [Spliterator](../java/util/Spliterator.md)\<E\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#spliterator()()` Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this queue. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#toArray()()` Returns an array containing all of the elements in this queue, in proper sequence. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this queue, in proper sequence; the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#toString()()` Returns a string representation of this collection. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#contains(java.util.AbstractCollection.E)(element: E?)` Returns `true` if this collection contains the specified element. More formally, returns `true` if and only if this collection contains at least one element `e` such that `Objects.equals(o, e)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#containsAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Returns `true` if this collection contains all of the elements in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#isEmpty()()` Returns `true` if this collection contains no elements. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#iterator()()` Returns an iterator over the elements contained in this collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#remove(java.util.AbstractCollection.E)(element: E?)` Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element `e` such that `Objects.equals(o, e)`, if this collection contains one or more such elements. Returns `true` if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#removeAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#retainAll(kotlin.collections.Collection)(elements: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html<E>)` Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#toArray()()` Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java/lang/Class.md)) is `Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#toArray(kotlin.Array)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>)` Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to `null`. (This is useful in determining the length of this collection *only* if the caller knows that this collection does not contain any `null` elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#toString()()` Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#` |---|---| | `E` | `https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#element()()` Retrieves, but does not remove, the head of this queue. This method differs from `https://developer.android.com/reference/kotlin/java/util/Queue.html#peek()` only in that it throws an exception if this queue is empty. This implementation returns the result of `peek` unless the queue is empty. <br /> | | `E` | `https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#remove()()` Retrieves and removes the head of this queue. This method differs from `https://developer.android.com/reference/kotlin/java/util/Queue.html#poll()` only in that it throws an exception if this queue is empty. This implementation returns the result of `poll` unless the queue is empty. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/Queue.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/util/Queue.html#offer(java.util.Queue.E)(e: E)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to `https://developer.android.com/reference/kotlin/java/util/Queue.html#add(java.util.Queue.E)`, which can fail to insert an element only by throwing an exception. <br /> | | `E?` | `https://developer.android.com/reference/kotlin/java/util/Queue.html#peek()()` Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty. <br /> | | `E?` | `https://developer.android.com/reference/kotlin/java/util/Queue.html#poll()()` Retrieves and removes the head of this queue, or returns `null` if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#size:kotlin.Int` Returns the number of elements in this queue. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#size:kotlin.Int` Returns the number of elements in this collection. If this collection contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`. <br /> | ||

## Public constructors

### ConcurrentLinkedQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentLinkedQueue()
```

Creates a `ConcurrentLinkedQueue` that is initially empty.

### ConcurrentLinkedQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConcurrentLinkedQueue(c: MutableCollection<out E>!)
```

Creates a `ConcurrentLinkedQueue` initially containing the elements of the given collection, added in traversal order of the collection's iterator.

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>!: the collection of elements to initially contain |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(element: E): Boolean
```

Inserts the specified element at the tail of this queue. As the queue is unbounded, this method will never throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` or return `false`.

| Parameters ||
|---|---|
| `e` | the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Collection.html#add(java.util.Collection.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this collection |

### addAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addAll(elements: Collection<E>): Boolean
```

Appends all of the elements in the specified collection to the end of this queue, in the order that they are returned by the specified collection's iterator. Attempts to `addAll` of a queue to itself result in `IllegalArgumentException`.

| Parameters ||
|---|---|
| `c` | the elements to be inserted into this queue |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this queue changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this collection |
| `java.lang.IllegalArgumentException` | if the collection is this queue |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this collection |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all of the elements from this queue. The queue will be empty after this call returns.

This implementation repeatedly invokes `https://developer.android.com/reference/kotlin/java/util/Queue.html#poll()` until it returns `null`.

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the `clear` operation is not supported by this collection |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun contains(element: E?): Boolean
```

Returns `true` if this queue contains the specified element. More formally, returns `true` if and only if this queue contains at least one element `e` such that `o.equals(e)`.

| Parameters ||
|---|---|
| `o` | object to be checked for containment in this queue |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this queue contains the specified element |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this collection (#) |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements (#) |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun forEach(action: Consumer<in E>): Unit
```

| Parameters ||
|---|---|
| `action` | [Consumer](../java/util/function/Consumer.md)\<in E\>: The action to be performed for each element |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified action is null |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isEmpty(): Boolean
```

Returns `true` if this queue contains no elements.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this queue contains no elements |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this queue in proper sequence. The elements will be returned in order from first (head) to last (tail).

The returned iterator is [*weakly consistent*](../java/util/concurrent/_package.md).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this queue in proper sequence |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offer(e: E): Boolean
```

Inserts the specified element at the tail of this queue. As the queue is unbounded, this method will never return `false`.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by `https://developer.android.com/reference/kotlin/java/util/Queue.html#offer(java.util.Queue.E)`) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |

### peek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun peek(): E?
```

Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty.

| Return ||
|---|---|
| `E?` | the head of this queue, or `null` if this queue is empty |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun poll(): E?
```

Retrieves and removes the head of this queue, or returns `null` if this queue is empty.

| Return ||
|---|---|
| `E?` | the head of this queue, or `null` if this queue is empty |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this queue, if it is present. More formally, removes an element `e` such that `o.equals(e)`, if this queue contains one or more such elements. Returns `true` if this queue contained the specified element (or equivalently, if this queue changed as a result of the call).

| Parameters ||
|---|---|
| `o` | element to be removed from this queue, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this queue changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this collection (#) |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements (#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

| Parameters ||
|---|---|
| `filter` | [Predicate](../java/util/function/Predicate.md)\<in E\>: a predicate which returns `true` for elements to be removed |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if any elements were removed |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if the `removeIf` operation is not supported by this collection |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this queue.

The returned spliterator is [*weakly consistent*](../java/util/concurrent/_package.md).

The `Spliterator` reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#<E>` | a `Spliterator` over the elements in this queue |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this queue, in proper sequence.

The returned array will be "safe" in that no references to it are maintained by this queue. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | an array containing all of the elements in this queue |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this queue, in proper sequence; the runtime type of the returned array is that of the specified array. If the queue fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this queue.

If this queue fits in the specified array with room to spare (i.e., the array has more elements than this queue), the element in the array immediately following the end of the queue is set to `null`.

Like the `https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue#toArray()` method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose `x` is a queue known to contain only strings. The following code can be used to dump the queue into a newly allocated array of `String`:

```kotlin
<code>String[] y = x.toArray(new String[0]);</code>
```
Note that `toArray(new Object[0])` is identical in function to `toArray()`.

| Parameters ||
|---|---|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>: the array into which the elements of the queue are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | an array containing all of the elements in this queue |

| Exceptions ||
|---|---|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this queue |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by `https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of elements in this queue. If this queue contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`.

Beware that, unlike in most collections, this method is *NOT* a constant-time operation. Because of the asynchronous nature of these queues, determining the current number of elements requires an O(n) traversal. Additionally, if elements are added or removed during execution of this method, the returned result may be inaccurate. Thus, this method is typically not very useful in concurrent applications.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this queue |
