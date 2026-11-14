# ExecuteInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteInput

Kotlin| [Java](https://developer.android.com/reference/android/adservices/ondevicepersonalization/ExecuteInput "View this page in Java") 

```
class ExecuteInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.ondevicepersonalization.ExecuteInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput#) |

The input data for [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedWorker#onExecute(android.adservices.ondevicepersonalization.ExecuteInput,%20android.os.OutcomeReceiver)).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecuteInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput#ExecuteInput(kotlin.String,%20android.os.PersistableBundle))`(`appPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appParams:` ` [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#)`)` Creates an [ExecuteInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput#). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAppPackageName](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput#getAppPackageName())`()` The package name of the calling app. |
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | [getAppParams](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput#getAppParams())`()` The parameters provided by the app to the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService). |

## Public constructors

### ExecuteInput

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecuteInput(
    appPackageName: String, 
    appParams: PersistableBundle)
```

Creates an [ExecuteInput](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/ExecuteInput#).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package name of the calling app. This value cannot be`null`. |
| `appParams` | [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#):the parameters provided by the app to the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService). The service defines the expected keys in this [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#). This value cannot be`null`. |

## Public methods

### getAppPackageName

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppPackageName(): String
```

The package name of the calling app.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getAppParams

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAppParams(): PersistableBundle
```

The parameters provided by the app to the [IsolatedService](https://developer.android.com/reference/kotlin/android/adservices/ondevicepersonalization/IsolatedService). The service defines the expected keys in this [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#).

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------|
| [PersistableBundle](https://developer.android.com/reference/kotlin/android/os/PersistableBundle.html#) | This value cannot be`null`. |
