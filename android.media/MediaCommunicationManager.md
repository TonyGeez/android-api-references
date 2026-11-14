# MediaCommunicationManager

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaCommunicationManager

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaCommunicationManager "View this page in Java") 

```
open class MediaCommunicationManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaCommunicationManager](https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager#) |

This API is not generally intended for third party application developers. Use [MediaSessionManager](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager) to obtain information about active media sessions on the device. Provides support for interacting with [MediaSession2s](https://developer.android.com/reference/kotlin/android/media/MediaSession2) that applications have published to express their ongoing media playback state.

## Summary

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token)!\> | [getSession2Tokens](https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager#getSession2Tokens())`()` This API is not generally intended for third party application developers. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager#getVersion())`()` Gets the version of this [MediaCommunicationManager](https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager#). |

## Public methods

### getSession2Tokens

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSession2Tokens(): MutableList<Session2Token!>
```

This API is not generally intended for third party application developers. Use the [AndroidX](https://developer.android.com/jetpack/androidx.html) [Media3 session Library](https://developer.android.com/media/media3/session/control-playback) for consistent behavior across all devices.

Gets a list of [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token) with type [Session2Token.TYPE_SESSION](https://developer.android.com/reference/kotlin/android/media/Session2Token#TYPE_SESSION:kotlin.Int) for the current user.

Although this API can be used without any restriction, each session owners can accept or reject your uses of [MediaSession2](https://developer.android.com/reference/kotlin/android/media/MediaSession2).

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token)!> | A list of [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token). This value cannot be`null`. |

### getVersion

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getVersion(): Int
```

Gets the version of this [MediaCommunicationManager](https://developer.android.com/reference/kotlin/android/media/MediaCommunicationManager#).

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 1 or greater |
