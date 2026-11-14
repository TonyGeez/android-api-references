# ExecuteInput

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExecuteInput

Kotlin| [Java](../android/adservices/ondevicepersonalization/ExecuteInput.md) 
| --- | --- |

```
class ExecuteInput
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.ondevicepersonalization.ExecuteInput](../android/adservices/ondevicepersonalization/ExecuteInput.md) |

The input data for [IsolatedWorker.onExecute(ExecuteInput, android.os.OutcomeReceiver)](../android/adservices/ondevicepersonalization/IsolatedWorker.md)).

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ExecuteInput](../android/adservices/ondevicepersonalization/ExecuteInput.md))`(`appPackageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `appParams:` ` [PersistableBundle](../android/os/PersistableBundle.md)`)` Creates an [ExecuteInput](../android/adservices/ondevicepersonalization/ExecuteInput.md). |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getAppPackageName](../android/adservices/ondevicepersonalization/ExecuteInput.md))`()` The package name of the calling app. |
| [PersistableBundle](../android/os/PersistableBundle.md) | [getAppParams](../android/adservices/ondevicepersonalization/ExecuteInput.md))`()` The parameters provided by the app to the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md). |

## Public constructors

### ExecuteInput

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ExecuteInput(
    appPackageName: String, 
    appParams: PersistableBundle)
```

Creates an [ExecuteInput](../android/adservices/ondevicepersonalization/ExecuteInput.md).

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `appPackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):the package name of the calling app. This value cannot be`null`. |
| `appParams` | [PersistableBundle](../android/os/PersistableBundle.md):the parameters provided by the app to the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md). The service defines the expected keys in this [PersistableBundle](../android/os/PersistableBundle.md). This value cannot be`null`. |

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

The parameters provided by the app to the [IsolatedService](../android/adservices/ondevicepersonalization/IsolatedService.md). The service defines the expected keys in this [PersistableBundle](../android/os/PersistableBundle.md).

| Return ||
|--------------------------------------------------------------------------------------------------------|-----------------------------|
| [PersistableBundle](../android/os/PersistableBundle.md) | This value cannot be`null`. |
