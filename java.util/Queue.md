# Queue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Queue

```
interface Queue<E : Any!> : MutableCollection<E>
```

| [java.util.Queue](Queue.md) |

| Known Direct Subclasses [AbstractQueue](AbstractQueue.md), [BlockingQueue](../java.util.concurrent/BlockingQueue.md), [ConcurrentLinkedQueue](../java.util.concurrent/ConcurrentLinkedQueue.md), [Deque](Deque.md) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AbstractQueue](AbstractQueue.md) | This class provides skeletal implementations of some [Queue](Queue.md) operations. | | [BlockingQueue](../java.util.concurrent/BlockingQueue.md) | A [Queue](Queue.md) that additionally supports operations that wait for the queue to become non-empty when retrieving an element, and wait for space to become available in the queue when storing an element. | | [ConcurrentLinkedQueue](../java.util.concurrent/ConcurrentLinkedQueue.md) | An unbounded thread-safe [queue](Queue.md) based on linked nodes. | | [Deque](Deque.md) | A linear collection that supports element insertion and removal at both ends. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [ArrayBlockingQueue](../java.util.concurrent/ArrayBlockingQueue.md), [ArrayBlockingQueue](../java.util.concurrent/ArrayBlockingQueue.md), [ArrayDeque](ArrayDeque.md), [BlockingDeque](../java.util.concurrent/BlockingDeque.md), [BlockingDeque](../java.util.concurrent/BlockingDeque.md), [ConcurrentLinkedDeque](../java.util.concurrent/ConcurrentLinkedDeque.md), [ConcurrentLinkedQueue](../java.util.concurrent/ConcurrentLinkedQueue.md), [DelayQueue](../java.util.concurrent/DelayQueue.md), [DelayQueue](../java.util.concurrent/DelayQueue.md), [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md), [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md), [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md), and 11 others. |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayBlockingQueue](../java.util.concurrent/ArrayBlockingQueue.md) | A bounded [blocking queue](../java.util.concurrent/BlockingQueue.md) backed by an array. | | [ArrayBlockingQueue](../java.util.concurrent/ArrayBlockingQueue.md) | A bounded [blocking queue](../java.util.concurrent/BlockingQueue.md) backed by an array. | | [ArrayDeque](ArrayDeque.md) | Resizable-array implementation of the [Deque](Deque.md) interface. | | [BlockingDeque](../java.util.concurrent/BlockingDeque.md) | A [Deque](Deque.md) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [BlockingDeque](../java.util.concurrent/BlockingDeque.md) | A [Deque](Deque.md) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [ConcurrentLinkedDeque](../java.util.concurrent/ConcurrentLinkedDeque.md) | An unbounded concurrent [deque](Deque.md) based on linked nodes. | | [ConcurrentLinkedQueue](../java.util.concurrent/ConcurrentLinkedQueue.md) | An unbounded thread-safe [queue](Queue.md) based on linked nodes. | | [DelayQueue](../java.util.concurrent/DelayQueue.md) | An unbounded [blocking queue](../java.util.concurrent/BlockingQueue.md) of [Delayed](../java.util.concurrent/Delayed.md) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [DelayQueue](../java.util.concurrent/DelayQueue.md) | An unbounded [blocking queue](../java.util.concurrent/BlockingQueue.md) of [Delayed](../java.util.concurrent/Delayed.md) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](../java.util.concurrent/BlockingDeque.md) based on linked nodes. | | [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](../java.util.concurrent/BlockingDeque.md) based on linked nodes. | | [LinkedBlockingDeque](../java.util.concurrent/LinkedBlockingDeque.md) | An optionally-bounded [blocking deque](../java.util.concurrent/BlockingDeque.md) based on linked nodes. | | [LinkedBlockingQueue](../java.util.concurrent/LinkedBlockingQueue.md) | An optionally-bounded [blocking queue](../java.util.concurrent/BlockingQueue.md) based on linked nodes. | | [LinkedBlockingQueue](../java.util.concurrent/LinkedBlockingQueue.md) | An optionally-bounded [blocking queue](../java.util.concurrent/BlockingQueue.md) based on linked nodes. | | [LinkedList](LinkedList.md) | Doubly-linked list implementation of the`List`and`Deque`interfaces. | | [LinkedTransferQueue](../java.util.concurrent/LinkedTransferQueue.md) | An unbounded [TransferQueue](../java.util.concurrent/TransferQueue.md) based on linked nodes. | | [LinkedTransferQueue](../java.util.concurrent/LinkedTransferQueue.md) | An unbounded [TransferQueue](../java.util.concurrent/TransferQueue.md) based on linked nodes. | | [PriorityBlockingQueue](../java.util.concurrent/PriorityBlockingQueue.md) | An unbounded [blocking queue](../java.util.concurrent/BlockingQueue.md) that uses the same ordering rules as class [PriorityQueue](PriorityQueue.md) and supplies blocking retrieval operations. | | [PriorityBlockingQueue](../java.util.concurrent/PriorityBlockingQueue.md) | An unbounded [blocking queue](../java.util.concurrent/BlockingQueue.md) that uses the same ordering rules as class [PriorityQueue](PriorityQueue.md) and supplies blocking retrieval operations. | | [PriorityQueue](PriorityQueue.md) | An unbounded priority [queue](Queue.md) based on a priority heap. | | [SynchronousQueue](../java.util.concurrent/SynchronousQueue.md) | A [blocking queue](../java.util.concurrent/BlockingQueue.md) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | | [SynchronousQueue](../java.util.concurrent/SynchronousQueue.md) | A [blocking queue](../java.util.concurrent/BlockingQueue.md) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | | [TransferQueue](../java.util.concurrent/TransferQueue.md) | A [BlockingQueue](../java.util.concurrent/BlockingQueue.md) in which producers may wait for consumers to receive elements. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A collection designed for holding elements prior to processing. Besides basic [Collection](Collection.md) operations, queues provide additional insertion, extraction, and inspection operations. Each of these methods exists in two forms: one throws an exception if the operation fails, the other returns a special value (either`null`or`false`, depending on the operation). The latter form of the insert operation is designed specifically for use with capacity-restricted`Queue`implementations; in most implementations, insert operations cannot fail.

