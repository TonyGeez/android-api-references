# MediaPlayer.OnDrmInfoListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDrmInfoListener

Kotlin| [Java](../android/media/MediaPlayer.OnDrmInfoListener.md) 
| --- | --- |

```
interface OnDrmInfoListener
```

| [android.media.MediaPlayer.OnDrmInfoListener](../android/media/MediaPlayer.OnDrmInfoListener.md) |

Interface definition of a callback to be invoked when the DRM info becomes available

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDrmInfo](../android/media/MediaPlayer.OnDrmInfoListener.md))`(`mp:` ` [MediaPlayer](../android/media/MediaPlayer.md)!`, `drmInfo:` ` [MediaPlayer.DrmInfo](../android/media/MediaPlayer.DrmInfo.md)!`)` Called to indicate DRM info is available |

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
| `mp` | [MediaPlayer](../android/media/MediaPlayer.md)!:the`MediaPlayer`associated with this callback |
| `drmInfo` | [MediaPlayer.DrmInfo](../android/media/MediaPlayer.DrmInfo.md)!:DRM info of the source including PSSH, and subset of crypto schemes supported by this device |
