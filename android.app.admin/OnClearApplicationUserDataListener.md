# DevicePolicyManager.OnClearApplicationUserDataListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClearApplicationUserDataListener

Kotlin| [Java](https://developer.android.com/reference/android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener "View this page in Java") 
| --- | --- |

```
interface OnClearApplicationUserDataListener
```

| [android.app.admin.DevicePolicyManager.OnClearApplicationUserDataListener](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener#) |

Callback used in [clearApplicationUserData](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#clearApplicationUserData(android.content.ComponentName,%20kotlin.String,%20java.util.concurrent.Executor,%20android.app.admin.DevicePolicyManager.OnClearApplicationUserDataListener))to indicate that the clearing of an application's user data is done.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onApplicationUserDataCleared](https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager.OnClearApplicationUserDataListener#onApplicationUserDataCleared(kotlin.String,%20kotlin.Boolean))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `succeeded:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Method invoked when clearing the application user data has completed. |

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
