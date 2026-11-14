# LinkedTransferQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkedTransferQueue

```
open class LinkedTransferQueue<E : Any!> : AbstractQueue<E>, Serializable, TransferQueue<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java.util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractQueue](../java.util/AbstractQueue.md)\<E\> ||
| | | ↳ | [java.util.concurrent.LinkedTransferQueue](LinkedTransferQueue.md) |
| --- | --- | --- | --- |

An unbounded [TransferQueue](TransferQueue.md) based on linked nodes. This queue orders elements FIFO (first-in-first-out) with respect to any given producer. The*head* of the queue is that element that has been on the queue the longest time for some producer. The*tail*of the queue is that element that has been on the queue the shortest time for some producer.

Beware that, unlike in most collections, the`size`method is*NOT*a constant-time operation. Because of the asynchronous nature of these queues, determining the current number of elements requires a traversal of the elements, and so may report inaccurate results if this collection is modified during traversal.

Bulk operations that add, remove, or examine multiple elements, such as [addAll](../java.util/AbstractQueue.md)), [removeIf](LinkedTransferQueue.md))or [forEach](LinkedTransferQueue.md)), are*not* guaranteed to be performed atomically. For example, a`forEach`traversal concurrent with an`addAll`operation might observe only some of the added elements.

This class and its iterator implement all of the*optional* methods of the [Collection](../java.util/Collection.md) and [Iterator](../java.util/Iterator.md) interfaces.

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a`LinkedTransferQueue` [*happen-before*](_package.md) actions subsequent to the access or removal of that element from the`LinkedTransferQueue`in another thread.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkedTransferQueue](LinkedTransferQueue.md))`()` Creates an initially empty`LinkedTransferQueue`. |
| [LinkedTransferQueue](LinkedTransferQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Creates a`LinkedTransferQueue`initially containing the elements of the given collection, added in traversal order of the collection's iterator. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](LinkedTransferQueue.md))`(`element:` `E`)` Inserts the specified element at the tail of this queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](LinkedTransferQueue.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](LinkedTransferQueue.md))`(`element:` `E?`)` Returns`true`if this queue contains the specified element. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](LinkedTransferQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](LinkedTransferQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](LinkedTransferQueue.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `E>`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWaitingConsumerCount](LinkedTransferQueue.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWaitingConsumer](LinkedTransferQueue.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](LinkedTransferQueue.md))`()` Returns`true`if this queue contains no elements. |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](LinkedTransferQueue.md))`()` Returns an iterator over the elements in this queue in proper sequence. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](LinkedTransferQueue.md))`(`e:` `E`)` Inserts the specified element at the tail of this queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](LinkedTransferQueue.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Inserts the specified element at the tail of this queue. |
| --- | --- |
| openE? | [peek](LinkedTransferQueue.md))`()` <br /> |
| openE? | [poll](LinkedTransferQueue.md))`()` <br /> |
| openE | [poll](LinkedTransferQueue.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](LinkedTransferQueue.md))`(`e:` `E`)` Inserts the specified element at the tail of this queue. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](LinkedTransferQueue.md))`()` Always returns`Integer.MAX_VALUE`because a`LinkedTransferQueue`is not capacity constrained. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](LinkedTransferQueue.md))`(`element:` `E?`)` Removes a single instance of the specified element from this queue, if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](LinkedTransferQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](LinkedTransferQueue.md))`(`filter:` ` [Predicate](../java.util.function/Predicate.md)<in` `E>`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](LinkedTransferQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| --- | --- |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | [spliterator](LinkedTransferQueue.md))`()` Returns a [Spliterator](../java.util/Spliterator.md) over the elements in this queue. |
| openE | [take](LinkedTransferQueue.md))`()` <br /> |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](LinkedTransferQueue.md))`()` Returns an array containing all of the elements in this queue, in proper sequence. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](LinkedTransferQueue.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this queue, in proper sequence; the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](LinkedTransferQueue.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transfer](LinkedTransferQueue.md))`(`e:` `E`)` Transfers the element to a consumer, waiting if necessary to do so. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryTransfer](LinkedTransferQueue.md))`(`e:` `E`)` Transfers the element to a waiting consumer immediately, if possible. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryTransfer](LinkedTransferQueue.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Transfers the element to a consumer if it is possible to do so before the timeout elapses. |

| Inherited functions ||
|---|---|
| From class [AbstractQueue](../java.util/AbstractQueue.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](../java.util/AbstractQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this queue. Attempts to addAll of a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. This implementation iterates over the specified collection, and adds each element returned by the iterator to this queue, in turn. A runtime exception encountered while trying to add an element (including, in particular, a`null`element) may result in only some of the elements having been successfully added when the associated exception is thrown. <br /> | | E | [element](../java.util/AbstractQueue.md))`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](../java.util/Queue.md))only in that it throws an exception if this queue is empty. This implementation returns the result of`peek`unless the queue is empty. <br /> | | E | [remove](../java.util/AbstractQueue.md))`()` <br /> Retrieves and removes the head of this queue. This method differs from [poll](../java.util/Queue.md))only in that it throws an exception if this queue is empty. This implementation returns the result of`poll`unless the queue is empty. <br /> | ||
| From class [AbstractCollection](../java.util/AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](../java.util/AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](../java.util/AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](../java.util/AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](../java.util/AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](../java.util/AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](../java.util/AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](../java.util/AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java.util/AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||
| From class [Queue](../java.util/Queue.md) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](../java.util/Queue.md))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](../java.util/Queue.md)), which can fail to insert an element only by throwing an exception. <br /> | | E? | [peek](../java.util/Queue.md))`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](../java.util/Queue.md))`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](LinkedTransferQueue.md) Returns the number of elements in this queue. |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](../java.util/AbstractCollection.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](../java.util/AbstractCollection.md) <br /> | ||

## Public constructors

### LinkedTransferQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedTransferQueue()
```

