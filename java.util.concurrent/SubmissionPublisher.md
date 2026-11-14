# SubmissionPublisher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SubmissionPublisher

```
open class SubmissionPublisher<T : Any!> : AutoCloseable, Flow.Publisher<T>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.SubmissionPublisher](../java/util/concurrent/SubmissionPublisher.md) |

A [Flow.Publisher](../java/util/concurrent/Flow.Publisher.md) that asynchronously issues submitted (non-null) items to current subscribers until it is closed. Each current subscriber receives newly submitted items in the same order unless drops or exceptions are encountered. Using a SubmissionPublisher allows item generators to act as compliant [reactive-streams](http://www.reactive-streams.org/) Publishers relying on drop handling and/or blocking for flow control.

A SubmissionPublisher uses the [Executor](../java/util/concurrent/Executor.md) supplied in its constructor for delivery to subscribers. The best choice of Executor depends on expected usage. If the generator(s) of submitted items run in separate threads, and the number of subscribers can be estimated, consider using a java.util.concurrent.Executors#newFixedThreadPool. Otherwise consider using the default, normally the [ForkJoinPool.commonPool](../java/util/concurrent/ForkJoinPool.md)).

Buffering allows producers and consumers to transiently operate at different rates. Each subscriber uses an independent buffer. Buffers are created upon first use and expanded as needed up to the given maximum. (The enforced capacity may be rounded up to the nearest power of two and/or bounded by the largest value supported by this implementation.) Invocations of [request](../java/util/concurrent/Flow.Subscription.md)) do not directly result in buffer expansion, but risk saturation if unfilled requests exceed the maximum capacity. The default value of [java.util.concurrent.Flow#defaultBufferSize()](../java/util/concurrent/Flow.md)) may provide a useful starting point for choosing a capacity based on expected rates, resources, and usages.

A single SubmissionPublisher may be shared among multiple sources. Actions in a source thread prior to publishing an item or issuing a signal [*happen-before*](../java/util/concurrent/_package.md) actions subsequent to the corresponding access by each subscriber. But reported estimates of lag and demand are designed for use in monitoring, not for synchronization control, and may reflect stale or inaccurate views of progress.

Publication methods support different policies about what to do when buffers are saturated. Method [submit](../java/util/concurrent/SubmissionPublisher.md)) blocks until resources are available. This is simplest, but least responsive. The `offer` methods may drop items (either immediately or with bounded timeout), but provide an opportunity to interpose a handler and then retry.

If any Subscriber method throws an exception, its subscription is cancelled. If a handler is supplied as a constructor argument, it is invoked before cancellation upon an exception in method [onNext](../java/util/concurrent/Flow.Subscriber.md)), but exceptions in methods [onSubscribe](../java/util/concurrent/Flow.Subscriber.md)), [onError](../java/util/concurrent/Flow.Subscriber.md)) and [onComplete](../java/util/concurrent/Flow.Subscriber.md)) are not recorded or handled before cancellation. If the supplied Executor throws [RejectedExecutionException](../java/util/concurrent/RejectedExecutionException.md) (or any other RuntimeException or Error) when attempting to execute a task, or a drop handler throws an exception when processing a dropped item, then the exception is rethrown. In these cases, not all subscribers will have been issued the published item. It is usually good practice to [closeExceptionally](../java/util/concurrent/SubmissionPublisher.md)) in these cases.

Method [consume(java.util.function.Consumer)](../java/util/concurrent/SubmissionPublisher.md)) simplifies support for a common case in which the only action of a subscriber is to request and process all items using a supplied function.

This class may also serve as a convenient base for subclasses that generate items, and use the methods in this class to publish them. For example here is a class that periodically publishes the items generated from a supplier. (In practice you might add methods to independently start and stop generation, to share Executors among publishers, and so on, or use a SubmissionPublisher as a component rather than a superclass.) 

```kotlin
<code>class PeriodicPublisher&lt;T&gt; extends SubmissionPublisher&lt;T&gt; {
    final ScheduledFuture&lt;?&gt; periodicTask;
    final ScheduledExecutorService scheduler;
    PeriodicPublisher(Executor executor, int maxBufferCapacity,
                      Supplier&lt;? extends T&gt; supplier,
                      long period, TimeUnit unit) {
      super(executor, maxBufferCapacity);
      scheduler = new ScheduledThreadPoolExecutor(1);
      periodicTask = scheduler.scheduleAtFixedRate(
        () -&gt; submit(supplier.get()), 0, period, unit);
    }
    public void close() {
      periodicTask.cancel(false);
      scheduler.shutdown();
      super.close();
    }
  }</code>
