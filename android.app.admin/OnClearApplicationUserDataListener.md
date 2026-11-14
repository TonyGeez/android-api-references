# DevicePolicyManager.OnClearApplicationUserDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClearApplicationUserDataListener

Kotlin| [Java](../android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener.md) 
| --- | --- |

```
interface OnClearApplicationUserDataListener
```

| [android.app.admin.DevicePolicyManager.OnClearApplicationUserDataListener](../android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener.md) |

Callback used in [clearApplicationUserData](../android/app/admin/DevicePolicyManager.md))to indicate that the clearing of an application's user data is done.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onApplicationUserDataCleared](../android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `succeeded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Method invoked when clearing the application user data has completed. |

## Public methods

### onApplicationUserDataCleared

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onApplicationUserDataCleared(
    packageName: String!, 
    succeeded: Boolean
): Unit
```

Method invoked when clearing the application user data has completed.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The name of the package which had its user data cleared. |
| `succeeded` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Whether the clearing succeeded. Clearing fails for device administrator apps and protected system packages. |
