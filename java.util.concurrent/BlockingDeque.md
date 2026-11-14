# BlockingDeque

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlockingDeque

```
interface BlockingDeque<E : Any!> : BlockingQueue<E>, Deque<E>
```

| [java.util.concurrent.BlockingDeque](BlockingDeque.md) |

| Known Direct Subclasses [LinkedBlockingDeque](LinkedBlockingDeque.md) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [LinkedBlockingDeque](LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](BlockingDeque.md) based on linked nodes. | |
| --- | --- | --- | --- | --- | --- | --- |

A [Deque](../java.util/Deque.md) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element.

`BlockingDeque` methods come in four forms, with different ways of handling operations that cannot be satisfied immediately, but may be satisfied at some point in the future: one throws an exception, the second returns a special value (either `null` or `false`, depending on the operation), the third blocks the current thread indefinitely until the operation can succeed, and the fourth blocks for only a given maximum time limit before giving up. These methods are summarized in the following table:

| First Element (Head) |||||
|---|------------------|---------------|--------|-----------|
| | Throws exception | Special value | Blocks | Times out |
| | Throws exception | Special value | Blocks | Times out |

Like any [BlockingQueue](BlockingQueue.md), a `BlockingDeque` is thread safe, does not permit null elements, and may (or may not) be capacity-constrained.

A `BlockingDeque` implementation may be used directly as a FIFO `BlockingQueue`. The methods inherited from the `BlockingQueue` interface are precisely equivalent to `BlockingDeque` methods as indicated in the following table:

