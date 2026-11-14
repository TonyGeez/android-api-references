# PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PriorityQueue

```
open class PriorityQueue<E : Any!> : AbstractQueue<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractQueue](AbstractQueue.md)\<E\> ||
| | | ↳ | [java.util.PriorityQueue](PriorityQueue.md) |
| --- | --- | --- | --- |

An unbounded priority [queue](Queue.md) based on a priority heap. The elements of the priority queue are ordered according to their [natural ordering](../java.lang/Comparable.md), or by a [Comparator](Comparator.md) provided at queue construction time, depending on which constructor is used. A priority queue does not permit`null`elements. A priority queue relying on natural ordering also does not permit insertion of non-comparable objects (doing so may result in`ClassCastException`).

The*head* of this queue is the*least* element with respect to the specified ordering. If multiple elements are tied for least value, the head is one of those elements -- ties are broken arbitrarily. The queue retrieval operations`poll`,`remove`,`peek`, and`element`access the element at the head of the queue.

A priority queue is unbounded, but has an internal*capacity*governing the size of an array used to store the elements on the queue. It is always at least as large as the queue size. As elements are added to a priority queue, its capacity grows automatically. The details of the growth policy are not specified.

This class and its iterator implement all of the*optional* methods of the [Collection](Collection.md) and [Iterator](Iterator.md) interfaces. The Iterator provided in method #iterator() and the Spliterator provided in method #spliterator() are*not* guaranteed to traverse the elements of the priority queue in any particular order. If you need ordered traversal, consider using`Arrays.sort(pq.toArray())`.

**Note that this implementation is not synchronized.** Multiple threads should not access a`PriorityQueue`instance concurrently if any of the threads modifies the queue. Instead, use the thread-safe class.

Implementation note: this implementation provides O(log(n)) time for the enqueuing and dequeuing methods (`offer`,`poll`,`remove()`and`add`); linear time for the`remove(Object)`and`contains(Object)`methods; and constant time for the retrieval methods (`peek`,`element`, and`size`).

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PriorityQueue](PriorityQueue.md))`()` Creates a`PriorityQueue`with the default initial capacity (11) that orders its elements according to their [natural ordering](../java.lang/Comparable.md). |
| [PriorityQueue](PriorityQueue.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`PriorityQueue`with the specified initial capacity that orders its elements according to their [natural ordering](../java.lang/Comparable.md). |
| [PriorityQueue](PriorityQueue.md))`(`initialCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `comparator:` ` [Comparator](Comparator.md)<in` `E>!`)` Creates a`PriorityQueue`with the specified initial capacity that orders its elements according to the specified comparator. |
| [PriorityQueue](PriorityQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<out` `E>!`)` Creates a`PriorityQueue`containing the elements in the specified collection. |
| [PriorityQueue](PriorityQueue.md))`(`comparator:` ` [Comparator](Comparator.md)<in` `E>!`)` Creates a`PriorityQueue`with the default initial capacity and whose elements are ordered according to the specified comparator. |
| [PriorityQueue](PriorityQueue.md))`(`c:` ` [PriorityQueue](PriorityQueue.md)<out` `E>!`)` Creates a`PriorityQueue`containing the elements in the specified priority queue. |
| [PriorityQueue](PriorityQueue.md))`(`c:` ` [SortedSet](SortedSet.md)<out` `E>!`)` Creates a`PriorityQueue`containing the elements in the specified sorted set. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](PriorityQueue.md))`(`element:` `E`)` Inserts the specified element into this priority queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](PriorityQueue.md))`()` Removes all of the elements from this priority queue. |
| open [Comparator](Comparator.md)\<inE\>! | [comparator](PriorityQueue.md))`()` Returns the comparator used to order the elements in this queue, or`null`if this queue is sorted according to the [natural ordering](../java.lang/Comparable.md) of its elements. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](PriorityQueue.md))`(`element:` `E?`)` Returns`true`if this queue contains the specified element. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [forEach](PriorityQueue.md))`(`action:` ` [Consumer](../java.util.function/Consumer.md)<in` `E>`)` <br /> |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | [iterator](PriorityQueue.md))`()` Returns an iterator over the elements in this queue. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](PriorityQueue.md))`(`e:` `E`)` Inserts the specified element into this priority queue. |
| openE? | [peek](PriorityQueue.md))`()` <br /> |
| openE? | [poll](PriorityQueue.md))`()` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](PriorityQueue.md))`(`element:` `E?`)` Removes a single instance of the specified element from this queue, if it is present. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](PriorityQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeIf](PriorityQueue.md))`(`filter:` ` [Predicate](../java.util.function/Predicate.md)<in` `E>`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](PriorityQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> |
| [Spliterator](Spliterator.md)\<E\> | [spliterator](PriorityQueue.md))`()` Creates a* [late-binding](Spliterator.md)* and*fail-fast* [Spliterator](Spliterator.md) over the elements in this queue. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | [toArray](PriorityQueue.md))`()` Returns an array containing all of the elements in this queue. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | [toArray](PriorityQueue.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` Returns an array containing all of the elements in this queue; the runtime type of the returned array is that of the specified array. |

