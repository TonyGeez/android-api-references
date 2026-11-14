Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ArrayBlockingQueue

```
open class ArrayBlockingQueue<E : Any!> : AbstractQueue<E>, BlockingQueue<E>, Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.util.AbstractCollection](../java.util/AbstractCollection.md)\<E\> |||
| | ↳ | [java.util.AbstractQueue](../java.util/AbstractQueue.md)\<E\> ||
| | | ↳ | [java.util.concurrent.ArrayBlockingQueue](ArrayBlockingQueue.md) |
| --- | --- | --- | --- |

A bounded [blocking queue](BlockingQueue.md) backed by an array. This queue orders elements FIFO (first-in-first-out). The *head* of the queue is that element that has been on the queue the longest time. The *tail* of the queue is that element that has been on the queue the shortest time. New elements are inserted at the tail of the queue, and the queue retrieval operations obtain elements at the head of the queue.

This is a classic "bounded buffer", in which a fixed-sized array holds elements inserted by producers and extracted by consumers. Once created, the capacity cannot be changed. Attempts to `put` an element into a full queue will result in the operation blocking; attempts to `take` an element from an empty queue will similarly block.

This class supports an optional fairness policy for ordering waiting producer and consumer threads. By default, this ordering is not guaranteed. However, a queue constructed with fairness set to `true` grants threads access in FIFO order. Fairness generally decreases throughput but reduces variability and avoids starvation.

This class and its iterator implement all of the *optional* methods of the `https://developer.android.com/reference/kotlin/java/util/Collection.html#` and `https://developer.android.com/reference/kotlin/java/util/Iterator.html#` interfaces.

This class is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public constructors ||
|---|---|
| ArrayBlockingQueue Creates an `ArrayBlockingQueue` with the given (fixed) capacity and default access policy. |
| ArrayBlockingQueue Creates an `ArrayBlockingQueue` with the given (fixed) capacity and the specified access policy. |
| ArrayBlockingQueue Creates an `ArrayBlockingQueue` with the given (fixed) capacity, the specified access policy and initially containing the elements of the given collection, added in traversal order of the collection's iterator. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | add Inserts the specified element at the tail of this queue if it is possible to do so immediately without exceeding the queue's capacity, returning `true` upon success and throwing an `IllegalStateException` if this queue is full. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | clear Atomically removes all of the elements from this queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | contains Returns `true` if this queue contains the specified element. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | drainTo <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | drainTo <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | forEach <br /> |
| --- | --- |
| open [MutableIterator](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html)\<E\> | iterator Returns an iterator over the elements in this queue in proper sequence. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offer Inserts the specified element at the tail of this queue if it is possible to do so immediately without exceeding the queue's capacity, returning `true` upon success and `false` if this queue is full. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | offer Inserts the specified element at the tail of this queue, waiting up to the specified wait time for space to become available if the queue is full. |
| --- | --- |
| open E? | peek Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty. |
| open E? | poll Retrieves and removes the head of this queue, or returns `null` if this queue is empty. |
| open E | poll Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | put Inserts the specified element at the tail of this queue, waiting for space to become available if the queue is full. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | remainingCapacity Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | remove Removes a single instance of the specified element from this queue, if it is present. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeAll <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeIf <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | retainAll <br /> |
| --- | --- |
| open [Spliterator](../java.util/Spliterator.md)\<E\> | spliterator Returns a `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#` over the elements in this queue. |
| open E | take Retrieves and removes the head of this queue, waiting if necessary until an element becomes available. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\> | toArray Returns an array containing all of the elements in this queue, in proper sequence. |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\<T\> | toArray Returns an array containing all of the elements in this queue, in proper sequence; the runtime type of the returned array is that of the specified array. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of this collection. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractQueue.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | addAll Adds all of the elements in the specified collection to this queue. Attempts to addAll of a queue to itself result in `IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. This implementation iterates over the specified collection, and adds each element returned by the iterator to this queue, in turn. A runtime exception encountered while trying to add an element (including, in particular, a `null` element) may result in only some of the elements having been successfully added when the associated exception is thrown. <br /> | | `E` | element Retrieves, but does not remove, the head of this queue. This method differs from peek only in that it throws an exception if this queue is empty. This implementation returns the result of `peek` unless the queue is empty. <br /> | | `E` | remove Retrieves and removes the head of this queue. This method differs from poll only in that it throws an exception if this queue is empty. This implementation returns the result of `poll` unless the queue is empty. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | contains Returns `true` if this collection contains the specified element. More formally, returns `true` if and only if this collection contains at least one element `e` such that `Objects.equals(o, e)`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | containsAll Returns `true` if this collection contains all of the elements in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isEmpty Returns `true` if this collection contains no elements. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | iterator Returns an iterator over the elements contained in this collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | remove Removes a single instance of the specified element from this collection, if it is present (optional operation). More formally, removes an element `e` such that `Objects.equals(o, e)`, if this collection contains one or more such elements. Returns `true` if this collection contained the specified element (or equivalently, if this collection changed as a result of the call). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | removeAll Removes all of this collection's elements that are also contained in the specified collection (optional operation). After this call returns, this collection will contain no elements in common with the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | retainAll Retains only the elements in this collection that are contained in the specified collection (optional operation). In other words, removes from this collection all of its elements that are not contained in the specified collection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>` | toArray Returns an array containing all of the elements in this collection. If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. The returned array's [runtime component type](../java.lang/Class.md)) is `Object`. The returned array will be "safe" in that no references to it are maintained by this collection. (In other words, this method must allocate a new array even if this collection is backed by an array). The caller is thus free to modify the returned array. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<T>` | toArray Returns an array containing all of the elements in this collection; the runtime type of the returned array is that of the specified array. If the collection fits in the specified array, it is returned therein. Otherwise, a new array is allocated with the runtime type of the specified array and the size of this collection. If this collection fits in the specified array with room to spare (i.e., the array has more elements than this collection), the element in the array immediately following the end of the collection is set to `null`. (This is useful in determining the length of this collection *only* if the caller knows that this collection does not contain any `null` elements.) If this collection makes any guarantees as to what order its elements are returned by its iterator, this method must return the elements in the same order. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | toString Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by valueOf. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/util/Queue.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | offer Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to add, which can fail to insert an element only by throwing an exception. <br /> | | `E?` | peek Retrieves, but does not remove, the head of this queue, or returns `null` if this queue is empty. <br /> | | `E?` | poll Retrieves and removes the head of this queue, or returns `null` if this queue is empty. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Properties ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue#size:kotlin.Int` Returns the number of elements in this queue. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/util/AbstractCollection.html#size:kotlin.Int` Returns the number of elements in this collection. If this collection contains more than `Integer.MAX_VALUE` elements, returns `Integer.MAX_VALUE`. <br /> | ||

