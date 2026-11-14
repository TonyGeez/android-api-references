# PersistentDataBlockManager

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PersistentDataBlockManager

Kotlin| [Java](PersistentDataBlockManager.md) 
| --- | --- |

```
open class PersistentDataBlockManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.service.persistentdata.PersistentDataBlockManager](PersistentDataBlockManager.md) |

Interface to the persistent data partition. Provides access to information about the state of factory reset protection. 
Restricted for SDK Runtime environment in API level 35.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFactoryResetProtectionActive](PersistentDataBlockManager.md))`()` Returns true if FactoryResetProtection (FRP) is active, meaning the device rebooted and has not been able to deactivate FRP because the deactivation secrets were wiped by an untrusted factory reset. |

## Public methods

### isFactoryResetProtectionActive

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isFactoryResetProtectionActive(): Boolean
```

Returns true if FactoryResetProtection (FRP) is active, meaning the device rebooted and has not been able to deactivate FRP because the deactivation secrets were wiped by an untrusted factory reset.
