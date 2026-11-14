# BatchResultCallback

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BatchResultCallback

Kotlin| [Java](https://developer.android.com/reference/android/app/appsearch/BatchResultCallback "View this page in Java") 

```
interface BatchResultCallback<KeyType : Any!, ValueType : Any!>
```

| [android.app.appsearch.BatchResultCallback](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#) |

The callback interface to return [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResult](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onResult(android.app.appsearch.AppSearchBatchResult))`(`result:` ` [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult)<KeyType,` `ValueType>`)` Called when [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) results are ready. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSystemError](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onSystemError(kotlin.Throwable))`(`throwable:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` Called when a system error occurs. |

## Public methods

### onResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onResult(result: AppSearchBatchResult<KeyType, ValueType>): Unit
```

Called when [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult) results are ready.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `result` | [AppSearchBatchResult](https://developer.android.com/reference/kotlin/android/app/appsearch/AppSearchBatchResult)\<KeyType,ValueType\>:The result of the executed request. This value cannot be`null`. |

### onSystemError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSystemError(throwable: Throwable?): Unit
```

Called when a system error occurs.

This method is only called the infrastructure is fundamentally broken or unavailable, such that none of the requests could be started. For example, it will be called if the AppSearch service unexpectedly fails to initialize and can't be recovered by any means, or if communicating to the server over Binder fails (for example system service crashed or device is rebooting).

The error is not expected to be recoverable and there is no specific recommended action other than displaying a permanent message to the user.

Normal errors that are caused by invalid inputs or recoverable/retriable situations are reported associated with the input that caused them via the [onResult](https://developer.android.com/reference/kotlin/android/app/appsearch/BatchResultCallback#onResult(android.app.appsearch.AppSearchBatchResult))method.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `throwable` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:an exception describing the system error This value may be`null`. |
