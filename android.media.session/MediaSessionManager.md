Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaSessionManager

```
class MediaSessionManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.session.MediaSessionManager](MediaSessionManager.md) |

Provides support for interacting with `https://developer.android.com/reference/kotlin/android/media/session/MediaSession` that applications have published to express their ongoing media playback state.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener` Listens for changes to the list of active sessions. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener` Listener to receive changes in the media key event session, which would receive a media key event unless specified. |
| abstract | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener` Listens for changes to the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()`. |
| --- | --- |
| | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.RemoteUserInfo` Information of a remote user of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession` or `https://developer.android.com/reference/kotlin/android/service/media/MediaBrowserService.html#`. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnActiveSessionsChangedListener(android.media.session.MediaSessionManager.OnActiveSessionsChangedListener,%20android.content.ComponentName)(sessionListener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener, notificationListener: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?)` Add a listener to be notified when the list of active sessions changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnActiveSessionsChangedListener(android.media.session.MediaSessionManager.OnActiveSessionsChangedListener,%20android.content.ComponentName,%20android.os.Handler)(sessionListener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener, notificationListener: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#?)` Add a listener to be notified when the list of active sessions changes. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnActiveSessionsForPackageChangedListener(kotlin.String,%20java.util.concurrent.Executor,%20android.content.ComponentName,%20android.media.session.MediaSessionManager.OnActiveSessionsChangedListener)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, notificationListener: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?, sessionListener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener)` Add a listener to be notified when the list of active controllers changes for the `packageName`, as returned by #getActiveSessionsForPackage. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnActiveSessionsForPackageChangedListener(kotlin.String,%20java.util.concurrent.Executor,%20android.media.session.MediaSessionManager.OnActiveSessionsChangedListener)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, sessionListener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener)` Add a listener to be notified when the list of active sessions changes for the `packageName`, as returned by #getActiveSessionsForPackage. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnMediaKeyEventSessionChangedListener(java.util.concurrent.Executor,%20android.media.session.MediaSessionManager.OnMediaKeyEventSessionChangedListener)(executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, listener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener)` Add a listener to be notified when the media key session is changed. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnSession2TokensChangedListener(android.media.session.MediaSessionManager.OnSession2TokensChangedListener)(listener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener)` Adds a listener to be notified when the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()` changes. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#addOnSession2TokensChangedListener(android.media.session.MediaSessionManager.OnSession2TokensChangedListener,%20android.os.Handler)(listener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#)` Adds a listener to be notified when the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()` changes. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaController](MediaController.md)!\> | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getActiveSessions(android.content.ComponentName)(notificationListener: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?)` Get a list of controllers for all active sessions. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaSession.Token](../android/media/session/MediaSession.Token.md)!\> | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getActiveSessionsForPackage(kotlin.String)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` Get a list of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` for all active sessions for the `packageName`. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaSession.Token](../android/media/session/MediaSession.Token.md)!\> | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getActiveSessionsForPackage(kotlin.String,%20android.content.ComponentName)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, notificationListener: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#?)` Get a list of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` for all active sessions for the `packageName`. |
| [MediaSession.Token](../android/media/session/MediaSession.Token.md)? | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getMediaKeyEventSession()()` Gets the media key event session, which would receive a media key event unless specified. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getMediaKeyEventSessionPackageName()()` Gets the package name of the media key event session. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Session2Token](../android.media/Session2Token.md)!\> | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()()` Gets a list of `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#` with type `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#TYPE_SESSION:kotlin.Int` for the current user. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#isTrustedForMediaControl(android.media.session.MediaSessionManager.RemoteUserInfo)(userInfo: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.RemoteUserInfo)` Checks whether the remote user is a trusted app. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#notifySession2Created(android.media.Session2Token)(token: https://developer.android.com/reference/kotlin/android/media/Session2Token.html#)` Notifies that a new `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#` with type `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#TYPE_SESSION:kotlin.Int` is created. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#removeOnActiveSessionsChangedListener(android.media.session.MediaSessionManager.OnActiveSessionsChangedListener)(sessionListener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener)` Stop receiving active sessions updates on the specified listener. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#removeOnActiveSessionsForPackageChangedListener(android.media.session.MediaSessionManager.OnActiveSessionsChangedListener)(sessionListener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnActiveSessionsChangedListener)` Stop receiving active sessions updates on the specified listener for package. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#removeOnMediaKeyEventSessionChangedListener(android.media.session.MediaSessionManager.OnMediaKeyEventSessionChangedListener)(listener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener)` Stop receiving updates on media key event session change on the specified listener. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#removeOnSession2TokensChangedListener(android.media.session.MediaSessionManager.OnSession2TokensChangedListener)(listener: https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener)` Removes the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener` to stop receiving session token updates. |

