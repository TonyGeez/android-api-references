# RemoveAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# RemoveAdSelectionFromOutcomesOverrideRequest

Kotlin| [Java](https://developer.android.com/reference/android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest "View this page in Java") 

```
open class RemoveAdSelectionFromOutcomesOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.adservices.adselection.RemoveAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest#) |

This POJO represents the [RemoveAdSelectionFromOutcomesOverrideRequest, Executor, OutcomeReceiver)](https://developer.android.com/reference/kotlin/android/adservices/adselection/TestAdSelectionManager) request

It contains one field, a [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) which serves as the identifier of the override to be removed

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RemoveAdSelectionFromOutcomesOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest#RemoveAdSelectionFromOutcomesOverrideRequest(android.adservices.adselection.AdSelectionFromOutcomesConfig))`(`config:` ` [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig)`)` Builds a [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest) instance. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) | [getAdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest#getAdSelectionFromOutcomesConfig())`()` <br /> |

## Public constructors

### RemoveAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
RemoveAdSelectionFromOutcomesOverrideRequest(config: AdSelectionFromOutcomesConfig)
```

Builds a [RemoveAdSelectionOverrideRequest](https://developer.android.com/reference/kotlin/android/adservices/adselection/RemoveAdSelectionOverrideRequest) instance.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig):This value cannot be`null`. |

## Public methods

### getAdSelectionFromOutcomesConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getAdSelectionFromOutcomesConfig(): AdSelectionFromOutcomesConfig
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [AdSelectionFromOutcomesConfig](https://developer.android.com/reference/kotlin/android/adservices/adselection/AdSelectionFromOutcomesConfig) | AdSelectionConfig, the configuration of the ad selection process. This value cannot be`null`. |