| | Throws exception | Returns special value |
| --- | --- | --- |

<br />

Queues typically, but do not necessarily, order elements in a FIFO (first-in-first-out) manner. Among the exceptions are priority queues, which order elements according to a supplied comparator, or the elements' natural ordering, and LIFO queues (or stacks) which order the elements LIFO (last-in-first-out). Whatever the ordering used, the*head* of the queue is that element which would be removed by a call to [remove()](Queue.md))or [poll()](Queue.md)). In a FIFO queue, all new elements are inserted at the*tail* of the queue. Other kinds of queues may use different placement rules. Every`Queue`implementation must specify its ordering properties.

The [offer](Queue.md))method inserts an element if possible, otherwise returning`false`. This differs from the [Collection.add](Collection.md))method, which can fail to add an element only by throwing an unchecked exception. The`offer`method is designed for use when failure is a normal, rather than exceptional occurrence, for example, in fixed-capacity (or "bounded") queues.

The [remove()](Queue.md))and [poll()](Queue.md))methods remove and return the head of the queue. Exactly which element is removed from the queue is a function of the queue's ordering policy, which differs from implementation to implementation. The`remove()`and`poll()`methods differ only in their behavior when the queue is empty: the`remove()`method throws an exception, while the`poll()`method returns`null`.

The [element()](Queue.md))and [peek()](Queue.md))methods return, but do not remove, the head of the queue.

The`Queue`interface does not define the*blocking queue methods* , which are common in concurrent programming. These methods, which wait for elements to appear or for space to become available, are defined in the [java.util.concurrent.BlockingQueue](../java.util.concurrent/BlockingQueue.md) interface, which extends this interface.

`Queue`implementations generally do not allow insertion of`null`elements, although some implementations, such as [LinkedList](LinkedList.md), do not prohibit insertion of`null`. Even in the implementations that permit it,`null`should not be inserted into a`Queue`, as`null`is also used as a special return value by the`poll`method to indicate that the queue contains no elements.

`Queue`implementations generally do not define element-based versions of methods`equals`and`hashCode`but instead inherit the identity based versions from class`Object`, because element-based equality is not always well-defined for queues with the same elements but different ordering properties.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](Queue.md))`(`element:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. |
| abstractE | [element](Queue.md))`()` Retrieves, but does not remove, the head of this queue. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](Queue.md))`(`e:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. |
| --- | --- |
| abstractE? | [peek](Queue.md))`()` Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. |
| abstractE? | [poll](Queue.md))`()` Retrieves and removes the head of this queue, or returns`null`if this queue is empty. |
| abstractE | [remove](Queue.md))`()` Retrieves and removes the head of this queue. |
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
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`(as specified by [Collection.add](Collection.md))) |

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

Retrieves, but does not remove, the head of this queue. This method differs from [peek](Queue.md))only in that it throws an exception if this queue is empty.

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

Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions. When using a capacity-restricted queue, this method is generally preferable to [add](Queue.md)), which can fail to insert an element only by throwing an exception.

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

Retrieves and removes the head of this queue. This method differs from [poll()](Queue.md))only in that it throws an exception if this queue is empty.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|------------------------------------|------------------------|
| `java.util.NoSuchElementException` | if this queue is empty |
