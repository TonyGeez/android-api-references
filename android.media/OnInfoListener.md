# MediaPlayer.OnInfoListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnInfoListener

Kotlin| [Java](../android/media/MediaPlayer.OnInfoListener.md) 
| --- | --- |

```
interface OnInfoListener
```

| [android.media.MediaPlayer.OnInfoListener](../android/media/MediaPlayer.OnInfoListener.md) |

Interface definition of a callback to be invoked to communicate some info and/or warning about the media or its playback.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onInfo](../android/media/MediaPlayer.OnInfoListener.md))`(`mp:` ` [MediaPlayer](MediaPlayer.md)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate an info or a warning. |

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
| `mp` | [MediaPlayer](MediaPlayer.md)!:the MediaPlayer the info pertains to. |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of info or warning. - [MEDIA_INFO_UNKNOWN](MediaPlayer.md) - [MEDIA_INFO_VIDEO_TRACK_LAGGING](MediaPlayer.md) - [MEDIA_INFO_VIDEO_RENDERING_START](MediaPlayer.md) - [MEDIA_INFO_BUFFERING_START](MediaPlayer.md) - [MEDIA_INFO_BUFFERING_END](MediaPlayer.md) - `MEDIA_INFO_NETWORK_BANDWIDTH (703)`- bandwidth information is available (as`extra`kbps) - [MEDIA_INFO_BAD_INTERLEAVING](MediaPlayer.md) - [MEDIA_INFO_NOT_SEEKABLE](MediaPlayer.md) - [MEDIA_INFO_METADATA_UPDATE](MediaPlayer.md) - [MEDIA_INFO_UNSUPPORTED_SUBTITLE](MediaPlayer.md) - [MEDIA_INFO_SUBTITLE_TIMED_OUT](MediaPlayer.md) |
| `extra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an extra code, specific to the info. Typically implementation dependent. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the method handled the info, false if it didn't. Returning false, or not having an OnInfoListener at all, will cause the info to be discarded. |
