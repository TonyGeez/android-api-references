# BatchResultCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BatchResultCallback

Kotlin| [Java](../android/app/appsearch/BatchResultCallback.md) 
| --- | --- |

```
interface BatchResultCallback<KeyType : Any!, ValueType : Any!>
```

| [android.app.appsearch.BatchResultCallback](../android/app/appsearch/BatchResultCallback.md) |

The callback interface to return [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResult](../android/app/appsearch/BatchResultCallback.md))`(`result:` ` [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md)<KeyType,` `ValueType>`)` Called when [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md) results are ready. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSystemError](../android/app/appsearch/BatchResultCallback.md))`(`throwable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Called when a system error occurs. |

## Public methods

### onResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onResult(result: AppSearchBatchResult<KeyType, ValueType>): Unit
```

Called when [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md) results are ready.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `result` | [AppSearchBatchResult](../android/app/appsearch/AppSearchBatchResult.md)\<KeyType,ValueType\>:The result of the executed request. This value cannot be`null`. |

### onSystemError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSystemError(throwable: Throwable?): Unit
```

Called when a system error occurs.

This method is only called the infrastructure is fundamentally broken or unavailable, such that none of the requests could be started. For example, it will be called if the AppSearch service unexpectedly fails to initialize and can't be recovered by any means, or if communicating to the server over Binder fails (for example system service crashed or device is rebooting).

The error is not expected to be recoverable and there is no specific recommended action other than displaying a permanent message to the user.

Normal errors that are caused by invalid inputs or recoverable/retriable situations are reported associated with the input that caused them via the [onResult](../android/app/appsearch/BatchResultCallback.md))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `throwable` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:an exception describing the system error This value may be`null`. |
