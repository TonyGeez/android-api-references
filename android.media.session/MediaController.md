# MediaController

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaController

Kotlin| [Java](../android/media/session/MediaController.md) 
| --- | --- |

```
class MediaController
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.session.MediaController](../android/media/session/MediaController.md) |

Allows an app to interact with an ongoing media session. Media buttons and other commands can be sent to the session. A callback may be registered to receive updates from the session, such as metadata and play state changes.

A MediaController can be created through [MediaSessionManager](../android/media/session/MediaSessionManager.md) if you hold the "android.permission.MEDIA_CONTENT_CONTROL" permission or are an enabled notification listener or by getting a [MediaSession.Token](../android/media/session/MediaSession.Token.md) directly from the session owner.

MediaController objects are thread-safe.

## Summary

| Nested classes ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Callback](../android/media/session/MediaController.Callback.md) Callback for receiving updates from the session. |
| | [PlaybackInfo](../android/media/session/MediaController.PlaybackInfo.md) Holds information about the current playback and how audio is handled for this session. |
| | [TransportControls](../android/media/session/MediaController.TransportControls.md) Interface for controlling media playback on a session. |
| --- | --- |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaController](../android/media/session/MediaController.md))`(`context:` ` [Context](../android/content/Context.md)`, `token:` ` [MediaSession.Token](../android/media/session/MediaSession.Token.md)`)` Create a new MediaController from a session's token. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustVolume](../android/media/session/MediaController.md))`(`direction:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Adjust the volume of the output this session is playing on. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [dispatchMediaButtonEvent](../android/media/session/MediaController.md))`(`keyEvent:` ` [KeyEvent](../android/view/KeyEvent.md)`)` Send the specified media button event to the session. |
| [Bundle](../android/os/Bundle.md)? | [getExtras](../android/media/session/MediaController.md))`()` Get the extras for this session. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getFlags](../android/media/session/MediaController.md))`()` Get the flags for this session. |
| [MediaMetadata](../android/media/MediaMetadata.md)? | [getMetadata](../android/media/session/MediaController.md))`()` Get the current metadata for this session. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getPackageName](../android/media/session/MediaController.md))`()` Get the session owner's package name. |
| --- | --- |
| [MediaController.PlaybackInfo](../android/media/session/MediaController.PlaybackInfo.md) | [getPlaybackInfo](../android/media/session/MediaController.md))`()` Returns the current playback info for this session. |
| [PlaybackState](../android/media/session/PlaybackState.md)? | [getPlaybackState](../android/media/session/MediaController.md))`()` Get the current playback state for this session. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaSession.QueueItem](../android/media/session/MediaSession.QueueItem.md)!\>? | [getQueue](../android/media/session/MediaController.md))`()` Get the current play queue for this session if one is set. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getQueueTitle](../android/media/session/MediaController.md))`()` Get the queue title for this session. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRatingType](../android/media/session/MediaController.md))`()` Get the rating type supported by the session. |
| [PendingIntent](../android/app/PendingIntent.md)? | [getSessionActivity](../android/media/session/MediaController.md))`()` Get an intent for launching UI associated with this session if one exists. |
| --- | --- |
| [Bundle](../android/os/Bundle.md) | [getSessionInfo](../android/media/session/MediaController.md))`()` Gets the additional session information which was set when the session was created. |
| [MediaSession.Token](../android/media/session/MediaSession.Token.md) | [getSessionToken](../android/media/session/MediaController.md))`()` Get the token for the session this is connected to. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTag](../android/media/session/MediaController.md))`()` Get the session's tag for debugging purposes. |
| --- | --- |
| [MediaController.TransportControls](../android/media/session/MediaController.TransportControls.md) | [getTransportControls](../android/media/session/MediaController.md))`()` Get a [TransportControls](../android/media/session/MediaController.TransportControls.md) instance to send transport actions to the associated session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](../android/media/session/MediaController.md))`(`callback:` ` [MediaController.Callback](../android/media/session/MediaController.Callback.md)`)` Registers a callback to receive updates from the Session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [registerCallback](../android/media/session/MediaController.md))`(`callback:` ` [MediaController.Callback](../android/media/session/MediaController.Callback.md)`, `handler:` ` [Handler](../android/os/Handler.md)?`)` Registers a callback to receive updates from the session. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [sendCommand](../android/media/session/MediaController.md))`(`command:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `args:` ` [Bundle](../android/os/Bundle.md)?`, `cb:` ` [ResultReceiver](../android/os/ResultReceiver.md)?`)` Sends a generic command to the session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setVolumeTo](../android/media/session/MediaController.md))`(`value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the volume of the output this session is playing on. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [unregisterCallback](../android/media/session/MediaController.md))`(`callback:` ` [MediaController.Callback](../android/media/session/MediaController.Callback.md)`)` Unregisters the specified callback. |
| --- | --- |

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
| `context` | [Context](../android/content/Context.md):The caller's context. This value cannot be`null`. |
| `token` | [MediaSession.Token](../android/media/session/MediaSession.Token.md):The token for the session. This value cannot be`null`. |