## Public methods

### addOnActiveSessionsChangedListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnActiveSessionsChangedListener(
    sessionListener: MediaSessionManager.OnActiveSessionsChangedListener, 
    notificationListener: ComponentName?
): Unit
```

Add a listener to be notified when the list of active sessions changes.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app. You may also retrieve this list if your app is an enabled notificationlistener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs, in which case you must pass the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of your enabled listener.

| Parameters ||
|---|---|
| `sessionListener` | [MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md): The listener to add. This value cannot be `null`. |
| `notificationListener` | [ComponentName](../android.content/ComponentName.md)?: The enabled notification listener component. May be null. |

### addOnActiveSessionsChangedListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnActiveSessionsChangedListener(
    sessionListener: MediaSessionManager.OnActiveSessionsChangedListener, 
    notificationListener: ComponentName?, 
    handler: Handler?
): Unit
```

Add a listener to be notified when the list of active sessions changes.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app. You may also retrieve this list if your app is an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs, in which case you must pass the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of your enabled listener. Updates will be posted to the handler specified or to the caller's thread if the handler is null.

| Parameters ||
|---|---|
| `sessionListener` | [MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md): The listener to add. This value cannot be `null`. |
| `notificationListener` | [ComponentName](../android.content/ComponentName.md)?: The enabled notification listener component. May be null. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler to post events to. This value may be `null`. |
| --- | --- |

### addOnActiveSessionsForPackageChangedListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnActiveSessionsForPackageChangedListener(
    packageName: String, 
    executor: Executor, 
    notificationListener: ComponentName?, 
    sessionListener: MediaSessionManager.OnActiveSessionsChangedListener
): Unit
```

Add a listener to be notified when the list of active controllers changes for the `packageName`, as returned by #getActiveSessionsForPackage. The registered listener can be removed by calling `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#removeOnActiveSessionsForPackageChangedListener(android.media.session.MediaSessionManager.OnActiveSessionsChangedListener)`.

If the `packageName` is different from the `https://developer.android.com/reference/kotlin/android/content/Context.html#getPackageName()`, it requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app. You may also attach a listener if your app is an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs, in which case you must pass the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of your enabled listener.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name filter to be applied for the listener. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor to be used for sending events to listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `notificationListener` | [ComponentName](../android.content/ComponentName.md)?: The enabled notification listener component. May be null. |
| --- | --- |
| `sessionListener` | [MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md): The listener to add. This value cannot be `null`. |

### addOnActiveSessionsForPackageChangedListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnActiveSessionsForPackageChangedListener(
    packageName: String, 
    executor: Executor, 
    sessionListener: MediaSessionManager.OnActiveSessionsChangedListener
): Unit
```

Add a listener to be notified when the list of active sessions changes for the `packageName`, as returned by #getActiveSessionsForPackage. The registered listener can be removed by calling `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#removeOnActiveSessionsForPackageChangedListener(android.media.session.MediaSessionManager.OnActiveSessionsChangedListener)`.

If the `packageName` is different from the `https://developer.android.com/reference/kotlin/android/content/Context.html#getPackageName()`, it requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package name filter to be applied for the listener. This value cannot be `null`. |
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor to be used for sending events to listener. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `sessionListener` | [MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md): The listener to add. This value cannot be `null`. |
| --- | --- |

### addOnMediaKeyEventSessionChangedListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnMediaKeyEventSessionChangedListener(
    executor: Executor, 
    listener: MediaSessionManager.OnMediaKeyEventSessionChangedListener
): Unit
```

Add a listener to be notified when the media key session is changed.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app, or the app has an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs. If none of them applies, it will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which the listener should be invoked. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `listener` | [MediaSessionManager.OnMediaKeyEventSessionChangedListener](../android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener.md): A `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener`. This value cannot be `null`. |

### addOnSession2TokensChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnSession2TokensChangedListener(listener: MediaSessionManager.OnSession2TokensChangedListener): Unit
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#` is deprecated.*

Adds a listener to be notified when the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()` changes.

This API is not generally intended for third party application developers. Apps wanting media session functionality should use the [AndroidX Media3 Session Library](../androidx/media3/session/_package.md).

| Parameters ||
|---|---|
| `listener` | [MediaSessionManager.OnSession2TokensChangedListener](../android/media/session/MediaSessionManager.OnSession2TokensChangedListener.md): The listener to add. This value cannot be `null`. |

### addOnSession2TokensChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun addOnSession2TokensChangedListener(
    listener: MediaSessionManager.OnSession2TokensChangedListener, 
    handler: Handler
): Unit
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#` is deprecated.*

Adds a listener to be notified when the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getSession2Tokens()` changes.

This API is not generally intended for third party application developers. Apps wanting media session functionality should use the [AndroidX Media3 Session Library](../androidx/media3/session/_package.md).

| Parameters ||
|---|---|
| `listener` | [MediaSessionManager.OnSession2TokensChangedListener](../android/media/session/MediaSessionManager.OnSession2TokensChangedListener.md): The listener to add. This value cannot be `null`. |
| `handler` | [Handler](../android.os/Handler.md): The handler to call listener on. This value cannot be `null`. |

### getActiveSessions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActiveSessions(notificationListener: ComponentName?): MutableList<MediaController!>
```

Get a list of controllers for all active sessions. The controllers will be provided in priority order with the most important controller at index 0.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app. You may also retrieve this list if your app is an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs, in which case you must pass the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of your enabled listener.

| Parameters ||
|---|---|
| `notificationListener` | [ComponentName](../android.content/ComponentName.md)?: The enabled notification listener component. May be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/session/MediaController!>` | A list of controllers for active sessions. This value cannot be `null`. |

### getActiveSessionsForPackage

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActiveSessionsForPackage(packageName: String): MutableList<MediaSession.Token!>
```

Get a list of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` for all active sessions for the `packageName`. The tokens will be provided in priority order with the most important controller at index 0.

If the `packageName` is provided and is different from `https://developer.android.com/reference/kotlin/android/content/Context.html#getPackageName()`, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package name of the application for which tokens should be fetched. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token!>` | A list of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` for active sessions of the calling application. This value cannot be `null`. |

### getActiveSessionsForPackage

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getActiveSessionsForPackage(
    packageName: String, 
    notificationListener: ComponentName?
): MutableList<MediaSession.Token!>
```

Get a list of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` for all active sessions for the `packageName`. The tokens will be provided in priority order with the most important controller at index 0.

If the `packageName` is provided and is different from `https://developer.android.com/reference/kotlin/android/content/Context.html#getPackageName()`, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app. You may also retrieve this list if your app is an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs, in which case you must pass the `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` of your enabled listener. If none of them applies, it will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package name of the application for which tokens should be fetched. This value cannot be `null`. |
| `notificationListener` | [ComponentName](../android.content/ComponentName.md)?: The enabled notification listener component. May be null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token!>` | A list of controllers for active sessions of the calling application. This value cannot be `null`. |

### getMediaKeyEventSession

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMediaKeyEventSession(): MediaSession.Token?
```

Gets the media key event session, which would receive a media key event unless specified.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app, or the app has an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs. If none of them applies, it will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token?` | The media key event session, which would receive key events by default, unless the caller has specified the target. Can be `null`. |

### getMediaKeyEventSessionPackageName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMediaKeyEventSessionPackageName(): String
```

Gets the package name of the media key event session.

This requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission be held by the calling app, or the app has an enabled notification listener using the `https://developer.android.com/reference/kotlin/android/service/notification/NotificationListenerService.html#` APIs. If none of them applies, it will throw a `https://developer.android.com/reference/kotlin/java/lang/SecurityException.html#`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | The package name of the media key event session or the last session's media button receiver if the media key event session is `null`. Returns an empty string if neither of them exists. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager#getMediaKeyEventSession()`

