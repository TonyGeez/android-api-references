# Flow

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Flow

```
class Flow
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.util.concurrent.Flow](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow#) |

Interrelated interfaces and static methods for establishing flow-controlled components in which [Publishers](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher) produce items consumed by one or more [Subscribers](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber), each managed by a [Subscription](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscription).

These interfaces correspond to the [reactive-streams](http://www.reactive-streams.org/) specification. They apply in both concurrent and distributed asynchronous settings: All (seven) methods are defined in`void`"one-way" message style. Communication relies on a simple form of flow control (method [Subscription.request](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscription#request(kotlin.Long))) that can be used to avoid resource management problems that may otherwise occur in "push" based systems.

**Examples.** A [Publisher](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher) usually defines its own [Subscription](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscription) implementation; constructing one in method`subscribe`and issuing it to the calling [Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber). It publishes items to the subscriber asynchronously, normally using an [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor). For example, here is a very simple publisher that only issues (when requested) a single`TRUE`item to a single subscriber. Because the subscriber receives only a single item, this class does not use buffering and ordering control required in most implementations. 

```kotlin
<code>class OneShotPublisher implements Publisher&lt;Boolean&gt; {
    private final ExecutorService executor = ForkJoinPool.commonPool(); // daemon-based
    private boolean subscribed; // true after first subscribe
    public synchronized void subscribe(Subscriber&lt;? super Boolean&gt; subscriber) {
      if (subscribed)
        subscriber.onError(new IllegalStateException()); // only one allowed
      else {
        subscribed = true;
        subscriber.onSubscribe(new OneShotSubscription(subscriber, executor));
      }
    }
    static class OneShotSubscription implements Subscription {
      private final Subscriber&lt;? super Boolean&gt; subscriber;
      private final ExecutorService executor;
      private Future&lt;?&gt; future; // to allow cancellation
      private boolean completed;
      OneShotSubscription(Subscriber&lt;? super Boolean&gt; subscriber,
                          ExecutorService executor) {
        this.subscriber = subscriber;
        this.executor = executor;
      }
      public synchronized void request(long n) {
        if (!completed) {
          completed = true;
          if (n &lt;= 0) {
            IllegalArgumentException ex = new IllegalArgumentException();
            executor.execute(() -&gt; subscriber.onError(ex));
          } else {
            future = executor.submit(() -&gt; {
              subscriber.onNext(Boolean.TRUE);
              subscriber.onComplete();
            });
          }
        }
      }
      public synchronized void cancel() {
        completed = true;
        if (future != null) future.cancel(false);
      }
    }
  }</code>
```

A [Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber) arranges that items be requested and processed. Items (invocations of [Subscriber.onNext](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber#onNext(java.util.concurrent.Flow.Subscriber.T))) are not issued unless requested, but multiple items may be requested. Many Subscriber implementations can arrange this in the style of the following example, where a buffer size of 1 single-steps, and larger sizes usually allow for more efficient overlapped processing with less communication; for example with a value of 64, this keeps total outstanding requests between 32 and 64. Because Subscriber method invocations for a given [Subscription](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscription) are strictly ordered, there is no need for these methods to use locks or volatiles unless a Subscriber maintains multiple Subscriptions (in which case it is better to instead define multiple Subscribers, each with its own Subscription). 

```kotlin
<code>class SampleSubscriber&lt;T&gt; implements Subscriber&lt;T&gt; {
    final Consumer&lt;? super T&gt; consumer;
    Subscription subscription;
    final long bufferSize;
    long count;
    SampleSubscriber(long bufferSize, Consumer&lt;? super T&gt; consumer) {
      this.bufferSize = bufferSize;
      this.consumer = consumer;
    }
    public void onSubscribe(Subscription subscription) {
      long initialRequestSize = bufferSize;
      count = bufferSize - bufferSize / 2; // re-request when half consumed
      (this.subscription = subscription).request(initialRequestSize);
    }
    public void onNext(T item) {
      if (--count &lt;= 0)
        subscription.request(count = bufferSize - bufferSize / 2);
      consumer.accept(item);
    }
    public void onError(Throwable ex) { ex.printStackTrace(); }
    public void onComplete() {}
  }</code>
```

The default value of [defaultBufferSize](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow#defaultBufferSize())may provide a useful starting point for choosing request sizes and capacities in Flow components based on expected rates, resources, and usages. Or, when flow control is never needed, a subscriber may initially request an effectively unbounded number of items, as in: 

```kotlin
<code>class UnboundedSubscriber&lt;T&gt; implements Subscriber&lt;T&gt; {
    public void onSubscribe(Subscription subscription) {
      subscription.request(Long.MAX_VALUE); // effectively unbounded
    }
    public void onNext(T item) { use(item); }
    public void onError(Throwable ex) { ex.printStackTrace(); }
    public void onComplete() {}
    void use(T item) { ... }
  }</code>
```

## Summary

| Nested classes ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Processor](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Processor) A component that acts as both a Subscriber and Publisher. |
| abstract | [Publisher](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher) A producer of items (and related control messages) received by Subscribers. |
| abstract | [Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber) A receiver of messages. |
| --- | --- |
| abstract | [Subscription](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscription) Message control linking a [Publisher](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher) and [Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber). |

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [defaultBufferSize](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow#defaultBufferSize())`()` Returns a default value for Publisher or Subscriber buffering, that may be used in the absence of other constraints. |

## Public methods

### defaultBufferSize

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun defaultBufferSize(): Int
```

Returns a default value for Publisher or Subscriber buffering, that may be used in the absence of other constraints.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the buffer size value |