| | `BlockingQueue` Method | Equivalent `BlockingDeque` Method |
| --- | --- | --- |

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a `BlockingDeque` [*happen-before*](_package.md) actions subsequent to the access or removal of that element from the `BlockingDeque` in another thread.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](BlockingDeque.md))`(`element:` `E`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and throwing an `IllegalStateException` if no space is currently available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFirst](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addLast](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](BlockingDeque.md))`(`element:` `E?`)` Returns `true` if this deque contains the specified element. |
| abstract E | [element](BlockingDeque.md))`()` Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque). |
| abstract [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](BlockingDeque.md))`()` Returns an iterator over the elements in this deque in proper sequence. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque) if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](BlockingDeque.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque), waiting up to the specified wait time if necessary for space to become available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerFirst](BlockingDeque.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Inserts the specified element at the front of this deque, waiting up to the specified wait time if necessary for space to become available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, returning `true` upon success and `false` if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offerLast](BlockingDeque.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Inserts the specified element at the end of this deque, waiting up to the specified wait time if necessary for space to become available. |
| --- | --- |
| abstract E? | [peek](BlockingDeque.md))`()` Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| abstract E? | [poll](BlockingDeque.md))`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty. |
| abstract E | [poll](BlockingDeque.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), waiting up to the specified wait time if necessary for an element to become available. |
| --- | --- |
| abstract E | [pollFirst](BlockingDeque.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Retrieves and removes the first element of this deque, waiting up to the specified wait time if necessary for an element to become available. |
| abstract E | [pollLast](BlockingDeque.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Retrieves and removes the last element of this deque, waiting up to the specified wait time if necessary for an element to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [push](BlockingDeque.md))`(`e:` `E`)` Pushes an element onto the stack represented by this deque (in other words, at the head of this deque) if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element into the queue represented by this deque (in other words, at the tail of this deque), waiting if necessary for space to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putFirst](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element at the front of this deque, waiting if necessary for space to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [putLast](BlockingDeque.md))`(`e:` `E`)` Inserts the specified element at the end of this deque, waiting if necessary for space to become available. |
| --- | --- |
| abstract E | [remove](BlockingDeque.md))`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](BlockingDeque.md))`(`element:` `E?`)` Removes the first occurrence of the specified element from this deque. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFirstOccurrence](BlockingDeque.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the first occurrence of the specified element from this deque. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeLastOccurrence](BlockingDeque.md))`(`o:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Removes the last occurrence of the specified element from this deque. |
| abstract E | [take](BlockingDeque.md))`()` Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), waiting if necessary until an element becomes available. |
| abstract E | [takeFirst](BlockingDeque.md))`()` Retrieves and removes the first element of this deque, waiting if necessary until an element becomes available. |
| --- | --- |
| abstract E | [takeLast](BlockingDeque.md))`()` Retrieves and removes the last element of this deque, waiting if necessary until an element becomes available. |

| Inherited functions ||
|---|---|
| From class [Deque](../java.util/Deque.md) |--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [descendingIterator](../java.util/Deque.md))`()` Returns an iterator over the elements in this deque in reverse sequential order. The elements will be returned in order from last (tail) to first (head). <br /> | | E | [getFirst](../java.util/Deque.md))`()` Retrieves, but does not remove, the first element of this deque. This method differs from [peekFirst](../java.util/Deque.md)) only in that it throws an exception if this deque is empty. <br /> | | E | [getLast](../java.util/Deque.md))`()` Retrieves, but does not remove, the last element of this deque. This method differs from [peekLast](../java.util/Deque.md)) only in that it throws an exception if this deque is empty. <br /> | | E? | [peekFirst](../java.util/Deque.md))`()` Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty. <br /> | | E? | [peekLast](../java.util/Deque.md))`()` Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty. <br /> | | E? | [pollFirst](../java.util/Deque.md))`()` Retrieves and removes the first element of this deque, or returns `null` if this deque is empty. <br /> | | E? | [pollLast](../java.util/Deque.md))`()` Retrieves and removes the last element of this deque, or returns `null` if this deque is empty. <br /> | | E | [pop](../java.util/Deque.md))`()` Pops an element from the stack represented by this deque. In other words, removes and returns the first element of this deque. This method is equivalent to [removeFirst()](../java.util/Deque.md)). <br /> | | E | [removeFirst](../java.util/Deque.md))`()` Retrieves and removes the first element of this deque. This method differs from [pollFirst](../java.util/Deque.md)) only in that it throws an exception if this deque is empty. <br /> | | E | [removeLast](../java.util/Deque.md))`()` Retrieves and removes the last element of this deque. This method differs from [pollLast](../java.util/Deque.md)) only in that it throws an exception if this deque is empty. <br /> | | [Deque](../java.util/Deque.md)<E> | [reversed](../java.util/Deque.md))`()` Returns a reverse-ordered [view](../java.util/Collection.md) of this collection. The encounter order of elements in the returned view is the inverse of the encounter order of elements in this collection. The reverse ordering affects all order-sensitive operations, including those on the view collections of the returned view. If the collection implementation permits modifications to this view, the modifications "write through" to the underlying collection. Changes to the underlying collection might or might not be visible in this reversed view, depending upon the implementation. <br /> | ||
| From class [BlockingQueue](BlockingQueue.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](BlockingQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` Removes all available elements from this queue and adds them to the given collection. This operation may be more efficient than repeatedly polling this queue. A failure encountered while attempting to add elements to collection `c` may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in `IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](BlockingQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes at most the given number of available elements from this queue and adds them to the given collection. A failure encountered while attempting to add elements to collection `c` may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in `IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](BlockingQueue.md))`()` Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking, or `Integer.MAX_VALUE` if there is no intrinsic limit. Note that you *cannot* always tell if an attempt to insert an element will succeed by inspecting `remainingCapacity` because it may be the case that another thread is about to insert or remove an element. <br /> | ||
| From class [Queue](../java.util/Queue.md) |----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [element](../java.util/Queue.md))`()` Retrieves, but does not remove, the head of this queue. This method differs from [peek](../java.util/Queue.md)) only in that it throws an exception if this queue is empty. <br /> | | E? | [peek](../java.util/Queue.md))`()` Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty. <br /> | | E? | [poll](../java.util/Queue.md))`()` Retrieves and removes the head of this queue, or returns `null` if this queue is empty. <br /> | | E | [remove](../java.util/Queue.md))`()` Retrieves and removes the head of this queue. This method differs from [poll()](../java.util/Queue.md)) only in that it throws an exception if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](BlockingDeque.md) Returns the number of elements in this deque. |

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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` (as specified by [Collection.add](../java.util/Collection.md))) |

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

Inserts the specified element at the front of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use [offerFirst](BlockingDeque.md)).

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

Inserts the specified element at the end of this deque if it is possible to do so immediately without violating capacity restrictions, throwing an `IllegalStateException` if no space is currently available. When using a capacity-restricted deque, it is generally preferable to use [offerLast](BlockingDeque.md)).

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

Retrieves, but does not remove, the head of the queue represented by this deque (in other words, the first element of this deque). This method differs from [peek](BlockingDeque.md)) only in that it throws an exception if this deque is empty.

This method is equivalent to [getFirst](../java.util/Deque.md)).

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

This method is equivalent to [offerLast](BlockingDeque.md)).

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

This method is equivalent to [offerLast](BlockingDeque.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E: the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
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
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
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
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
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

This method is equivalent to [peekFirst](../java.util/Deque.md)).

| Return ||
|----|----------------------------------------------------------|
| E? | the head of this deque, or `null` if this deque is empty |

### poll

Added in [API level 9](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(): E?
```

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque), or returns `null` if this deque is empty.

This method is equivalent to [pollFirst()](../java.util/Deque.md)).

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

This method is equivalent to [pollFirst](BlockingDeque.md)).

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

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
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

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
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

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

This method is equivalent to [putLast](BlockingDeque.md)).

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

Retrieves and removes the head of the queue represented by this deque (in other words, the first element of this deque). This method differs from [poll()](BlockingDeque.md)) only in that it throws an exception if this deque is empty.

This method is equivalent to [removeFirst](../java.util/Deque.md)).

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

This method is equivalent to [removeFirstOccurrence](BlockingDeque.md)).

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

This method is equivalent to [takeFirst](BlockingDeque.md)).

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
