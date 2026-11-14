# Event

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Event

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/Event "View this page in Java") 
| --- | --- |

```
abstract class Event
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.metrics.Event](https://developer.android.com/reference/kotlin/android/media/metrics/Event#) |

| Known Direct Subclasses [EditingEndedEvent](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent), [NetworkEvent](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent), [PlaybackErrorEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent), [PlaybackStateEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent), [TrackChangeEvent](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------| | [EditingEndedEvent](https://developer.android.com/reference/kotlin/android/media/metrics/EditingEndedEvent) | Event for an editing operation having ended. | | [NetworkEvent](https://developer.android.com/reference/kotlin/android/media/metrics/NetworkEvent) | Media network event. | | [PlaybackErrorEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackErrorEvent) | Playback error event. | | [PlaybackStateEvent](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackStateEvent) | Playback state event. | | [TrackChangeEvent](https://developer.android.com/reference/kotlin/android/media/metrics/TrackChangeEvent) | Playback track change event. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract class for metrics events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getMetricsBundle](https://developer.android.com/reference/kotlin/android/media/metrics/Event#getMetricsBundle())`()` Gets metrics-related information that is not supported by dedicated methods. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](https://developer.android.com/reference/kotlin/android/media/metrics/Event#getTimeSinceCreatedMillis())`()` Gets time since the corresponding log session is created in millisecond. |

## Public methods

### getMetricsBundle

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMetricsBundle(): Bundle
```

Gets metrics-related information that is not supported by dedicated methods.

It is intended to be used for backwards compatibility by the metrics infrastructure.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

### getTimeSinceCreatedMillis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimeSinceCreatedMillis(): Long
```

Gets time since the corresponding log session is created in millisecond.

| Return ||
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the timestamp since the instance is created, or -1 if unknown. Value is -1 or greater |

**See Also**

- [android.media.metrics.LogSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/LogSessionId)
- [android.media.metrics.PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession)
- [android.media.metrics.RecordingSession](https://developer.android.com/reference/kotlin/android/media/metrics/RecordingSession)
