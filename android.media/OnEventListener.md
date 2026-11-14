# MediaDrm.OnEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEventListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDrm.OnEventListener "View this page in Java") 

```
interface OnEventListener
```

| [android.media.MediaDrm.OnEventListener](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener#) |

Interface definition for a callback to be invoked when a drm event occurs

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](https://developer.android.com/reference/kotlin/android/media/MediaDrm.OnEventListener#onEvent(android.media.MediaDrm,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int,%20kotlin.ByteArray))`(`md:` ` [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm)`, `sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Called when an event occurs that requires the app to be notified |

## Public methods

### onEvent

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEvent(
    md: MediaDrm, 
    sessionId: ByteArray?, 
    event: Int, 
    extra: Int, 
    data: ByteArray?
): Unit
```

Called when an event occurs that requires the app to be notified

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `md` | [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm):the MediaDrm object on which the event occurred This value cannot be`null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the DRM session ID on which the event occurred, or`null`if there is no session ID associated with the event. |
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates the event type Value is [android.media.MediaDrm#EVENT_PROVISION_REQUIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_PROVISION_REQUIRED:kotlin.Int), [android.media.MediaDrm#EVENT_KEY_REQUIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_KEY_REQUIRED:kotlin.Int), [android.media.MediaDrm#EVENT_KEY_EXPIRED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_KEY_EXPIRED:kotlin.Int), [android.media.MediaDrm#EVENT_VENDOR_DEFINED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_VENDOR_DEFINED:kotlin.Int), or [android.media.MediaDrm#EVENT_SESSION_RECLAIMED](https://developer.android.com/reference/kotlin/android/media/MediaDrm#EVENT_SESSION_RECLAIMED:kotlin.Int) |
| `extra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an secondary error code |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:optional byte array of data that may be associated with the event This value may be`null`. |
