# RemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteControlClient

Kotlin| [Java](RemoteControlClient.md) 
| --- | --- |

```
open class RemoteControlClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.RemoteControlClient](RemoteControlClient.md) |

| **This class was deprecated in API level 21.**
|
| Use [MediaSession](../android.media.session/MediaSession.md) instead.

RemoteControlClient enables exposing information meant to be consumed by remote controls capable of displaying metadata, artwork and media transport control buttons.

A remote control client object is associated with a media button event receiver. This event receiver must have been previously registered with [AudioManager.registerMediaButtonEventReceiver(ComponentName)](AudioManager.md))before the RemoteControlClient can be registered through [AudioManager.registerRemoteControlClient(RemoteControlClient)](AudioManager.md)).

Here is an example of creating a RemoteControlClient instance after registering a media button event receiver: 

```kotlin
ComponentName myEventReceiver = new ComponentName(getPackageName(), MyRemoteControlEventReceiver.class.getName());
  AudioManager myAudioManager = (AudioManager) getSystemService(Context.AUDIO_SERVICE);
  myAudioManager.registerMediaButtonEventReceiver(myEventReceiver);
  // build the PendingIntent for the remote control client
  Intent mediaButtonIntent = new Intent(Intent.ACTION_MEDIA_BUTTON);
  mediaButtonIntent.setComponent(myEventReceiver);
  PendingIntent mediaPendingIntent = PendingIntent.getBroadcast(getApplicationContext(), 0, mediaButtonIntent, PendingIntent.FLAG_MUTABLE_UNAUDITED);
  // create and register the remote control client
  RemoteControlClient myRemoteControlClient = new RemoteControlClient(mediaPendingIntent);
  myAudioManager.registerRemoteControlClient(myRemoteControlClient);
```

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md) Class used to modify metadata in a [RemoteControlClient](RemoteControlClient.md) object. |
| abstract | [OnGetPlaybackPositionListener](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md) Interface definition for a callback to be invoked when the media playback position is queried. |
| abstract | [OnMetadataUpdateListener](../android/media/RemoteControlClient.OnMetadataUpdateListener.md) Interface definition for a callback to be invoked when one of the metadata values has been updated. |
| --- | --- |
| abstract | [OnPlaybackPositionUpdateListener](../android/media/RemoteControlClient.OnPlaybackPositionUpdateListener.md) Interface definition for a callback to be invoked when the media playback position is requested to be updated. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_FAST_FORWARD](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "fast forward" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_NEXT](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "next" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PAUSE](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "pause" media key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PLAY](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "play" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PLAY_PAUSE](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "play/pause" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_POSITION_UPDATE](RemoteControlClient.md) Flag indicating a RemoteControlClient can receive changes in the media playback position through the [OnPlaybackPositionUpdateListener](../android/media/RemoteControlClient.OnPlaybackPositionUpdateListener.md) interface. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PREVIOUS](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "previous" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_RATING](RemoteControlClient.md) Flag indicating a RemoteControlClient supports ratings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_REWIND](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "rewind" media key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_STOP](RemoteControlClient.md) Flag indicating a RemoteControlClient makes use of the "stop" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_BUFFERING](RemoteControlClient.md) Playback state of a RemoteControlClient which is buffering data to play before it can start or resume playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_ERROR](RemoteControlClient.md) Playback state of a RemoteControlClient which cannot perform any playback related operation because of an internal error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_FAST_FORWARDING](RemoteControlClient.md) Playback state of a RemoteControlClient which is fast forwarding in the media it is currently playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_PAUSED](RemoteControlClient.md) Playback state of a RemoteControlClient which is paused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_PLAYING](RemoteControlClient.md) Playback state of a RemoteControlClient which is playing media. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_REWINDING](RemoteControlClient.md) Playback state of a RemoteControlClient which is fast rewinding in the media it is currently playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_SKIPPING_BACKWARDS](RemoteControlClient.md) Playback state of a RemoteControlClient which is skipping back to the previous logical chapter (such as a song in a playlist) in the media it is currently playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_SKIPPING_FORWARDS](RemoteControlClient.md) Playback state of a RemoteControlClient which is skipping to the next logical chapter (such as a song in a playlist) in the media it is currently playing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_STOPPED](RemoteControlClient.md) Playback state of a RemoteControlClient which is stopped. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RemoteControlClient](RemoteControlClient.md))`(`mediaButtonIntent:` ` [PendingIntent](../android.app/PendingIntent.md)!`)` Class constructor. |
| [RemoteControlClient](RemoteControlClient.md))`(`mediaButtonIntent:` ` [PendingIntent](../android.app/PendingIntent.md)!`, `looper:` ` [Looper](../android.os/Looper.md)!`)` Class constructor for a remote control client whose internal event handling happens on a user-provided Looper. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RemoteControlClient.MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md)! | [editMetadata](RemoteControlClient.md))`(`startEmpty:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a [MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md). |
| open [MediaSession](../android.media.session/MediaSession.md)! | [getMediaSession](RemoteControlClient.md))`()` Get a [MediaSession](../android.media.session/MediaSession.md) associated with this RCC. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMetadataUpdateListener](RemoteControlClient.md))`(`l:` ` [RemoteControlClient.OnMetadataUpdateListener](../android/media/RemoteControlClient.OnMetadataUpdateListener.md)!`)` Sets the listener to be called whenever the metadata is updated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnGetPlaybackPositionListener](RemoteControlClient.md))`(`l:` ` [RemoteControlClient.OnGetPlaybackPositionListener](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md)!`)` Sets the listener to be called whenever the media current playback position is needed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackPositionUpdateListener](RemoteControlClient.md))`(`l:` ` [RemoteControlClient.OnPlaybackPositionUpdateListener](../android/media/RemoteControlClient.OnPlaybackPositionUpdateListener.md)!`)` Sets the listener to be called whenever the media playback position is requested to be updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackState](RemoteControlClient.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current playback state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackState](RemoteControlClient.md))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeInMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `playbackSpeed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the current playback state and the matching media position for the current playback speed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTransportControlFlags](RemoteControlClient.md))`(`transportControlFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the flags for the media transport control buttons that this client supports. |

