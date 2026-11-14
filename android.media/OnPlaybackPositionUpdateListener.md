# AudioTrack.OnPlaybackPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPlaybackPositionUpdateListener

Kotlin| [Java](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md) 
| --- | --- |

```
interface OnPlaybackPositionUpdateListener
```

| [android.media.AudioTrack.OnPlaybackPositionUpdateListener](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md) |

Interface definition for a callback to be invoked when the playback head position of an AudioTrack has reached a notification marker or has increased by a certain period.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMarkerReached](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md))`(`track:` ` [AudioTrack](../android/media/AudioTrack.md)!`)` Called on the listener to notify it that the previously set marker has been reached by the playback head. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicNotification](../android/media/AudioTrack.OnPlaybackPositionUpdateListener.md))`(`track:` ` [AudioTrack](../android/media/AudioTrack.md)!`)` Called on the listener to periodically notify it that the playback head has reached a multiple of the notification period. |

## Public methods

### onMarkerReached

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMarkerReached(track: AudioTrack!): Unit
```

Called on the listener to notify it that the previously set marker has been reached by the playback head. 

### onPeriodicNotification

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPeriodicNotification(track: AudioTrack!): Unit
```

Called on the listener to periodically notify it that the playback head has reached a multiple of the notification period.
