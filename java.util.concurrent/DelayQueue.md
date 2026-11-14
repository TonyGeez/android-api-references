# DelayQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DelayQueue

```
open class DelayQueue<E : Delayed!> : AbstractQueue<E>, BlockingQueue<E>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#)\<E\> |||
| | ↳ | [java.util.AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#)\<E\> ||
| | | ↳ | [java.util.concurrent.DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#) |
| --- | --- | --- | --- |

An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) elements, in which an element generally becomes eligible for removal when its delay has expired.

An element is considered*expired* when its`getDelay(TimeUnit.NANOSECONDS)`method would return a value less than or equal to zero.

An element is considered the*head*of the queue if it is the element with the earliest expiration time, whether in the past or the future, if there is such an element.

An element is considered the*expired head* of the queue if it is the*expired* element with the earliest expiration time in the past, if there is such an element. The*expired head* , when present, is also the*head*.

While this class implements the`BlockingQueue`interface, it intentionally violates the general contract of`BlockingQueue`, in that the following methods disregard the presence of unexpired elements and only ever remove the*expired head*:

- [poll()](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#poll())
- [poll(long,java.util.concurrent.TimeUnit)](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))
- [take()](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#take())
- [remove()](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#remove())

All other methods operate on both expired and unexpired elements. For example, the [size()](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#size:kotlin.Int) method returns the count of all elements. Method [peek()](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#peek())may return the (non-null)*head* even when`take()`would block waiting for that element to expire.

This queue does not permit null elements.

This class and its iterator implement all of the*optional* methods of the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) and [Iterator](https://developer.android.com/reference/kotlin/java/util/Iterator.html#) interfaces. The Iterator provided in method #iterator() is*not*guaranteed to traverse the elements of the DelayQueue in any particular order.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#DelayQueue())`()` Creates a new`DelayQueue`that is initially empty. |
| [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#DelayQueue(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Creates a`DelayQueue`initially containing the elements of the given collection of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) instances. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#add(java.util.concurrent.DelayQueue.E))`(`element:` `E`)` Inserts the specified element into this delay queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#clear())`()` Atomically removes all of the elements from this delay queue. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#drainTo(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#drainTo(kotlin.collections.MutableCollection,%20kotlin.Int))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#iterator())`()` Returns an iterator over all the elements (both expired and unexpired) in this queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#offer(java.util.concurrent.DelayQueue.E))`(`e:` `E`)` Inserts the specified element into this delay queue. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#offer(java.util.concurrent.DelayQueue.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Inserts the specified element into this delay queue. |
| openE? | [peek](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#peek())`()` Retrieves, but does not remove, the [head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#head) of this queue, or returns`null`if this queue is empty. |
| openE? | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#poll())`()` Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, or returns`null`if this queue has no [expired elements](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired). |
| --- | --- |
| openE | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, waiting if necessary until an [expired element](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired) is available on this queue, or the specified wait time expires. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#put(java.util.concurrent.DelayQueue.E))`(`e:` `E`)` Inserts the specified element into this delay queue. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#remainingCapacity())`()` Always returns`Integer.MAX_VALUE`because a`DelayQueue`is not capacity constrained. |
| --- | --- |
| openE | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#remove())`()` Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, or throws an exception if this queue has no [expired elements](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired). |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#remove(java.util.concurrent.DelayQueue.E))`(`element:` `E?`)` Removes a single instance of the specified element from this queue, if it is present, whether or not it has expired. |
| openE | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#take())`()` Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, waiting if necessary until an [expired element](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired) is available on this queue. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#toArray())`()` Returns an array containing all of the elements in this queue. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this queue; the runtime type of the returned array is that of the specified array. |

| Inherited functions ||
|---|---|
| From class [AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#addAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this queue. Attempts to addAll of a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. This implementation iterates over the specified collection, and adds each element returned by the iterator to this queue, in turn. A runtime exception encountered while trying to add an element (including, in particular, a`null`element) may result in only some of the elements having been successfully added when the associated exception is thrown. <br /> | | E | [element](https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#element())`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())only in that it throws an exception if this queue is empty. This implementation returns the result of`peek`unless the queue is empty. <br /> | ||
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#contains(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#containsAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#isEmpty())`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#iterator())`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#remove(java.util.AbstractCollection.E))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#removeAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#retainAll(kotlin.collections.Collection))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#toArray())`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](https://developer.android.com/reference/kotlin/java/lang/Class.html#getComponentType())is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#toArray(kotlin.Array))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#toString())`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](https://developer.android.com/reference/kotlin/java/lang/String.html#valueOf(kotlin.Any)). <br /> | ||
| From class [Queue](https://developer.android.com/reference/kotlin/java/util/Queue.html#) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/Queue.html#offer(java.util.Queue.E))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](https://developer.android.com/reference/kotlin/java/util/Queue.html#add(java.util.Queue.E)), which can fail to insert an element only by throwing an exception. <br /> | | E? | [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll())`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#size:kotlin.Int) <br /> |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#size:kotlin.Int) <br /> | ||

## Public constructors

### DelayQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DelayQueue()
```

Creates a new`DelayQueue`that is initially empty. 

### DelayQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DelayQueue(c: MutableCollection<out E>!)
```

Creates a`DelayQueue`initially containing the elements of the given collection of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) instances.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:the collection of elements to initially contain |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Inserts the specified element into this delay queue.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection.html#add(java.util.Collection.E))) |

