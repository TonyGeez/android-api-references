# OnDevicePersonalizationException

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDevicePersonalizationException

Kotlin| [Java](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) 
| --- | --- |

```
open class OnDevicePersonalizationException : Exception
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||
| | | ↳ | [android.adservices.ondevicepersonalization.OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) |
| --- | --- | --- | --- |

Exception thrown by OnDevicePersonalization APIs.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INFERENCE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) [ModelManager](../android/adservices/ondevicepersonalization/ModelManager.md) failed to run inference. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INFERENCE_MODEL_NOT_FOUND](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) Inference failed due to [ModelManager](../android/adservices/ondevicepersonalization/ModelManager.md) not finding the downloaded model. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_INVALID_TRAINING_MANIFEST](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md)'s call to android. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) that was invoked failed to run. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_LOADING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The ODP module was unable to load the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The ODP specific manifest settings for the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) are either missing or misconfigured. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_ISOLATED_SERVICE_TIMEOUT](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) was invoked but timed out before returning successfully. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_PERSONALIZATION_DISABLED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) was not started because personalization is disabled by device configuration. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ERROR_SCHEDULE_TRAINING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md)'s call to android. |
| --- | --- |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |
| [OnDevicePersonalizationException](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md))`(`errorCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cause:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getErrorCode](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md))`()` Returns the error code for this exception. |

## Constants

### ERROR_INFERENCE_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INFERENCE_FAILED: Int
```

[ModelManager](../android/adservices/ondevicepersonalization/ModelManager.md) failed to run inference.

Retrying may be successful if the issue is due to a platform internal error. 

 Value: 9

### ERROR_INFERENCE_MODEL_NOT_FOUND

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INFERENCE_MODEL_NOT_FOUND: Int
```

Inference failed due to [ModelManager](../android/adservices/ondevicepersonalization/ModelManager.md) not finding the downloaded model. 

 Value: 8

### ERROR_INVALID_TRAINING_MANIFEST

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_INVALID_TRAINING_MANIFEST: Int
```

The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md)'s call to android.adservices.ondevicepersonalization.FederatedComputeScheduler#schedule failed due to missing or misconfigured federated compute settings URL in the manifest. 

 Value: 7

### ERROR_ISOLATED_SERVICE_FAILED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_FAILED: Int
```

The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) that was invoked failed to run. 

 Value: 1

### ERROR_ISOLATED_SERVICE_LOADING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_LOADING_FAILED: Int
```

The ODP module was unable to load the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md).

Retrying may be successful for platform internal errors. 

 Value: 3

### ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED: Int
```

The ODP specific manifest settings for the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) are either missing or misconfigured. 

 Value: 4

### ERROR_ISOLATED_SERVICE_TIMEOUT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_ISOLATED_SERVICE_TIMEOUT: Int
```

The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) was invoked but timed out before returning successfully.

This is likely due to an issue with the [IsolatedWorker](../android/adservices/ondevicepersonalization/IsolatedWorker.md) implementation taking too long and retries are likely to fail. 

 Value: 5

### ERROR_PERSONALIZATION_DISABLED

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_PERSONALIZATION_DISABLED: Int
```

The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md) was not started because personalization is disabled by device configuration. 

 Value: 2

### ERROR_SCHEDULE_TRAINING_FAILED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ERROR_SCHEDULE_TRAINING_FAILED: Int
```

The [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md)'s call to android.adservices.ondevicepersonalization.FederatedComputeScheduler#schedule failed.

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
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) |

### OnDevicePersonalizationException

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OnDevicePersonalizationException(
    errorCode: Int, 
    message: String?)
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) |
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
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) |
| `message` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `cause` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)?:This value may be`null`. |
| --- | --- |

### OnDevicePersonalizationException

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
OnDevicePersonalizationException(
    errorCode: Int, 
    cause: Throwable?)
```

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `errorCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_PERSONALIZATION_DISABLED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_LOADING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_MANIFEST_PARSING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_ISOLATED_SERVICE_TIMEOUT](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_SCHEDULE_TRAINING_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INVALID_TRAINING_MANIFEST](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_MODEL_NOT_FOUND](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md), or [android.adservices.ondevicepersonalization.OnDevicePersonalizationException#ERROR_INFERENCE_FAILED](../android/adservices/ondevicepersonalization/OnDevicePersonalizationException.md) |
