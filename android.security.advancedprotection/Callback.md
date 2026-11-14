# AdvancedProtectionManager.Callback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Callback

Kotlin| [Java](https://developer.android.com/reference/android/security/advancedprotection/AdvancedProtectionManager.Callback "View this page in Java") 
| --- | --- |

```
interface Callback
```

| [android.security.advancedprotection.AdvancedProtectionManager.Callback](https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback#) |

A callback class for monitoring changes to Advanced Protection state

To register a callback, implement this interface, and register it with [AdvancedProtectionManager.registerAdvancedProtectionCallback(Executor, Callback)](https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager#registerAdvancedProtectionCallback(java.util.concurrent.Executor,%20android.security.advancedprotection.AdvancedProtectionManager.Callback)). Methods are called when the state changes, as well as once on initial registration.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAdvancedProtectionChanged](https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback#onAdvancedProtectionChanged(kotlin.Boolean))`(`enabled:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when advanced protection state changes |

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