## Public constructors

### ArrayBlockingQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArrayBlockingQueue(capacity: Int)
```

Creates an `ArrayBlockingQueue` with the given (fixed) capacity and default access policy.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the capacity of this queue |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `capacity < 1` |

### ArrayBlockingQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArrayBlockingQueue(
    capacity: Int, 
    fair: Boolean)
```

Creates an `ArrayBlockingQueue` with the given (fixed) capacity and the specified access policy.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the capacity of this queue |
| `fair` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` then queue accesses for threads blocked on insertion or removal, are processed in FIFO order; if `false` the access order is unspecified. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `capacity < 1` |

### ArrayBlockingQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ArrayBlockingQueue(
    capacity: Int, 
    fair: Boolean, 
    c: MutableCollection<out E>!)
```

Creates an `ArrayBlockingQueue` with the given (fixed) capacity, the specified access policy and initially containing the elements of the given collection, added in traversal order of the collection's iterator.

| Parameters ||
|---|---|
| `capacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the capacity of this queue |
| `fair` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true` then queue accesses for threads blocked on insertion or removal, are processed in FIFO order; if `false` the access order is unspecified. |
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<out E\>!: the collection of elements to initially contain |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `capacity` is less than `c.size()`, or less than 1. |
| `java.lang.NullPointerException` | if the specified collection or any of its elements are null |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(element: E): Boolean
```

Inserts the specified element at the tail of this queue if it is possible to do so immediately without exceeding the queue's capacity, returning `true` upon success and throwing an `IllegalStateException` if this queue is full.

| Parameters ||
|---|---|
| `e` | the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` (as specified by add) |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if this queue is full |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.UnsupportedOperationException` | if the `add` operation is not supported by this collection |

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Atomically removes all of the elements from this queue. The queue will be empty after this call returns.

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
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this queue ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |

### drainTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun drainTo(c: MutableCollection<in E>!): Int
```

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<in E\>!: the collection to transfer elements into |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements transferred |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this queue prevents it from being added to the specified collection |
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if addition of elements is not supported by the specified collection |

### drainTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun drainTo(
    c: MutableCollection<in E>!, 
    maxElements: Int
): Int
```

| Parameters ||
|---|---|
| `c` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\<in E\>!: the collection to transfer elements into |
| `maxElements` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum number of elements to transfer |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements transferred |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of an element of this queue prevents it from being added to the specified collection |
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |
| `java.lang.NullPointerException` | if the specified collection is null |
| --- | --- |
| `java.lang.UnsupportedOperationException` | if addition of elements is not supported by the specified collection |

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

### iterator

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun iterator(): MutableIterator<E>
```

Returns an iterator over the elements in this queue in proper sequence. The elements will be returned in order from first (head) to last (tail).

The returned iterator is [*weakly consistent*](_package.md).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-iterator/index.html<E>` | an iterator over the elements in this queue in proper sequence |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun offer(e: E): Boolean
```

Inserts the specified element at the tail of this queue if it is possible to do so immediately without exceeding the queue's capacity, returning `true` upon success and `false` if this queue is full. This method is generally preferable to method #add, which can fail to insert an element only by throwing an exception.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the element was added to this queue, else `false` |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
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

Inserts the specified element at the tail of this queue, waiting up to the specified wait time for space to become available if the queue is full.

| Parameters ||
|---|---|
| `e` | E: the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if successful, or `false` if the specified waiting time elapses before space is available |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.InterruptedException` | if interrupted while waiting |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null |

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

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available.

| Parameters ||
|---|---|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait before giving up, in units of `unit` |
| `unit` | [TimeUnit](TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |

| Return ||
|---|---|
| `E` | the head of this queue, or `null` if the specified waiting time elapses before an element is available |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if interrupted while waiting |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun put(e: E): Unit
```

Inserts the specified element at the tail of this queue, waiting for space to become available if the queue is full.

| Parameters ||
|---|---|
| `e` | E: the element to add |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.InterruptedException` | if interrupted while waiting |
| --- | --- |
| `java.lang.NullPointerException` | if the specified element is null |

### remainingCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remainingCapacity(): Int
```

Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking. This is always equal to the initial capacity of this queue less the current `size` of this queue.

Note that you *cannot* always tell if an attempt to insert an element will succeed by inspecting `remainingCapacity` because it may be the case that another thread is about to insert or remove an element.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the remaining capacity |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(element: E?): Boolean
```

Removes a single instance of the specified element from this queue, if it is present. More formally, removes an element `e` such that `o.equals(e)`, if this queue contains one or more such elements. Returns `true` if this queue contained the specified element (or equivalently, if this queue changed as a result of the call).

Removal of interior elements in circular array based queues is an intrinsically slow and disruptive operation, so should be undertaken only in exceptional circumstances, ideally only when the queue is known not to be accessible by other threads.

| Parameters ||
|---|---|
| `o` | element to be removed from this queue, if present |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this queue changed as a result of the call |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the class of the specified element is incompatible with this queue ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
| `java.lang.NullPointerException` | if the specified element is null ([optional](https://developer.android.com//reference/java/util/Collection.html#optional-restrictions)) |
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
| `filter` | [Predicate](../java.util.function/Predicate.md)\<in E\>: a predicate which returns `true` for elements to be removed |

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

The returned spliterator is [*weakly consistent*](_package.md).

The `Spliterator` reports `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#CONCURRENT:kotlin.Int`, `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#ORDERED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#NONNULL:kotlin.Int`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/Spliterator.html#<E>` | a `Spliterator` over the elements in this queue |

### take

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun take(): E
```

Retrieves and removes the head of this queue, waiting if necessary until an element becomes available.

| Return ||
|---|---|
| `E` | the head of this queue |

| Exceptions ||
|---|---|
| `java.lang.InterruptedException` | if interrupted while waiting |

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

Like the toArray method, this method acts as bridge between array-based and collection-based APIs. Further, this method allows precise control over the runtime type of the output array, and may, under certain circumstances, be used to save allocation costs.

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

Returns a string representation of this collection. The string representation consists of a list of the collection's elements in the order they are returned by its iterator, enclosed in square brackets (`"[]"`). Adjacent elements are separated by the characters `", "` (comma and space). Elements are converted to strings as by valueOf.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

## Properties

### size

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open val size: Int
```

Returns the number of elements in this queue.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of elements in this queue |
