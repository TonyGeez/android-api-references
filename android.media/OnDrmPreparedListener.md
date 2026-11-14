# MediaPlayer.OnDrmPreparedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrmPreparedListener

Kotlin| [Java](../android/media/MediaPlayer.OnDrmPreparedListener.md) 
| --- | --- |

```
interface OnDrmPreparedListener
```

| [android.media.MediaPlayer.OnDrmPreparedListener](../android/media/MediaPlayer.OnDrmPreparedListener.md) |

Interface definition of a callback to notify the app when the DRM is ready for key request/response

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrmPrepared](../android/media/MediaPlayer.OnDrmPreparedListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to notify the app that prepareDrm is finished and ready for key request/response |

## Public methods

### onDrmPrepared

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrmPrepared(
    mp: MediaPlayer!, 
    status: Int
): Unit
```

Called to notify the app that prepareDrm is finished and ready for key request/response

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the`MediaPlayer`associated with this callback |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result of DRM preparation which can be [PREPARE_DRM_STATUS_SUCCESS](../android/media/MediaPlayer.md), [PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR](../android/media/MediaPlayer.md), [PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR](../android/media/MediaPlayer.md), or [PREPARE_DRM_STATUS_PREPARATION_ERROR](../android/media/MediaPlayer.md). Value is [android.media.MediaPlayer#PREPARE_DRM_STATUS_SUCCESS](../android/media/MediaPlayer.md), [android.media.MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR](../android/media/MediaPlayer.md), [android.media.MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR](../android/media/MediaPlayer.md), or [android.media.MediaPlayer#PREPARE_DRM_STATUS_PREPARATION_ERROR](../android/media/MediaPlayer.md) |
