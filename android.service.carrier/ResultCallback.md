# CarrierMessagingService.ResultCallback

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResultCallback

Kotlin| [Java](../android/service/carrier/CarrierMessagingService.ResultCallback.md) 
| --- | --- |

```
interface ResultCallback<T : Any!>
```

| [android.service.carrier.CarrierMessagingService.ResultCallback](../android/service/carrier/CarrierMessagingService.ResultCallback.md) |

A callback interface used to provide results asynchronously.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceiveResult](../android/service/carrier/CarrierMessagingService.ResultCallback.md))`(`result:` `T`)` Invoked when the result is available. |

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
