# BlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlockingDeque

```
interface BlockingDeque<E : Any!> : BlockingQueue<E>, Deque<E>
```

| [java.util.concurrent.BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#) |

| Known Direct Subclasses [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#) based on linked nodes. | |
| --- | --- | --- | --- | --- | --- | --- |

A [Deque](https://developer.android.com/reference/kotlin/java/util/Deque.html#) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element.

`BlockingDeque` methods come in four forms, with different ways of handling operations that cannot be satisfied immediately, but may be satisfied at some point in the future: one throws an exception, the second returns a special value (either `null` or `false`, depending on the operation), the third blocks the current thread indefinitely until the operation can succeed, and the fourth blocks for only a given maximum time limit before giving up. These methods are summarized in the following table:

| First Element (Head) |||||
|---|------------------|---------------|--------|-----------|
| | Throws exception | Special value | Blocks | Times out |
| | Throws exception | Special value | Blocks | Times out |

Like any [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue), a `BlockingDeque` is thread safe, does not permit null elements, and may (or may not) be capacity-constrained.

A `BlockingDeque` implementation may be used directly as a FIFO `BlockingQueue`. The methods inherited from the `BlockingQueue` interface are precisely equivalent to `BlockingDeque` methods as indicated in the following table:

| | `BlockingQueue` Method | Equivalent `BlockingDeque` Method |
| --- | --- | --- |

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a `BlockingDeque` [*happen-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#MemoryVisibility) actions subsequent to the access or removal of that element from the `BlockingDeque` in another thread.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#add(java.util.concurrent.BlockingDeque.E))`(`element:` `E`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#addFirst(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#addLast(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#contains(java.util.concurrent.BlockingDeque.E))`(`element:` `E?`)` Returns `true` if this deque contains the specified element. |
| abstract E | [element](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#element())`()` Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque). |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#iterator())`()` Returns an iterator over the elements in this deque in proper sequence. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offer(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offer(java.util.concurrent.BlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque), waiting up to the specified wait time if necessary for space to become available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerFirst(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerFirst(java.util.concurrent.BlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Inserts the specified element at the front of this deque, waiting up to the specified wait time if necessary for space to become available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerLast(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerLast(java.util.concurrent.BlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Inserts the specified element at the end of this deque, waiting up to the specified wait time if necessary for space to become available. |
| --- | --- |
| abstract E? | [peek](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#peek())`()` Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| abstract E? | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#poll())`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| abstract E | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), waiting up to the specified wait time if necessary for an element to become available. |
| --- | --- |
| abstract E | [pollFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#pollFirst(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Retrieves and removes the first element of this deque, waiting up to the specified wait time if necessary for an element to become available. |
| abstract E | [pollLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#pollLast(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Retrieves and removes the last element of this deque, waiting up to the specified wait time if necessary for an element to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [push](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#push(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#put(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque), waiting if necessary for space to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#putFirst(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element at the front of this deque, waiting if necessary for space to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#putLast(java.util.concurrent.BlockingDeque.E))`(`e:` `E`)` Inserts the specified element at the end of this deque, waiting if necessary for space to become available. |
| --- | --- |
| abstract E | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#remove())`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#remove(java.util.concurrent.BlockingDeque.E))`(`element:` `E?`)` Removes the first occurrence of the specified element from this deque. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFirstOccurrence](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#removeFirstOccurrence(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the first occurrence of the specified element from this deque. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeLastOccurrence](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#removeLastOccurrence(kotlin.Any))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the last occurrence of the specified element from this deque. |
| abstract E | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#take())`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), waiting if necessary until an element becomes available. |
| abstract E | [takeFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#takeFirst())`()` Retrieves and removes the first element of this deque, waiting if necessary until an element becomes available. |
| --- | --- |
| abstract E | [takeLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#takeLast())`()` Retrieves and removes the last element of this deque, waiting if necessary until an element becomes available. |

| Inherited functions ||
|---|---|
| From class [Deque](https://developer.android.com/reference/kotlin/java/util/Deque.html#) |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [descendingIterator](https://developer.android.com/reference/kotlin/java/util/Deque.html#descendingIterator())`()` Returns an iterator over the elements in this deque in reverse sequential order. The elements will be returned in order from last (tail) to first (head). <br /> | | E | [getFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#getFirst())`()` Retrieves, but does not remove, the first element of this deque. This method differs from [peekFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#peekFirst()) only in that it throws an exception if this deque is empty. <br /> | | E | [getLast](https://developer.android.com/reference/kotlin/java/util/Deque.html#getLast())`()` Retrieves, but does not remove, the last element of this deque. This method differs from [peekLast](https://developer.android.com/reference/kotlin/java/util/Deque.html#peekLast()) only in that it throws an exception if this deque is empty. <br /> | | E? | [peekFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#peekFirst())`()` Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty. <br /> | | E? | [peekLast](https://developer.android.com/reference/kotlin/java/util/Deque.html#peekLast())`()` Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty. <br /> | | E? | [pollFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#pollFirst())`()` Retrieves and removes the first element of this deque, or returns `null` if this deque is empty. <br /> | | E? | [pollLast](https://developer.android.com/reference/kotlin/java/util/Deque.html#pollLast())`()` Retrieves and removes the last element of this deque, or returns `null` if this deque is empty. <br /> | | E | [pop](https://developer.android.com/reference/kotlin/java/util/Deque.html#pop())`()` Pops an element from the stack represented by this deque. In other words, removes and returns the first element of this deque. This method is equivalent to [removeFirst()](https://developer.android.com/reference/kotlin/java/util/Deque.html#removeFirst()). <br /> | | E | [removeFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#removeFirst())`()` Retrieves and removes the first element of this deque. This method differs from [pollFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#pollFirst()) only in that it throws an exception if this deque is empty. <br /> | | E | [removeLast](https://developer.android.com/reference/kotlin/java/util/Deque.html#removeLast())`()` Retrieves and removes the last element of this deque. This method differs from [pollLast](https://developer.android.com/reference/kotlin/java/util/Deque.html#pollLast()) only in that it throws an exception if this deque is empty. <br /> | | [Deque](https://developer.android.com/reference/kotlin/java/util/Deque.html#)<E> | [reversed](https://developer.android.com/reference/kotlin/java/util/Deque.html#reversed())`()` Returns a reverse-ordered [view](https://developer.android.com/reference/kotlin/java/util/Collection.html#view) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation. <br /> | ||
| From class [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#drainTo(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` Removes all available elements from this queue and adds them to the given collection. This operation may be more efficient than repeatedly polling this queue. A failure encountered while attempting to add elements to collection `c` may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in `IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#drainTo(kotlin.collections.MutableCollection,%20kotlin.Int))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes at most the given number of available elements from this queue and adds them to the given collection. A failure encountered while attempting to add elements to collection `c` may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in `IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#remainingCapacity())`()` Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking, or `Integer.MAX_VALUE` if there is no intrinsic limit. Note that you *cannot* always tell if an attempt to insert an element will succeed by inspecting `remainingCapacity` because it may be the case that another thread is about to insert or remove an element. <br /> | ||
| From class [Queue](https://developer.android.com/reference/kotlin/java/util/Queue.html#) |----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [element](https://developer.android.com/reference/kotlin/java/util/Queue.html#element())`()` Retrieves, but does not remove, the head of this queue. This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek()) only in that it throws an exception if this queue is empty. <br /> | | E? | [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())`()` Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty. <br /> | | E? | [poll](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll())`()` Retrieves and removes the head of this queue, or returns `null` if this queue is empty. <br /> | | E | [remove](https://developer.android.com/reference/kotlin/java/util/Queue.html#remove())`()` Retrieves and removes the head of this queue. This method differs from [poll()](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll()) only in that it throws an exception if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#size:kotlin.Int) Returns the number of elements in this deque. |

## Public methods

### add

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(element: E): Boolean
```

Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use #offer(java.lang.Object).

This method is equivalent to #addLast(java.lang.Object).

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` (as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection.html#add(java.util.Collection.E))) |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### addFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addFirst(e: E): Unit
```

Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use [offerFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerFirst(java.util.concurrent.BlockingDeque.E)).

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### addLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addLast(e: E): Unit
```

Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerLast(java.util.concurrent.BlockingDeque.E)).

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if this collection implementation does not support this operation |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| --- | --- |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### contains

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun contains(element: E?): Boolean
```

Returns `true` if this deque contains the specified element. More formally, returns `true` if and only if this deque contains at least one element `e` such that `o.equals(e)`.

| Parameters ||
|-----|----------------------------------------------------|
| `o` | object to be checked for containment in this deque |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this deque contains the specified element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### element

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun element(): E
```

Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque). This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#peek()) only in that it throws an exception if this deque is empty.

This method is equivalent to [getFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#getFirst()).

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### iterator

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this deque in proper sequence. The elements will be returned in order from first (head) to last (tail).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this deque in proper sequence |

### offer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offer(e: E): Boolean
```

Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. When using a capacity-restricted deque, this method is generally preferable to the #add method, which can fail to insert an element only by throwing an exception.

This method is equivalent to [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerLast(java.util.concurrent.BlockingDeque.E)).

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offer

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque), waiting up to the specified wait time if necessary for space to become available.

This method is equivalent to [offerLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#offerLast(java.util.concurrent.BlockingDeque.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E: the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offerFirst(e: E): Boolean
```

Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. When using a capacity-restricted deque, this method is generally preferable to the #addFirst(java.lang.Object) method, which can fail to insert an element only by throwing an exception.

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offerFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offerFirst(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Inserts the specified element at the front of this deque, waiting up to the specified wait time if necessary for space to become available.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E: the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if successful, or `false` if the specified waiting time elapses before space is available |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offerLast(e: E): Boolean
```

Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. When using a capacity-restricted deque, this method is generally preferable to the #addLast(java.lang.Object) method, which can fail to insert an element only by throwing an exception.

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the element was added to this deque, else `false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |
| --- | --- |

### offerLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offerLast(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Inserts the specified element at the end of this deque, waiting up to the specified wait time if necessary for space to become available.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E: the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if successful, or `false` if the specified waiting time elapses before space is available |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### peek

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(): E?
```

Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to [peekFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#peekFirst()).

| Return ||
|----|----------------------------------------------------------|
| E? | the head of this deque, or `null` if this deque is empty |

### poll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(): E?
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to [pollFirst()](https://developer.android.com/reference/kotlin/java/util/Deque.html#pollFirst()).

| Return ||
|----|----------------------------------------------------------|
| E? | the head of this deque, or `null` if this deque is empty |

### poll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), waiting up to the specified wait time if necessary for an element to become available.

This method is equivalent to [pollFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#pollFirst(kotlin.Long,%20java.util.concurrent.TimeUnit)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

| Return ||
|---|--------------------------------------------------------------------------------------------------------|
| E | the head of this deque, or `null` if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### pollFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pollFirst(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the first element of this deque, waiting up to the specified wait time if necessary for an element to become available.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

| Return ||
|---|--------------------------------------------------------------------------------------------------------|
| E | the head of this deque, or `null` if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### pollLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pollLast(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the last element of this deque, waiting up to the specified wait time if necessary for an element to become available.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

| Return ||
|---|--------------------------------------------------------------------------------------------------------|
| E | the tail of this deque, or `null` if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### push

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun push(e: E): Unit
```

Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available.

This method is equivalent to #addFirst(java.lang.Object).

| Parameters ||
|-----|------------------------|
| `e` | E: the element to push |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### put

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(e: E): Unit
```

Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque), waiting if necessary for space to become available.

This method is equivalent to [putLast](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#putLast(java.util.concurrent.BlockingDeque.E)).

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### putFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun putFirst(e: E): Unit
```

Inserts the specified element at the front of this deque, waiting if necessary for space to become available.

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### putLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun putLast(e: E): Unit
```

Inserts the specified element at the end of this deque, waiting if necessary for space to become available.

| Parameters ||
|-----|-----------------------|
| `e` | E: the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this deque |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this deque |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(): E
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). This method differs from [poll()](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#poll()) only in that it throws an exception if this deque is empty.

This method is equivalent to [removeFirst](https://developer.android.com/reference/kotlin/java/util/Deque.html#removeFirst()).

| Return ||
|---|-------------------------------------------------|
| E | the head of the queue represented by this deque |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this deque is empty |

### remove

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(element: E?): Boolean
```

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element `e` such that `o.equals(e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

This method is equivalent to [removeFirstOccurrence](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#removeFirstOccurrence(kotlin.Any)).

| Parameters ||
|-----|---------------------------------------------------|
| `o` | element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this deque changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.UnsupportedOperationException` | if the `remove` operation is not supported by this collection |
| --- | --- |

### removeFirstOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeFirstOccurrence(o: Any?): Boolean
```

Removes the first occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the first element `e` such that `o.equals(e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if an element was removed as a result of this call |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### removeLastOccurrence

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeLastOccurrence(o: Any?): Boolean
```

Removes the last occurrence of the specified element from this deque. If the deque does not contain the element, it is unchanged. More formally, removes the last element `e` such that `o.equals(e)` (if such an element exists). Returns `true` if this deque contained the specified element (or equivalently, if this deque changed as a result of the call).

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------|
| `o` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?: element to be removed from this deque, if present |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if an element was removed as a result of this call |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this deque ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### take

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun take(): E
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), waiting if necessary until an element becomes available.

This method is equivalent to [takeFirst](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque#takeFirst()).

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### takeFirst

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun takeFirst(): E
```

Retrieves and removes the first element of this deque, waiting if necessary until an element becomes available.

| Return ||
|---|------------------------|
| E | the head of this deque |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### takeLast

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun takeLast(): E
```

Retrieves and removes the last element of this deque, waiting if necessary until an element becomes available.

| Return ||
|---|------------------------|
| E | the tail of this deque |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

## Properties

### size

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract val size: Int
```

Returns the number of elements in this deque.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this deque |
