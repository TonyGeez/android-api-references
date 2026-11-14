Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnExpirationUpdateListener

Kotlin | [Java](../android/media/MediaDrm.OnExpirationUpdateListener.md)
| --- | --- |

```
interface OnExpirationUpdateListener
```

| [android.media.MediaDrm.OnExpirationUpdateListener](../android/media/MediaDrm.OnExpirationUpdateListener.md) |

Interface definition for a callback to be invoked when a drm session expiration update occurs

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onExpirationUpdate Called when a session expiration update occurs, to inform the app about the change in expiration time |

## Public methods

### onExpirationUpdate

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onExpirationUpdate(
    md: MediaDrm, 
    sessionId: ByteArray, 
    expirationTime: Long
): Unit
```

Called when a session expiration update occurs, to inform the app about the change in expiration time

| Parameters ||
|---|---|
| `md` | [MediaDrm](MediaDrm.md): the MediaDrm object on which the event occurred. This value cannot be `null`. |
| `sessionId` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html): the DRM session ID on which the event occurred. This value cannot be `null`. |
| `expirationTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): the new expiration time for the keys in the session. The time is in milliseconds, relative to the Unix epoch. A time of 0 indicates that the keys never expire. |
| --- | --- |