| Inherited functions ||
|---|---|
| From class [AbstractQueue](AbstractQueue.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addAll](AbstractQueue.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Adds all of the elements in the specified collection to this queue. Attempts to addAll of a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. This implementation iterates over the specified collection, and adds each element returned by the iterator to this queue, in turn. A runtime exception encountered while trying to add an element (including, in particular, a`null`element) may result in only some of the elements having been successfully added when the associated exception is thrown. <br /> | | E | [element](AbstractQueue.md))`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](Queue.md))only in that it throws an exception if this queue is empty. This implementation returns the result of`peek`unless the queue is empty. <br /> | | E | [remove](AbstractQueue.md))`()` <br /> Retrieves and removes the head of this queue. This method differs from [poll](Queue.md))only in that it throws an exception if this queue is empty. This implementation returns the result of`poll`unless the queue is empty. <br /> | ||
| From class [AbstractCollection](AbstractCollection.md) |-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](AbstractCollection.md))`(`element:` `E?`)` <br /> Returns`true`if this collection contains the specified element. More formally, returns`true`if and only if this collection contains at least one element`e`such that`Objects.equals(o, e)`. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [containsAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Returns`true`if this collection contains all of the elements in the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isEmpty](AbstractCollection.md))`()` <br /> Returns`true`if this collection contains no elements. <br /> | | [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | [iterator](AbstractCollection.md))`()` <br /> Returns an iterator over the elements contained in this collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](AbstractCollection.md))`(`element:` `E?`)` <br /> Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element`e`such that`Objects.equals(o, e)`, if this collection contains one or more such elements. Returns`true`if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [retainAll](AbstractCollection.md))`(`elements:` ` [Collection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-collection/index.html)<E>`)` <br /> Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!> | [toArray](AbstractCollection.md))`()` <br /> Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md))is`Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T> | [toArray](AbstractCollection.md))`(`a:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)<T>`)` <br /> Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to`null`. (This is useful in determining the length of this collection*only* if the caller knows that this collection does not contain any`null`elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](AbstractCollection.md))`()` <br /> Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters`", "`(comma and space). Elements are converted to strings as by [String.valueOf(Object)](../java.lang/String.md)). <br /> | ||
| From class [Queue](Queue.md) |------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](Queue.md))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](Queue.md)), which can fail to insert an element only by throwing an exception. <br /> | | E? | [peek](Queue.md))`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](Queue.md))`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](PriorityQueue.md) <br /> |

| Inherited properties ||
|---|---|
| From class [AbstractCollection](AbstractCollection.md) |----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [size](AbstractCollection.md) <br /> | ||

## Public constructors

### PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue()
```

Creates a`PriorityQueue`with the default initial capacity (11) that orders its elements according to their [natural ordering](../java.lang/Comparable.md). 

### PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue(initialCapacity: Int)
```

Creates a`PriorityQueue`with the specified initial capacity that orders its elements according to their [natural ordering](../java.lang/Comparable.md).

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity for this priority queue |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if`initialCapacity`is less than 1 |

### PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue(
    initialCapacity: Int, 
    comparator: Comparator<in E>!)
```

Creates a`PriorityQueue`with the specified initial capacity that orders its elements according to the specified comparator.

| Parameters ||
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `initialCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the initial capacity for this priority queue |
| `comparator` | [Comparator](Comparator.md)\<inE\>!:the comparator that will be used to order this priority queue. If`null`, the [natural ordering](../java.lang/Comparable.md) of the elements will be used. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | if`initialCapacity`is less than 1 |

### PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue(c: MutableCollection<out E>!)
```

Creates a`PriorityQueue`containing the elements in the specified collection. If the specified collection is an instance of a [SortedSet](SortedSet.md) or is another`PriorityQueue`, this priority queue will be ordered according to the same ordering. Otherwise, this priority queue will be ordered according to the [natural ordering](../java.lang/Comparable.md) of its elements.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<outE\>!:the collection whose elements are to be placed into this priority queue |

| Exceptions ||
|----------------------------------|----------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if elements of the specified collection cannot be compared to one another according to the priority queue's ordering |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

### PriorityQueue

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue(comparator: Comparator<in E>!)
```

Creates a`PriorityQueue`with the default initial capacity and whose elements are ordered according to the specified comparator.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `comparator` | [Comparator](Comparator.md)\<inE\>!:the comparator that will be used to order this priority queue. If`null`, the [natural ordering](../java.lang/Comparable.md) of the elements will be used. |

### PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue(c: PriorityQueue<out E>!)
```

Creates a`PriorityQueue`containing the elements in the specified priority queue. This priority queue will be ordered according to the same ordering as the given priority queue.

| Parameters ||
|-----|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [PriorityQueue](PriorityQueue.md)\<outE\>!:the priority queue whose elements are to be placed into this priority queue |

| Exceptions ||
|----------------------------------|-------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if elements of`c`cannot be compared to one another according to`c`'s ordering |
| `java.lang.NullPointerException` | if the specified priority queue or any of its elements are null |

### PriorityQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
PriorityQueue(c: SortedSet<out E>!)
```

Creates a`PriorityQueue`containing the elements in the specified sorted set. This priority queue will be ordered according to the same ordering as the given sorted set.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `c` | [SortedSet](SortedSet.md)\<outE\>!:the sorted set whose elements are to be placed into this priority queue |

| Exceptions ||
|----------------------------------|------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if elements of the specified sorted set cannot be compared to one another according to the sorted set's ordering |
| `java.lang.NullPointerException` | if the specified sorted set or any of its elements are null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(element: E): Boolean
```

Inserts the specified element into this priority queue.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](Collection.md))) |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the specified element cannot be compared with elements currently in this priority queue according to the priority queue's ordering |
| `java.lang.NullPointerException` | if the specified element is null |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clear(): Unit
```

Removes all of the elements from this priority queue. The queue will be empty after this call returns.

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`clear`operation is not supported by this collection |

### comparator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun comparator(): Comparator<in E>!
```

Returns the comparator used to order the elements in this queue, or`null`if this queue is sorted according to the [natural ordering](../java.lang/Comparable.md) of its elements.

| Return ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [Comparator](Comparator.md)<in` `E>! | the comparator used to order this queue, or`null`if this queue is sorted according to the natural ordering of its elements |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements (java.util.Collection#) |

### forEach

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun forEach(action: Consumer<in E>): Unit
```

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|
| `action` | [Consumer](../java.util.function/Consumer.md)\<inE\>:The action to be performed for each element |

| Exceptions ||
|----------------------------------|---------------------------------|
| `java.lang.NullPointerException` | if the specified action is null |

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this queue. The iterator does not return the elements in any particular order.

| Return ||
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)<E> | an iterator over the elements in this queue |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(e: E): Boolean
```

Inserts the specified element into this priority queue.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Queue.offer](Queue.md))) |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the specified element cannot be compared with elements currently in this priority queue according to the priority queue's ordering |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| --- | --- |

### peek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peek(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this queue, or`null`if this queue is empty |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun poll(): E?
```

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this queue, or`null`if this queue is empty |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this queue, if it is present. More formally, removes an element`e`such that`o.equals(e)`, if this queue contains one or more such elements. Returns`true`if and only if this queue contained the specified element (or equivalently, if this queue changed as a result of the call).

| Parameters ||
|-----|---------------------------------------------------|
| `o` | element to be removed from this queue, if present |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this queue changed as a result of the call |

| Exceptions ||
|-------------------------------------------|------------------------------------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the type of the specified element is incompatible with this collection (java.util.Collection#) |
| `java.lang.NullPointerException` | if the specified element is null and this collection does not permit null elements (java.util.Collection#) |
| `java.lang.UnsupportedOperationException` | if the`remove`operation is not supported by this collection |
| --- | --- |

### removeAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `filter` | [Predicate](../java.util.function/Predicate.md)\<inE\>:a predicate which returns`true`for elements to be removed |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if any elements were removed |

| Exceptions ||
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.NullPointerException` | if the specified filter is null |
| `java.lang.UnsupportedOperationException` | if elements cannot be removed from this collection. Implementations may throw this exception if a matching element cannot be removed or if, in general, removal is not supported. |

### retainAll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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
fun spliterator(): Spliterator<E>
```

Creates a* [late-binding](Spliterator.md)* and*fail-fast* [Spliterator](Spliterator.md) over the elements in this queue. The spliterator does not traverse elements in any particular order (the [ORDERED](Spliterator.md) characteristic is not reported).

The`Spliterator`reports [Spliterator.SIZED](Spliterator.md), [Spliterator.SUBSIZED](Spliterator.md), and [Spliterator.NONNULL](Spliterator.md). Overriding implementations should document the reporting of additional characteristic values.

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------|
| [Spliterator](Spliterator.md)<E> | a`Spliterator`over the elements in this queue |

### toArray

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toArray(): Array<Any!>
```

Returns an array containing all of the elements in this queue. The elements are in no particular order.

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

If the queue fits in the specified array with room to spare (i.e., the array has more elements than the queue), the element in the array immediately following the end of the collection is set to`null`.

Like the #toArray() method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

Suppose`x`is a queue known to contain only strings. The following code can be used to dump the queue into a newly allocated array of`String`: 

```kotlin
<code>String[] y = x.toArray(new String[0]);</code>
```
Note that`toArray(new Object[0])`is identical in function to`toArray()`.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<T>` | the component type of the array to contain the collection |
| `a` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\>:the array into which the elements of the queue are to be stored, if it is big enough; otherwise, a new array of the same runtime type is allocated for this purpose. |

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