| Exceptions ||
|-------------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Atomically removes all of the elements from this delay queue. The queue will be empty after this call returns. Elements with an unexpired delay are not waited for; they are simply discarded from the queue.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

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

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over all the elements (both expired and unexpired) in this queue. The iterator does not return the elements in any particular order.

The returned iterator is [*weakly consistent*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#Weakly).

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this queue |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(e: E): Boolean
```

Inserts the specified element into this delay queue.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|--------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` |

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

Inserts the specified element into this delay queue. As the queue is unbounded this method will never block.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):This parameter is ignored as the method never blocks |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:This parameter is ignored as the method never blocks |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` |

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

Retrieves, but does not remove, the [head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#head) of this queue, or returns`null`if this queue is empty. Unlike`poll`, if no expired elements are available in the queue, this method returns the element that will expire next, if one exists.

| Return ||
|----|---------------------------------------------------------|
| E? | the*head* of this queue, or`null`if this queue is empty |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): E?
```

Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, or returns`null`if this queue has no [expired elements](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired).

| Return ||
|----|----------------------------------------------------------------------------------------------|
| E? | the*expired head* of this queue, or`null`if this queue has no elements with an expired delay |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, waiting if necessary until an [expired element](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired) is available on this queue, or the specified wait time expires.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|------------------------------------------------------------------------------------------------------------------------------------------|
| E | the*expired head* of this queue, or`null`if the specified waiting time elapses before an element with an expired delay becomes available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun put(e: E): Unit
```

Inserts the specified element into this delay queue. As the queue is unbounded this method will never block.

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

Always returns`Integer.MAX_VALUE`because a`DelayQueue`is not capacity constrained.

| Return ||
|----------------------------------------------------------------------------|---------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `Integer.MAX_VALUE` |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(): E
```

Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, or throws an exception if this queue has no [expired elements](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired).

| Return ||
|---|--------------------------------|
| E | the*expired head*of this queue |

| Exceptions ||
|------------------------------------|-----------------------------------------------------|
| `java.util.NoSuchElementException` | if this queue has no elements with an expired delay |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this queue, if it is present, whether or not it has expired.

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

### take

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun take(): E
```

Retrieves and removes the [expired head](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired-head) of this queue, waiting if necessary until an [expired element](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#expired) is available on this queue.

| Return ||
|---|--------------------------------|
| E | the*expired head*of this queue |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this queue. The returned array elements are in no particular order.

The returned array will be "safe" in that no references to it are maintained by this queue. (In other words, this method must allocate a new array). The caller is thus free to modify the returned array.

This method acts as bridge between array-based and collection-based APIs.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | an array containing all of the elements in this queue |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : Any!> toArray(a: Array<T>): Array<T>
```

Returns an array containing all of the elements in this queue; the runtime type of the returned array is that of the specified array. The returned array elements are in no particular order. If the queue fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this queue.

If this queue fits in the specified array with room to spare (i.e., the array has more elements than this queue), the element in the array immediately following the end of the queue is set to`null`.

Like the [toArray()](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue#toArray())method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

The following code can be used to dump a delay queue into a newly allocated array of`Delayed`: 

```kotlin
<code>Delayed[] a = q.toArray(new Delayed[0]);</code>
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

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open val size: Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of elements in this collection |