Creates an initially empty`LinkedTransferQueue`. 

### LinkedTransferQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkedTransferQueue(c: MutableCollection<out E>!)
```

Creates a`LinkedTransferQueue`initially containing the elements of the given collection, added in traversal order of the collection's iterator.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:the collection of elements to initially contain |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

## Public methods

### add

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Inserts the specified element at the tail of this queue. As the queue is unbounded, this method will never throw [IllegalStateException](../java.lang/IllegalStateException.md) or return`false`.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](../java.util/Collection.md))) |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### clear

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### contains

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun contains(element: E?): Boolean
```

Returns`true`if this queue contains the specified element. More formally, returns`true`if and only if this queue contains at least one element`e`such that`o.equals(e)`.

| Parameters ||
|-----|----------------------------------------------------|
| `o` | object to be checked for containment in this queue |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this queue contains the specified element |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this queue ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### drainTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: Consumer<in E>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inE\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### getWaitingConsumerCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWaitingConsumerCount(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of consumers waiting to receive elements |

### hasWaitingConsumer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasWaitingConsumer(): Boolean
```

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there is at least one waiting consumer |

### isEmpty

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isEmpty(): Boolean
```

Returns`true`if this queue contains no elements.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this queue contains no elements |

### iterator

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this queue in proper sequence. The elements will be returned in order from first (head) to last (tail).

The returned iterator is [*weakly consistent*](_package.md).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this queue in proper sequence |

### offer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(e: E): Boolean
```

Inserts the specified element at the tail of this queue. As the queue is unbounded, this method will never return`false`.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Queue.offer](../java.util/Queue.md))) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| --- | --- |

### offer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Inserts the specified element at the tail of this queue. As the queue is unbounded, this method will never block or return`false`.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [BlockingQueue.offer](BlockingQueue.md))) |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

### peek

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peek(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this queue, or`null`if this queue is empty |

### poll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this queue, or`null`if this queue is empty |

### poll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| E | the head of this queue, or`null`if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### put

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(e: E): Unit
```

Inserts the specified element at the tail of this queue. As the queue is unbounded, this method will never block.

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remainingCapacity(): Int
```

Always returns`Integer.MAX_VALUE`because a`LinkedTransferQueue`is not capacity constrained.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `Integer.MAX_VALUE`(as specified by [BlockingQueue.remainingCapacity()](BlockingQueue.md))) |

### remove

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this queue, if it is present. More formally, removes an element`e`such that`o.equals(e)`, if this queue contains one or more such elements. Returns`true`if this queue contained the specified element (or equivalently, if this queue changed as a result of the call).

| Parameters ||
|-----|---------------------------------------------------|
| `o` | element to be removed from this queue, if present |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this queue changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this queue ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeAll(elements: Collection<E>): Boolean
```

