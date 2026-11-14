Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LifecycleListener

```
interface LifecycleListener
```

| [android.app.AppInteractionSession.LifecycleListener](../android/app/AppInteractionSession.LifecycleListener.md) |

Listener for session lifecycle events.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | onAppInteractionSessionClosed Called when the session is closed. |

## Public methods

### onAppInteractionSessionClosed

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onAppInteractionSessionClosed(
    session: AppInteractionSession, 
    reason: Int
): Unit
```

Called when the session is closed.

A session may be closed explicitly via close or implicitly by the system when the session reaches its maximum duration timeout.

If the session is already closed, the listener will be invoked immediately.

| Parameters ||
|---|---|
| `session` | [AppInteractionSession](AppInteractionSession.md): The session that is closed. This value cannot be `null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The reason why the session is closed. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_TIMEOUT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_CALLER_INITIATED:kotlin.Int` |
