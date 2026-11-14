Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaSession

```
class MediaSession
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.session.MediaSession](MediaSession.md) |

Allows interaction with media controllers, volume keys, media buttons, and transport controls.

A MediaSession should be created when an app wants to publish media playback information or handle media keys. In general an app only needs one session for all playback, though multiple sessions can be created to provide finer grain controls of media.

Once a session is created the owner of the session may pass its getSessionToken to other processes to allow them to create a MediaController to interact with the session.

To receive commands, media keys, and other events a `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback` must be set with setCallback. To make the session discoverable by other apps, including system apps, setActive must be called.

When an app is finished performing playback it must call release to clean up the session and notify any controllers.

MediaSession objects are thread safe.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback` Receives media buttons, transport controls, and commands from controllers and the system. |
| | `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.QueueItem` A single item that is part of the play queue. |
| | `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` Represents an ongoing session. |
| --- | --- |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#FLAG_HANDLES_MEDIA_BUTTONS:kotlin.Int` Set this flag on the session to indicate that it can handle media button events. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#FLAG_HANDLES_TRANSPORT_CONTROLS:kotlin.Int` Set this flag on the session to indicate that it handles transport control commands through its `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback`. |

| Public constructors ||
|---|---|
| MediaSession Creates a new session. |
| MediaSession Creates a new session. |
| MediaSession Creates a new session with a different session owner from the calling app. |

| Public methods ||
|---|---|
| static [Size](../android.util/Size.md) | getBitmapSizeLimit Gets the media metadata bitmap size limit from a specified context |
| [MediaController](MediaController.md) | getController Get a controller for this session. |
| [MediaSessionManager.RemoteUserInfo](../android/media/session/MediaSessionManager.RemoteUserInfo.md) | getCurrentControllerInfo Gets the controller information who sent the current request. |
| --- | --- |
| [MediaSession.Token](../android/media/session/MediaSession.Token.md) | getSessionToken Retrieve a token object that can be used by apps to create a MediaController for interacting with this session. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isActive Get the current active state of this session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | release This must be called when an app has finished performing playback. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | sendSessionEvent Send a proprietary event to all MediaControllers listening to this Session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setActive Set if this session is currently active. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCallback Set the callback to receive updates for the MediaSession. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setCallback Set the callback to receive updates for the MediaSession. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExtras Set some extras that can be associated with the MediaSession. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setFlags Set any flags for the session. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMediaButtonBroadcastReceiver Set the component name of the manifest-declared `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` class that should receive media buttons. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMediaButtonReceiver Set a pending intent for your media button receiver to allow restarting playback after the session has been stopped. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setMetadata Update the current metadata. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlaybackState Update the current playback state. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlaybackToLocal Set the attributes for this session's audio. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setPlaybackToRemote Configure this session to use remote volume handling. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setQueue Update the list of items in the play queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setQueueTitle Set the title of the play queue. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRatingType Set the style of rating used by this session. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSessionActivity Set an intent for launching UI for this Session. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | finalize Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### FLAG_HANDLES_MEDIA_BUTTONS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HANDLES_MEDIA_BUTTONS: Int
```

**Deprecated:** *This flag is no longer used. All media sessions are expected to handle media button events now.*

Set this flag on the session to indicate that it can handle media button events.

 Value: 1

### FLAG_HANDLES_TRANSPORT_CONTROLS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HANDLES_TRANSPORT_CONTROLS: Int
```

**Deprecated:** *This flag is no longer used. All media sessions are expected to handle transport controls now.*

Set this flag on the session to indicate that it handles transport control commands through its `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback`.

 Value: 2

## Public constructors

### MediaSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaSession(
    context: Context, 
    tag: String)
```

Creates a new session. The session will automatically be registered with the system but will not be published until setActive is called. You must call release when finished with the session.

Note that `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will be thrown if an app creates too many sessions.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context to use to create the session. This value cannot be `null`. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A short name for debugging purposes. This value cannot be `null`. |

### MediaSession

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaSession(
    context: Context, 
    tag: String, 
    sessionInfo: Bundle?)
```

Creates a new session. The session will automatically be registered with the system, but will not be published until setActive is called. You must call release when finished with the session.

The `sessionInfo` can include additional unchanging information about this session. For example, it can include the version of the application, or the list of the custom commands that this session supports.

Note that `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will be thrown if an app creates too many sessions.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context to use to create the session. This value cannot be `null`. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A short name for debugging purposes. This value cannot be `null`. |
| `sessionInfo` | [Bundle](../android.os/Bundle.md)?: A bundle for additional information about this session. Controllers can get this information by calling getSessionInfo. An `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if this contains any non-framework Parcelable objects. This value may be `null`. |
| --- | --- |

### MediaSession

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaSession(
    context: Context, 
    tag: String, 
    sessionInfo: Bundle?, 
    overridePackageName: String)
```

Creates a new session with a different session owner from the calling app. The session will automatically be registered with the system, but will not be published until setActive is called. You must call release when finished with the session.

If the package of caller app is same as that of `overridePackageName`, prefer using MediaSession.

