# MediaMetricsManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaMetricsManager

Kotlin| [Java](https://developer.android.com/reference/android/media/metrics/MediaMetricsManager "View this page in Java") 

```
class MediaMetricsManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.metrics.MediaMetricsManager](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#) |

This class gives information about, and interacts with media metrics.

## Summary

| Constants ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [INVALID_TIMESTAMP](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#INVALID_TIMESTAMP:kotlin.Long) <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BundleSession](https://developer.android.com/reference/kotlin/android/media/metrics/BundleSession) | [createBundleSession](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#createBundleSession())`()` Creates a generic bundle session. |
| [EditingSession](https://developer.android.com/reference/kotlin/android/media/metrics/EditingSession) | [createEditingSession](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#createEditingSession())`()` Creates a editing session. |
| [PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession) | [createPlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#createPlaybackSession())`()` Creates a playback session. |
| [RecordingSession](https://developer.android.com/reference/kotlin/android/media/metrics/RecordingSession) | [createRecordingSession](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#createRecordingSession())`()` Creates a recording session. |
| [TranscodingSession](https://developer.android.com/reference/kotlin/android/media/metrics/TranscodingSession) | [createTranscodingSession](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#createTranscodingSession())`()` Creates a transcoding session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [releaseSessionId](https://developer.android.com/reference/kotlin/android/media/metrics/MediaMetricsManager#releaseSessionId(kotlin.String))`(`sessionId:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a generic bundle session. |

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
| [BundleSession](https://developer.android.com/reference/kotlin/android/media/metrics/BundleSession) | This value cannot be`null`. |

### createEditingSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createEditingSession(): EditingSession
```

Creates a editing session.

| Return ||
|-------------------------------------------------------------------------------------------------------|-----------------------------|
| [EditingSession](https://developer.android.com/reference/kotlin/android/media/metrics/EditingSession) | This value cannot be`null`. |

### createPlaybackSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createPlaybackSession(): PlaybackSession
```

Creates a playback session.

| Return ||
|---------------------------------------------------------------------------------------------------------|-----------------------------|
| [PlaybackSession](https://developer.android.com/reference/kotlin/android/media/metrics/PlaybackSession) | This value cannot be`null`. |

### createRecordingSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createRecordingSession(): RecordingSession
```

Creates a recording session.

| Return ||
|-----------------------------------------------------------------------------------------------------------|-----------------------------|
| [RecordingSession](https://developer.android.com/reference/kotlin/android/media/metrics/RecordingSession) | This value cannot be`null`. |

### createTranscodingSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createTranscodingSession(): TranscodingSession
```

Creates a transcoding session.

| Return ||
|---------------------------------------------------------------------------------------------------------------|-----------------------------|
| [TranscodingSession](https://developer.android.com/reference/kotlin/android/media/metrics/TranscodingSession) | This value cannot be`null`. |

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
