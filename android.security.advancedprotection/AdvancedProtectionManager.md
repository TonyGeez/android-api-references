Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvancedProtectionManager

Kotlin | [Java](AdvancedProtectionManager.md)
| --- | --- |

```
class AdvancedProtectionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.security.advancedprotection.AdvancedProtectionManager](AdvancedProtectionManager.md) |

Advanced Protection is a mode that users can enroll their device into, that enhances security by enabling features and restrictions across both the platform and user apps.

This class provides methods to query and control the advanced protection mode for the device.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback` A callback class for monitoring changes to Advanced Protection state |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isAdvancedProtectionEnabled Checks if advanced protection is enabled on the device. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | registerAdvancedProtectionCallback Registers a `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback` to be notified of changes to the Advanced Protection state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | unregisterAdvancedProtectionCallback Unregister an existing `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback`. |
| --- | --- |

## Public methods

### isAdvancedProtectionEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAdvancedProtectionEnabled(): Boolean
```

Checks if advanced protection is enabled on the device. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#QUERY_ADVANCED_PROTECTION_MODE:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if advanced protection is enabled, `false` otherwise. |

### registerAdvancedProtectionCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun registerAdvancedProtectionCallback(
    executor: Executor, 
    callback: AdvancedProtectionManager.Callback
): Unit
```

Registers a `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback` to be notified of changes to the Advanced Protection state.

The provided callback will be called on the specified executor with the updated state. Methods are called when the state changes, as well as once on initial registration. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#QUERY_ADVANCED_PROTECTION_MODE:kotlin.String`

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor of where the callback will execute. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [AdvancedProtectionManager.Callback](../android/security/advancedprotection/AdvancedProtectionManager.Callback.md): The `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback` object to register.. This value cannot be `null`. |

### unregisterAdvancedProtectionCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun unregisterAdvancedProtectionCallback(callback: AdvancedProtectionManager.Callback): Unit
```

Unregister an existing `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#QUERY_ADVANCED_PROTECTION_MODE:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [AdvancedProtectionManager.Callback](../android/security/advancedprotection/AdvancedProtectionManager.Callback.md): The `https://developer.android.com/reference/kotlin/android/security/advancedprotection/AdvancedProtectionManager.Callback` object to unregister. This value cannot be `null`. |
