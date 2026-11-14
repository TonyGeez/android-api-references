# BlockingQueue

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BlockingQueue

```
interface BlockingQueue<E : Any!> : Queue<E>
```

| [java.util.concurrent.BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) |

| Known Direct Subclasses [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue), [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque), [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue), [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue), [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue), [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue), [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) |--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [ArrayBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/ArrayBlockingQueue) | A bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) backed by an array. | | [BlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) | A [Deque](https://developer.android.com/reference/kotlin/java/util/Deque.html#) that additionally supports blocking operations that wait for the deque to become non-empty when retrieving an element, and wait for space to become available in the deque when storing an element. | | [DelayQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/DelayQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) of [Delayed](https://developer.android.com/reference/kotlin/java/util/concurrent/Delayed) elements, in which an element generally becomes eligible for removal when its delay has expired. | | [LinkedBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingQueue) | An optionally-bounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) based on linked nodes. | | [PriorityBlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/PriorityBlockingQueue) | An unbounded [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) that uses the same ordering rules as class [PriorityQueue](https://developer.android.com/reference/kotlin/java/util/PriorityQueue.html#) and supplies blocking retrieval operations. | | [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue) | A [blocking queue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) in which each insert operation must wait for a corresponding remove operation by another thread, and vice versa. | | [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) | A [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#) in which producers may wait for consumers to receive elements. | |

| Known Indirect Subclasses [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque), [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) |----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------| | [LinkedBlockingDeque](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedBlockingDeque) | An optionally-bounded [blocking deque](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingDeque) based on linked nodes. | | [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) | An unbounded [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue) based on linked nodes. | |

A [Queue](https://developer.android.com/reference/kotlin/java/util/Queue.html#) that additionally supports operations that wait for the queue to become non-empty when retrieving an element, and wait for space to become available in the queue when storing an element.

`BlockingQueue`methods come in four forms, with different ways of handling operations that cannot be satisfied immediately, but may be satisfied at some point in the future: one throws an exception, the second returns a special value (either`null`or`false`, depending on the operation), the third blocks the current thread indefinitely until the operation can succeed, and the fourth blocks for only a given maximum time limit before giving up. These methods are summarized in the following table:

| | Throws exception | Special value | Blocks | Times out |

A`BlockingQueue`does not accept`null`elements. Implementations throw`NullPointerException`on attempts to`add`,`put`or`offer`a`null`. A`null`is used as a sentinel value to indicate failure of`poll`operations.

A`BlockingQueue`may be capacity bounded. At any given time it may have a`remainingCapacity`beyond which no additional elements can be`put`without blocking. A`BlockingQueue`without any intrinsic capacity constraints always reports a remaining capacity of`Integer.MAX_VALUE`.

`BlockingQueue`implementations are designed to be used primarily for producer-consumer queues, but additionally support the [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) interface. So, for example, it is possible to remove an arbitrary element from a queue using`remove(x)`. However, such operations are in general*not*performed very efficiently, and are intended for only occasional use, such as when a queued message is cancelled.

`BlockingQueue`implementations are thread-safe. All queuing methods achieve their effects atomically using internal locks or other forms of concurrency control. However, the*bulk* Collection operations`addAll`,`containsAll`,`retainAll`and`removeAll`are*not* necessarily performed atomically unless specified otherwise in an implementation. So it is possible, for example, for`addAll(c)`to fail (throwing an exception) after adding only some of the elements in`c`.

A`BlockingQueue`does*not* intrinsically support any kind of "close" or "shutdown" operation to indicate that no more items will be added. The needs and usage of such features tend to be implementation-dependent. For example, a common tactic is for producers to insert special*end-of-stream* or*poison*objects, that are interpreted accordingly when taken by consumers.

Usage example, based on a typical producer-consumer scenario. Note that a`BlockingQueue`can safely be used with multiple producers and multiple consumers. 

```kotlin
<code>class Producer implements Runnable {
    private final BlockingQueue queue;
    Producer(BlockingQueue q) { queue = q; }
    public void run() {
      try {
        while (true) { queue.put(produce()); }
      } catch (InterruptedException ex) { ... handle ...}
    }
    Object produce() { ... }
  }
 
  class Consumer implements Runnable {
    private final BlockingQueue queue;
    Consumer(BlockingQueue q) { queue = q; }
    public void run() {
      try {
        while (true) { consume(queue.take()); }
      } catch (InterruptedException ex) { ... handle ...}
    }
    void consume(Object x) { ... }
  }
 
  class Setup {
    void main() {
      BlockingQueue q = new SomeQueueImplementation();
      Producer p = new Producer(q);
      Consumer c1 = new Consumer(q);
      Consumer c2 = new Consumer(q);
      new Thread(p).start();
      new Thread(c1).start();
      new Thread(c2).start();
    }
  }</code>
```

Memory consistency effects: As with other concurrent collections, actions in a thread prior to placing an object into a`BlockingQueue` [*happen-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#MemoryVisibility) actions subsequent to the access or removal of that element from the`BlockingQueue`in another thread.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#add(java.util.concurrent.BlockingQueue.E))`(`element:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#contains(java.util.concurrent.BlockingQueue.E))`(`element:` `E`)` Returns`true`if this queue contains the specified element. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#drainTo(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` Removes all available elements from this queue and adds them to the given collection. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#drainTo(kotlin.collections.MutableCollection,%20kotlin.Int))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Removes at most the given number of available elements from this queue and adds them to the given collection. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#offer(java.util.concurrent.BlockingQueue.E))`(`e:` `E`)` Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and`false`if no space is currently available. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#offer(java.util.concurrent.BlockingQueue.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Inserts the specified element into this queue, waiting up to the specified wait time if necessary for space to become available. |
| abstractE | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#put(java.util.concurrent.BlockingQueue.E))`(`e:` `E`)` Inserts the specified element into this queue, waiting if necessary for space to become available. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#remainingCapacity())`()` Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking, or`Integer.MAX_VALUE`if there is no intrinsic limit. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#remove(java.util.concurrent.BlockingQueue.E))`(`element:` `E`)` Removes a single instance of the specified element from this queue, if it is present. |
| abstractE | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())`()` Retrieves and removes the head of this queue, waiting if necessary until an element becomes available. |

| Inherited functions ||
|---|---|
| From class [Queue](https://developer.android.com/reference/kotlin/java/util/Queue.html#) |----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [element](https://developer.android.com/reference/kotlin/java/util/Queue.html#element())`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())only in that it throws an exception if this queue is empty. <br /> | | E? | [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll())`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | | E | [remove](https://developer.android.com/reference/kotlin/java/util/Queue.html#remove())`()` <br /> Retrieves and removes the head of this queue. This method differs from [poll()](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll())only in that it throws an exception if this queue is empty. <br /> | ||

## Public methods

### add

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun add(element: E): Boolean
```

Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. When using a capacity-restricted queue, it is generally preferable to use [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#offer(java.util.concurrent.BlockingQueue.E)).

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
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |
| `java.lang.IllegalStateException` | if the element cannot be added at this time due to capacity restrictions |

### contains

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun contains(element: E): Boolean
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

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun drainTo(c: MutableCollection<in E>!): Int
```

Removes all available elements from this queue and adds them to the given collection. This operation may be more efficient than repeatedly polling this queue. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress.

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
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |

### drainTo

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun drainTo(
    c: MutableCollection<in E>!, 
    maxElements: Int
): Int
```

Removes at most the given number of available elements from this queue and adds them to the given collection. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress.

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
| `java.lang.IllegalArgumentException` | if the specified collection is this queue, or some property of an element of this queue prevents it from being added to the specified collection |

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offer(e: E): Boolean
```

Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and`false`if no space is currently available. When using a capacity-restricted queue, this method is generally preferable to #add, which can fail to insert an element only by throwing an exception.

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

### offer

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun offer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Inserts the specified element into this queue, waiting up to the specified wait time if necessary for space to become available.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to add |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if successful, or`false`if the specified waiting time elapses before space is available |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

### poll

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(
    timeout: Long, 
    unit: TimeUnit!
): E
```

Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |

| Return ||
|---|------------------------------------------------------------------------------------------------------|
| E | the head of this queue, or`null`if the specified waiting time elapses before an element is available |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(e: E): Unit
```

Inserts the specified element into this queue, waiting if necessary for space to become available.

| Parameters ||
|-----|----------------------|
| `e` | E:the element to add |

| Exceptions ||
|--------------------------------------|--------------------------------------------------------------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
| `java.lang.ClassCastException` | if the class of the specified element prevents it from being added to this queue |
| `java.lang.NullPointerException` | if the specified element is null |
| `java.lang.IllegalArgumentException` | if some property of the specified element prevents it from being added to this queue |

### remainingCapacity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remainingCapacity(): Int
```

Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking, or`Integer.MAX_VALUE`if there is no intrinsic limit.

Note that you*cannot* always tell if an attempt to insert an element will succeed by inspecting`remainingCapacity`because it may be the case that another thread is about to insert or remove an element.

| Return ||
|----------------------------------------------------------------------------|------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the remaining capacity |

### remove

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun remove(element: E): Boolean
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

### take

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun take(): E
```

Retrieves and removes the head of this queue, waiting if necessary until an element becomes available.

| Return ||
|---|------------------------|
| E | the head of this queue |

| Exceptions ||
|----------------------------------|------------------------------|
| `java.lang.InterruptedException` | if interrupted while waiting |
