# MediaDrm.OnSessionLostStateListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSessionLostStateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrm.OnSessionLostStateListener "View this page in Java") 
| --- | --- |

```
interface OnSessionLostStateListener
```

| [android.media.MediaDrm.OnSessionLostStateListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener#) |

Interface definition for a callback to be invoked when the session state has been lost and is now invalid

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSessionLostState](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnSessionLostStateListener#onSessionLostState(android.media.MediaDrm,%20kotlin.ByteArray))`(`md:` ` [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm)`, `sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`)` Called when session state has lost state, to inform the app about the condition so it can close the session and open a new one to resume operation. |

## Public methods

### onSessionLostState

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSessionLostState(
    md: MediaDrm, 
    sessionId: ByteArray
): Unit
```

Called when session state has lost state, to inform the app about the condition so it can close the session and open a new one to resume operation.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `md` | [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm):the MediaDrm object on which the event occurred This value cannot be`null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the DRM session ID on which the event occurred This value cannot be`null`. |
