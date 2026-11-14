# MediaPlayer.OnDrmInfoListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrmInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnDrmInfoListener "View this page in Java") 
| --- | --- |

```
interface OnDrmInfoListener
```

| [android.media.MediaPlayer.OnDrmInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnDrmInfoListener#) |

Interface definition of a callback to be invoked when the DRM info becomes available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrmInfo](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnDrmInfoListener#onDrmInfo(android.media.MediaPlayer,%20android.media.MediaPlayer.DrmInfo))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`, `drmInfo:` ` [MediaPlayer.DrmInfo](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.DrmInfo)!`)` Called to indicate DRM info is available |

## Public methods

### onDrmInfo

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrmInfo(
    mp: MediaPlayer!, 
    drmInfo: MediaPlayer.DrmInfo!
): Unit
```

Called to indicate DRM info is available

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the`MediaPlayer`associated with this callback |
| `drmInfo` | [MediaPlayer.DrmInfo](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.DrmInfo)!:DRM info of the source including PSSH, and subset of crypto schemes supported by this device |
