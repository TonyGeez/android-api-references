# MediaSessionManager.OnActiveSessionsChangedListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnActiveSessionsChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener "View this page in Java") 
| --- | --- |

```
interface OnActiveSessionsChangedListener
```

| [android.media.session.MediaSessionManager.OnActiveSessionsChangedListener](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener#) |

Listens for changes to the list of active sessions. This can be added using #addOnActiveSessionsChangedListener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActiveSessionsChanged](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener#onActiveSessionsChanged(kotlin.collections.MutableList))`(`controllers:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaController](https://developer.android.com/reference/kotlin/android/media/session/MediaController)!>?`)` <br /> |

## Public methods

### onActiveSessionsChanged

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActiveSessionsChanged(controllers: MutableList<MediaController!>?): Unit
```

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controllers` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaController](https://developer.android.com/reference/kotlin/android/media/session/MediaController)!\>?:This value may be`null`. |
