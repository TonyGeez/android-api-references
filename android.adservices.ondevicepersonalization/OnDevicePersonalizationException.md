# OnDevicePersonalizationException

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDevicePersonalizationException

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/OnDevicePersonalizationException "View this page in Java") 

```
open class OnDevicePersonalizationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#) ||
| | | ↳ | [android.adservices.ondevicepersonalization.OnDevicePersonalizationException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#) |

Exception thrown by OnDevicePersonalization APIs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INFERENCE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_FAILED:kotlin.Int) [ModelManager](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager) failed to run inference. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INFERENCE_MODEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND:kotlin.Int) Inference failed due to [ModelManager](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager) not finding the downloaded model. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_TRAINING_MANIFEST](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int) The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService)'s call to android. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int) The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) that was invoked failed to run. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_LOADING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED:kotlin.Int) The ODP module was unable to load the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED:kotlin.Int) The ODP specific manifest settings for the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) are either missing or misconfigured. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_TIMEOUT](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT:kotlin.Int) The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) was invoked but timed out before returning successfully. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PERSONALIZATION_DISABLED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED:kotlin.Int) The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) was not started because personalization is disabled by device configuration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SCHEDULE_TRAINING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int) The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService)'s call to android. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OnDevicePersonalizationException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#OnDevicePersonalizationException(kotlin.Int))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OnDevicePersonalizationException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#OnDevicePersonalizationException(kotlin.Int,%20kotlin.String))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [OnDevicePersonalizationException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#OnDevicePersonalizationException(kotlin.Int,%20kotlin.String,%20kotlin.Throwable))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |
| [OnDevicePersonalizationException](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#OnDevicePersonalizationException(kotlin.Int,%20kotlin.Throwable))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#getErrorCode())`()` Returns the error code for this exception. |

## Constants

### ERROR_INFERENCE_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INFERENCE_FAILED: Int
```

[ModelManager](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager) failed to run inference.

Retrying may be successful if the issue is due to a platform internal error. 

 Value: 9

### ERROR_INFERENCE_MODEL_NOT_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INFERENCE_MODEL_NOT_FOUND: Int
```

Inference failed due to [ModelManager](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ModelManager) not finding the downloaded model. 

 Value: 8

### ERROR_INVALID_TRAINING_MANIFEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_TRAINING_MANIFEST: Int
```

The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService)'s call to android.adservices.ondevicepersonalization.FederatedComputeScheduler#schedule failed due to missing or misconfigured federated compute settings URL in the manifest. 

 Value: 7

### ERROR_ISOLATED_SERVICE_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_FAILED: Int
```

The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) that was invoked failed to run. 

 Value: 1

### ERROR_ISOLATED_SERVICE_LOADING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_LOADING_FAILED: Int
```

The ODP module was unable to load the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService).

Retrying may be successful for platform internal errors. 

 Value: 3

### ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED: Int
```

The ODP specific manifest settings for the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) are either missing or misconfigured. 

 Value: 4

### ERROR_ISOLATED_SERVICE_TIMEOUT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_TIMEOUT: Int
```

The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) was invoked but timed out before returning successfully.

This is likely due to an issue with the [IsolatedWorker](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker) implementation taking too long and retries are likely to fail. 

 Value: 5

### ERROR_PERSONALIZATION_DISABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PERSONALIZATION_DISABLED: Int
```

The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService) was not started because personalization is disabled by device configuration. 

 Value: 2

### ERROR_SCHEDULE_TRAINING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SCHEDULE_TRAINING_FAILED: Int
```

The [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService)'s call to android.adservices.ondevicepersonalization.FederatedComputeScheduler#schedule failed.

Retrying may be successful if the issue is due to a platform internal error. 

 Value: 6

## Public constructors

### OnDevicePersonalizationException

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OnDevicePersonalizationException(errorCode: Int)
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND:kotlin.Int), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_FAILED:kotlin.Int) |

### OnDevicePersonalizationException

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OnDevicePersonalizationException(
    errorCode: Int, 
    message: String?)
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND:kotlin.Int), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_FAILED:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

### OnDevicePersonalizationException

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OnDevicePersonalizationException(
    errorCode: Int, 
    message: String?, 
    cause: Throwable?)
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND:kotlin.Int), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_FAILED:kotlin.Int) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |

### OnDevicePersonalizationException

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OnDevicePersonalizationException(
    errorCode: Int, 
    cause: Throwable?)
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND:kotlin.Int), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_FAILED:kotlin.Int) |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |

## Public methods

### getErrorCode

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getErrorCode(): Int
```

Returns the error code for this exception.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST:kotlin.Int), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND:kotlin.Int), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/OnDevicePersonalizationException#ERROR_INFERENCE_FAILED:kotlin.Int) |
