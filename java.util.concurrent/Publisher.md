# Flow.Publisher

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Publisher

```
@FunctionalInterface interface Publisher<T : Any!>
```

| [java.util.concurrent.Flow.Publisher](../java/util/concurrent/Flow.Publisher.md) |

| Known Direct Subclasses [Flow.Processor](../java/util/concurrent/Flow.Processor.md), [SubmissionPublisher](SubmissionPublisher.md) |----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Flow.Processor](../java/util/concurrent/Flow.Processor.md) | A component that acts as both a Subscriber and Publisher. | | [SubmissionPublisher](SubmissionPublisher.md) | A [Flow.Publisher](../java/util/concurrent/Flow.Publisher.md) that asynchronously issues submitted (non-null) items to current subscribers until it is closed. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A producer of items (and related control messages) received by Subscribers. Each current [Subscriber](../java/util/concurrent/Flow.Subscriber.md) receives the same items (via method`onNext`) in the same order, unless drops or errors are encountered. If a Publisher encounters an error that does not allow items to be issued to a Subscriber, that Subscriber receives`onError`, and then receives no further messages. Otherwise, when it is known that no further messages will be issued to it, a subscriber receives`onComplete`. Publishers ensure that Subscriber method invocations for each subscription are strictly ordered in [*happens-before*](_package.md) order.

Publishers may vary in policy about whether drops (failures to issue an item because of resource limitations) are treated as unrecoverable errors. Publishers may also vary about whether Subscribers receive items that were produced or available before they subscribed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [subscribe](../java/util/concurrent/Flow.Publisher.md))`(`subscriber:` ` [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)<in` `T>!`)` Adds the given Subscriber if possible. |

## Public methods

### subscribe

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun subscribe(subscriber: Flow.Subscriber<in T>!): Unit
```

Adds the given Subscriber if possible. If already subscribed, or the attempt to subscribe fails due to policy violations or errors, the Subscriber's`onError`method is invoked with an [IllegalStateException](../java.lang/IllegalStateException.md). Otherwise, the Subscriber's`onSubscribe`method is invoked with a new [Subscription](../java/util/concurrent/Flow.Subscription.md). Subscribers may enable receiving items by invoking the`request`method of this Subscription, and may unsubscribe by invoking its`cancel`method.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| `subscriber` | [Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md)\<inT\>!:the subscriber |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | if subscriber is null |
