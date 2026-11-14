# MediaSessionManager.OnMediaKeyEventSessionChangedListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnMediaKeyEventSessionChangedListener

Kotlin| [Java](../android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener.md) 
| --- | --- |

```
interface OnMediaKeyEventSessionChangedListener
```

| [android.media.session.MediaSessionManager.OnMediaKeyEventSessionChangedListener](../android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener.md) |

Listener to receive changes in the media key event session, which would receive a media key event unless specified.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMediaKeyEventSessionChanged](../android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener.md))`(`packageName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `sessionToken:` ` [MediaSession.Token](../android/media/session/MediaSession.Token.md)?`)` Called when the media key session is changed to the given media session. |

## Public methods

### onMediaKeyEventSessionChanged

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMediaKeyEventSessionChanged(
    packageName: String, 
    sessionToken: MediaSession.Token?
): Unit
```

Called when the media key session is changed to the given media session. The key event session is the media session which would receive key event by default, unless the caller has specified the target.

The session token can be`null`if the media button session is unset. In that case, packageName will return the package name of the last session's media button receiver, or an empty string if the last session didn't set a media button receiver.

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The package name of the component that will receive the media key event. Can be empty. This value cannot be`null`. |
| `sessionToken` | [MediaSession.Token](../android/media/session/MediaSession.Token.md)?:The media session's token. Can be`null`. |
