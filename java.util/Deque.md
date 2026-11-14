Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Deque

```
interface Deque<E : Any!> : Queue<E>, SequencedCollection<E>
```

| [java.util.Deque](Deque.md) |

| Known Direct Subclasses [ArrayDeque](ArrayDeque.md), [BlockingDeque](../java.util.concurrent/BlockingDeque.md), [ConcurrentLinkedDeque](../java.util.concurrent/ConcurrentLinkedDeque.md), [LinkedList](LinkedList.md) |---|---| | [ArrayDeque](ArrayDeque.md) | Resizable-array implementation of the Deque interface. | | [BlockingDeque](../java.util.concurrent/BlockingDeque.md) | A Deque that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [ConcurrentLinkedDeque](../java.util.concurrent/ConcurrentLinkedDeque.md) | An unbounded concurrent [deque](Deque.md) based on linked nodes. | | [LinkedList](LinkedList.md) | Doubly-linked list implementation of the `List` and `Deque` interfaces. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md) |---|---| | [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](../java.util.concurrent/BlockingDeque.md) based on linked nodes. | |
| --- | --- | --- | --- | --- | --- | --- |

A linear collection that supports element insertion and removal at both ends. The name *deque* is short for "double ended queue" and is usually pronounced "deck". Most `Deque` implementations place no fixed limits on the number of elements they may contain, but this interface supports capacity-restricted deques as well as those with no fixed size limit.

This interface defines methods to access the elements at both ends of the deque. Methods are provided to insert, remove, and examine the element. Each of these methods exists in two forms: one throws an exception if the operation fails, the other returns a special value (either `null` or `false`, depending on the operation). The latter form of the insert operation is designed specifically for use with capacity-restricted `Deque` implementations; in most implementations, insert operations cannot fail.

The twelve methods described above are summarized in the following table:

| | First Element (Head) || Last Element (Tail) ||
| --- | --- | --- | --- | --- |
| |

This interface extends the Queue interface. When a deque is used as a queue, FIFO (First-In-First-Out) behavior results. Elements are added at the end of the deque and removed from the beginning. The methods inherited from the `Queue` interface are precisely equivalent to `Deque` methods as indicated in the following table:

| `Queue` Method | Equivalent `Deque` Method |
| --- | --- |
| add | addLast |
| offer | offerLast |
| remove | removeFirst |
| --- | --- |
| poll | pollFirst |
| element | getFirst |
| peek | peekFirst |
|---|---|

Deques can also be used as LIFO (Last-In-First-Out) stacks. This interface should be used in preference to the legacy Stack class. When a deque is used as a stack, elements are pushed and popped from the beginning of the deque. Stack methods are equivalent to `Deque` methods as indicated in the table below:

| Stack Method | Equivalent `Deque` Method |
| --- | --- |
| push | addFirst |
| pop | removeFirst |
| peek | peekFirst |
|---|---|

Note that the peek method works equally well when a deque is used as a queue or a stack; in either case, elements are drawn from the beginning of the deque.

This interface provides two methods to remove interior elements, removeFirstOccurrence and removeLastOccurrence.

Unlike the List interface, this interface does not provide support for indexed access to elements.

While `Deque` implementations are not strictly required to prohibit the insertion of null elements, they are strongly encouraged to do so. Users of any `Deque` implementations that do allow null elements are strongly encouraged *not* to take advantage of the ability to insert nulls. This is so because `null` is used as a special return value by various methods to indicate that the deque is empty.

`Deque` implementations generally do not define element-based versions of the `equals` and `hashCode` methods, but instead inherit the identity-based versions from class `Object`.

## Summary

| Public methods ||
|---|---|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | add Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | addAll Adds all of the elements in the specified collection at the end of this deque, as if by calling addLast on each one, in the order that they are returned by the collection's iterator. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addFirst Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addLast Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Returns `true` if this deque contains the specified element. |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | descendingIterator Returns an iterator over the elements in this deque in reverse sequential order. |
| --- | --- |
| abstract E | element Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque). |
| abstract E | getFirst Retrieves, but does not remove, the first element of this deque. |
| abstract E | getLast Retrieves, but does not remove, the last element of this deque. |
| --- | --- |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | iterator Returns an iterator over the elements in this deque in proper sequence. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offer Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offerFirst Inserts the specified element at the front of this deque unless it would violate capacity restrictions. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offerLast Inserts the specified element at the end of this deque unless it would violate capacity restrictions. |
| abstract E? | peek Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| abstract E? | peekFirst Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty. |
| --- | --- |
| abstract E? | peekLast Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty. |
| abstract E? | poll Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| abstract E? | pollFirst Retrieves and removes the first element of this deque, or returns `null` if this deque is empty. |
| --- | --- |
| abstract E? | pollLast Retrieves and removes the last element of this deque, or returns `null` if this deque is empty. |
| abstract E | pop Pops an element from the stack represented by this deque. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | push Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| --- | --- |
| abstract E | remove Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | remove Removes the first occurrence of the specified element from this deque. |
| abstract E | removeFirst Retrieves and removes the first element of this deque. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeFirstOccurrence Removes the first occurrence of the specified element from this deque. |
| abstract E | removeLast Retrieves and removes the last element of this deque. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeLastOccurrence Removes the last occurrence of the specified element from this deque. |
| --- | --- |
| open [Deque](Deque.md)\<E\> | reversed Returns a reverse-ordered [view](Collection.md) of this collection. |

| Properties ||
|---|---|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/Deque#size:kotlin.Int` Returns the number of elements in this deque. |

## Public methods

### add

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun add(element: E): Boolean
```

Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use offer.

This method is equivalent to addLast.

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
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this collection |

### addAll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addAll(elements: Collection<E>): Boolean
```

