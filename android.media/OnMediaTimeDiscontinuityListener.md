# MediaPlayer.OnMediaTimeDiscontinuityListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnMediaTimeDiscontinuityListener

Kotlin| [Java](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md) 
| --- | --- |

```
interface OnMediaTimeDiscontinuityListener
```

| [android.media.MediaPlayer.OnMediaTimeDiscontinuityListener](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md) |

Interface definition of a callback to be invoked when discontinuity in the normal progression of the media time is detected. The "normal progression" of media time is defined as the expected increase of the playback position when playing media, relative to the playback speed (for instance every second, media time increases by two seconds when playing at 2x). 
Discontinuities are encountered in the following cases:

- when the player is starved for data and cannot play anymore
- when the player encounters a playback error
- when the a seek operation starts, and when it's completed
- when the playback speed changes
- when the playback state changes
- when the player is reset

See the [MediaPlayer.setOnMediaTimeDiscontinuityListener(OnMediaTimeDiscontinuityListener, Handler)](MediaPlayer.md))method to set a listener for these events.

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMediaTimeDiscontinuity](../android/media/MediaPlayer.OnMediaTimeDiscontinuityListener.md))`(`mp:` ` [MediaPlayer](MediaPlayer.md)`, `mts:` ` [MediaTimestamp](MediaTimestamp.md)`)` Called to indicate a time discontinuity has occured. |

## Public methods

### onMediaTimeDiscontinuity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMediaTimeDiscontinuity(
    mp: MediaPlayer, 
    mts: MediaTimestamp
): Unit
```

Called to indicate a time discontinuity has occured.

| Parameters ||
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](MediaPlayer.md):the MediaPlayer for which the discontinuity has occured. This value cannot be`null`. |
| `mts` | [MediaTimestamp](MediaTimestamp.md):the timestamp that correlates media time, system time and clock rate, or [MediaTimestamp.TIMESTAMP_UNKNOWN](MediaTimestamp.md) in an error case. This value cannot be`null`. |
