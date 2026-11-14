# MediaPlayer.OnErrorListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnErrorListener

Kotlin| [Java](../android/media/MediaPlayer.OnErrorListener.md) 
| --- | --- |

```
interface OnErrorListener
```

| [android.media.MediaPlayer.OnErrorListener](../android/media/MediaPlayer.OnErrorListener.md) |

Interface definition of a callback to be invoked when there has been an error during an asynchronous operation (other errors will throw exceptions at method call time).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onError](../android/media/MediaPlayer.OnErrorListener.md))`(`mp:` ` [MediaPlayer](MediaPlayer.md)!`, `what:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `extra:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to indicate an error. |

## Public methods

### onError

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onError(
    mp: MediaPlayer!, 
    what: Int, 
    extra: Int
): Boolean
```

Called to indicate an error.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mp` | [MediaPlayer](MediaPlayer.md)!:the MediaPlayer the error pertains to |
| `what` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the type of error that has occurred: - [MEDIA_ERROR_UNKNOWN](MediaPlayer.md) - [MEDIA_ERROR_SERVER_DIED](MediaPlayer.md) |
| `extra` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an extra code, specific to the error. Typically implementation dependent. - [MEDIA_ERROR_IO](MediaPlayer.md) - [MEDIA_ERROR_MALFORMED](MediaPlayer.md) - [MEDIA_ERROR_UNSUPPORTED](MediaPlayer.md) - [MEDIA_ERROR_TIMED_OUT](MediaPlayer.md) - `MEDIA_ERROR_SYSTEM (-2147483648)`- low-level system error. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the method handled the error, false if it didn't. Returning false, or not having an OnErrorListener at all, will cause the OnCompletionListener to be called. |
