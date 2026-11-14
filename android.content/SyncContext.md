# SyncContext

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncContext

Kotlin| [Java](https://developer.android.com/reference/android/content/SyncContext "View this page in Java") 

```
open class SyncContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.content.SyncContext](https://developer.android.com/reference/kotlin/android/content/SyncContext#) |

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)! | [getSyncContextBinder](https://developer.android.com/reference/kotlin/android/content/SyncContext#getSyncContextBinder())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](https://developer.android.com/reference/kotlin/android/content/SyncContext#onFinished(android.content.SyncResult))`(`result:` ` [SyncResult](https://developer.android.com/reference/kotlin/android/content/SyncResult)!`)` <br /> |

## Public methods

### getSyncContextBinder

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSyncContextBinder(): IBinder!
```  

### onFinished

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onFinished(result: SyncResult!): Unit
```
