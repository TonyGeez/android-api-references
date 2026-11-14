# MediaController2

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaController2

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaController2 "View this page in Java") 
| --- | --- |

```
open class MediaController2 : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaController2](https://developer.android.com/reference/kotlin/android/media/MediaController2#) |

This API is not generally intended for third party application developers. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media3 session Library](https://developer.android.com/media/media3/session/control-playback) for consistent behavior across all devices. Allows an app to interact with an active [MediaSession2](https://developer.android.com/reference/kotlin/android/media/MediaSession2) or a [MediaSession2Service](https://developer.android.com/reference/kotlin/android/media/MediaSession2Service) which would provide [MediaSession2](https://developer.android.com/reference/kotlin/android/media/MediaSession2).

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/MediaController2.Builder) This API is not generally intended for third party application developers. |
| abstract | [ControllerCallback](https://developer.android.com/reference/kotlin/android/media/MediaController2.ControllerCallback) This API is not generally intended for third party application developers. |

| Public methods ||
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelSessionCommand](https://developer.android.com/reference/kotlin/android/media/MediaController2#cancelSessionCommand(kotlin.Any))`(`token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`)` Cancels the session command previously sent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/android/media/MediaController2#close())`()` <br /> |
| open [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token)? | [getConnectedToken](https://developer.android.com/reference/kotlin/android/media/MediaController2#getConnectedToken())`()` Returns [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token) of the connected session. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaybackActive](https://developer.android.com/reference/kotlin/android/media/MediaController2#isPlaybackActive())`()` Returns whether the session's playback is active. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [sendSessionCommand](https://developer.android.com/reference/kotlin/android/media/MediaController2#sendSessionCommand(android.media.Session2Command,%20android.os.Bundle))`(`command:` ` [Session2Command](https://developer.android.com/reference/kotlin/android/media/Session2Command)`, `args:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Sends a session command to the session |

## Public methods

### cancelSessionCommand

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelSessionCommand(token: Any): Unit
```

Cancels the session command previously sent.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the token which is returned from [sendSessionCommand](https://developer.android.com/reference/kotlin/android/media/MediaController2#sendSessionCommand(android.media.Session2Command,%20android.os.Bundle)). This value cannot be`null`. |

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getConnectedToken

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConnectedToken(): Session2Token?
```

Returns [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token) of the connected session. If it is not connected yet, it returns`null`.

This may differ with the [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token) from the constructor. For example, if the controller is created with the token for [MediaSession2Service](https://developer.android.com/reference/kotlin/android/media/MediaSession2Service), this would return token for the [MediaSession2](https://developer.android.com/reference/kotlin/android/media/MediaSession2) in the service.

| Return ||
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token)? | Session2Token of the connected session, or`null`if not connected |

### isPlaybackActive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPlaybackActive(): Boolean
```

Returns whether the session's playback is active.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if playback active.`false`otherwise. |

**See Also**

- [android.media.MediaController2.ControllerCallback#onPlaybackActiveChanged(MediaController2, boolean)](https://developer.android.com/reference/kotlin/android/media/MediaController2.ControllerCallback#onPlaybackActiveChanged(android.media.MediaController2,%20kotlin.Boolean)) 

### sendSessionCommand

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendSessionCommand(
    command: Session2Command, 
    args: Bundle?
): Any
```

Sends a session command to the session

<br />

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Session2Command](https://developer.android.com/reference/kotlin/android/media/Session2Command):the session command This value cannot be`null`. |
| `args` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:optional arguments This value may be`null`. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a token which will be sent together in [ControllerCallback.onCommandResult](https://developer.android.com/reference/kotlin/android/media/MediaController2.ControllerCallback#onCommandResult(android.media.MediaController2,%20kotlin.Any,%20android.media.Session2Command,%20android.media.Session2Command.Result))when its result is received. This value cannot be`null`. |