## Public methods

### adjustVolume

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun adjustVolume(
    direction: Int, 
    flags: Int
): Unit
```

Adjust the volume of the output this session is playing on. The direction must be one of [AudioManager.ADJUST_LOWER](../android/media/AudioManager.md), [AudioManager.ADJUST_RAISE](../android/media/AudioManager.md), or [AudioManager.ADJUST_SAME](../android/media/AudioManager.md). The command will be ignored if the session does not support [VolumeProvider.VOLUME_CONTROL_RELATIVE](../android/media/VolumeProvider.md) or [VolumeProvider.VOLUME_CONTROL_ABSOLUTE](../android/media/VolumeProvider.md). The flags in [AudioManager](../android/media/AudioManager.md) may be used to affect the handling.

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
| `keyEvent` | [KeyEvent](../android/view/KeyEvent.md):The media button event to dispatch. This value cannot be`null`. |

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
| [Bundle](../android/os/Bundle.md)? | This value may be`null`. |

### getFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Long
```

Get the flags for this session. Flags are defined in [MediaSession](../android/media/session/MediaSession.md).

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
| [MediaMetadata](../android/media/MediaMetadata.md)? | The current MediaMetadata or null. |

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
| [MediaController.PlaybackInfo](../android/media/session/MediaController.PlaybackInfo.md) | This value cannot be`null`. |

### getPlaybackState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlaybackState(): PlaybackState?
```

Get the current playback state for this session.

| Return ||
|------------------------------------------------------------------------------------------------------|-----------------------------------|
| [PlaybackState](../android/media/session/PlaybackState.md)? | The current PlaybackState or null |

### getQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getQueue(): MutableList<MediaSession.QueueItem!>?
```

Get the current play queue for this session if one is set. If you only care about the current item [getMetadata()](../android/media/session/MediaController.md))should be used.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaSession.QueueItem](../android/media/session/MediaSession.QueueItem.md)!>? | The current play queue or null. |

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

- [Rating.RATING_NONE](../android/media/Rating.md)
- [Rating.RATING_HEART](../android/media/Rating.md)
- [Rating.RATING_THUMB_UP_DOWN](../android/media/Rating.md)
- [Rating.RATING_3_STARS](../android/media/Rating.md)
- [Rating.RATING_4_STARS](../android/media/Rating.md)
- [Rating.RATING_5_STARS](../android/media/Rating.md)
- [Rating.RATING_PERCENTAGE](../android/media/Rating.md)

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
| [PendingIntent](../android/app/PendingIntent.md)? | A [PendingIntent](../android/app/PendingIntent.md) to launch UI or null. |

### getSessionInfo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionInfo(): Bundle
```

Gets the additional session information which was set when the session was created.

| Return ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android/os/Bundle.md) | The additional session information, or an empty [Bundle](../android/os/Bundle.md) if not set. This value cannot be`null`. |

### getSessionToken

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSessionToken(): MediaSession.Token
```

Get the token for the session this is connected to.

| Return ||
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [MediaSession.Token](../android/media/session/MediaSession.Token.md) | The token for the connected session. This value cannot be`null`. |

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

Get a [TransportControls](../android/media/session/MediaController.TransportControls.md) instance to send transport actions to the associated session.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| [MediaController.TransportControls](../android/media/session/MediaController.TransportControls.md) | A transport controls instance. This value cannot be`null`. |

### registerCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerCallback(callback: MediaController.Callback): Unit
```

Registers a callback to receive updates from the Session. Updates will be posted on the caller's thread.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [MediaController.Callback](../android/media/session/MediaController.Callback.md):The callback object, must not be null. |

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
| `callback` | [MediaController.Callback](../android/media/session/MediaController.Callback.md):The callback object, must not be null. |
| `handler` | [Handler](../android/os/Handler.md)?:The handler to post updates on. If null the callers thread will be used. |

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
| `args` | [Bundle](../android/os/Bundle.md)?:Any parameters to include with the command This value may be`null`. |
| `cb` | [ResultReceiver](../android/os/ResultReceiver.md)?:The callback to receive the result on This value may be`null`. |
| --- | --- |

### setVolumeTo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setVolumeTo(
    value: Int, 
    flags: Int
): Unit
```

Set the volume of the output this session is playing on. The command will be ignored if it does not support [VolumeProvider.VOLUME_CONTROL_ABSOLUTE](../android/media/VolumeProvider.md). The flags in [AudioManager](../android/media/AudioManager.md) may be used to affect the handling.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The value to set it to, between 0 and the reported max. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Flags from [AudioManager](../android/media/AudioManager.md) to include with the volume request. |

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
| `callback` | [MediaController.Callback](../android/media/session/MediaController.Callback.md):The callback to remove. This value cannot be`null`. |