| Parameters ||
|-----|-------------------------------------------------------------------|
| `c` | collection containing elements to be removed from this collection |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection changed as a result of the call |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`removeAll`method is not supported by this collection |
| `java.lang.ClassCastException` | if the types of one or more elements in this collection are incompatible with the specified collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if this collection contains one or more null elements and the specified collection does not support null elements (java.util.Collection#) or if the specified collection is null |
| --- | --- |

### removeIf

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun removeIf(filter: Predicate<in E>): Boolean
```

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](../java.util.function/Predicate.md)\<inE\>:a predicate which returns`true`for elements to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements were removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if elements cannot be removed from this collection. Implementations may throw this exception if a matching element cannot be removed or if, in general, removal is not supported. |

### retainAll

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun retainAll(elements: Collection<E>): Boolean
```

| Parameters ||
|-----|------------------------------------------------------------------|
| `c` | collection containing elements to be retained in this collection |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this collection changed as a result of the call |

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

Returns a [Spliterator](../java.util/Spliterator.md) over the elements in this queue.

The returned spliterator is [*weakly consistent*](_package.md).

The`Spliterator`reports [Spliterator.CONCURRENT](../java.util/Spliterator.md), [Spliterator.ORDERED](../java.util/Spliterator.md), and [Spliterator.NONNULL](../java.util/Spliterator.md).

| Return ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| [Spliterator](../java.util/Spliterator.md)<E> | a`Spliterator`over the elements in this queue |

### take

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun take(): E
```

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### toArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this queue, in proper sequence.

The returned array will be "safe" in that no references to it are maintained by this queue. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all of the elements in this queue |

### toArray

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this queue, in proper sequence; the runtime type of the returned array is that of the specified array. If the queue fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this queue.

If this queue fits in the specified array with room to spare (i.e., the array has more elements than this queue), the element in the array immediately following the end of the queue is set to`null`.

Like the [toArray()](LinkedTransferQueue.md))method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose`x`is a queue known to contain only strings. The following code can be used to dump the queue into a newly allocated array of`String`: 

```kotlin
<code>String[] y = x.toArray(new String[0]);</code>
```
Note that`toArray(new Object[0])`is identical in function to`toArray()`.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of the queue are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose |

| Return ||
|-----------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | an array containing all of the elements in this queue |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.ArrayStoreException` | if the runtime type of the specified array is not a supertype of the runtime type of every element in this queue |
| `java.lang.NullPointerException` | if the specified array is null |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### transfer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun transfer(e: E): Unit
```

Transfers the element to a consumer, waiting if necessary to do so.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](LinkedTransferQueue.md))or timed [poll](LinkedTransferQueue.md))), else inserts the specified element at the tail of this queue and waits until the element is received by a consumer.

| Parameters ||
|-----|---------------------------|
| `e` | E:the element to transfer |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case the element is not left enqueued |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

### tryTransfer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryTransfer(e: E): Boolean
```

Transfers the element to a waiting consumer immediately, if possible.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](LinkedTransferQueue.md))or timed [poll](LinkedTransferQueue.md))), otherwise returning`false`without enqueuing the element.

| Parameters ||
|-----|---------------------------|
| `e` | E:the element to transfer |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was transferred, else`false` |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| --- | --- |

### tryTransfer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun tryTransfer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Transfers the element to a consumer if it is possible to do so before the timeout elapses.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](LinkedTransferQueue.md))or timed [poll](LinkedTransferQueue.md))), else inserts the specified element at the tail of this queue and waits until the element is received by a consumer, returning`false`if the specified wait time elapses before the element can be transferred.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to transfer |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](TimeUnit.md)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, or`false`if the specified waiting time elapses before completion, in which case the element is not left enqueued |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting, in which case the element is not left enqueued |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

## Properties

### size

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

Returns the number of elements in this queue. If this queue contains more than`Integer.MAX_VALUE`elements, returns`Integer.MAX_VALUE`.

Beware that, unlike in most collections, this method is*NOT*a constant-time operation. Because of the asynchronous nature of these queues, determining the current number of elements requires an O(n) traversal.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this queue |
