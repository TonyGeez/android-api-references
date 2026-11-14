# MediaCommunicationManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCommunicationManager

Kotlin| [Java](../android/media/MediaCommunicationManager.md) 
| --- | --- |

```
open class MediaCommunicationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.MediaCommunicationManager](../android/media/MediaCommunicationManager.md) |

This API is not generally intended for third party application developers. Use [MediaSessionManager](../android/media/session/MediaSessionManager.md) to obtain information about active media sessions on the device. Provides support for interacting with [MediaSession2s](../android/media/MediaSession2.md) that applications have published to express their ongoing media playback state.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Session2Token](../android/media/Session2Token.md)!\> | [getSession2Tokens](../android/media/MediaCommunicationManager.md))`()` This API is not generally intended for third party application developers. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](../android/media/MediaCommunicationManager.md))`()` Gets the version of this [MediaCommunicationManager](../android/media/MediaCommunicationManager.md). |

## Public methods

### getSession2Tokens

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSession2Tokens(): MutableList<Session2Token!>
```

This API is not generally intended for third party application developers. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media3 session Library](https://developer.android.com/media/media3/session/control-playback) for consistent behavior across all devices.

Gets a list of [Session2Token](../android/media/Session2Token.md) with type [Session2Token.TYPE_SESSION](../android/media/Session2Token.md) for the current user.

Although this API can be used without any restriction, each session owners can accept or reject your uses of [MediaSession2](../android/media/MediaSession2.md).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Session2Token](../android/media/Session2Token.md)!> | A list of [Session2Token](../android/media/Session2Token.md). This value cannot be`null`. |

### getVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVersion(): Int
```

Gets the version of this [MediaCommunicationManager](../android/media/MediaCommunicationManager.md).

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |
