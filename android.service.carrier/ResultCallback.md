# CarrierMessagingService.ResultCallback

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResultCallback

Kotlin| [Java](https://developer.android.com/reference/android/service/carrier/CarrierMessagingService.ResultCallback "View this page in Java") 
| --- | --- |

```
interface ResultCallback<T : Any!>
```

| [android.service.carrier.CarrierMessagingService.ResultCallback](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingService.ResultCallback#) |

A callback interface used to provide results asynchronously.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceiveResult](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierMessagingService.ResultCallback#onReceiveResult(android.service.carrier.CarrierMessagingService.ResultCallback.T))`(`result:` `T`)` Invoked when the result is available. |

## Public methods

### onReceiveResult

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onReceiveResult(result: T): Unit
```

Invoked when the result is available.

| Parameters ||
|----------|------------------------------------------|
| `result` | T:the result This value cannot be`null`. |