The `sessionInfo` can include additional unchanging information about this session. For example, it can include the version of the application, or the list of the custom commands that this session supports.

Note that `https://developer.android.com/reference/kotlin/java/lang/RuntimeException.html#` will be thrown if an app creates too many sessions. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#OVERRIDE_MEDIA_SESSION_OWNER:kotlin.String`

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context to use to create the session. This value cannot be `null`. |
| `tag` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): A short name for debugging purposes. This value cannot be `null`. |
| `sessionInfo` | [Bundle](../android.os/Bundle.md)?: A bundle for additional information about this session. Controllers can get this information by calling getSessionInfo. An `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` will be thrown if this contains any non-framework Parcelable objects. This value may be `null`. |
| --- | --- |
| `overridePackageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): Package name override for the session. This value cannot be `null`. |

## Public methods

### getBitmapSizeLimit

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getBitmapSizeLimit(context: Context): Size
```

Gets the media metadata bitmap size limit from a specified context

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): The context to get the bitmap size limit from. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/util/Size.html#` | This value cannot be `null`. |

### getController

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getController(): MediaController
```

Get a controller for this session. This is a convenience method to avoid having to cache your own controller in process.

| Return ||
|---|---|
| MediaController | A controller for this session. This value cannot be `null`. |

### getCurrentControllerInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCurrentControllerInfo(): MediaSessionManager.RemoteUserInfo
```

Gets the controller information who sent the current request.

Note: This is only valid while in a request callback, such as onPlay.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/session/MediaSessionManager.RemoteUserInfo` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If this method is called outside of `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Callback` methods. |

**See Also**

- isTrustedForMediaControl

### getSessionToken

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSessionToken(): MediaSession.Token
```

Retrieve a token object that can be used by apps to create a MediaController for interacting with this session. The owner of the session is responsible for deciding how to distribute these tokens.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/session/MediaSession.Token` | A token that can be used to create a MediaController for this session. This value cannot be `null`. |

### isActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isActive(): Boolean
```

Get the current active state of this session.

If false then your session's controller will not be discoverable via getActiveSessions by other apps, including system apps.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the session is active, false otherwise. |

### release

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun release(): Unit
```

This must be called when an app has finished performing playback. If playback is expected to start again shortly the session can be left open, but it must be released if your activity or service is being destroyed.

### sendSessionEvent

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun sendSessionEvent(
    event: String, 
    extras: Bundle?
): Unit
```

Send a proprietary event to all MediaControllers listening to this Session. It's up to the Controller/Session owner to determine the meaning of any events.

| Parameters ||
|---|---|
| `event` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The name of the event to send. This value cannot be `null`. |
| `extras` | [Bundle](../android.os/Bundle.md)?: Any extras included with the event. This value may be `null`. |

### setActive

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setActive(active: Boolean): Unit
```

Set if this session is currently active.

If set to false then your session's controller will not be discoverable via getActiveSessions by other apps, including system apps.

| Parameters ||
|---|---|
| `active` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether this session is active or not. |

### setCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallback(callback: MediaSession.Callback?): Unit
```

Set the callback to receive updates for the MediaSession. This includes media button events and transport controls. The caller's thread will be used to post updates.

Set the callback to null to stop receiving updates.

| Parameters ||
|---|---|
| `callback` | [MediaSession.Callback](../android/media/session/MediaSession.Callback.md)?: The callback object. This value may be `null`. |

### setCallback

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCallback(
    callback: MediaSession.Callback?, 
    handler: Handler?
): Unit
```

Set the callback to receive updates for the MediaSession. This includes media button events and transport controls.

Set the callback to null to stop receiving updates.

| Parameters ||
|---|---|
| `callback` | [MediaSession.Callback](../android/media/session/MediaSession.Callback.md)?: The callback to receive updates on. This value may be `null`. |
| `handler` | [Handler](../android.os/Handler.md)?: The handler that events should be posted on. This value may be `null`. |

### setExtras

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setExtras(extras: Bundle?): Unit
```

Set some extras that can be associated with the MediaSession. No assumptions should be made as to how a MediaController will handle these extras. Keys should be fully qualified (e.g. com.example.MY_EXTRA) to avoid conflicts.

| Parameters ||
|---|---|
| `extras` | [Bundle](../android.os/Bundle.md)?: The extras associated with the MediaSession. This value may be `null`. |

### setFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setFlags(flags: Int): Unit
```

Set any flags for the session.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags to set for this session. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#FLAG_HANDLES_MEDIA_BUTTONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/session/MediaSession#FLAG_HANDLES_TRANSPORT_CONTROLS:kotlin.Int` |

### setMediaButtonBroadcastReceiver

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMediaButtonBroadcastReceiver(broadcastReceiver: ComponentName?): Unit
```

Set the component name of the manifest-declared `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` class that should receive media buttons. This allows restarting playback after the session has been stopped. If your app is started in this way an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BUTTON:kotlin.String` intent will be sent to the broadcast receiver. On apps targeting Android U and above, this will throw an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` if the provided `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` does not resolve to an existing `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#`.

