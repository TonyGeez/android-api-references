# SynchronousQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SynchronousQueue

```
open class SynchronousQueue<E : Any!> : AbstractQueue<E>, BlockingQueue<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java.util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractQueue](../java.util/AbstractQueue.md)\<E\> ||
| | | ↳ | [java.util.concurrent.SynchronousQueue](SynchronousQueue.md) |
| --- | --- | --- | --- |

A [blocking queue](BlockingQueue.md) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. A synchronous queue does not have any internal capacity, not even a capacity of one. You cannot`peek`at a synchronous queue because an element is only present when you try to remove it; you cannot insert an element (using any method) unless another thread is trying to remove it; you cannot iterate as there is nothing to iterate. The*head* of the queue is the element that the first queued inserting thread is trying to add to the queue; if there is no such queued thread then no element is available for removal and`poll()`will return`null`. For purposes of other`Collection`methods (for example`contains`), a`SynchronousQueue`acts as an empty collection. This queue does not permit`null`elements.

Synchronous queues are similar to rendezvous channels used in CSP and Ada. They are well suited for handoff designs, in which an object running in one thread must sync up with an object running in another thread in order to hand it some information, event, or task.

This class supports an optional fairness policy for ordering waiting producer and consumer threads. By default, this ordering is not guaranteed. However, a queue constructed with fairness set to`true`grants threads access in FIFO order.

This class and its iterator implement all of the*optional* methods of the [Collection](../java.util/Collection.md) and [Iterator](../java.util/Iterator.md) interfaces.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SynchronousQueue](SynchronousQueue.md))`()` Creates a`SynchronousQueue`with nonfair access policy. |
| [SynchronousQueue](SynchronousQueue.md))`(`fair:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a`SynchronousQueue`with the specified fairness policy. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](SynchronousQueue.md))`()` Does nothing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](SynchronousQueue.md))`(`element:` `E?`)` Always returns`false`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](SynchronousQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Returns`false`unless the given collection is empty. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](SynchronousQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](SynchronousQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](SynchronousQueue.md))`()` Always returns`true`. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](SynchronousQueue.md))`()` Returns an empty iterator in which`hasNext`always returns`false`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](SynchronousQueue.md))`(`e:` `E`)` Inserts the specified element into this queue, if another thread is waiting to receive it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](SynchronousQueue.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Inserts the specified element into this queue, waiting if necessary up to the specified wait time for another thread to receive it. |
| --- | --- |
| openE? | [peek](SynchronousQueue.md))`()` Always returns`null`. |
| openE? | [poll](SynchronousQueue.md))`()` Retrieves and removes the head of this queue, if another thread is currently making an element available. |
| openE | [poll](SynchronousQueue.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Retrieves and removes the head of this queue, waiting if necessary up to the specified wait time, for another thread to insert it. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](SynchronousQueue.md))`(`e:` `E`)` Adds the specified element to this queue, waiting if necessary for another thread to receive it. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](SynchronousQueue.md))`()` Always returns zero. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](SynchronousQueue.md))`(`element:` `E?`)` Always returns`false`. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](SynchronousQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Always returns`false`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](SynchronousQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` Always returns`false`. |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | [spliterator](SynchronousQueue.md))`()` Returns an empty spliterator in which calls to [trySplit](../java.util/Spliterator.md))always return`null`. |
| --- | --- |
| openE | [take](SynchronousQueue.md))`()` Retrieves and removes the head of this queue, waiting if necessary for another thread to insert it. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](SynchronousQueue.md))`()` Returns a zero-length array. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](SynchronousQueue.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Sets the zeroth element of the specified array to`null`(if the array has non-zero length) and returns it. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](SynchronousQueue.md))`()` Always returns`"[]"`. |

| Inherited functions ||
|---|---|
| From class [AbstractQueue](../java.util/AbstractQueue.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](../java.util/AbstractQueue.md))`(`element:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. This implementation returns`true`if`offer`succeeds, else throws an`IllegalStateException`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java.util/AbstractQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this queue. Attempts to addAll of a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. This implementation iterates over the specified collection, and adds each element returned by the iterator to this queue, in turn. A runtime exception encountered while trying to add an element (including, in particular, a`null`element) may result in only some of the elements having been successfully added when the associated exception is thrown. <br /> | | E | [element](../java.util/AbstractQueue.md))`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](../java.util/Queue.md))only in that it throws an exception if this queue is empty. This implementation returns the result of`peek`unless the queue is empty. <br /> | | E | [remove](../java.util/AbstractQueue.md))`()` <br /> Retrieves and removes the head of this queue. This method differs from [poll](../java.util/Queue.md))only in that it throws an exception if this queue is empty. This implementation returns the result of`poll`unless the queue is empty. <br /> | ||
| From class [AbstractCollection](../java.util/AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java.util/AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java.util/AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](../java.util/AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java.util/AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java.util/AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java.util/AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||
| From class [Queue](../java.util/Queue.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](../java.util/Queue.md))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](../java.util/Queue.md)), which can fail to insert an element only by throwing an exception. <br /> | | E? | [peek](../java.util/Queue.md))`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](../java.util/Queue.md))`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](SynchronousQueue.md) Always returns zero. |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](../java.util/AbstractCollection.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java.util/AbstractCollection.md) <br /> | ||

## Public constructors

### SynchronousQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SynchronousQueue()
```

