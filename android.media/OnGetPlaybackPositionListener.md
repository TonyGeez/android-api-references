# RemoteControlClient.OnGetPlaybackPositionListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnGetPlaybackPositionListener

Kotlin| [Java](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md) 
| --- | --- |

```
interface OnGetPlaybackPositionListener
```

| [android.media.RemoteControlClient.OnGetPlaybackPositionListener](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Interface definition for a callback to be invoked when the media playback position is queried.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [onGetPlaybackPosition](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md))`()` Called on the implementer of the interface to query the current playback position. |

## Public methods

### onGetPlaybackPosition

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onGetPlaybackPosition(): Long
```

**Deprecated:** *Deprecated in Java.*

Called on the implementer of the interface to query the current playback position.

| Return ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a negative value if the current playback position (or the last valid playback position) is not known, or a zero or positive value expressed in ms indicating the current position, or the last valid known position. |
