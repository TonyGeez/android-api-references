# MediaMetricsManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetricsManager

Kotlin| [Java](MediaMetricsManager.md) 
| --- | --- |

```
class MediaMetricsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.metrics.MediaMetricsManager](MediaMetricsManager.md) |

This class gives information about, and interacts with media metrics.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [INVALID_TIMESTAMP](MediaMetricsManager.md) <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BundleSession](BundleSession.md) | [createBundleSession](MediaMetricsManager.md))`()` Creates a generic bundle session. |
| [EditingSession](EditingSession.md) | [createEditingSession](MediaMetricsManager.md))`()` Creates a editing session. |
| [PlaybackSession](PlaybackSession.md) | [createPlaybackSession](MediaMetricsManager.md))`()` Creates a playback session. |
| --- | --- |
| [RecordingSession](RecordingSession.md) | [createRecordingSession](MediaMetricsManager.md))`()` Creates a recording session. |
| [TranscodingSession](TranscodingSession.md) | [createTranscodingSession](MediaMetricsManager.md))`()` Creates a transcoding session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseSessionId](MediaMetricsManager.md))`(`sessionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a generic bundle session. |
| --- | --- |

## Constants

### INVALID_TIMESTAMP

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID_TIMESTAMP: Long
```  

 Value: -1L

## Public methods

### createBundleSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createBundleSession(): BundleSession
```

Creates a generic bundle session.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [BundleSession](BundleSession.md) | This value cannot be`null`. |

### createEditingSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createEditingSession(): EditingSession
```

Creates a editing session.

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------|
| [EditingSession](EditingSession.md) | This value cannot be`null`. |

### createPlaybackSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createPlaybackSession(): PlaybackSession
```

Creates a playback session.

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [PlaybackSession](PlaybackSession.md) | This value cannot be`null`. |

### createRecordingSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createRecordingSession(): RecordingSession
```

Creates a recording session.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------|
| [RecordingSession](RecordingSession.md) | This value cannot be`null`. |

### createTranscodingSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createTranscodingSession(): TranscodingSession
```

Creates a transcoding session.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TranscodingSession](TranscodingSession.md) | This value cannot be`null`. |

### releaseSessionId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun releaseSessionId(sessionId: String): Unit
```

Creates a generic bundle session.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------|
| `sessionId` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |
