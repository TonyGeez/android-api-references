# RemoveAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions)

# RemoveAdSelectionFromOutcomesOverrideRequest

Kotlin| [Java](RemoveAdSelectionFromOutcomesOverrideRequest.md) 
| --- | --- |

```
open class RemoveAdSelectionFromOutcomesOverrideRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.adservices.adselection.RemoveAdSelectionFromOutcomesOverrideRequest](RemoveAdSelectionFromOutcomesOverrideRequest.md) |

This POJO represents the [RemoveAdSelectionFromOutcomesOverrideRequest, Executor, OutcomeReceiver)](TestAdSelectionManager.md) request

It contains one field, a [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) which serves as the identifier of the override to be removed

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RemoveAdSelectionFromOutcomesOverrideRequest](RemoveAdSelectionFromOutcomesOverrideRequest.md))`(`config:` ` [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md)`)` Builds a [RemoveAdSelectionOverrideRequest](RemoveAdSelectionOverrideRequest.md) instance. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) | [getAdSelectionFromOutcomesConfig](RemoveAdSelectionFromOutcomesOverrideRequest.md))`()` <br /> |

## Public constructors

### RemoveAdSelectionFromOutcomesOverrideRequest

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
RemoveAdSelectionFromOutcomesOverrideRequest(config: AdSelectionFromOutcomesConfig)
```

Builds a [RemoveAdSelectionOverrideRequest](RemoveAdSelectionOverrideRequest.md) instance.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md):This value cannot be`null`. |

## Public methods

### getAdSelectionFromOutcomesConfig

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [Ad Services Extensions 10](https://developer.android.com/sdkExtensions) 

```
open fun getAdSelectionFromOutcomesConfig(): AdSelectionFromOutcomesConfig
```

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [AdSelectionFromOutcomesConfig](AdSelectionFromOutcomesConfig.md) | AdSelectionConfig, the configuration of the ad selection process. This value cannot be`null`. |
