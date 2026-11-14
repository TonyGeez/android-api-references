# MediaSessionManager.OnSession2TokensChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSession2TokensChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/session/MediaSessionManager.OnSession2TokensChangedListener "View this page in Java") 
| --- | --- |

```
interface OnSession2TokensChangedListener
```

| [android.media.session.MediaSessionManager.OnSession2TokensChangedListener](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener#) |

Listens for changes to the [getSession2Tokens()](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()). This can be added using [addOnSession2TokensChangedListener(android.media.session.MediaSessionManager.OnSession2TokensChangedListener,android.os.Handler)](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnSession2TokensChangedListener(android.media.session.MediaSessionManager.OnSession2TokensChangedListener,%20android.os.Handler)).

This API is not generally intended for third party application developers. Apps wanting media session functionality should use the [AndroidX Media3 Session Library](https://developer.android.com/reference/androidx/media3/session/package-summary.html).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSession2TokensChanged](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener#onSession2TokensChanged(kotlin.collections.MutableList))`(`tokens:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token.html#)!>`)` Called when the [getSession2Tokens()](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens())is changed. |

## Public methods

### onSession2TokensChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSession2TokensChanged(tokens: MutableList<Session2Token!>): Unit
```

Called when the [getSession2Tokens()](https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens())is changed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tokens` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token.html#)!\>:list of [Session2Token](https://developer.android.com/reference/kotlin/android/media/Session2Token.html#) This value cannot be`null`. |
