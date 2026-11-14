# Flow.Subscriber

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Subscriber

```
interface Subscriber<T : Any!>
```

| [java.util.concurrent.Flow.Subscriber](../java/util/concurrent/Flow.Subscriber.md) |

| Known Direct Subclasses [Flow.Processor](../java/util/concurrent/Flow.Processor.md) |------------------------------------------------------------------------------------------------------|-----------------------------------------------------------| | [Flow.Processor](../java/util/concurrent/Flow.Processor.md) | A component that acts as both a Subscriber and Publisher. | |
| --- | --- | --- | --- | --- | --- | --- |

A receiver of messages. The methods in this interface are invoked in strict sequential order for each [Subscription](../java/util/concurrent/Flow.Subscription.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onComplete](../java/util/concurrent/Flow.Subscriber.md))`()` Method invoked when it is known that no additional Subscriber method invocations will occur for a Subscription that is not already terminated by error, after which no other Subscriber methods are invoked by the Subscription. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onError](../java/util/concurrent/Flow.Subscriber.md))`(`throwable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`)` Method invoked upon an unrecoverable error encountered by a Publisher or Subscription, after which no other Subscriber methods are invoked by the Subscription. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onNext](../java/util/concurrent/Flow.Subscriber.md))`(`item:` `T`)` Method invoked with a Subscription's next item. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSubscribe](../java/util/concurrent/Flow.Subscriber.md))`(`subscription:` ` [Flow.Subscription](../java/util/concurrent/Flow.Subscription.md)!`)` Method invoked prior to invoking any other Subscriber methods for the given Subscription. |

## Public methods

### onComplete

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onComplete(): Unit
```

Method invoked when it is known that no additional Subscriber method invocations will occur for a Subscription that is not already terminated by error, after which no other Subscriber methods are invoked by the Subscription. If this method throws an exception, resulting behavior is undefined. 

### onError

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(throwable: Throwable!): Unit
```

Method invoked upon an unrecoverable error encountered by a Publisher or Subscription, after which no other Subscriber methods are invoked by the Subscription. If this method itself throws an exception, resulting behavior is undefined.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------|
| `throwable` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:the exception |

### onNext

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNext(item: T): Unit
```

Method invoked with a Subscription's next item. If this method throws an exception, resulting behavior is not guaranteed, but may cause the Subscription to be cancelled.

| Parameters ||
|--------|------------|
| `item` | T:the item |

### onSubscribe

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSubscribe(subscription: Flow.Subscription!): Unit
```

Method invoked prior to invoking any other Subscriber methods for the given Subscription. If this method throws an exception, resulting behavior is not guaranteed, but may cause the Subscription not to be established or to be cancelled.

Typically, implementations of this method invoke`subscription.request`to enable receiving items.

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------|
| `subscription` | [Flow.Subscription](../java/util/concurrent/Flow.Subscription.md)!:a new subscription |
