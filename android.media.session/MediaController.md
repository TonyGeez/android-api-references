# MediaController

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaController

Kotlin| [Java](https://developer.android.com/reference/android/media/session/MediaController "View this page in Java") 

```
class MediaController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.session.MediaController](https://developer.android.com/reference/kotlin/android/media/session/MediaController#) |

Allows an app to interact with an ongoing media session. Media buttons and other commands can be sent to the session. A callback may be registered to receive updates from the session, such as metadata and play state changes.

A MediaController can be created through [MediaSessionManager](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager) if you hold the "android.permission.MEDIA_CONTENT_CONTROL" permission or are an enabled notification listener or by getting a [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token) directly from the session owner.

MediaController objects are thread-safe.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback) Callback for receiving updates from the session. |
| | [PlaybackInfo](https://developer.android.com/reference/kotlin/android/media/session/MediaController.PlaybackInfo) Holds information about the current playback and how audio is handled for this session. |
| | [TransportControls](https://developer.android.com/reference/kotlin/android/media/session/MediaController.TransportControls) Interface for controlling media playback on a session. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaController](https://developer.android.com/reference/kotlin/android/media/session/MediaController#MediaController(android.content.Context,%20android.media.session.MediaSession.Token))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)`, `token:` ` [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token)`)` Create a new MediaController from a session's token. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustVolume](https://developer.android.com/reference/kotlin/android/media/session/MediaController#adjustVolume(kotlin.Int,%20kotlin.Int))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adjust the volume of the output this session is playing on. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchMediaButtonEvent](https://developer.android.com/reference/kotlin/android/media/session/MediaController#dispatchMediaButtonEvent(android.view.KeyEvent))`(`keyEvent:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)`)` Send the specified media button event to the session. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getExtras](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getExtras())`()` Get the extras for this session. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getFlags())`()` Get the flags for this session. |
| [MediaMetadata](https://developer.android.com/reference/kotlin/android/media/MediaMetadata.html#)? | [getMetadata](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getMetadata())`()` Get the current metadata for this session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPackageName](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getPackageName())`()` Get the session owner's package name. |
| [MediaController.PlaybackInfo](https://developer.android.com/reference/kotlin/android/media/session/MediaController.PlaybackInfo) | [getPlaybackInfo](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getPlaybackInfo())`()` Returns the current playback info for this session. |
| [PlaybackState](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState)? | [getPlaybackState](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getPlaybackState())`()` Get the current playback state for this session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaSession.QueueItem](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.QueueItem)!\>? | [getQueue](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getQueue())`()` Get the current play queue for this session if one is set. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getQueueTitle](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getQueueTitle())`()` Get the queue title for this session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRatingType](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getRatingType())`()` Get the rating type supported by the session. |
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | [getSessionActivity](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getSessionActivity())`()` Get an intent for launching UI associated with this session if one exists. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getSessionInfo](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getSessionInfo())`()` Gets the additional session information which was set when the session was created. |
| [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token) | [getSessionToken](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getSessionToken())`()` Get the token for the session this is connected to. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTag](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getTag())`()` Get the session's tag for debugging purposes. |
| [MediaController.TransportControls](https://developer.android.com/reference/kotlin/android/media/session/MediaController.TransportControls) | [getTransportControls](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getTransportControls())`()` Get a [TransportControls](https://developer.android.com/reference/kotlin/android/media/session/MediaController.TransportControls) instance to send transport actions to the associated session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/media/session/MediaController#registerCallback(android.media.session.MediaController.Callback))`(`callback:` ` [MediaController.Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback)`)` Registers a callback to receive updates from the Session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](https://developer.android.com/reference/kotlin/android/media/session/MediaController#registerCallback(android.media.session.MediaController.Callback,%20android.os.Handler))`(`callback:` ` [MediaController.Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback)`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?`)` Registers a callback to receive updates from the session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendCommand](https://developer.android.com/reference/kotlin/android/media/session/MediaController#sendCommand(kotlin.String,%20android.os.Bundle,%20android.os.ResultReceiver))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `cb:` ` [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#)?`)` Sends a generic command to the session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolumeTo](https://developer.android.com/reference/kotlin/android/media/session/MediaController#setVolumeTo(kotlin.Int,%20kotlin.Int))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the volume of the output this session is playing on. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](https://developer.android.com/reference/kotlin/android/media/session/MediaController#unregisterCallback(android.media.session.MediaController.Callback))`(`callback:` ` [MediaController.Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback)`)` Unregisters the specified callback. |

## Public constructors

### MediaController

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
MediaController(
    context: Context, 
    token: MediaSession.Token)
```

Create a new MediaController from a session's token.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#):The caller's context. This value cannot be`null`. |
| `token` | [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token):The token for the session. This value cannot be`null`. |

## Public methods

### adjustVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adjustVolume(
    direction: Int, 
    flags: Int
): Unit
```

Adjust the volume of the output this session is playing on. The direction must be one of [AudioManager.ADJUST_LOWER](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#ADJUST_LOWER:kotlin.Int), [AudioManager.ADJUST_RAISE](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#ADJUST_RAISE:kotlin.Int), or [AudioManager.ADJUST_SAME](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#ADJUST_SAME:kotlin.Int). The command will be ignored if the session does not support [VolumeProvider.VOLUME_CONTROL_RELATIVE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider.html#VOLUME_CONTROL_RELATIVE:kotlin.Int) or [VolumeProvider.VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider.html#VOLUME_CONTROL_ABSOLUTE:kotlin.Int). The flags in [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#) may be used to affect the handling.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------|
| `direction` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The direction to adjust the volume in. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Any flags to pass with the command. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/session/MediaController#getPlaybackInfo()> 

### dispatchMediaButtonEvent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun dispatchMediaButtonEvent(keyEvent: KeyEvent): Boolean
```

Send the specified media button event to the session. Only media keys can be sent by this method, other keys will be ignored.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyEvent` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#):The media button event to dispatch. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the event was sent to the session, false otherwise. |

### getExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle?
```

Get the extras for this session.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | This value may be`null`. |

### getFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Long
```

Get the flags for this session. Flags are defined in [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession).

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The current set of flags for the session. |

### getMetadata

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMetadata(): MediaMetadata?
```

Get the current metadata for this session.

| Return ||
|----------------------------------------------------------------------------------------------------|------------------------------------|
| [MediaMetadata](https://developer.android.com/reference/kotlin/android/media/MediaMetadata.html#)? | The current MediaMetadata or null. |

### getPackageName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPackageName(): String!
```

Get the session owner's package name.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | The package name of the session owner. |

### getPlaybackInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlaybackInfo(): MediaController.PlaybackInfo
```

Returns the current playback info for this session.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MediaController.PlaybackInfo](https://developer.android.com/reference/kotlin/android/media/session/MediaController.PlaybackInfo) | This value cannot be`null`. |

### getPlaybackState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlaybackState(): PlaybackState?
```

Get the current playback state for this session.

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------|
| [PlaybackState](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState)? | The current PlaybackState or null |

### getQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQueue(): MutableList<MediaSession.QueueItem!>?
```

Get the current play queue for this session if one is set. If you only care about the current item [getMetadata()](https://developer.android.com/reference/kotlin/android/media/session/MediaController#getMetadata())should be used.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaSession.QueueItem](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.QueueItem)!>? | The current play queue or null. |

### getQueueTitle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQueueTitle(): CharSequence?
```

Get the queue title for this session.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getRatingType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRatingType(): Int
```

Get the rating type supported by the session. One of:

- [Rating.RATING_NONE](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_NONE:kotlin.Int)
- [Rating.RATING_HEART](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_HEART:kotlin.Int)
- [Rating.RATING_THUMB_UP_DOWN](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_THUMB_UP_DOWN:kotlin.Int)
- [Rating.RATING_3_STARS](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_3_STARS:kotlin.Int)
- [Rating.RATING_4_STARS](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_4_STARS:kotlin.Int)
- [Rating.RATING_5_STARS](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_5_STARS:kotlin.Int)
- [Rating.RATING_PERCENTAGE](https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_PERCENTAGE:kotlin.Int)

<br />

| Return ||
|----------------------------------------------------------------------------|---------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The supported rating type |

### getSessionActivity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionActivity(): PendingIntent?
```

Get an intent for launching UI associated with this session if one exists.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)? | A [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#) to launch UI or null. |

### getSessionInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionInfo(): Bundle
```

Gets the additional session information which was set when the session was created.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | The additional session information, or an empty [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) if not set. This value cannot be`null`. |

### getSessionToken

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionToken(): MediaSession.Token
```

Get the token for the session this is connected to.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MediaSession.Token](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token) | The token for the connected session. This value cannot be`null`. |

### getTag

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTag(): String
```

Get the session's tag for debugging purposes.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The session's tag. This value cannot be`null`. |

### getTransportControls

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransportControls(): MediaController.TransportControls
```

Get a [TransportControls](https://developer.android.com/reference/kotlin/android/media/session/MediaController.TransportControls) instance to send transport actions to the associated session.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MediaController.TransportControls](https://developer.android.com/reference/kotlin/android/media/session/MediaController.TransportControls) | A transport controls instance. This value cannot be`null`. |

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: MediaController.Callback): Unit
```

Registers a callback to receive updates from the Session. Updates will be posted on the caller's thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaController.Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback):The callback object, must not be null. |

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(
    callback: MediaController.Callback, 
    handler: Handler?
): Unit
```

Registers a callback to receive updates from the session. Updates will be posted on the specified handler's thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaController.Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback):The callback object, must not be null. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)?:The handler to post updates on. If null the callers thread will be used. |

### sendCommand

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun sendCommand(
    command: String, 
    args: Bundle?, 
    cb: ResultReceiver?
): Unit
```

Sends a generic command to the session. It is up to the session creator to decide what commands and parameters they will support. As such, commands should only be sent to sessions that the controller owns.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The command to send This value cannot be`null`. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Any parameters to include with the command This value may be`null`. |
| `cb` | [ResultReceiver](https://developer.android.com/reference/kotlin/android/os/ResultReceiver.html#)?:The callback to receive the result on This value may be`null`. |

### setVolumeTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVolumeTo(
    value: Int, 
    flags: Int
): Unit
```

Set the volume of the output this session is playing on. The command will be ignored if it does not support [VolumeProvider.VOLUME_CONTROL_ABSOLUTE](https://developer.android.com/reference/kotlin/android/media/VolumeProvider.html#VOLUME_CONTROL_ABSOLUTE:kotlin.Int). The flags in [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#) may be used to affect the handling.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value to set it to, between 0 and the reported max. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags from [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager.html#) to include with the volume request. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/media/session/MediaController#getPlaybackInfo()> 

### unregisterCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterCallback(callback: MediaController.Callback): Unit
```

Unregisters the specified callback. If an update has already been posted you may still receive it after calling this method.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaController.Callback](https://developer.android.com/reference/kotlin/android/media/session/MediaController.Callback):The callback to remove. This value cannot be`null`. |
