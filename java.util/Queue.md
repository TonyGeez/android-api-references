# Queue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Queue

```
interface Queue<E : Any!> : MutableCollection<E>
```

| [java.util.Queue](https://developer.android.com/reference/kotlin/java/util/Queue#) |

| Known Direct Subclasses [AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue), [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue), [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue), [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractQueue](https://developer.android.com/reference/kotlin/java/util/AbstractQueue) | This class provides skeletal implementations of some [Queue](https://developer.android.com/reference/kotlin/java/util/Queue#) operations. | | [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) | A [Queue](https://developer.android.com/reference/kotlin/java/util/Queue#) that additionally supports operations that wait for the queue to become non-empty when retrieving an element, and wait for space to become available in the queue when storing an element. | | [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue) | An unbounded thread-safe [queue](https://developer.android.com/reference/kotlin/java/util/Queue#) based on linked nodes. | | [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) | A linear collection that supports element insertion and removal at both ends. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue), [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue), [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque), [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque), [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque), [ConcurrentLinkedDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque), [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue), [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue), [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue), [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), and 11 others. |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue) | A bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) backed by an array. | | [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue) | A bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) backed by an array. | | [ArrayDeque](https://developer.android.com/reference/kotlin/java/util/ArrayDeque) | Resizable-array implementation of the [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) interface. | | [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) | A [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) | A [Deque](https://developer.android.com/reference/kotlin/java/util/Deque) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [ConcurrentLinkedDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedDeque) | An unbounded concurrent [deque](https://developer.android.com/reference/kotlin/java/util/Deque) based on linked nodes. | | [ConcurrentLinkedQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ConcurrentLinkedQueue) | An unbounded thread-safe [queue](https://developer.android.com/reference/kotlin/java/util/Queue#) based on linked nodes. | | [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) | An optionally-bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) based on linked nodes. | | [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) | An optionally-bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) based on linked nodes. | | [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | | [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) | An unbounded [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) based on linked nodes. | | [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) | An unbounded [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) based on linked nodes. | | [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) that uses the same ordering rules as class [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) and supplies blocking retrieval operations. | | [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) that uses the same ordering rules as class [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) and supplies blocking retrieval operations. | | [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue) | An unbounded priority [queue](https://developer.android.com/reference/kotlin/java/util/Queue#) based on a priority heap. | | [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue) | A [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | | [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue) | A [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | | [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) | A [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) in which producers may wait for consumers to receive elements. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A collection designed for holding elements prior to processing. Besides basic [Collection](https://developer.android.com/reference/kotlin/java/util/Collection) operations, queues provide additional insertion, extraction, and inspection operations. Each of these methods exists in two forms: one throws an exception if the operation fails, the other returns a special value (either`null`or`false`, depending on the operation). The latter form of the insert operation is designed specifically for use with capacity-restricted`Queue`implementations; in most implementations, insert operations cannot fail.

| | Throws exception | Returns special value |
| --- | --- | --- |

<br />

Queues typically, but do not necessarily, order elements in a FIFO (first-in-first-out) manner. Among the exceptions are priority queues, which order elements according to a supplied comparator, or the elements' natural ordering, and LIFO queues (or stacks) which order the elements LIFO (last-in-first-out). Whatever the ordering used, the*head* of the queue is that element which would be removed by a call to [remove()](https://developer.android.com/reference/kotlin/java/util/Queue#remove())or [poll()](https://developer.android.com/reference/kotlin/java/util/Queue#poll()). In a FIFO queue, all new elements are inserted at the*tail* of the queue. Other kinds of queues may use different placement rules. Every`Queue`implementation must specify its ordering properties.

The [offer](https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E))method inserts an element if possible, otherwise returning`false`. This differs from the [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection#add(java.util.Collection.E))method, which can fail to add an element only by throwing an unchecked exception. The`offer`method is designed for use when failure is a normal, rather than exceptional occurrence, for example, in fixed-capacity (or "bounded") queues.

The [remove()](https://developer.android.com/reference/kotlin/java/util/Queue#remove())and [poll()](https://developer.android.com/reference/kotlin/java/util/Queue#poll())methods remove and return the head of the queue. Exactly which element is removed from the queue is a function of the queue's ordering policy, which differs from implementation to implementation. The`remove()`and`poll()`methods differ only in their behavior when the queue is empty: the`remove()`method throws an exception, while the`poll()`method returns`null`.

The [element()](https://developer.android.com/reference/kotlin/java/util/Queue#element())and [peek()](https://developer.android.com/reference/kotlin/java/util/Queue#peek())methods return, but do not remove, the head of the queue.

The`Queue`interface does not define the*blocking queue methods* , which are common in concurrent programming. These methods, which wait for elements to appear or for space to become available, are defined in the [java.util.concurrent.BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) interface, which extends this interface.

`Queue`implementations generally do not allow insertion of`null`elements, although some implementations, such as [LinkedList](https://developer.android.com/reference/kotlin/java/util/LinkedList), do not prohibit insertion of`null`. Even in the implementations that permit it,`null`should not be inserted into a`Queue`, as`null`is also used as a special return value by the`poll`method to indicate that the queue contains no elements.

`Queue`implementations generally do not define element-based versions of methods`equals`and`hashCode`but instead inherit the identity based versions from class`Object`, because element-based equality is not always well-defined for queues with the same elements but different ordering properties.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/Queue#add(java.util.Queue.E))`(`element:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. |
| abstractE | [element](https://developer.android.com/reference/kotlin/java/util/Queue#element())`()` Retrieves, but does not remove, the head of this queue. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/Queue#offer(java.util.Queue.E))`(`e:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. |
| --- | --- |
| abstractE? | [peek](https://developer.android.com/reference/kotlin/java/util/Queue#peek())`()` Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. |
| abstractE? | [poll](https://developer.android.com/reference/kotlin/java/util/Queue#poll())`()` Retrieves and removes the head of this queue, or returns`null`if this queue is empty. |
| abstractE | [remove](https://developer.android.com/reference/kotlin/java/util/Queue#remove())`()` Retrieves and removes the head of this queue. |
| --- | --- |

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(element: E): Boolean
```

Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available.

| Parameters ||
|-----|--------------------|
| `e` | the element to add |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](https://developer.android.com/reference/kotlin/java/util/Collection#add(java.util.Collection.E))) |

| Exceptions ||
|-------------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.UnsupportedOperationException` | if the`add`operation is not supported by this collection |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null and this queue does not permit null elements |
| --- | --- |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### element

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun element(): E
```

Retrieves, but does not remove, the head of this queue. This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/Queue#peek())only in that it throws an exception if this queue is empty.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this queue is empty |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offer(e: E): Boolean
```

Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](https://developer.android.com/reference/kotlin/java/util/Queue#add(java.util.Queue.E)), which can fail to insert an element only by throwing an exception.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the element was added to this queue, else`false` |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------|
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null and this queue does not permit null elements |
| `java.lang.IllegalArgumentException` | if some property of this element prevents it from being added to this queue |
| --- | --- |

### peek

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun peek(): E?
```

Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty.

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this queue, or`null`if this queue is empty |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(): E?
```

Retrieves and removes the head of this queue, or returns`null`if this queue is empty.

| Return ||
|----|--------------------------------------------------------|
| E? | the head of this queue, or`null`if this queue is empty |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(): E
```

Retrieves and removes the head of this queue. This method differs from [poll()](https://developer.android.com/reference/kotlin/java/util/Queue#poll())only in that it throws an exception if this queue is empty.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this queue is empty |
