# AdvancedProtectionManager.Callback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](../android/security/advancedprotection/AdvancedProtectionManager.Callback.md) 
| --- | --- |

```
interface Callback
```

| [android.security.advancedprotection.AdvancedProtectionManager.Callback](../android/security/advancedprotection/AdvancedProtectionManager.Callback.md) |

A callback class for monitoring changes to Advanced Protection state

To register a callback, implement this interface, and register it with [AdvancedProtectionManager.registerAdvancedProtectionCallback(Executor, Callback)](AdvancedProtectionManager.md)). Methods are called when the state changes, as well as once on initial registration.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvancedProtectionChanged](../android/security/advancedprotection/AdvancedProtectionManager.Callback.md))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when advanced protection state changes |

## Public methods

### onAdvancedProtectionChanged

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAdvancedProtectionChanged(enabled: Boolean): Unit
```

Called when advanced protection state changes

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the new state |
