Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppInteractionSession

```
class AppInteractionSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.app.AppInteractionSession](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#) |

Represents an app interaction session.

The session is used to associate app interactions with a continuous context. For example, a session can be used to keep track of the user consent for the lifetime of the session. Developers could use it to associate with relevant queries from users. For example, in a thread where a user starts asking an agent to perform a task, developers could start a session and keep track of all relevant actions within that session. So that if they need to access the same apps twice during that thread, they don't need to ask permission twice.

The session will be automatically closed when reaching the maximum allowed lifetime. The session owner will be notified of the close event via the `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener#onAppInteractionSessionClosed(android.app.AppInteractionSession,%20kotlin.Int)` with `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_TIMEOUT:kotlin.Int`.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.CreateParams` Parameters to create an `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#`, provided to `https://developer.android.com/reference/kotlin/android/app/AppInteractionManager#createSession(android.app.AppInteractionSession.CreateParams,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |
| abstract | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener` Listener for session lifecycle events. |
| | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.UpdateParams` Parameters to update an `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#`, provided to `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#update(android.app.AppInteractionSession.UpdateParams,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_CALLER_INITIATED:kotlin.Int` The session is closed due to the caller calling `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#close()`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_TIMEOUT:kotlin.Int` The session is closed due to timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#CLOSE_REASON_UNKNOWN:kotlin.Int` Unknown reason for the session to be closed. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#addLifecycleListener(java.util.concurrent.Executor,%20android.app.AppInteractionSession.LifecycleListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener)` Adds a listener to receive session lifecycle events. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#close()()` Closes the session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#removeLifecycleListener(android.app.AppInteractionSession.LifecycleListener)(listener: https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener)` Removes a previously registered session lifecycle listener. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#update(android.app.AppInteractionSession.UpdateParams,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)(params: https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.UpdateParams, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#<https://developer.android.com/reference/kotlin/java/lang/Void.html#!, https://developer.android.com/reference/kotlin/android/app/AppInteractionException!>)` Updates the session with the given `params`. |

## Constants

### CLOSE_REASON_CALLER_INITIATED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CLOSE_REASON_CALLER_INITIATED: Int
```

The session is closed due to the caller calling `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession#close()`.

 Value: 2

### CLOSE_REASON_TIMEOUT

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CLOSE_REASON_TIMEOUT: Int
```

The session is closed due to timeout.

 Value: 1

### CLOSE_REASON_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CLOSE_REASON_UNKNOWN: Int
```

Unknown reason for the session to be closed.

 Value: 0

## Public methods

### addLifecycleListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addLifecycleListener(
    executor: Executor, 
    listener: AppInteractionSession.LifecycleListener
): Unit
```

Adds a listener to receive session lifecycle events.

| Parameters ||
|---|---|
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [AppInteractionSession.LifecycleListener](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener): The `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener` to receive lifecycle events. This value cannot be `null`. |

### close

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Closes the session.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### removeLifecycleListener

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeLifecycleListener(listener: AppInteractionSession.LifecycleListener): Unit
```

Removes a previously registered session lifecycle listener.

| Parameters ||
|---|---|
| `listener` | [AppInteractionSession.LifecycleListener](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener): The `https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.LifecycleListener` that should no longer receive lifecycle events. This value cannot be `null`. |

### update

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun update(
    params: AppInteractionSession.UpdateParams, 
    executor: Executor, 
    callback: OutcomeReceiver<Void!, AppInteractionException!>
): Unit
```

Updates the session with the given `params`.

| Parameters ||
|---|---|
| `params` | [AppInteractionSession.UpdateParams](https://developer.android.com/reference/kotlin/android/app/AppInteractionSession.UpdateParams): The parameters to update the session with. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` on which to invoke the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [OutcomeReceiver](https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#)\< [Void](https://developer.android.com/reference/kotlin/java/lang/Void.html#)!, [AppInteractionException](https://developer.android.com/reference/kotlin/android/app/AppInteractionException)!\>: The `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver.html#` to receive the result of the update. This value cannot be `null`. |
