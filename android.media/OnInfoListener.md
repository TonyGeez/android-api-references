# MediaPlayer.OnInfoListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInfoListener

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaPlayer.OnInfoListener "View this page in Java") 
| --- | --- |

```
interface OnInfoListener
```

| [android.media.MediaPlayer.OnInfoListener](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnInfoListener#) |

Interface definition of a callback to be invoked to communicate some info and/or warning about the media or its playback.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onInfo](https://developer.android.com/reference/kotlin/android/media/MediaPlayer.OnInfoListener#onInfo(android.media.MediaPlayer,%20kotlin.Int,%20kotlin.Int))`(`mp:` ` [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate an info or a warning. |

## Public methods

### onInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onInfo(
    mp: MediaPlayer!, 
    what: Int, 
    extra: Int
): Boolean
```

Called to indicate an info or a warning.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer)!:the MediaPlayer the info pertains to. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of info or warning. - [MEDIA_INFO_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_UNKNOWN:kotlin.Int) - [MEDIA_INFO_VIDEO_TRACK_LAGGING](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_VIDEO_TRACK_LAGGING:kotlin.Int) - [MEDIA_INFO_VIDEO_RENDERING_START](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_VIDEO_RENDERING_START:kotlin.Int) - [MEDIA_INFO_BUFFERING_START](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_BUFFERING_START:kotlin.Int) - [MEDIA_INFO_BUFFERING_END](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_BUFFERING_END:kotlin.Int) - `MEDIA_INFO_NETWORK_BANDWIDTH (703)`- bandwidth information is available (as`extra`kbps) - [MEDIA_INFO_BAD_INTERLEAVING](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_BAD_INTERLEAVING:kotlin.Int) - [MEDIA_INFO_NOT_SEEKABLE](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_NOT_SEEKABLE:kotlin.Int) - [MEDIA_INFO_METADATA_UPDATE](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_METADATA_UPDATE:kotlin.Int) - [MEDIA_INFO_UNSUPPORTED_SUBTITLE](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_UNSUPPORTED_SUBTITLE:kotlin.Int) - [MEDIA_INFO_SUBTITLE_TIMED_OUT](https://developer.android.com/reference/kotlin/android/media/MediaPlayer#MEDIA_INFO_SUBTITLE_TIMED_OUT:kotlin.Int) |
| `extra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an extra code, specific to the info. Typically implementation dependent. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the method handled the info, false if it didn't. Returning false, or not having an OnInfoListener at all, will cause the info to be discarded. |
