# MediaDrm.OnKeyStatusChangeListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnKeyStatusChangeListener

Kotlin| [Java](../android/media/MediaDrm.OnKeyStatusChangeListener.md) 
| --- | --- |

```
interface OnKeyStatusChangeListener
```

| [android.media.MediaDrm.OnKeyStatusChangeListener](../android/media/MediaDrm.OnKeyStatusChangeListener.md) |

Interface definition for a callback to be invoked when the keys in a drm session change states.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKeyStatusChange](../android/media/MediaDrm.OnKeyStatusChangeListener.md))`(`md:` ` [MediaDrm](../android/media/MediaDrm.md)`, `sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)`, `keyInformation:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaDrm.KeyStatus](../android/media/MediaDrm.KeyStatus.md)!>`, `hasNewUsableKey:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the keys in a session change status, such as when the license is renewed or expires. |

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
| `md` | [MediaDrm](../android/media/MediaDrm.md):the MediaDrm object on which the event occurred This value cannot be`null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html):the DRM session ID on which the event occurred This value cannot be`null`. |
| `keyInformation` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaDrm.KeyStatus](../android/media/MediaDrm.KeyStatus.md)!\>:a list of [MediaDrm.KeyStatus](../android/media/MediaDrm.KeyStatus.md) instances indicating the status for each key in the session This value cannot be`null`. |
| --- | --- |
| `hasNewUsableKey` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):indicates if a key has been added that is usable, which may trigger an attempt to resume playback on the media stream if it is currently blocked waiting for a key. |