```

Here is an example of a [Flow.Processor](../java/util/concurrent/Flow.Processor.md) implementation. It uses single-step requests to its publisher for simplicity of illustration. A more adaptive version could monitor flow using the lag estimate returned from `submit`, along with other utility methods. 

```kotlin
<code>class TransformProcessor&lt;S,T&gt; extends SubmissionPublisher&lt;T&gt;
    implements Flow.Processor&lt;S,T&gt; {
    final Function&lt;? super S, ? extends T&gt; function;
    Flow.Subscription subscription;
    TransformProcessor(Executor executor, int maxBufferCapacity,
                       Function&lt;? super S, ? extends T&gt; function) {
      super(executor, maxBufferCapacity);
      this.function = function;
    }
    public void onSubscribe(Flow.Subscription subscription) {
      (this.subscription = subscription).request(1);
    }
    public void onNext(S item) {
      subscription.request(1);
      submit(function.apply(item));
    }
    public void onError(Throwable ex) { closeExceptionally(ex); }
    public void onComplete() { close(); }
  }</code>
```

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SubmissionPublisher](../java/util/concurrent/SubmissionPublisher.md))`()` Creates a new SubmissionPublisher using the [java.util.concurrent.ForkJoinPool#commonPool()](../java/util/concurrent/ForkJoinPool.md)) for async delivery to subscribers (unless it does not support a parallelism level of at least two, in which case, a new Thread is created to run each task), with maximum buffer capacity of [Flow.defaultBufferSize](../java/util/concurrent/Flow.md)), and no handler for Subscriber exceptions in method [onNext](../java/util/concurrent/Flow.Subscriber.md)). |
| [SubmissionPublisher](../java/util/concurrent/SubmissionPublisher.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)!`, `maxBufferCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a new SubmissionPublisher using the given Executor for async delivery to subscribers, with the given maximum buffer size for each subscriber, and no handler for Subscriber exceptions in method [onNext](../java/util/concurrent/Flow.Subscriber.md)). |
| [SubmissionPublisher](../java/util/concurrent/SubmissionPublisher.md))`(`executor:` ` [Executor](../java/util/concurrent/Executor.md)!`, `maxBufferCapacity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `handler:` ` [BiConsumer](../java/util/function/BiConsumer.md)<in` ` [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!,` `in` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!>!`)` Creates a new SubmissionPublisher using the given Executor for async delivery to subscribers, with the given maximum buffer size for each subscriber, and, if non-null, the given handler invoked when any Subscriber throws an exception in method [onNext](../java/util/concurrent/Flow.Subscriber.md)). |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/util/concurrent/SubmissionPublisher.md))`()` Unless already closed, issues [onComplete](../java/util/concurrent/Flow.Subscriber.md)) signals to current subscribers, and disallows subsequent attempts to publish. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [closeExceptionally](../java/util/concurrent/SubmissionPublisher.md))`(`error:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Unless already closed, issues [onError](../java/util/concurrent/Flow.Subscriber.md)) signals to current subscribers with the given error, and disallows subsequent attempts to publish. |
| open [CompletableFuture](../java/util/concurrent/CompletableFuture.md)\< [Void](../java/lang/Void.md)!\>! | [consume](../java/util/concurrent/SubmissionPublisher.md))`(`consumer:` ` [Consumer](../java/util/function/Consumer.md)<in` `T>!`)` Processes all published items using the given Consumer function. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [estimateMaximumLag](../java/util/concurrent/SubmissionPublisher.md))`()` Returns an estimate of the maximum number of items produced but not yet consumed among all current subscribers. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [estimateMinimumDemand](../java/util/concurrent/SubmissionPublisher.md))`()` Returns an estimate of the minimum number of items requested (via [request](../java/util/concurrent/Flow.Subscription.md))) but not yet produced, among all current subscribers. |
| open [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | [getClosedException](../java/util/concurrent/SubmissionPublisher.md))`()` Returns the exception associated with [closeExceptionally](../java/util/concurrent/SubmissionPublisher.md)), or null if not closed or if closed normally. |
| --- | --- |
| open [Executor](../java/util/concurrent/Executor.md)! | [getExecutor](../java/util/concurrent/SubmissionPublisher.md))`()` Returns the Executor used for asynchronous delivery. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxBufferCapacity](../java/util/concurrent/SubmissionPublisher.md))`()` Returns the maximum per-subscriber buffer capacity. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNumberOfSubscribers](../java/util/concurrent/SubmissionPublisher.md))`()` Returns the number of current subscribers. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<in T\>!\>! | [getSubscribers](../java/util/concurrent/SubmissionPublisher.md))`()` Returns a list of current subscribers for monitoring and tracking purposes, not for invoking [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md) methods on the subscribers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasSubscribers](../java/util/concurrent/SubmissionPublisher.md))`()` Returns true if this publisher has any subscribers. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isClosed](../java/util/concurrent/SubmissionPublisher.md))`()` Returns true if this publisher is not accepting submissions. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSubscribed](../java/util/concurrent/SubmissionPublisher.md))`(`subscriber:` ` [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!`)` Returns true if the given Subscriber is currently subscribed. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [offer](../java/util/concurrent/SubmissionPublisher.md))`(`item:` `T`, `onDrop:` ` [BiPredicate](../java/util/function/BiPredicate.md)< [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!,` `in` `T>!`)` Publishes the given item, if possible, to each current subscriber by asynchronously invoking its [onNext](../java/util/concurrent/Flow.Subscriber.md)) method. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [offer](../java/util/concurrent/SubmissionPublisher.md))`(`item:` `T`, `timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`, `onDrop:` ` [BiPredicate](../java/util/function/BiPredicate.md)< [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!,` `in` `T>!`)` Publishes the given item, if possible, to each current subscriber by asynchronously invoking its [onNext](../java/util/concurrent/Flow.Subscriber.md)) method, blocking while resources for any subscription are unavailable, up to the specified timeout or until the caller thread is interrupted, at which point the given handler (if non-null) is invoked, and if it returns true, retried once. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [submit](../java/util/concurrent/SubmissionPublisher.md))`(`item:` `T`)` Publishes the given item to each current subscriber by asynchronously invoking its [onNext](../java/util/concurrent/Flow.Subscriber.md)) method, blocking uninterruptibly while resources for any subscriber are unavailable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](../java/util/concurrent/SubmissionPublisher.md))`(`subscriber:` ` [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!`)` Adds the given Subscriber unless already subscribed. |

## Public constructors

### SubmissionPublisher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubmissionPublisher()
```

Creates a new SubmissionPublisher using the [java.util.concurrent.ForkJoinPool#commonPool()](../java/util/concurrent/ForkJoinPool.md)) for async delivery to subscribers (unless it does not support a parallelism level of at least two, in which case, a new Thread is created to run each task), with maximum buffer capacity of [Flow.defaultBufferSize](../java/util/concurrent/Flow.md)), and no handler for Subscriber exceptions in method [onNext](../java/util/concurrent/Flow.Subscriber.md)). 

### SubmissionPublisher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubmissionPublisher(
    executor: Executor!, 
    maxBufferCapacity: Int)
```

Creates a new SubmissionPublisher using the given Executor for async delivery to subscribers, with the given maximum buffer size for each subscriber, and no handler for Subscriber exceptions in method [onNext](../java/util/concurrent/Flow.Subscriber.md)).

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md)!: the executor to use for async delivery, supporting creation of at least one independent thread |
| `maxBufferCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum capacity for each subscriber's buffer (the enforced capacity may be rounded up to the nearest power of two and/or bounded by the largest value supported by this implementation; method [getMaxBufferCapacity](../java/util/concurrent/SubmissionPublisher.md)) returns the actual value) |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if executor is null |
| `java.lang.IllegalArgumentException` | if maxBufferCapacity not positive |

### SubmissionPublisher

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SubmissionPublisher(
    executor: Executor!, 
    maxBufferCapacity: Int, 
    handler: BiConsumer<in Flow.Subscriber<in T>!, in Throwable!>!)
```

Creates a new SubmissionPublisher using the given Executor for async delivery to subscribers, with the given maximum buffer size for each subscriber, and, if non-null, the given handler invoked when any Subscriber throws an exception in method [onNext](../java/util/concurrent/Flow.Subscriber.md)).

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `executor` | [Executor](../java/util/concurrent/Executor.md)!: the executor to use for async delivery, supporting creation of at least one independent thread |
| `maxBufferCapacity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum capacity for each subscriber's buffer (the enforced capacity may be rounded up to the nearest power of two and/or bounded by the largest value supported by this implementation; method [getMaxBufferCapacity](../java/util/concurrent/SubmissionPublisher.md)) returns the actual value) |
| `handler` | [BiConsumer](../java/util/function/BiConsumer.md)\<in [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<in T\>!, in [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!\>!: if non-null, procedure to invoke upon exception thrown in method `onNext` |
| --- | --- |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | if executor is null |
| `java.lang.IllegalArgumentException` | if maxBufferCapacity not positive |

## Public methods

### close

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Unless already closed, issues [onComplete](../java/util/concurrent/Flow.Subscriber.md)) signals to current subscribers, and disallows subsequent attempts to publish. Upon return, this method does *NOT* guarantee that all subscribers have yet completed.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### closeExceptionally

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeExceptionally(error: Throwable!): Unit
```

Unless already closed, issues [onError](../java/util/concurrent/Flow.Subscriber.md)) signals to current subscribers with the given error, and disallows subsequent attempts to publish. Future subscribers also receive the given error. Upon return, this method does *NOT* guarantee that all subscribers have yet completed.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------|
| `error` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!: the `onError` argument sent to subscribers |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | if error is null |

### consume

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun consume(consumer: Consumer<in T>!): CompletableFuture<Void!>!
```

Processes all published items using the given Consumer function. Returns a CompletableFuture that is completed normally when this publisher signals [onComplete](../java/util/concurrent/Flow.Subscriber.md)), or completed exceptionally upon any error, or an exception is thrown by the Consumer, or the returned CompletableFuture is cancelled, in which case no further items are processed.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `consumer` | [Consumer](../java/util/function/Consumer.md)\<in T\>!: the function applied to each onNext item |

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [CompletableFuture](../java/util/concurrent/CompletableFuture.md)< [Void](../java/lang/Void.md)!>! | a CompletableFuture that is completed normally when the publisher signals onComplete, and exceptionally upon any error or cancellation |

| Exceptions ||
|----------------------------------|---------------------|
| `java.lang.NullPointerException` | if consumer is null |

### estimateMaximumLag

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun estimateMaximumLag(): Int
```

Returns an estimate of the maximum number of items produced but not yet consumed among all current subscribers.

| Return ||
|----------------------------------------------------------------------------|--------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the estimate |

### estimateMinimumDemand

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun estimateMinimumDemand(): Long
```

Returns an estimate of the minimum number of items requested (via [request](../java/util/concurrent/Flow.Subscription.md))) but not yet produced, among all current subscribers.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the estimate, or zero if no subscribers |

### getClosedException

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getClosedException(): Throwable!
```

Returns the exception associated with [closeExceptionally](../java/util/concurrent/SubmissionPublisher.md)), or null if not closed or if closed normally.

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------|
| [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)! | the exception, or null if none |

### getExecutor

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getExecutor(): Executor!
```

Returns the Executor used for asynchronous delivery.

| Return ||
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [Executor](../java/util/concurrent/Executor.md)! | the Executor used for asynchronous delivery |

### getMaxBufferCapacity

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMaxBufferCapacity(): Int
```

Returns the maximum per-subscriber buffer capacity.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum per-subscriber buffer capacity |

### getNumberOfSubscribers

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumberOfSubscribers(): Int
```

Returns the number of current subscribers.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of current subscribers |

### getSubscribers

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSubscribers(): MutableList<Flow.Subscriber<in T>!>!
```

Returns a list of current subscribers for monitoring and tracking purposes, not for invoking [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md) methods on the subscribers.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!>! | list of current subscribers |

### hasSubscribers

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasSubscribers(): Boolean
```

Returns true if this publisher has any subscribers.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this publisher has any subscribers |

### isClosed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isClosed(): Boolean
```

Returns true if this publisher is not accepting submissions.

| Return ||
|------------------------------------------------------------------------------------|----------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if closed |

### isSubscribed

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSubscribed(subscriber: Flow.Subscriber<in T>!): Boolean
```

Returns true if the given Subscriber is currently subscribed.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `subscriber` | [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<in T\>!: the subscriber |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if currently subscribed |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if subscriber is null |

### offer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(
    item: T, 
    onDrop: BiPredicate<Flow.Subscriber<in T>!, in T>!
): Int
```

Publishes the given item, if possible, to each current subscriber by asynchronously invoking its [onNext](../java/util/concurrent/Flow.Subscriber.md)) method. The item may be dropped by one or more subscribers if resource limits are exceeded, in which case the given handler (if non-null) is invoked, and if it returns true, retried once. Other calls to methods in this class by other threads are blocked while the handler is invoked. Unless recovery is assured, options are usually limited to logging the error and/or issuing an [onError](../java/util/concurrent/Flow.Subscriber.md)) signal to the subscriber.

This method returns a status indicator: If negative, it represents the (negative) number of drops (failed attempts to issue the item to a subscriber). Otherwise it is an estimate of the maximum lag (number of items submitted but not yet consumed) among all current subscribers. This value is at least one (accounting for this submitted item) if there are any subscribers, else zero.

If the Executor for this publisher throws a RejectedExecutionException (or any other RuntimeException or Error) when attempting to asynchronously notify subscribers, or the drop handler throws an exception when processing a dropped item, then this exception is rethrown.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `item` | T: the (non-null) item to publish |
| `onDrop` | [BiPredicate](../java/util/function/BiPredicate.md)\< [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<in T\>!, in T\>!: if non-null, the handler invoked upon a drop to a subscriber, with arguments of the subscriber and item; if it returns true, an offer is re-attempted (once) |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | if negative, the (negative) number of drops; otherwise an estimate of maximum lag |

| Exceptions ||
|---------------------------------------------------|-----------------------|
| `java.lang.IllegalStateException` | if closed |
| `java.lang.NullPointerException` | if item is null |
| `java.util.concurrent.RejectedExecutionException` | if thrown by Executor |
| --- | --- |

### offer

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun offer(
    item: T, 
    timeout: Long, 
    unit: TimeUnit!, 
    onDrop: BiPredicate<Flow.Subscriber<in T>!, in T>!
): Int
```

Publishes the given item, if possible, to each current subscriber by asynchronously invoking its [onNext](../java/util/concurrent/Flow.Subscriber.md)) method, blocking while resources for any subscription are unavailable, up to the specified timeout or until the caller thread is interrupted, at which point the given handler (if non-null) is invoked, and if it returns true, retried once. (The drop handler may distinguish timeouts from interrupts by checking whether the current thread is interrupted.) Other calls to methods in this class by other threads are blocked while the handler is invoked. Unless recovery is assured, options are usually limited to logging the error and/or issuing an [onError](../java/util/concurrent/Flow.Subscriber.md)) signal to the subscriber.

