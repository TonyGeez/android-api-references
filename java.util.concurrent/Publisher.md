# Flow.Publisher

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Publisher

```
@FunctionalInterface interface Publisher<T : Any!>
```

| [java.util.concurrent.Flow.Publisher](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher#) |

| Known Direct Subclasses [Flow.Processor](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Processor), [SubmissionPublisher](https://developer.android.com/reference/kotlin/java/util/concurrent/SubmissionPublisher) |----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Flow.Processor](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Processor) | A component that acts as both a Subscriber and Publisher. | | [SubmissionPublisher](https://developer.android.com/reference/kotlin/java/util/concurrent/SubmissionPublisher) | A [Flow.Publisher](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher#) that asynchronously issues submitted (non-null) items to current subscribers until it is closed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A producer of items (and related control messages) received by Subscribers. Each current [Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber) receives the same items (via method`onNext`) in the same order, unless drops or errors are encountered. If a Publisher encounters an error that does not allow items to be issued to a Subscriber, that Subscriber receives`onError`, and then receives no further messages. Otherwise, when it is known that no further messages will be issued to it, a subscriber receives`onComplete`. Publishers ensure that Subscriber method invocations for each subscription are strictly ordered in [*happens-before*](https://developer.android.com/reference/kotlin/java/util/concurrent/package-summary#MemoryVisibility) order.

Publishers may vary in policy about whether drops (failures to issue an item because of resource limitations) are treated as unrecoverable errors. Publishers may also vary about whether Subscribers receive items that were produced or available before they subscribed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Publisher#subscribe(java.util.concurrent.Flow.Subscriber))`(`subscriber:` ` [Flow.Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber)<in` `T>!`)` Adds the given Subscriber if possible. |

## Public methods

### subscribe

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subscribe(subscriber: Flow.Subscriber<in T>!): Unit
```

Adds the given Subscriber if possible. If already subscribed, or the attempt to subscribe fails due to policy violations or errors, the Subscriber's`onError`method is invoked with an [IllegalStateException](https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#). Otherwise, the Subscriber's`onSubscribe`method is invoked with a new [Subscription](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscription). Subscribers may enable receiving items by invoking the`request`method of this Subscription, and may unsubscribe by invoking its`cancel`method.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| `subscriber` | [Flow.Subscriber](https://developer.android.com/reference/kotlin/java/util/concurrent/Flow.Subscriber)\<inT\>!:the subscriber |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if subscriber is null |
