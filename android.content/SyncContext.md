# SyncContext

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SyncContext

Kotlin| [Java](SyncContext.md) 
| --- | --- |

```
open class SyncContext
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.SyncContext](SyncContext.md) |

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [IBinder](../android.os/IBinder.md)! | [getSyncContextBinder](SyncContext.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](SyncContext.md))`(`result:` ` [SyncResult](SyncResult.md)!`)` <br /> |

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
