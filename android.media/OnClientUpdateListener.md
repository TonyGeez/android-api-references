# RemoteController.OnClientUpdateListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnClientUpdateListener

Kotlin| [Java](../android/media/RemoteController.OnClientUpdateListener.md) 
| --- | --- |

```
interface OnClientUpdateListener
```

| [android.media.RemoteController.OnClientUpdateListener](../android/media/RemoteController.OnClientUpdateListener.md) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Interface definition for the callbacks to be invoked whenever media events, metadata and playback status are available.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientChange](../android/media/RemoteController.OnClientUpdateListener.md))`(`clearing:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called whenever all information, previously received through the other methods of the listener, is no longer valid and is about to be refreshed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientMetadataUpdate](../android/media/RemoteController.OnClientUpdateListener.md))`(`metadataEditor:` ` [RemoteController.MetadataEditor](../android/media/RemoteController.MetadataEditor.md)!`)` Called whenever new metadata is available. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientPlaybackStateUpdate](../android/media/RemoteController.OnClientUpdateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the playback state has changed. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientPlaybackStateUpdate](../android/media/RemoteController.OnClientUpdateListener.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `stateChangeTimeMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `currentPosMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `speed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Called whenever the playback state has changed, and playback position and speed are known. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClientTransportControlUpdate](../android/media/RemoteController.OnClientUpdateListener.md))`(`transportControlFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called whenever the transport control flags have changed. |

## Public methods

### onClientChange

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientChange(clearing: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever all information, previously received through the other methods of the listener, is no longer valid and is about to be refreshed. This is typically called whenever a new [RemoteControlClient](RemoteControlClient.md) has been selected by the system to have its media information published.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clearing` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if there is no selected RemoteControlClient and no information is available. |

### onClientMetadataUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientMetadataUpdate(metadataEditor: RemoteController.MetadataEditor!): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever new metadata is available. See the [MediaMetadataEditor.putLong(int, long)](MediaMetadataEditor.md)), [MediaMetadataEditor.putString(int, String)](MediaMetadataEditor.md)), [MediaMetadataEditor.putBitmap(int, Bitmap)](MediaMetadataEditor.md)), and [MediaMetadataEditor.putObject(int, Object)](MediaMetadataEditor.md))methods for the various keys that can be queried.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `metadataEditor` | [RemoteController.MetadataEditor](../android/media/RemoteController.MetadataEditor.md)!:the container of the new metadata. |

### onClientPlaybackStateUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientPlaybackStateUpdate(state: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the playback state has changed. It is called when no information is known about the playback progress in the media and the playback speed.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the playback states authorized in [RemoteControlClient.setPlaybackState(int)](RemoteControlClient.md)). |

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
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the playback states authorized in [RemoteControlClient.setPlaybackState(int)](RemoteControlClient.md)). |
| `stateChangeTimeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the system time at which the state change was reported, expressed in ms. Based on [android.os.SystemClock#elapsedRealtime()](../android.os/SystemClock.md)). |
| `currentPosMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a positive value for the current media playback position expressed in ms, a negative value if the position is temporarily unknown. |
| --- | --- |
| `speed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a value expressed as a ratio of 1x playback: 1.0f is normal playback, 2.0f is 2x, 0.5f is half-speed, -2.0f is rewind at 2x speed. 0.0f means nothing is playing (e.g. when state is [RemoteControlClient.PLAYSTATE_ERROR](RemoteControlClient.md)). |

### onClientTransportControlUpdate

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClientTransportControlUpdate(transportControlFlags: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the transport control flags have changed.

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transportControlFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):one of the flags authorized in [RemoteControlClient.setTransportControlFlags(int)](RemoteControlClient.md)). |