Creates a`SynchronousQueue`with nonfair access policy. 

### SynchronousQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SynchronousQueue(fair: Boolean)
```

Creates a`SynchronousQueue`with the specified fairness policy.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fair` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, waiting threads contend in FIFO order for access; otherwise the order is unspecified. |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Does nothing. A`SynchronousQueue`has no internal capacity.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E?): Boolean
```

Always returns`false`. A`SynchronousQueue`has no internal capacity.

| Parameters ||
|-----|-------------|
| `o` | the element |

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false` |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this queue ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### containsAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun containsAll(elements: Collection<E>): Boolean
```

Returns`false`unless the given collection is empty. A`SynchronousQueue`has no internal capacity.

| Parameters ||
|-----|----------------|
| `c` | the collection |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false`unless given collection is empty |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the types of one or more elements in the specified collection are incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified collection contains one or more null elements and this collection does not permit null elements (java.util.Collection#) or if the specified collection is null. |

### drainTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drainTo(c: MutableCollection<in E>!): Int
```

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<inE\>!:the collection to transfer elements into |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements transferred |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if addition of elements is not supported by the specified collection |
| `java.lang.ClassCastException` | if the class of an element of this queue prevents it from being added to the specified collection |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |

### drainTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun drainTo(
    c: MutableCollection<in E>!, 
    maxElements: Int
): Int
```

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<inE\>!:the collection to transfer elements into |
| `maxElements` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum number of elements to transfer |

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements transferred |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if addition of elements is not supported by the specified collection |
| `java.lang.ClassCastException` | if the class of an element of this queue prevents it from being added to the specified collection |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |

### isEmpty

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Always returns`true`. A`SynchronousQueue`has no internal capacity.

| Return ||
|------------------------------------------------------------------------------------|--------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an empty iterator in which`hasNext`always returns`false`.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|-------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an empty iterator |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(e: E): Boolean
```

Inserts the specified element into this queue, if another thread is waiting to receive it.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was added to this queue, else`false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| --- | --- |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Inserts the specified element into this queue, waiting if necessary up to the specified wait time for another thread to receive it.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, or`false`if the specified waiting time elapses before a consumer appears |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

### peek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peek(): E?
```

Always returns`null`. A`SynchronousQueue`does not return elements unless actively waited on.

| Return ||
|----|--------|
| E? | `null` |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): E?
```

Retrieves and removes the head of this queue, if another thread is currently making an element available.

| Return ||
|----|------------------------------------------------------------|
| E? | the head of this queue, or`null`if no element is available |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the head of this queue, waiting if necessary up to the specified wait time, for another thread to insert it.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|----------------------------------------------------------------------------------------------------|
| E | the head of this queue, or`null`if the specified waiting time elapses before an element is present |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(e: E): Unit
```

Adds the specified element to this queue, waiting if necessary for another thread to receive it.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

### remainingCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remainingCapacity(): Int
```

Always returns zero. A`SynchronousQueue`has no internal capacity.

| Return ||
|----------------------------------------------------------------------------|------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Always returns`false`. A`SynchronousQueue`has no internal capacity.

| Parameters ||
|-----|-----------------------|
| `o` | the element to remove |

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false` |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this queue ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

Always returns`false`. A`SynchronousQueue`has no internal capacity.

| Parameters ||
|-----|----------------|
| `c` | the collection |

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false` |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`method is not supported by this collection |
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not support null elements (java.util.Collection#) or if the specified collection is null |
| --- | --- |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainAll(elements: Collection<E>): Boolean
```

Always returns`false`. A`SynchronousQueue`has no internal capacity.

| Parameters ||
|-----|----------------|
| `c` | the collection |

| Return ||
|------------------------------------------------------------------------------------|---------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `false` |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`retainAll`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not permit null elements (java.util.Collection#) or if the specified collection is null |
| --- | --- |

### spliterator

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun spliterator(): Spliterator<E>
```

Returns an empty spliterator in which calls to [trySplit](../java.util/Spliterator.md))always return`null`.

| Return ||
|----------------------------------------------------------------------------------------------|----------------------|
| [Spliterator](../java.util/Spliterator.md)<E> | an empty spliterator |

### take

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun take(): E
```

Retrieves and removes the head of this queue, waiting if necessary for another thread to insert it.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns a zero-length array.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | a zero-length array |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Sets the zeroth element of the specified array to`null`(if the array has non-zero length) and returns it.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array |

| Return ||
|-----------------------------------------------------------------------------------|---------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | the specified array |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of any element in this collection is not assignable to the [runtime component type](../java.lang/Class.md))of the specified array |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Always returns`"[]"`.

| Return ||
|----------------------------------------------------------------------------------|--------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `"[]"` |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Always returns zero. A`SynchronousQueue`has no internal capacity.

| Return ||
|----------------------------------------------------------------------------|------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | zero |
