# Flow.Subscription

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Subscription

```
interface Subscription
```

| [java.util.concurrent.Flow.Subscription](../java/util/concurrent/Flow.Subscription.md) |

Message control linking a [Publisher](../java/util/concurrent/Flow.Publisher.md) and [Subscriber](../java/util/concurrent/Flow.Subscriber.md). Subscribers receive items only when requested, and may cancel at any time. The methods in this interface are intended to be invoked only by their Subscribers; usages in other contexts have undefined effects.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../java/util/concurrent/Flow.Subscription.md))`()` Causes the Subscriber to (eventually) stop receiving messages. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [request](../java/util/concurrent/Flow.Subscription.md))`(`n:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Adds the given number`n`of items to the current unfulfilled demand for this subscription. |

## Public methods

### cancel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Causes the Subscriber to (eventually) stop receiving messages. Implementation is best-effort -- additional messages may be received after invoking this method. A cancelled subscription need not ever receive an`onComplete`or`onError`signal. 

### request

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun request(n: Long): Unit
```

Adds the given number`n`of items to the current unfulfilled demand for this subscription. If`n`is less than or equal to zero, the Subscriber will receive an`onError`signal with an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) argument. Otherwise, the Subscriber will receive up to`n`additional`onNext`invocations (or fewer if terminated).

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `n` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the increment of demand; a value of`Long.MAX_VALUE`may be considered as effectively unbounded |
