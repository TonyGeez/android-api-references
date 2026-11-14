# MediaSessionManager.OnSession2TokensChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnSession2TokensChangedListener

Kotlin| [Java](../android/media/session/MediaSessionManager.OnSession2TokensChangedListener.md) 
| --- | --- |

```
interface OnSession2TokensChangedListener
```

| [android.media.session.MediaSessionManager.OnSession2TokensChangedListener](../android/media/session/MediaSessionManager.OnSession2TokensChangedListener.md) |

Listens for changes to the [getSession2Tokens()](MediaSessionManager.md)). This can be added using [addOnSession2TokensChangedListener(android.media.session.MediaSessionManager.OnSession2TokensChangedListener,android.os.Handler)](MediaSessionManager.md)).

This API is not generally intended for third party application developers. Apps wanting media session functionality should use the [AndroidX Media3 Session Library](../androidx/media3/session/_package.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSession2TokensChanged](../android/media/session/MediaSessionManager.OnSession2TokensChangedListener.md))`(`tokens:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Session2Token](../android.media/Session2Token.md)!>`)` Called when the [getSession2Tokens()](MediaSessionManager.md))is changed. |

## Public methods

### onSession2TokensChanged

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSession2TokensChanged(tokens: MutableList<Session2Token!>): Unit
```

Called when the [getSession2Tokens()](MediaSessionManager.md))is changed.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tokens` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Session2Token](../android.media/Session2Token.md)!\>:list of [Session2Token](../android.media/Session2Token.md) This value cannot be`null`. |
