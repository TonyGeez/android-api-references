# MediaSessionManager.OnActiveSessionsChangedListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActiveSessionsChangedListener

Kotlin| [Java](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md) 
| --- | --- |

```
interface OnActiveSessionsChangedListener
```

| [android.media.session.MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md) |

Listens for changes to the list of active sessions. This can be added using #addOnActiveSessionsChangedListener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActiveSessionsChanged](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md))`(`controllers:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaController](../android/media/session/MediaController.md)!>?`)` <br /> |

## Public methods

### onActiveSessionsChanged

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActiveSessionsChanged(controllers: MutableList<MediaController!>?): Unit
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controllers` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaController](../android/media/session/MediaController.md)!\>?:This value may be`null`. |
