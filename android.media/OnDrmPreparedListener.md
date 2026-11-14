# MediaPlayer.OnDrmPreparedListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrmPreparedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnDrmPreparedListener "View this page in Java") 

```
interface OnDrmPreparedListener
```

| [android.media.MediaPlayer.OnDrmPreparedListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnDrmPreparedListener#) |

Interface definition of a callback to notify the app when the DRM is ready for key request/response

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrmPrepared](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnDrmPreparedListener#onDrmPrepared(android.media.MediaPlayer,%20kotlin.Int))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to notify the app that prepareDrm is finished and ready for key request/response |

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
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the`MediaPlayer`associated with this callback |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the result of DRM preparation which can be [PREPARE_DRM_STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_SUCCESS:kotlin.Int), [PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR:kotlin.Int), [PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR:kotlin.Int), or [PREPARE_DRM_STATUS_PREPARATION_ERROR](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_PREPARATION_ERROR:kotlin.Int). Value is [android.media.MediaPlayer#PREPARE_DRM_STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_SUCCESS:kotlin.Int), [android.media.MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_NETWORK_ERROR:kotlin.Int), [android.media.MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_PROVISIONING_SERVER_ERROR:kotlin.Int), or [android.media.MediaPlayer#PREPARE_DRM_STATUS_PREPARATION_ERROR](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#PREPARE_DRM_STATUS_PREPARATION_ERROR:kotlin.Int) |
