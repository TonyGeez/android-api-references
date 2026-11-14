Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteController

```
class RemoteController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.RemoteController](RemoteController.md) |

> [!CAUTION]
> **This class was deprecated in API level 21.**
>
> Use `https://developer.android.com/reference/kotlin/android/media/session/MediaController` instead.

The RemoteController class is used to control media playback, display and update media metadata and playback status, published by applications using the `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient` class.

A RemoteController shall be registered through `https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteController(android.media.RemoteController)` in order for the system to send media event updates to the `https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener` listener set in the class constructor. Implement the methods of the interface to receive the information published by the active `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient` instances. 
By default an `https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener` implementation will not receive bitmaps for album art. Use `https://developer.android.com/reference/kotlin/android/media/RemoteController#setArtworkConfiguration(kotlin.Int,%20kotlin.Int)` to receive images as well.

Registration requires the `https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener` listener to be one of the enabled notification listeners (see `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#`).

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor` A class to read the metadata published by a `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient`, or send a `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient` new values for keys that can be edited. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener` Interface definition for the callbacks to be invoked whenever media events, metadata and playback status are available. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#POSITION_SYNCHRONIZATION_CHECK:kotlin.Int` The playback position synchronization mode where the RemoteControlClient instances which expose their playback position to the framework, will be regularly polled to check whether any drift has been noticed between their estimated position and the one they report. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#POSITION_SYNCHRONIZATION_NONE:kotlin.Int` Default playback position synchronization mode where the RemoteControlClient is not asked regularly for its playback position to see if it has drifted from the estimated position. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/RemoteController#RemoteController(android.content.Context,%20android.media.RemoteController.OnClientUpdateListener)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, updateListener: https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener!)` Class constructor. |
| `https://developer.android.com/reference/kotlin/android/media/RemoteController#RemoteController(android.content.Context,%20android.media.RemoteController.OnClientUpdateListener,%20android.os.Looper)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, updateListener: https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener!, looper: https://developer.android.com/reference/kotlin/android/os/Looper.html#!)` Class constructor. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#clearArtworkConfiguration()()` Prevents this RemoteController from receiving artwork images. |
| [RemoteController.MetadataEditor](../android/media/RemoteController.MetadataEditor.md)! | `https://developer.android.com/reference/kotlin/android/media/RemoteController#editMetadata()()` Creates a `https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor` for updating metadata values of the editable keys of the current `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient`. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#getEstimatedMediaPosition()()` Return the estimated playback position of the current media track or a negative value if not available. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#seekTo(kotlin.Long)(timeMs: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the new playback position. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#sendMediaKeyEvent(android.view.KeyEvent)(keyEvent: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Send a simulated key event for a media button to be received by the current client. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#setArtworkConfiguration(kotlin.Int,%20kotlin.Int)(width: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, height: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the maximum artwork image dimensions to be received in the metadata. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/RemoteController#setSynchronizationMode(kotlin.Int)(sync: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the playback position synchronization mode. |

## Constants

### POSITION_SYNCHRONIZATION_CHECK

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POSITION_SYNCHRONIZATION_CHECK: Int
```

**Deprecated:** *Deprecated in Java.*

The playback position synchronization mode where the RemoteControlClient instances which expose their playback position to the framework, will be regularly polled to check whether any drift has been noticed between their estimated position and the one they report. Note that this mode should only ever be used when needing to display very accurate playback position, as regularly polling a RemoteControlClient for its position may have an impact on battery life (if applicable) when this query will trigger network transactions in the case of remote playback.

 Value: 1

### POSITION_SYNCHRONIZATION_NONE

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val POSITION_SYNCHRONIZATION_NONE: Int
```

**Deprecated:** *Deprecated in Java.*

Default playback position synchronization mode where the RemoteControlClient is not asked regularly for its playback position to see if it has drifted from the estimated position.

 Value: 0

## Public constructors

### RemoteController

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteController(
    context: Context!, 
    updateListener: RemoteController.OnClientUpdateListener!)
