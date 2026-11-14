# TransferQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransferQueue

```
interface TransferQueue<E : Any!> : BlockingQueue<E>
```

| [java.util.concurrent.TransferQueue](TransferQueue.md) |

| Known Direct Subclasses [LinkedTransferQueue](LinkedTransferQueue.md) |----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------| | [LinkedTransferQueue](LinkedTransferQueue.md) | An unbounded [TransferQueue](TransferQueue.md) based on linked nodes. | |
| --- | --- | --- | --- | --- | --- | --- |

A [BlockingQueue](BlockingQueue.md) in which producers may wait for consumers to receive elements. A`TransferQueue`may be useful for example in message passing applications in which producers sometimes (using method [transfer](TransferQueue.md))) await receipt of elements by consumers invoking`take`or`poll`, while at other times enqueue elements (via method`put`) without waiting for receipt. [Non-blocking](TransferQueue.md))and [time-out](TransferQueue.md))versions of`tryTransfer`are also available. A`TransferQueue`may also be queried, via [hasWaitingConsumer](TransferQueue.md)), whether there are any threads waiting for items, which is a converse analogy to a`peek`operation.

Like other blocking queues, a`TransferQueue`may be capacity bounded. If so, an attempted transfer operation may initially block waiting for available space, and/or subsequently block waiting for reception by a consumer. Note that in a queue with zero capacity, such as [SynchronousQueue](SynchronousQueue.md),`put`and`transfer`are effectively synonymous.

This interface is a member of the [Java Collections Framework](https://developer.android.com//reference/java/util/package-summary.html#CollectionsFramework).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getWaitingConsumerCount](TransferQueue.md))`()` Returns an estimate of the number of consumers waiting to receive elements via [take](BlockingQueue.md))or timed [poll](BlockingQueue.md)). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasWaitingConsumer](TransferQueue.md))`()` Returns`true`if there is at least one consumer waiting to receive an element via [take](BlockingQueue.md))or timed [poll](BlockingQueue.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transfer](TransferQueue.md))`(`e:` `E`)` Transfers the element to a consumer, waiting if necessary to do so. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryTransfer](TransferQueue.md))`(`e:` `E`)` Transfers the element to a waiting consumer immediately, if possible. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [tryTransfer](TransferQueue.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` Transfers the element to a consumer if it is possible to do so before the timeout elapses. |

| Inherited functions ||
|---|---|
| From class [BlockingQueue](BlockingQueue.md) |------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [add](BlockingQueue.md))`(`element:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and throwing an`IllegalStateException`if no space is currently available. When using a capacity-restricted queue, it is generally preferable to use [offer](BlockingQueue.md)). <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [contains](BlockingQueue.md))`(`element:` `E`)` <br /> Returns`true`if this queue contains the specified element. More formally, returns`true`if and only if this queue contains at least one element`e`such that`o.equals(e)`. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](BlockingQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`)` <br /> Removes all available elements from this queue and adds them to the given collection. This operation may be more efficient than repeatedly polling this queue. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [drainTo](BlockingQueue.md))`(`c:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)<in` `E>!`, `maxElements:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Removes at most the given number of available elements from this queue and adds them to the given collection. A failure encountered while attempting to add elements to collection`c`may result in elements being in neither, either or both collections when the associated exception is thrown. Attempts to drain a queue to itself result in`IllegalArgumentException`. Further, the behavior of this operation is undefined if the specified collection is modified while the operation is in progress. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](BlockingQueue.md))`(`e:` `E`)` <br /> Inserts the specified element into this queue if it is possible to do so immediately without violating capacity restrictions, returning`true`upon success and`false`if no space is currently available. When using a capacity-restricted queue, this method is generally preferable to #add, which can fail to insert an element only by throwing an exception. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [offer](BlockingQueue.md))`(`e:` `E`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Inserts the specified element into this queue, waiting up to the specified wait time if necessary for space to become available. <br /> | | E | [poll](BlockingQueue.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](TimeUnit.md)!`)` <br /> Retrieves and removes the head of this queue, waiting up to the specified wait time if necessary for an element to become available. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](BlockingQueue.md))`(`e:` `E`)` <br /> Inserts the specified element into this queue, waiting if necessary for space to become available. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [remainingCapacity](BlockingQueue.md))`()` <br /> Returns the number of additional elements that this queue can ideally (in the absence of memory or resource constraints) accept without blocking, or`Integer.MAX_VALUE`if there is no intrinsic limit. Note that you*cannot* always tell if an attempt to insert an element will succeed by inspecting`remainingCapacity`because it may be the case that another thread is about to insert or remove an element. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [remove](BlockingQueue.md))`(`element:` `E`)` <br /> Removes a single instance of the specified element from this queue, if it is present. More formally, removes an element`e`such that`o.equals(e)`, if this queue contains one or more such elements. Returns`true`if this queue contained the specified element (or equivalently, if this queue changed as a result of the call). <br /> | | E | [take](BlockingQueue.md))`()` <br /> Retrieves and removes the head of this queue, waiting if necessary until an element becomes available. <br /> | ||
| From class [Queue](../java.util/Queue.md) |----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | E | [element](../java.util/Queue.md))`()` <br /> Retrieves, but does not remove, the head of this queue. This method differs from [peek](../java.util/Queue.md))only in that it throws an exception if this queue is empty. <br /> | | E? | [peek](../java.util/Queue.md))`()` <br /> Retrieves, but does not remove, the head of this queue, or returns`null`if this queue is empty. <br /> | | E? | [poll](../java.util/Queue.md))`()` <br /> Retrieves and removes the head of this queue, or returns`null`if this queue is empty. <br /> | | E | [remove](../java.util/Queue.md))`()` <br /> Retrieves and removes the head of this queue. This method differs from [poll()](../java.util/Queue.md))only in that it throws an exception if this queue is empty. <br /> | ||

## Public methods

### getWaitingConsumerCount

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getWaitingConsumerCount(): Int
```

Returns an estimate of the number of consumers waiting to receive elements via [take](BlockingQueue.md))or timed [poll](BlockingQueue.md)). The return value is an approximation of a momentary state of affairs, that may be inaccurate if consumers have completed or given up waiting. The value may be useful for monitoring and heuristics, but not for synchronization control. Implementations of this method are likely to be noticeably slower than those for [hasWaitingConsumer](TransferQueue.md)).

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of consumers waiting to receive elements |

### hasWaitingConsumer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasWaitingConsumer(): Boolean
```

Returns`true`if there is at least one consumer waiting to receive an element via [take](BlockingQueue.md))or timed [poll](BlockingQueue.md)). The return value represents a momentary state of affairs.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if there is at least one waiting consumer |

### transfer

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun transfer(e: E): Unit
```

Transfers the element to a consumer, waiting if necessary to do so.

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](BlockingQueue.md))or timed [poll](BlockingQueue.md))), else waits until the element is received by a consumer.

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

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](BlockingQueue.md))or timed [poll](BlockingQueue.md))), otherwise returning`false`without enqueuing the element.

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

More precisely, transfers the specified element immediately if there exists a consumer already waiting to receive it (in [take](BlockingQueue.md))or timed [poll](BlockingQueue.md))), else waits until the element is received by a consumer, returning`false`if the specified wait time elapses before the element can be transferred.

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