Note: The given `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` should belong to the same package as the context that was given when creating MediaSession.

| Parameters ||
|---|---|
| `broadcastReceiver` | [ComponentName](../android.content/ComponentName.md)?: the component name of the BroadcastReceiver class. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `broadcastReceiver` does not exist on apps targeting Android U and above |

### setMediaButtonReceiver

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMediaButtonReceiver(mbr: PendingIntent?): Unit
```

**Deprecated:** *Use setMediaButtonBroadcastReceiver instead.*

Set a pending intent for your media button receiver to allow restarting playback after the session has been stopped.

If your app is started in this way an `https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BUTTON:kotlin.String` intent will be sent via the pending intent.

The provided `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` must not target an activity. On apps targeting Android V and above, passing an activity pending intent to this method causes an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#`. On apps targeting Android U and below, passing an activity pending intent causes the call to be ignored. Refer to this [guide](https://developer.android.com/guide/components/activities/background-starts) for more information.

The pending intent is recommended to be explicit to follow the security recommendation of getService.

| Parameters ||
|---|---|
| `mbr` | [PendingIntent](../android.app/PendingIntent.md)?: The `https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#` to send the media button event to. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the pending intent targets an activity on apps targeting Android V and above. |

### setMetadata

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setMetadata(metadata: MediaMetadata?): Unit
```

Update the current metadata. New metadata can be created using `https://developer.android.com/reference/kotlin/android/media/MediaMetadata.Builder.html#`. This operation may take time proportional to the size of the bitmap to replace large bitmaps with a scaled down copy.

| Parameters ||
|---|---|
| `metadata` | [MediaMetadata](../android.media/MediaMetadata.md)?: The new metadata. This value may be `null`. |

**See Also**

- putBitmap

### setPlaybackState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPlaybackState(state: PlaybackState?): Unit
```

Update the current playback state.

| Parameters ||
|---|---|
| `state` | [PlaybackState](PlaybackState.md)?: The current state of playback. This value may be `null`. |

### setPlaybackToLocal

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPlaybackToLocal(attributes: AudioAttributes!): Unit
```

Set the attributes for this session's audio. This will affect the system's volume handling for this session. If setPlaybackToRemote was previously called it will stop receiving volume commands and the system will begin sending volume changes to the appropriate stream.

By default sessions use attributes for media.

| Parameters ||
|---|---|
| `attributes` | [AudioAttributes](../android.media/AudioAttributes.md)!: The `https://developer.android.com/reference/kotlin/android/media/AudioAttributes.html#` for this session's audio. |

### setPlaybackToRemote

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPlaybackToRemote(volumeProvider: VolumeProvider): Unit
```

Configure this session to use remote volume handling. This must be called to receive volume button events, otherwise the system will adjust the appropriate stream volume for this session. If setPlaybackToLocal was previously called the system will stop handling volume changes for this session and pass them to the volume provider instead.

| Parameters ||
|---|---|
| `volumeProvider` | [VolumeProvider](../android.media/VolumeProvider.md): The provider that will handle volume changes. May not be null. |

### setQueue

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setQueue(queue: MutableList<MediaSession.QueueItem!>?): Unit
```

Update the list of items in the play queue. It is an ordered list and should contain the current item, and previous or upcoming items if they exist. Specify null if there is no current play queue.

The queue should be of reasonable size. If the play queue is unbounded within your app, it is better to send a reasonable amount in a sliding window instead.

| Parameters ||
|---|---|
| `queue` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [MediaSession.QueueItem](../android/media/session/MediaSession.QueueItem.md)!\>?: A list of items in the play queue. This value may be `null`. |

### setQueueTitle

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setQueueTitle(title: CharSequence?): Unit
```

Set the title of the play queue. The UI should display this title along with the play queue itself. e.g. "Play Queue", "Now Playing", or an album name.

| Parameters ||
|---|---|
| `title` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)?: The title of the play queue. This value may be `null`. |

### setRatingType

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setRatingType(type: Int): Unit
```

Set the style of rating used by this session. Apps trying to set the rating should use this style. Must be one of the following:

- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_NONE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_3_STARS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_4_STARS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_5_STARS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_HEART:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_PERCENTAGE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_THUMB_UP_DOWN:kotlin.Int`

<br />

| Parameters ||
|---|---|
| `type` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_HEART:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_THUMB_UP_DOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_3_STARS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_4_STARS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_5_STARS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/Rating.html#RATING_PERCENTAGE:kotlin.Int` |

### setSessionActivity

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setSessionActivity(pi: PendingIntent?): Unit
```

Set an intent for launching UI for this Session. This can be used as a quick link to an ongoing media screen. The intent should be for an activity that may be started using android.app.Activity#startActivity(android.content.Intent).

| Parameters ||
|---|---|
| `pi` | [PendingIntent](../android.app/PendingIntent.md)?: The intent to launch to show UI for this Session. This value may be `null`. |

## Protected methods

### finalize

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