## Constants

### FLAG_KEY_MEDIA_FAST_FORWARD

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_FAST_FORWARD: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "fast forward" media key. 

 Value: 64

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_FAST_FORWARD](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_NEXT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_NEXT: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "next" media key. 

 Value: 128

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_NEXT](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_PAUSE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PAUSE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "pause" media key. 

 Value: 16

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_PAUSE](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_PLAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PLAY: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "play" media key. 

 Value: 4

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_PLAY](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_PLAY_PAUSE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PLAY_PAUSE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "play/pause" media key. 

 Value: 8

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_PLAY_PAUSE](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_POSITION_UPDATE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_POSITION_UPDATE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient can receive changes in the media playback position through the [OnPlaybackPositionUpdateListener](../android/media/RemoteControlClient.OnPlaybackPositionUpdateListener.md) interface. This flag must be set in order for components that display the RemoteControlClient information, to display and let the user control media playback position. 

 Value: 256

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [#setOnGetPlaybackPositionListener(OnGetPlaybackPositionListener)](RemoteControlClient.md))
- [#setPlaybackPositionUpdateListener(OnPlaybackPositionUpdateListener)](RemoteControlClient.md)) 

### FLAG_KEY_MEDIA_PREVIOUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PREVIOUS: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "previous" media key. 

 Value: 1

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_PREVIOUS](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_RATING

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_RATING: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient supports ratings. This flag must be set in order for components that display the RemoteControlClient information, to display ratings information, and, if ratings are declared editable (by calling [MediaMetadataEditor.addEditableKey(int)](MediaMetadataEditor.md))with the [MediaMetadataEditor.RATING_KEY_BY_USER](MediaMetadataEditor.md) key), it will enable the user to rate the media, with values being received through the interface set with [setMetadataUpdateListener(android.media.RemoteControlClient.OnMetadataUpdateListener)](RemoteControlClient.md)). 

 Value: 512

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md)) 

### FLAG_KEY_MEDIA_REWIND

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_REWIND: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "rewind" media key. 

 Value: 2

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_REWIND](../android.view/KeyEvent.md) 

### FLAG_KEY_MEDIA_STOP

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_STOP: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "stop" media key. 

 Value: 32

**See Also**

