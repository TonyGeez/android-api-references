# TransferQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransferQueue

```
interface TransferQueue<E : Any!> : BlockingQueue<E>
```

| [java.util.concurrent.TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#) |

| Known Direct Subclasses [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [LinkedTransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/LinkedTransferQueue) | An unbounded [TransferQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#) based on linked nodes. | |
| --- | --- | --- | --- | --- | --- | --- |

A [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) in which producers may wait for consumers to receive elements. A`TransferQueue`may be useful for example in message passing applications in which producers sometimes (using method [transfer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#transfer(java.util.concurrent.TransferQueue.E))) await receipt of elements by consumers invoking`take`or`poll`, while at other times enqueue elements (via method`put`) without waiting for receipt. [Non-blocking](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#tryTransfer(java.util.concurrent.TransferQueue.E))and [time-out](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#tryTransfer(java.util.concurrent.TransferQueue.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))versions of`tryTransfer`are also available. A`TransferQueue`may also be queried, via [hasWaitingConsumer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#hasWaitingConsumer()), whether there are any threads waiting for items, which is a converse analogy to a`peek`operation.

Like other blocking queues, a`TransferQueue`may be capacity bounded. If so, an attempted transfer operation may initially block waiting for available space, and/or subsequently block waiting for reception by a consumer. Note that in a queue with zero capacity, such as [SynchronousQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/SynchronousQueue),`put`and`transfer`are effectively synonymous.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWaitingConsumerCount](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#getWaitingConsumerCount())`()` Returns an estimate of the number of consumers waiting to receive elements via [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWaitingConsumer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#hasWaitingConsumer())`()` Returns`true`if there is at least one consumer waiting to receive an element via [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transfer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#transfer(java.util.concurrent.TransferQueue.E))`(`e:` `E`)` Transfers the element to a consumer, waiting if necessary to do so. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryTransfer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#tryTransfer(java.util.concurrent.TransferQueue.E))`(`e:` `E`)` Transfers the element to a waiting consumer immediately, if possible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryTransfer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#tryTransfer(java.util.concurrent.TransferQueue.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` Transfers the element to a consumer if it is possible to do so before the timeout elapses. |

| Inherited functions ||
|---|---|
| From class [BlockingQueue](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#add(java.util.concurrent.BlockingQueue.E))`(`element:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. When using a capacity-restricted queue, it is generally preferable to use [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#offer(java.util.concurrent.BlockingQueue.E)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#contains(java.util.concurrent.BlockingQueue.E))`(`element:` `E`)` <br /> Returns`true`if this queue contains the specified element. More formally, returns`true`if and only if this queue contains at least one element`e`such that`o.equals(e)`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#drainTo(kotlin.collections.MutableCollection))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> Removes all available elements from this queue and adds them to the given collection. This operation may be more efficient than repeatedly polling this queue. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#drainTo(kotlin.collections.MutableCollection,%20kotlin.Int))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Removes at most the given number of available elements from this queue and adds them to the given collection. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#offer(java.util.concurrent.BlockingQueue.E))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and`false`if no space is currently available. When using a capacity-restricted queue, this method is generally preferable to #add, which can fail to insert an element only by throwing an exception. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#offer(java.util.concurrent.BlockingQueue.E,%20kotlin.Long,%20java.util.concurrent.TimeUnit))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Inserts the specified element into this queue, waiting up to the specified wait time if necessary for space to become available. <br /> | | E | [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!`)` <br /> Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#put(java.util.concurrent.BlockingQueue.E))`(`e:` `E`)` <br /> Inserts the specified element into this queue, waiting if necessary for space to become available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#remainingCapacity())`()` <br /> Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking, or`Integer.MAX_VALUE`if there is no intrinsic limit. Note that you*cannot* always tell if an attempt to insert an element will succeed by inspecting`remainingCapacity`because it may be the case that another thread is about to insert or remove an element. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#remove(java.util.concurrent.BlockingQueue.E))`(`element:` `E`)` <br /> Removes a single instance of the specified element from this queue, if it is present. More formally, removes an element`e`such that`o.equals(e)`, if this queue contains one or more such elements. Returns`true`if this queue contained the specified element (or equivalently, if this queue changed as a result of the call). <br /> | | E | [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())`()` <br /> Retrieves and removes the head of this queue, waiting if necessary until an element becomes available. <br /> | ||
| From class [Queue](https://developer.android.com/reference/kotlin/java/util/Queue.html#) |----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [element](https://developer.android.com/reference/kotlin/java/util/Queue.html#element())`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())only in that it throws an exception if this queue is empty. <br /> | | E? | [peek](https://developer.android.com/reference/kotlin/java/util/Queue.html#peek())`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll())`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | | E | [remove](https://developer.android.com/reference/kotlin/java/util/Queue.html#remove())`()` <br /> Retrieves and removes the head of this queue. This method differs from [poll()](https://developer.android.com/reference/kotlin/java/util/Queue.html#poll())only in that it throws an exception if this queue is empty. <br /> | ||

## Public methods

### getWaitingConsumerCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWaitingConsumerCount(): Int
```

Returns an estimate of the number of consumers waiting to receive elements via [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit)). The return value is an approximation of a momentary state of affairs, that may be inaccurate if consumers have completed or given up waiting. The value may be useful for monitoring and heuristics, but not for synchronization control. Implementations of this method are likely to be noticeably slower than those for [hasWaitingConsumer](https://developer.android.com/reference/kotlin/java/util/concurrent/TransferQueue#hasWaitingConsumer()).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of consumers waiting to receive elements |

### hasWaitingConsumer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasWaitingConsumer(): Boolean
```

Returns`true`if there is at least one consumer waiting to receive an element via [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit)). The return value represents a momentary state of affairs.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there is at least one waiting consumer |

### transfer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun transfer(e: E): Unit
```

Transfers the element to a consumer, waiting if necessary to do so.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))), else waits until the element is received by a consumer.

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
abstract fun tryTransfer(e: E): Boolean
```

Transfers the element to a waiting consumer immediately, if possible.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))), otherwise returning`false`without enqueuing the element.

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
abstract fun tryTransfer(
    e: E, 
    timeout: Long, 
    unit: TimeUnit!
): Boolean
```

Transfers the element to a consumer if it is possible to do so before the timeout elapses.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#take())or timed [poll](https://developer.android.com/reference/kotlin/java/util/concurrent/BlockingQueue#poll(kotlin.Long,%20java.util.concurrent.TimeUnit))), else waits until the element is received by a consumer, returning`false`if the specified wait time elapses before the element can be transferred.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | E:the element to transfer |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how long to wait before giving up, in units of`unit` |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit)!:a`TimeUnit`determining how to interpret the`timeout`parameter |
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