This method returns a status indicator: If negative, it represents the (negative) number of drops (failed attempts to issue the item to a subscriber). Otherwise it is an estimate of the maximum lag (number of items submitted but not yet consumed) among all current subscribers. This value is at least one (accounting for this submitted item) if there are any subscribers, else zero.

If the Executor for this publisher throws a RejectedExecutionException (or any other RuntimeException or Error) when attempting to asynchronously notify subscribers, or the drop handler throws an exception when processing a dropped item, then this exception is rethrown.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `item` | T: the (non-null) item to publish |
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): how long to wait for resources for any subscriber before giving up, in units of `unit` |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!: a `TimeUnit` determining how to interpret the `timeout` parameter |
| --- | --- |
| `onDrop` | [BiPredicate](../java/util/function/BiPredicate.md)\< [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<in T\>!, in T\>!: if non-null, the handler invoked upon a drop to a subscriber, with arguments of the subscriber and item; if it returns true, an offer is re-attempted (once) |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | if negative, the (negative) number of drops; otherwise an estimate of maximum lag |

| Exceptions ||
|---------------------------------------------------|-----------------------|
| `java.lang.IllegalStateException` | if closed |
| `java.lang.NullPointerException` | if item is null |
| `java.util.concurrent.RejectedExecutionException` | if thrown by Executor |
| --- | --- |

### submit

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun submit(item: T): Int
```

Publishes the given item to each current subscriber by asynchronously invoking its [onNext](../java/util/concurrent/Flow.Subscriber.md)) method, blocking uninterruptibly while resources for any subscriber are unavailable. This method returns an estimate of the maximum lag (number of items submitted but not yet consumed) among all current subscribers. This value is at least one (accounting for this submitted item) if there are any subscribers, else zero.

If the Executor for this publisher throws a RejectedExecutionException (or any other RuntimeException or Error) when attempting to asynchronously notify subscribers, then this exception is rethrown, in which case not all subscribers will have been issued this item.

| Parameters ||
|--------|-----------------------------------|
| `item` | T: the (non-null) item to publish |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the estimated maximum lag among subscribers |

| Exceptions ||
|---------------------------------------------------|-----------------------|
| `java.lang.IllegalStateException` | if closed |
| `java.lang.NullPointerException` | if item is null |
| `java.util.concurrent.RejectedExecutionException` | if thrown by Executor |
| --- | --- |

### subscribe

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun subscribe(subscriber: Flow.Subscriber<in T>!): Unit
```

Adds the given Subscriber unless already subscribed. If already subscribed, the Subscriber's [onError](../java/util/concurrent/Flow.Subscriber.md)) method is invoked on the existing subscription with an [IllegalStateException](../java/lang/IllegalStateException.md). Otherwise, upon success, the Subscriber's [onSubscribe](../java/util/concurrent/Flow.Subscriber.md)) method is invoked asynchronously with a new [Flow.Subscription](../java/util/concurrent/Flow.Subscription.md). If [onSubscribe](../java/util/concurrent/Flow.Subscriber.md)) throws an exception, the subscription is cancelled. Otherwise, if this SubmissionPublisher was closed exceptionally, then the subscriber's [onError](../java/util/concurrent/Flow.Subscriber.md)) method is invoked with the corresponding exception, or if closed without exception, the subscriber's [onComplete](../java/util/concurrent/Flow.Subscriber.md)) method is invoked. Subscribers may enable receiving items by invoking the [request](../java/util/concurrent/Flow.Subscription.md)) method of the new Subscription, and may unsubscribe by invoking its [cancel](../java/util/concurrent/Flow.Subscription.md)) method.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------|
| `subscriber` | [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<in T\>!: the subscriber |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if subscriber is null |
