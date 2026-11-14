# SyncContext

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncContext

Kotlin| [Java](../android/content/SyncContext.md) 
| --- | --- |

```
open class SyncContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.SyncContext](../android/content/SyncContext.md) |

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IBinder](../android/os/IBinder.md)! | [getSyncContextBinder](../android/content/SyncContext.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](../android/content/SyncContext.md))`(`result:` ` [SyncResult](../android/content/SyncResult.md)!`)` <br /> |

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
