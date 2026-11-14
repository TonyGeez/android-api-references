# RemoveAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# RemoveAdSelectionFromOutcomesOverrideRequest

Kotlin| [Java](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md) 
| --- | --- |

```
open class RemoveAdSelectionFromOutcomesOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.RemoveAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md) |

This POJO represents the [RemoveAdSelectionFromOutcomesOverrideRequest, Executor, OutcomeReceiver)](../android/adservices/adselection/TestAdSelectionManager.md) request

It contains one field, a [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) which serves as the identifier of the override to be removed

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RemoveAdSelectionFromOutcomesOverrideRequest](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md))`(`config:` ` [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md)`)` Builds a [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md) instance. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) | [getAdSelectionFromOutcomesConfig](../android/adservices/adselection/RemoveAdSelectionFromOutcomesOverrideRequest.md))`()` <br /> |

## Public constructors

### RemoveAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
RemoveAdSelectionFromOutcomesOverrideRequest(config: AdSelectionFromOutcomesConfig)
```

Builds a [RemoveAdSelectionOverrideRequest](../android/adservices/adselection/RemoveAdSelectionOverrideRequest.md) instance.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md):This value cannot be`null`. |

## Public methods

### getAdSelectionFromOutcomesConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getAdSelectionFromOutcomesConfig(): AdSelectionFromOutcomesConfig
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [AdSelectionFromOutcomesConfig](../android/adservices/adselection/AdSelectionFromOutcomesConfig.md) | AdSelectionConfig, the configuration of the ad selection process. This value cannot be`null`. |