```

Class constructor.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the `https://developer.android.com/reference/kotlin/android/content/Context.html#`, must be non-null. |
| `updateListener` | [RemoteController.OnClientUpdateListener](../android/media/RemoteController.OnClientUpdateListener.md)!: the listener to be called whenever new client information is available, must be non-null. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### RemoteController

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteController(
    context: Context!, 
    updateListener: RemoteController.OnClientUpdateListener!, 
    looper: Looper!)
```

Class constructor.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md)!: the `https://developer.android.com/reference/kotlin/android/content/Context.html#`, must be non-null. |
| `updateListener` | [RemoteController.OnClientUpdateListener](../android/media/RemoteController.OnClientUpdateListener.md)!: the listener to be called whenever new client information is available, must be non-null. |
| `looper` | [Looper](../android.os/Looper.md)!: the `https://developer.android.com/reference/kotlin/android/os/Looper.html#` on which to run the event loop, or null to use the current thread's looper. |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

## Public methods

### clearArtworkConfiguration

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun clearArtworkConfiguration(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Prevents this RemoteController from receiving artwork images.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if receiving artwork images was successfully disabled. |

### editMetadata

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun editMetadata(): RemoteController.MetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Creates a `https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor` for updating metadata values of the editable keys of the current `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient`. This method can only be called on a registered RemoteController.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/RemoteController.MetadataEditor!` | a new MetadataEditor instance. |

### getEstimatedMediaPosition

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEstimatedMediaPosition(): Long
```

**Deprecated:** *Deprecated in Java.*

Return the estimated playback position of the current media track or a negative value if not available.

The value returned is estimated by the current process and may not be perfect. The time returned by this method is calculated from the last state change time based on the current play position at that time and the last known playback speed. An application may call `https://developer.android.com/reference/kotlin/android/media/RemoteController#setSynchronizationMode(kotlin.Int)` to apply a synchronization policy that will periodically re-sync the estimated position with the RemoteControlClient.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the current estimated playback position in milliseconds or a negative value if not available |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/RemoteController.OnClientUpdateListener#onClientPlaybackStateUpdate(kotlin.Int,%20kotlin.Long,%20kotlin.Long,%20kotlin.Float)`

### seekTo

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun seekTo(timeMs: Long): Boolean
```

**Deprecated:** *Deprecated in Java.*

Sets the new playback position. This method can only be called on a registered RemoteController.

| Parameters ||
|---|---|
| `timeMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): a 0 or positive value for the new playback position, expressed in ms. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the command to set the playback position was successfully sent. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### sendMediaKeyEvent

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendMediaKeyEvent(keyEvent: KeyEvent!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Send a simulated key event for a media button to be received by the current client. To simulate a key press, you must first send a KeyEvent built with a `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_DOWN:kotlin.Int` action, then another event with the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#ACTION_UP:kotlin.Int` action.

The key event will be sent to the registered receiver (see `https://developer.android.com/reference/kotlin/android/media/AudioManager#registerMediaButtonEventReceiver(android.app.PendingIntent)`) whose associated `https://developer.android.com/reference/kotlin/android/media/RemoteControlClient`'s metadata and playback state is published (there may be none under some circumstances).

| Parameters ||
|---|---|
| `keyEvent` | [KeyEvent](../android.view/KeyEvent.md)!: a media session `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#`, as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#isMediaSessionKey(kotlin.Int)`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the event was successfully sent, false otherwise. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the provided `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#` is not a media session key, as defined by `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#isMediaSessionKey(kotlin.Int)`. |

### setArtworkConfiguration

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setArtworkConfiguration(
    width: Int, 
    height: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Set the maximum artwork image dimensions to be received in the metadata. No bitmaps will be received unless this has been specified.

| Parameters ||
|---|---|
| `width` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum width in pixels |
| `height` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the maximum height in pixels |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the artwork dimension was successfully set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |

### setSynchronizationMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSynchronizationMode(sync: Int): Boolean
```

**Deprecated:** *Deprecated in Java.*

Set the playback position synchronization mode. Must be called on a registered RemoteController.

| Parameters ||
|---|---|
| `sync` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): `https://developer.android.com/reference/kotlin/android/media/RemoteController#POSITION_SYNCHRONIZATION_NONE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/media/RemoteController#POSITION_SYNCHRONIZATION_CHECK:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the synchronization mode was successfully set. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | |
