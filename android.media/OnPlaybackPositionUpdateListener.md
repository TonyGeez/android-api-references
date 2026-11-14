# AudioTrack.OnPlaybackPositionUpdateListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPlaybackPositionUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioTrack.OnPlaybackPositionUpdateListener "View this page in Java") 

```
interface OnPlaybackPositionUpdateListener
```

| [android.media.AudioTrack.OnPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnPlaybackPositionUpdateListener#) |

Interface definition for a callback to be invoked when the playback head position of an AudioTrack has reached a notification marker or has increased by a certain period.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMarkerReached](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnPlaybackPositionUpdateListener#onMarkerReached(android.media.AudioTrack))`(`track:` ` [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack)!`)` Called on the listener to notify it that the previously set marker has been reached by the playback head. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPeriodicNotification](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnPlaybackPositionUpdateListener#onPeriodicNotification(android.media.AudioTrack))`(`track:` ` [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack)!`)` Called on the listener to periodically notify it that the playback head has reached a multiple of the notification period. |

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