Adds all of the elements in the specified collection at the end of this deque, as if by calling addLast on each one, in the order that they are returned by the collection's iterator.

When using a capacity-restricted deque, it is generally preferable to call offer separately on each element.

An exception encountered while trying to add an element may result in only some of the elements having been successfully added when the associated exception is thrown.

| Parameters ||
|---|---|
| `c` | the elements to be inserted into this deque |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this deque changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of the specified collection prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of an element of the specified collection prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if not all the elements can be added at this time due to insertion restrictions |
| --- | --- |
| `java.lang.NullPointerException` | if the specified collection contains a null element and this deque does not permit null elements, or if the specified collection is null |
| `java.lang.UnsupportedOperationException` | if the `addAll` operation is not supported by this collection |

### addFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addFirst(e: E): Unit
```

Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use method offerFirst.

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

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun addLast(e: E): Unit
```

Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use method offerLast.

This method is equivalent to add.

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

### contains

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun contains(element: E?): Boolean
```

Returns `true` if this deque contains the specified element. More formally, returns `true` if and only if this deque contains at least one element `e` such that `Objects.equals(o, e)`.

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

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun descendingIterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in reverse sequential order. The elements will be returned in order from last (tail) to first (head).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this deque in reverse sequence |

### element

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun element(): E
```

Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque). This method differs from peek only in that it throws an exception if this deque is empty.

This method is equivalent to getFirst.

| Return ||
|---|---|
| `E` | the head of the queue represented by this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### getFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getFirst(): E
```

Retrieves, but does not remove, the first element of this deque. This method differs from peekFirst only in that it throws an exception if this deque is empty.

| Return ||
|---|---|
| `E` | the head of this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### getLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLast(): E
```

Retrieves, but does not remove, the last element of this deque. This method differs from peekLast only in that it throws an exception if this deque is empty.

| Return ||
|---|---|
| `E` | the tail of this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in proper sequence. The elements will be returned in order from first (head) to last (tail).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this deque in proper sequence |

### offer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun offer(e: E): Boolean
```

Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. When using a capacity-restricted deque, this method is generally preferable to the add method, which can fail to insert an element only by throwing an exception.

This method is equivalent to offerLast.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| --- | --- |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun offerFirst(e: E): Boolean
```

Inserts the specified element at the front of this deque unless it would violate capacity restrictions. When using a capacity-restricted deque, this method is generally preferable to the addFirst method, which can fail to insert an element only by throwing an exception.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| --- | --- |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun offerLast(e: E): Boolean
```

Inserts the specified element at the end of this deque unless it would violate capacity restrictions. When using a capacity-restricted deque, this method is generally preferable to the addLast method, which can fail to insert an element only by throwing an exception.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements |
| --- | --- |

### peek

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun peek(): E?
```

Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to peekFirst.

| Return ||
|---|---|
| `E?` | the head of the queue represented by this deque, or `null` if this deque is empty |

### peekFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun peekFirst(): E?
```

Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the head of this deque, or `null` if this deque is empty |

### peekLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun peekLast(): E?
```

Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the tail of this deque, or `null` if this deque is empty |

### poll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun poll(): E?
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to pollFirst.

| Return ||
|---|---|
| `E?` | the first element of this deque, or `null` if this deque is empty |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun pollFirst(): E?
```

Retrieves and removes the first element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the head of this deque, or `null` if this deque is empty |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun pollLast(): E?
```

Retrieves and removes the last element of this deque, or returns `null` if this deque is empty.

| Return ||
|---|---|
| `E?` | the tail of this deque, or `null` if this deque is empty |

### pop

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun pop(): E
```

Pops an element from the stack represented by this deque. In other words, removes and returns the first element of this deque.

This method is equivalent to removeFirst.

| Return ||
|---|---|
| `E` | the element at the front of this deque (which is the top of the stack represented by this deque) |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### push

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun push(e: E): Unit
```

Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available.

This method is equivalent to addFirst.

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

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(): E
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). This method differs from poll only in that it throws an exception if this deque is empty.

This method is equivalent to removeFirst.

| Return ||
|---|---|
| `E` | the head of the queue represented by this deque |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if this deque is empty |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun remove(element: E?): Boolean
```

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element `e` such that `Objects.equals(o, e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

This method is equivalent to removeFirstOccurrence.

| Parameters ||
|---|---|
| `o` | element to be removed from this deque, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if an element was removed as a result of this call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this collection |
| --- | --- |

### removeFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeFirst(): E
```

Retrieves and removes the first element of this deque. This method differs from pollFirst only in that it throws an exception if this deque is empty.

| Return ||
|---|---|
| `E` | the head of this deque |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this deque is empty |

### removeFirstOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeFirstOccurrence(o: Any?): Boolean
```

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element `e` such that `Objects.equals(o, e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this deque, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if an element was removed as a result of this call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### removeLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeLast(): E
```

Retrieves and removes the last element of this deque. This method differs from pollLast only in that it throws an exception if this deque is empty.

| Return ||
|---|---|
| `E` | the tail of this deque |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.util.NoSuchElementException` | if this deque is empty |

### removeLastOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun removeLastOccurrence(o: Any?): Boolean
```

Removes the last occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the last element `e` such that `Objects.equals(o, e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|---|---|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this deque, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if an element was removed as a result of this call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this deque does not permit null elements (java.util.Collection#) |

### reversed

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun reversed(): Deque<E>
```

Returns a reverse-ordered [view](Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Deque#<E>` | a reverse-ordered view of this collection, as a `Deque` |

## Properties

### size

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract val size: Int
```

Returns the number of elements in this deque.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this deque |