### getSession2Tokens

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSession2Tokens(): MutableList<Session2Token!>
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#` is deprecated.*

Gets a list of `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#` with type `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#TYPE_SESSION:kotlin.Int` for the current user.

Although this API can be used without any restriction, each session owners can accept or reject your uses of `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#`.

This API is not generally intended for third party application developers. Apps wanting media session functionality should use the [AndroidX Media3 Session Library](../androidx/media3/session/_package.md).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/media/Session2Token.html#!>` | A list of `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#`. This value cannot be `null`. |

### isTrustedForMediaControl

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isTrustedForMediaControl(userInfo: MediaSessionManager.RemoteUserInfo): Boolean
```

Checks whether the remote user is a trusted app.

An app is trusted if the app holds the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#MEDIA_CONTENT_CONTROL:kotlin.String` permission or has an enabled notification listener.

| Parameters ||
|---|---|
| `userInfo` | [MediaSessionManager.RemoteUserInfo](../android/media/session/MediaSessionManager.RemoteUserInfo.md): The remote user info from either `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#getCurrentControllerInfo()` or `https://developer.android.com/reference/kotlin/android/service/media/MediaBrowserService.html#getCurrentBrowserInfo()`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the remote user is trusted and its package name matches with the UID. `false` otherwise. |

### notifySession2Created

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun notifySession2Created(token: Session2Token): Unit
```

**Deprecated:** *Don't use this method. A new media session is notified automatically.*

Notifies that a new `https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#` with type `https://developer.android.com/reference/kotlin/android/media/Session2Token.html#TYPE_SESSION:kotlin.Int` is created.

Do not use this API directly, but create a new instance through the `https://developer.android.com/reference/kotlin/android/media/MediaSession2.Builder.html#` instead.

| Parameters ||
|---|---|
| `token` | [Session2Token](../android.media/Session2Token.md): newly created session2 token. This value cannot be `null`. |

### removeOnActiveSessionsChangedListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnActiveSessionsChangedListener(sessionListener: MediaSessionManager.OnActiveSessionsChangedListener): Unit
```

Stop receiving active sessions updates on the specified listener.

| Parameters ||
|---|---|
| `sessionListener` | [MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md): The listener to remove. This value cannot be `null`. |

### removeOnActiveSessionsForPackageChangedListener

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnActiveSessionsForPackageChangedListener(sessionListener: MediaSessionManager.OnActiveSessionsChangedListener): Unit
```

Stop receiving active sessions updates on the specified listener for package.

| Parameters ||
|---|---|
| `sessionListener` | [MediaSessionManager.OnActiveSessionsChangedListener](../android/media/session/MediaSessionManager.OnActiveSessionsChangedListener.md): The listener to remove. This value cannot be `null`. |

### removeOnMediaKeyEventSessionChangedListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnMediaKeyEventSessionChangedListener(listener: MediaSessionManager.OnMediaKeyEventSessionChangedListener): Unit
```

Stop receiving updates on media key event session change on the specified listener.

| Parameters ||
|---|---|
| `listener` | [MediaSessionManager.OnMediaKeyEventSessionChangedListener](../android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener.md): A `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnMediaKeyEventSessionChangedListener`. This value cannot be `null`. |

### removeOnSession2TokensChangedListener

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun removeOnSession2TokensChangedListener(listener: MediaSessionManager.OnSession2TokensChangedListener): Unit
```

**Deprecated:** *`https://developer.android.com/reference/kotlin/android/media/MediaSession2.html#` is deprecated.*

Removes the `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.OnSession2TokensChangedListener` to stop receiving session token updates.

This API is not generally intended for third party application developers. Apps wanting media session functionality should use the [AndroidX Media3 Session Library](../androidx/media3/session/_package.md).

| Parameters ||
|---|---|
| `listener` | [MediaSessionManager.OnSession2TokensChangedListener](../android/media/session/MediaSessionManager.OnSession2TokensChangedListener.md): The listener to remove. This value cannot be `null`. |