- [#setTransportControlFlags(int)](RemoteControlClient.md))
- [android.view.KeyEvent#KEYCODE_MEDIA_STOP](../android.view/KeyEvent.md) 

### PLAYSTATE_BUFFERING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_BUFFERING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is buffering data to play before it can start or resume playback. 

 Value: 8

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_ERROR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which cannot perform any playback related operation because of an internal error. Examples of such situations are no network connectivity when attempting to stream data from a server, or expired user credentials when trying to play subscription-based content. 

 Value: 9

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_FAST_FORWARDING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_FAST_FORWARDING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is fast forwarding in the media it is currently playing. 

 Value: 4

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_PAUSED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_PAUSED: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is paused. 

 Value: 2

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_PLAYING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_PLAYING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is playing media. 

 Value: 3

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_REWINDING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_REWINDING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is fast rewinding in the media it is currently playing. 

 Value: 5

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_SKIPPING_BACKWARDS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_SKIPPING_BACKWARDS: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is skipping back to the previous logical chapter (such as a song in a playlist) in the media it is currently playing. 

 Value: 7

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_SKIPPING_FORWARDS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_SKIPPING_FORWARDS: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is skipping to the next logical chapter (such as a song in a playlist) in the media it is currently playing. 

 Value: 6

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md)) 

### PLAYSTATE_STOPPED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_STOPPED: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is stopped. 

 Value: 1

**See Also**

- [#setPlaybackState(int)](RemoteControlClient.md))

## Public constructors

### RemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RemoteControlClient(mediaButtonIntent: PendingIntent!)
```

Class constructor.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaButtonIntent` | [PendingIntent](../android.app/PendingIntent.md)!:The intent that will be sent for the media button events sent by remote controls. This intent needs to have been constructed with the [Intent.ACTION_MEDIA_BUTTON](../android.content/Intent.md) action, and have a component that will handle the intent (set with [Intent.setComponent(ComponentName)](../android.content/Intent.md))) registered with [AudioManager.registerMediaButtonEventReceiver(ComponentName)](AudioManager.md))before this new RemoteControlClient can itself be registered with [AudioManager.registerRemoteControlClient(RemoteControlClient)](AudioManager.md)). |

**See Also**

- [android.media.AudioManager#registerMediaButtonEventReceiver(ComponentName)](AudioManager.md))
- [android.media.AudioManager#registerRemoteControlClient(RemoteControlClient)](AudioManager.md)) 

### RemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RemoteControlClient(
    mediaButtonIntent: PendingIntent!, 
    looper: Looper!)
```

Class constructor for a remote control client whose internal event handling happens on a user-provided Looper.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaButtonIntent` | [PendingIntent](../android.app/PendingIntent.md)!:The intent that will be sent for the media button events sent by remote controls. This intent needs to have been constructed with the [Intent.ACTION_MEDIA_BUTTON](../android.content/Intent.md) action, and have a component that will handle the intent (set with [Intent.setComponent(ComponentName)](../android.content/Intent.md))) registered with [AudioManager.registerMediaButtonEventReceiver(ComponentName)](AudioManager.md))before this new RemoteControlClient can itself be registered with [AudioManager.registerRemoteControlClient(RemoteControlClient)](AudioManager.md)). |
| `looper` | [Looper](../android.os/Looper.md)!:The Looper running the event loop. |

**See Also**

