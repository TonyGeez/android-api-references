# Event

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Event

Kotlin| [Java](Event.md) 
| --- | --- |

```
abstract class Event
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.metrics.Event](Event.md) |

| Known Direct Subclasses [EditingEndedEvent](EditingEndedEvent.md), [NetworkEvent](NetworkEvent.md), [PlaybackErrorEvent](PlaybackErrorEvent.md), [PlaybackStateEvent](PlaybackStateEvent.md), [TrackChangeEvent](TrackChangeEvent.md) |---------------------------------------------------------------------------------------------------------------|----------------------------------------------| | [EditingEndedEvent](EditingEndedEvent.md) | Event for an editing operation having ended. | | [NetworkEvent](NetworkEvent.md) | Media network event. | | [PlaybackErrorEvent](PlaybackErrorEvent.md) | Playback error event. | | [PlaybackStateEvent](PlaybackStateEvent.md) | Playback state event. | | [TrackChangeEvent](TrackChangeEvent.md) | Playback track change event. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Abstract class for metrics events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Bundle](../android.os/Bundle.md) | [getMetricsBundle](Event.md))`()` Gets metrics-related information that is not supported by dedicated methods. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimeSinceCreatedMillis](Event.md))`()` Gets time since the corresponding log session is created in millisecond. |

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
| [Bundle](../android.os/Bundle.md) | This value cannot be`null`. |

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

- [android.media.metrics.LogSessionId](LogSessionId.md)
- [android.media.metrics.PlaybackSession](PlaybackSession.md)
- [android.media.metrics.RecordingSession](RecordingSession.md)
