# MediaSession2

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaSession2

Kotlin| [Java](../android/media/MediaSession2.md) 
| --- | --- |

```
open class MediaSession2 : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaSession2](../android/media/MediaSession2.md) |

This API is not generally intended for third party application developers. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media3 session Library](https://developer.android.com/media/media3/session/control-playback) for consistent behavior across all devices.

Allows a media app to expose its transport controls and playback information in a process to other processes including the Android framework and other apps.

## Summary

| Nested classes ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/MediaSession2.Builder.md) This API is not generally intended for third party application developers. |
| | [ControllerInfo](../android/media/MediaSession2.ControllerInfo.md) This API is not generally intended for third party application developers. |
| abstract | [SessionCallback](../android/media/MediaSession2.SessionCallback.md) This API is not generally intended for third party application developers. |
| --- | --- |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [broadcastSessionCommand](../android/media/MediaSession2.md))`(`command:` ` [Session2Command](../android/media/Session2Command.md)`, `args:` ` [Bundle](../android/os/Bundle.md)?`)` Broadcasts a session command to all the connected controllers |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancelSessionCommand](../android/media/MediaSession2.md))`(`controller:` ` [MediaSession2.ControllerInfo](../android/media/MediaSession2.ControllerInfo.md)`, `token:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)`)` Cancels the session command previously sent. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../android/media/MediaSession2.md))`()` <br /> |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaSession2.ControllerInfo](../android/media/MediaSession2.ControllerInfo.md)!\> | [getConnectedControllers](../android/media/MediaSession2.md))`()` Gets the list of the connected controllers |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getId](../android/media/MediaSession2.md))`()` Returns the session ID |
| open [Session2Token](../android/media/Session2Token.md) | [getToken](../android/media/MediaSession2.md))`()` Returns the [Session2Token](../android/media/Session2Token.md) for creating [MediaController2](../android/media/MediaController2.md). |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPlaybackActive](../android/media/MediaSession2.md))`()` Returns whether the playback is active (i.e. playing something) |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | [sendSessionCommand](../android/media/MediaSession2.md))`(`controller:` ` [MediaSession2.ControllerInfo](../android/media/MediaSession2.ControllerInfo.md)`, `command:` ` [Session2Command](../android/media/Session2Command.md)`, `args:` ` [Bundle](../android/os/Bundle.md)?`)` Sends a session command to a specific controller |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackActive](../android/media/MediaSession2.md))`(`playbackActive:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Sets whether the playback is active (i.e. playing something) |
| --- | --- |

## Public methods

### broadcastSessionCommand

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun broadcastSessionCommand(
    command: Session2Command, 
    args: Bundle?
): Unit
```

Broadcasts a session command to all the connected controllers

<br />

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `command` | [Session2Command](../android/media/Session2Command.md):the session command This value cannot be`null`. |
| `args` | [Bundle](../android/os/Bundle.md)?:optional arguments This value may be`null`. |

### cancelSessionCommand

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun cancelSessionCommand(
    controller: MediaSession2.ControllerInfo, 
    token: Any
): Unit
```

Cancels the session command previously sent.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [MediaSession2.ControllerInfo](../android/media/MediaSession2.ControllerInfo.md):the controller to get the session command This value cannot be`null`. |
| `token` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html):the token which is returned from [sendSessionCommand](../android/media/MediaSession2.md)). This value cannot be`null`. |

### close

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |

### getConnectedControllers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getConnectedControllers(): MutableList<MediaSession2.ControllerInfo!>
```

Gets the list of the connected controllers

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [MediaSession2.ControllerInfo](../android/media/MediaSession2.ControllerInfo.md)!> | list of the connected controllers. This value cannot be`null`. |

### getId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getId(): String
```

Returns the session ID

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getToken

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getToken(): Session2Token
```

Returns the [Session2Token](../android/media/Session2Token.md) for creating [MediaController2](../android/media/MediaController2.md).

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------|
| [Session2Token](../android/media/Session2Token.md) | This value cannot be`null`. |

### isPlaybackActive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPlaybackActive(): Boolean
```

Returns whether the playback is active (i.e. playing something)

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the playback active,`false`otherwise. |

### sendSessionCommand

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun sendSessionCommand(
    controller: MediaSession2.ControllerInfo, 
    command: Session2Command, 
    args: Bundle?
): Any
```

Sends a session command to a specific controller

<br />

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [MediaSession2.ControllerInfo](../android/media/MediaSession2.ControllerInfo.md):the controller to get the session command This value cannot be`null`. |
| `command` | [Session2Command](../android/media/Session2Command.md):the session command This value cannot be`null`. |
| `args` | [Bundle](../android/os/Bundle.md)?:optional arguments This value may be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) | a token which will be sent together in [SessionCallback.onCommandResult](../android/media/MediaSession2.SessionCallback.md))when its result is received. This value cannot be`null`. |

### setPlaybackActive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlaybackActive(playbackActive: Boolean): Unit
```

Sets whether the playback is active (i.e. playing something)

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `playbackActive` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):`true`if the playback active,`false`otherwise. |
