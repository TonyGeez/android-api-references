# MediaDrm.OnEventListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEventListener

Kotlin| [Java](../android/media/MediaDrm.OnEventListener.md) 
| --- | --- |

```
interface OnEventListener
```

| [android.media.MediaDrm.OnEventListener](../android/media/MediaDrm.OnEventListener.md) |

Interface definition for a callback to be invoked when a drm event occurs

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](../android/media/MediaDrm.OnEventListener.md))`(`md:` ` [MediaDrm](MediaDrm.md)`, `sessionId:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`, `event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?`)` Called when an event occurs that requires the app to be notified |

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
| `md` | [MediaDrm](MediaDrm.md):the MediaDrm object on which the event occurred This value cannot be`null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:the DRM session ID on which the event occurred, or`null`if there is no session ID associated with the event. |
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):indicates the event type Value is [android.media.MediaDrm#EVENT_PROVISION_REQUIRED](MediaDrm.md), [android.media.MediaDrm#EVENT_KEY_REQUIRED](MediaDrm.md), [android.media.MediaDrm#EVENT_KEY_EXPIRED](MediaDrm.md), [android.media.MediaDrm#EVENT_VENDOR_DEFINED](MediaDrm.md), or [android.media.MediaDrm#EVENT_SESSION_RECLAIMED](MediaDrm.md) |
| --- | --- |
| `extra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an secondary error code |
| `data` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)?:optional byte array of data that may be associated with the event This value may be`null`. |
