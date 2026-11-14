Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SavedDatasetsInfoCallback

Kotlin | [Java](SavedDatasetsInfoCallback.md)
| --- | --- |

```
interface SavedDatasetsInfoCallback
```

| [android.service.autofill.SavedDatasetsInfoCallback](SavedDatasetsInfoCallback.md) |

Handles the response to onSavedDatasetsInfoRequest.

Use onSuccess to return the computed info about the datasets the user saved to this service. If there was an error querying the info, or if the service is unable to do so at this time (for example, if the user isn't logged in), call onError.

This callback can be used only once.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback#ERROR_NEEDS_USER_ACTION:kotlin.Int` The result cannot be computed until the user takes some action, such as setting up their account. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback#ERROR_OTHER:kotlin.Int` The result could not be computed for any other reason. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback#ERROR_UNSUPPORTED:kotlin.Int` The service does not support this request. |
| --- | --- |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onError Respond to the request with an error. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onSuccess Successfully respond to the request with the info on each type of saved datasets. |

## Constants

### ERROR_NEEDS_USER_ACTION

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_NEEDS_USER_ACTION: Int
```

The result cannot be computed until the user takes some action, such as setting up their account.

 Value: 2

### ERROR_OTHER

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_OTHER: Int
```

The result could not be computed for any other reason.

 Value: 0

### ERROR_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR_UNSUPPORTED: Int
```

The service does not support this request.

 Value: 1

## Public methods

### onError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onError(error: Int): Unit
```

Respond to the request with an error. System settings may display a suitable notice to the user.

| Parameters ||
|---|---|
| `error` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback#ERROR_OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback#ERROR_UNSUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/service/autofill/SavedDatasetsInfoCallback#ERROR_NEEDS_USER_ACTION:kotlin.Int` |

### onSuccess

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onSuccess(results: MutableSet<SavedDatasetsInfo!>): Unit
```

Successfully respond to the request with the info on each type of saved datasets.

| Parameters ||
|---|---|
| `results` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [SavedDatasetsInfo](SavedDatasetsInfo.md)!\>: This value cannot be `null`. |