- [android.media.AudioManager#registerMediaButtonEventReceiver(ComponentName)](AudioManager.md))
- [android.media.AudioManager#registerRemoteControlClient(RemoteControlClient)](AudioManager.md))

## Public methods

### editMetadata

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun editMetadata(startEmpty: Boolean): RemoteControlClient.MetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Creates a [MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md).

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startEmpty` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to false if you want the MetadataEditor to contain the metadata that was previously applied to the RemoteControlClient, or true if it is to be created empty. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [RemoteControlClient.MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md)! | a new MetadataEditor instance. |

### getMediaSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMediaSession(): MediaSession!
```

**Deprecated:** *Deprecated in Java.*

Get a [MediaSession](../android.media.session/MediaSession.md) associated with this RCC. It will only have a session while it is registered with [AudioManager.registerRemoteControlClient](AudioManager.md)). The session returned should not be modified directly by the application but may be used with other APIs that require a session.

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------------|
| [MediaSession](../android.media.session/MediaSession.md)! | A media session object or null. |

### setMetadataUpdateListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMetadataUpdateListener(l: RemoteControlClient.OnMetadataUpdateListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to be called whenever the metadata is updated. New metadata values will be received in the same thread as the one in which RemoteControlClient was created.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [RemoteControlClient.OnMetadataUpdateListener](../android/media/RemoteControlClient.OnMetadataUpdateListener.md)!:the metadata update listener |

### setOnGetPlaybackPositionListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setOnGetPlaybackPositionListener(l: RemoteControlClient.OnGetPlaybackPositionListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to be called whenever the media current playback position is needed. Queries will be received in the same thread as the one in which RemoteControlClient was created.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [RemoteControlClient.OnGetPlaybackPositionListener](../android/media/RemoteControlClient.OnGetPlaybackPositionListener.md)!:the listener to be called to retrieve the playback position |

### setPlaybackPositionUpdateListener

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlaybackPositionUpdateListener(l: RemoteControlClient.OnPlaybackPositionUpdateListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the listener to be called whenever the media playback position is requested to be updated. Notifications will be received in the same thread as the one in which RemoteControlClient was created.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `l` | [RemoteControlClient.OnPlaybackPositionUpdateListener](../android/media/RemoteControlClient.OnPlaybackPositionUpdateListener.md)!:the position update listener to be called |

### setPlaybackState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlaybackState(state: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current playback state.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current playback state, one of the following values: [PLAYSTATE_STOPPED](RemoteControlClient.md), [PLAYSTATE_PAUSED](RemoteControlClient.md), [PLAYSTATE_PLAYING](RemoteControlClient.md), [PLAYSTATE_FAST_FORWARDING](RemoteControlClient.md), [PLAYSTATE_REWINDING](RemoteControlClient.md), [PLAYSTATE_SKIPPING_FORWARDS](RemoteControlClient.md), [PLAYSTATE_SKIPPING_BACKWARDS](RemoteControlClient.md), [PLAYSTATE_BUFFERING](RemoteControlClient.md), [PLAYSTATE_ERROR](RemoteControlClient.md). |

### setPlaybackState

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlaybackState(
    state: Int, 
    timeInMs: Long, 
    playbackSpeed: Float
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current playback state and the matching media position for the current playback speed.

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current playback state, one of the following values: [PLAYSTATE_STOPPED](RemoteControlClient.md), [PLAYSTATE_PAUSED](RemoteControlClient.md), [PLAYSTATE_PLAYING](RemoteControlClient.md), [PLAYSTATE_FAST_FORWARDING](RemoteControlClient.md), [PLAYSTATE_REWINDING](RemoteControlClient.md), [PLAYSTATE_SKIPPING_FORWARDS](RemoteControlClient.md), [PLAYSTATE_SKIPPING_BACKWARDS](RemoteControlClient.md), [PLAYSTATE_BUFFERING](RemoteControlClient.md), [PLAYSTATE_ERROR](RemoteControlClient.md). |
| `timeInMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a 0 or positive value for the current media position expressed in ms (same unit as for when sending the media duration, if applicable, with [android.media.MediaMetadataRetriever#METADATA_KEY_DURATION](MediaMetadataRetriever.md) in the [RemoteControlClient.MetadataEditor](../android/media/RemoteControlClient.MetadataEditor.md)). Negative values imply that position is not known (e.g. listening to a live stream of a radio) or not applicable (e.g. when state is [PLAYSTATE_BUFFERING](RemoteControlClient.md) and nothing had played yet). |
| `playbackSpeed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a value expressed as a ratio of 1x playback: 1.0f is normal playback, 2.0f is 2x, 0.5f is half-speed, -2.0f is rewind at 2x speed. 0.0f means nothing is playing (e.g. when state is [PLAYSTATE_ERROR](RemoteControlClient.md)). |
| --- | --- |

### setTransportControlFlags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setTransportControlFlags(transportControlFlags: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the flags for the media transport control buttons that this client supports.

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transportControlFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of the following flags: [FLAG_KEY_MEDIA_PREVIOUS](RemoteControlClient.md), [FLAG_KEY_MEDIA_REWIND](RemoteControlClient.md), [FLAG_KEY_MEDIA_PLAY](RemoteControlClient.md), [FLAG_KEY_MEDIA_PLAY_PAUSE](RemoteControlClient.md), [FLAG_KEY_MEDIA_PAUSE](RemoteControlClient.md), [FLAG_KEY_MEDIA_STOP](RemoteControlClient.md), [FLAG_KEY_MEDIA_FAST_FORWARD](RemoteControlClient.md), [FLAG_KEY_MEDIA_NEXT](RemoteControlClient.md), [FLAG_KEY_MEDIA_POSITION_UPDATE](RemoteControlClient.md), [FLAG_KEY_MEDIA_RATING](RemoteControlClient.md). |
