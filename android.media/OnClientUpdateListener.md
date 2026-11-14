# RemoteController.OnClientUpdateListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClientUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/RemoteController.OnClientUpdateListener "View this page in Java") 
| --- | --- |

```
interface OnClientUpdateListener
```

| [android.media.RemoteController.OnClientUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Interface definition for the callbacks to be invoked whenever media events, metadata and playback status are available.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientChange](https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#onClientChange(kotlin.Boolean))`(`clearing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called whenever all information, previously received through the other methods of the listener, is no longer valid and is about to be refreshed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientMetadataUpdate](https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#onClientMetadataUpdate(android.media.RemoteController.MetadataEditor))`(`metadataEditor:` ` [RemoteController.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor)!`)` Called whenever new metadata is available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientPlaybackStateUpdate](https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#onClientPlaybackStateUpdate(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the playback state has changed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientPlaybackStateUpdate](https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#onClientPlaybackStateUpdate(kotlin.Int,%20kotlin.Long,%20kotlin.Long,%20kotlin.Float))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stateChangeTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `currentPosMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `speed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called whenever the playback state has changed, and playback position and speed are known. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientTransportControlUpdate](https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#onClientTransportControlUpdate(kotlin.Int))`(`transportControlFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the transport control flags have changed. |

## Public methods

### onClientChange

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientChange(clearing: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever all information, previously received through the other methods of the listener, is no longer valid and is about to be refreshed. This is typically called whenever a new [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient) has been selected by the system to have its media information published.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clearing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if there is no selected RemoteControlClient and no information is available. |

### onClientMetadataUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientMetadataUpdate(metadataEditor: RemoteController.MetadataEditor!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever new metadata is available. See the [MediaMetadataEditor.putLong(int, long)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putLong(kotlin.Int,%20kotlin.Long)), [MediaMetadataEditor.putString(int, String)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putString(kotlin.Int,%20kotlin.String)), [MediaMetadataEditor.putBitmap(int, Bitmap)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putBitmap(kotlin.Int,%20android.graphics.Bitmap)), and [MediaMetadataEditor.putObject(int, Object)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#putObject(kotlin.Int,%20kotlin.Any))methods for the various keys that can be queried.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metadataEditor` | [RemoteController.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor)!:the container of the new metadata. |

### onClientPlaybackStateUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientPlaybackStateUpdate(state: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the playback state has changed. It is called when no information is known about the playback progress in the media and the playback speed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the playback states authorized in [RemoteControlClient.setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)). |

### onClientPlaybackStateUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientPlaybackStateUpdate(
    state: Int, 
    stateChangeTimeMs: Long, 
    currentPosMs: Long, 
    speed: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the playback state has changed, and playback position and speed are known.

| Parameters ||
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the playback states authorized in [RemoteControlClient.setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)). |
| `stateChangeTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the system time at which the state change was reported, expressed in ms. Based on [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime()). |
| `currentPosMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a positive value for the current media playback position expressed in ms, a negative value if the position is temporarily unknown. |
| --- | --- |
| `speed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a value expressed as a ratio of 1x playback: 1.0f is normal playback, 2.0f is 2x, 0.5f is half-speed, -2.0f is rewind at 2x speed. 0.0f means nothing is playing (e.g. when state is [RemoteControlClient.PLAYSTATE_ERROR](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_ERROR:kotlin.Int)). |

### onClientTransportControlUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientTransportControlUpdate(transportControlFlags: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the transport control flags have changed.

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transportControlFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the flags authorized in [RemoteControlClient.setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int)). |
