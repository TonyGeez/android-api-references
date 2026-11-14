# MediaDrm.OnKeyStatusChangeListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnKeyStatusChangeListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrm.OnKeyStatusChangeListener "View this page in Java") 
| --- | --- |

```
interface OnKeyStatusChangeListener
```

| [android.media.MediaDrm.OnKeyStatusChangeListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener#) |

Interface definition for a callback to be invoked when the keys in a drm session change states.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKeyStatusChange](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnKeyStatusChangeListener#onKeyStatusChange(android.media.MediaDrm,%20kotlin.ByteArray,%20kotlin.collections.MutableList,%20kotlin.Boolean))`(`md:` ` [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm)`, `sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `keyInformation:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaDrm.KeyStatus](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyStatus)!>`, `hasNewUsableKey:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the keys in a session change status, such as when the license is renewed or expires. |

## Public methods

### onKeyStatusChange

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyStatusChange(
    md: MediaDrm, 
    sessionId: ByteArray, 
    keyInformation: MutableList<MediaDrm.KeyStatus!>, 
    hasNewUsableKey: Boolean
): Unit
```

Called when the keys in a session change status, such as when the license is renewed or expires.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `md` | [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm):the MediaDrm object on which the event occurred This value cannot be`null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the DRM session ID on which the event occurred This value cannot be`null`. |
| `keyInformation` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaDrm.KeyStatus](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyStatus)!\>:a list of [MediaDrm.KeyStatus](https://developer.android.com/reference/kotlin/android/media/MediaDrm.KeyStatus) instances indicating the status for each key in the session This value cannot be`null`. |
| --- | --- |
| `hasNewUsableKey` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates if a key has been added that is usable, which may trigger an attempt to resume playback on the media stream if it is currently blocked waiting for a key. |
