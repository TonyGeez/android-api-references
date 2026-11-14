# RemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteControlClient

Kotlin| [Java](https://developer.android.com/reference/android/media/RemoteControlClient "View this page in Java") 
| --- | --- |

```
open class RemoteControlClient
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#) |

| **This class was deprecated in API level 21.**
|
| Use [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession) instead.

RemoteControlClient enables exposing information meant to be consumed by remote controls capable of displaying metadata, artwork and media transport control buttons.

A remote control client object is associated with a media button event receiver. This event receiver must have been previously registered with [AudioManager.registerMediaButtonEventReceiver(ComponentName)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerMediaButtonEventReceiver(android.content.ComponentName))before the RemoteControlClient can be registered through [AudioManager.registerRemoteControlClient(RemoteControlClient)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteControlClient(android.media.RemoteControlClient)).

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
| open | [MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor) Class used to modify metadata in a [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#) object. |
| abstract | [OnGetPlaybackPositionListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnGetPlaybackPositionListener) Interface definition for a callback to be invoked when the media playback position is queried. |
| abstract | [OnMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener) Interface definition for a callback to be invoked when one of the metadata values has been updated. |
| --- | --- |
| abstract | [OnPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnPlaybackPositionUpdateListener) Interface definition for a callback to be invoked when the media playback position is requested to be updated. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_FAST_FORWARD](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_FAST_FORWARD:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "fast forward" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_NEXT](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_NEXT:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "next" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PAUSE](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PAUSE:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "pause" media key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PLAY](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PLAY:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "play" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PLAY_PAUSE](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PLAY_PAUSE:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "play/pause" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_POSITION_UPDATE](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_POSITION_UPDATE:kotlin.Int) Flag indicating a RemoteControlClient can receive changes in the media playback position through the [OnPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnPlaybackPositionUpdateListener) interface. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PREVIOUS:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "previous" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_RATING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_RATING:kotlin.Int) Flag indicating a RemoteControlClient supports ratings. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_REWIND](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_REWIND:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "rewind" media key. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_KEY_MEDIA_STOP](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_STOP:kotlin.Int) Flag indicating a RemoteControlClient makes use of the "stop" media key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_BUFFERING:kotlin.Int) Playback state of a RemoteControlClient which is buffering data to play before it can start or resume playback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_ERROR](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_ERROR:kotlin.Int) Playback state of a RemoteControlClient which cannot perform any playback related operation because of an internal error. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_FAST_FORWARDING:kotlin.Int) Playback state of a RemoteControlClient which is fast forwarding in the media it is currently playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_PAUSED:kotlin.Int) Playback state of a RemoteControlClient which is paused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_PLAYING:kotlin.Int) Playback state of a RemoteControlClient which is playing media. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_REWINDING:kotlin.Int) Playback state of a RemoteControlClient which is fast rewinding in the media it is currently playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_SKIPPING_BACKWARDS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_SKIPPING_BACKWARDS:kotlin.Int) Playback state of a RemoteControlClient which is skipping back to the previous logical chapter (such as a song in a playlist) in the media it is currently playing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_SKIPPING_FORWARDS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_SKIPPING_FORWARDS:kotlin.Int) Playback state of a RemoteControlClient which is skipping to the next logical chapter (such as a song in a playlist) in the media it is currently playing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PLAYSTATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_STOPPED:kotlin.Int) Playback state of a RemoteControlClient which is stopped. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#RemoteControlClient(android.app.PendingIntent))`(`mediaButtonIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!`)` Class constructor. |
| [RemoteControlClient](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#RemoteControlClient(android.app.PendingIntent,%20android.os.Looper))`(`mediaButtonIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!`, `looper:` ` [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)!`)` Class constructor for a remote control client whose internal event handling happens on a user-provided Looper. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RemoteControlClient.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor)! | [editMetadata](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#editMetadata(kotlin.Boolean))`(`startEmpty:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a [MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor). |
| open [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession)! | [getMediaSession](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#getMediaSession())`()` Get a [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession) associated with this RCC. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setMetadataUpdateListener(android.media.RemoteControlClient.OnMetadataUpdateListener))`(`l:` ` [RemoteControlClient.OnMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener)!`)` Sets the listener to be called whenever the metadata is updated. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnGetPlaybackPositionListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setOnGetPlaybackPositionListener(android.media.RemoteControlClient.OnGetPlaybackPositionListener))`(`l:` ` [RemoteControlClient.OnGetPlaybackPositionListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnGetPlaybackPositionListener)!`)` Sets the listener to be called whenever the media current playback position is needed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackPositionUpdateListener(android.media.RemoteControlClient.OnPlaybackPositionUpdateListener))`(`l:` ` [RemoteControlClient.OnPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnPlaybackPositionUpdateListener)!`)` Sets the listener to be called whenever the media playback position is requested to be updated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackState](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the current playback state. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPlaybackState](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int,%20kotlin.Long,%20kotlin.Float))`(`state:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeInMs:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `playbackSpeed:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the current playback state and the matching media position for the current playback speed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTransportControlFlags](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))`(`transportControlFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the flags for the media transport control buttons that this client supports. |

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

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_FAST_FORWARD](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_FAST_FORWARD:kotlin.Int) 

### FLAG_KEY_MEDIA_NEXT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_NEXT: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "next" media key. 

 Value: 128

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_NEXT](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_NEXT:kotlin.Int) 

### FLAG_KEY_MEDIA_PAUSE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PAUSE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "pause" media key. 

 Value: 16

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_PAUSE](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_PAUSE:kotlin.Int) 

### FLAG_KEY_MEDIA_PLAY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PLAY: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "play" media key. 

 Value: 4

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_PLAY](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_PLAY:kotlin.Int) 

### FLAG_KEY_MEDIA_PLAY_PAUSE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PLAY_PAUSE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "play/pause" media key. 

 Value: 8

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_PLAY_PAUSE](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_PLAY_PAUSE:kotlin.Int) 

### FLAG_KEY_MEDIA_POSITION_UPDATE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_POSITION_UPDATE: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient can receive changes in the media playback position through the [OnPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnPlaybackPositionUpdateListener) interface. This flag must be set in order for components that display the RemoteControlClient information, to display and let the user control media playback position. 

 Value: 256

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [#setOnGetPlaybackPositionListener(OnGetPlaybackPositionListener)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setOnGetPlaybackPositionListener(android.media.RemoteControlClient.OnGetPlaybackPositionListener))
- [#setPlaybackPositionUpdateListener(OnPlaybackPositionUpdateListener)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackPositionUpdateListener(android.media.RemoteControlClient.OnPlaybackPositionUpdateListener)) 

### FLAG_KEY_MEDIA_PREVIOUS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_PREVIOUS: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "previous" media key. 

 Value: 1

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_PREVIOUS](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_PREVIOUS:kotlin.Int) 

### FLAG_KEY_MEDIA_RATING

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_RATING: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient supports ratings. This flag must be set in order for components that display the RemoteControlClient information, to display ratings information, and, if ratings are declared editable (by calling [MediaMetadataEditor.addEditableKey(int)](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#addEditableKey(kotlin.Int))with the [MediaMetadataEditor.RATING_KEY_BY_USER](https://developer.android.com/reference/kotlin/android/media/MediaMetadataEditor#RATING_KEY_BY_USER:kotlin.Int) key), it will enable the user to rate the media, with values being received through the interface set with [setMetadataUpdateListener(android.media.RemoteControlClient.OnMetadataUpdateListener)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setMetadataUpdateListener(android.media.RemoteControlClient.OnMetadataUpdateListener)). 

 Value: 512

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int)) 

### FLAG_KEY_MEDIA_REWIND

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_REWIND: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "rewind" media key. 

 Value: 2

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_REWIND](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_REWIND:kotlin.Int) 

### FLAG_KEY_MEDIA_STOP

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_KEY_MEDIA_STOP: Int
```

**Deprecated:** *Deprecated in Java.*

Flag indicating a RemoteControlClient makes use of the "stop" media key. 

 Value: 32

**See Also**

- [#setTransportControlFlags(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setTransportControlFlags(kotlin.Int))
- [android.view.KeyEvent#KEYCODE_MEDIA_STOP](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_MEDIA_STOP:kotlin.Int) 

### PLAYSTATE_BUFFERING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_BUFFERING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is buffering data to play before it can start or resume playback. 

 Value: 8

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_ERROR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which cannot perform any playback related operation because of an internal error. Examples of such situations are no network connectivity when attempting to stream data from a server, or expired user credentials when trying to play subscription-based content. 

 Value: 9

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_FAST_FORWARDING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_FAST_FORWARDING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is fast forwarding in the media it is currently playing. 

 Value: 4

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_PAUSED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_PAUSED: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is paused. 

 Value: 2

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_PLAYING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_PLAYING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is playing media. 

 Value: 3

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_REWINDING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_REWINDING: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is fast rewinding in the media it is currently playing. 

 Value: 5

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_SKIPPING_BACKWARDS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_SKIPPING_BACKWARDS: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is skipping back to the previous logical chapter (such as a song in a playlist) in the media it is currently playing. 

 Value: 7

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_SKIPPING_FORWARDS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_SKIPPING_FORWARDS: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is skipping to the next logical chapter (such as a song in a playlist) in the media it is currently playing. 

 Value: 6

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int)) 

### PLAYSTATE_STOPPED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYSTATE_STOPPED: Int
```

**Deprecated:** *Deprecated in Java.*

Playback state of a RemoteControlClient which is stopped. 

 Value: 1

**See Also**

- [#setPlaybackState(int)](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#setPlaybackState(kotlin.Int))

## Public constructors

### RemoteControlClient

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RemoteControlClient(mediaButtonIntent: PendingIntent!)
```

Class constructor.

| Parameters ||
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaButtonIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!:The intent that will be sent for the media button events sent by remote controls. This intent needs to have been constructed with the [Intent.ACTION_MEDIA_BUTTON](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BUTTON:kotlin.String) action, and have a component that will handle the intent (set with [Intent.setComponent(ComponentName)](https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName))) registered with [AudioManager.registerMediaButtonEventReceiver(ComponentName)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerMediaButtonEventReceiver(android.content.ComponentName))before this new RemoteControlClient can itself be registered with [AudioManager.registerRemoteControlClient(RemoteControlClient)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteControlClient(android.media.RemoteControlClient)). |

**See Also**

- [android.media.AudioManager#registerMediaButtonEventReceiver(ComponentName)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerMediaButtonEventReceiver(android.content.ComponentName))
- [android.media.AudioManager#registerRemoteControlClient(RemoteControlClient)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteControlClient(android.media.RemoteControlClient)) 

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
| `mediaButtonIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)!:The intent that will be sent for the media button events sent by remote controls. This intent needs to have been constructed with the [Intent.ACTION_MEDIA_BUTTON](https://developer.android.com/reference/kotlin/android/content/Intent.html#ACTION_MEDIA_BUTTON:kotlin.String) action, and have a component that will handle the intent (set with [Intent.setComponent(ComponentName)](https://developer.android.com/reference/kotlin/android/content/Intent.html#setComponent(android.content.ComponentName))) registered with [AudioManager.registerMediaButtonEventReceiver(ComponentName)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerMediaButtonEventReceiver(android.content.ComponentName))before this new RemoteControlClient can itself be registered with [AudioManager.registerRemoteControlClient(RemoteControlClient)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteControlClient(android.media.RemoteControlClient)). |
| `looper` | [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#)!:The Looper running the event loop. |

**See Also**

- [android.media.AudioManager#registerMediaButtonEventReceiver(ComponentName)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerMediaButtonEventReceiver(android.content.ComponentName))
- [android.media.AudioManager#registerRemoteControlClient(RemoteControlClient)](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteControlClient(android.media.RemoteControlClient))

## Public methods

### editMetadata

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun editMetadata(startEmpty: Boolean): RemoteControlClient.MetadataEditor!
```

**Deprecated:** *Deprecated in Java.*

Creates a [MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor).

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `startEmpty` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Set to false if you want the MetadataEditor to contain the metadata that was previously applied to the RemoteControlClient, or true if it is to be created empty. |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| [RemoteControlClient.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor)! | a new MetadataEditor instance. |

### getMediaSession

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMediaSession(): MediaSession!
```

**Deprecated:** *Deprecated in Java.*

Get a [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession) associated with this RCC. It will only have a session while it is registered with [AudioManager.registerRemoteControlClient](https://developer.android.com/reference/kotlin/android/media/AudioManager#registerRemoteControlClient(android.media.RemoteControlClient)). The session returned should not be modified directly by the application but may be used with other APIs that require a session.

| Return ||
|----------------------------------------------------------------------------------------------------|---------------------------------|
| [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession)! | A media session object or null. |

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
| `l` | [RemoteControlClient.OnMetadataUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnMetadataUpdateListener)!:the metadata update listener |

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
| `l` | [RemoteControlClient.OnGetPlaybackPositionListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnGetPlaybackPositionListener)!:the listener to be called to retrieve the playback position |

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
| `l` | [RemoteControlClient.OnPlaybackPositionUpdateListener](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.OnPlaybackPositionUpdateListener)!:the position update listener to be called |

### setPlaybackState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setPlaybackState(state: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the current playback state.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current playback state, one of the following values: [PLAYSTATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_STOPPED:kotlin.Int), [PLAYSTATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_PAUSED:kotlin.Int), [PLAYSTATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_PLAYING:kotlin.Int), [PLAYSTATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_FAST_FORWARDING:kotlin.Int), [PLAYSTATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_REWINDING:kotlin.Int), [PLAYSTATE_SKIPPING_FORWARDS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_SKIPPING_FORWARDS:kotlin.Int), [PLAYSTATE_SKIPPING_BACKWARDS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_SKIPPING_BACKWARDS:kotlin.Int), [PLAYSTATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_BUFFERING:kotlin.Int), [PLAYSTATE_ERROR](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_ERROR:kotlin.Int). |

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
| `state` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The current playback state, one of the following values: [PLAYSTATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_STOPPED:kotlin.Int), [PLAYSTATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_PAUSED:kotlin.Int), [PLAYSTATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_PLAYING:kotlin.Int), [PLAYSTATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_FAST_FORWARDING:kotlin.Int), [PLAYSTATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_REWINDING:kotlin.Int), [PLAYSTATE_SKIPPING_FORWARDS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_SKIPPING_FORWARDS:kotlin.Int), [PLAYSTATE_SKIPPING_BACKWARDS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_SKIPPING_BACKWARDS:kotlin.Int), [PLAYSTATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_BUFFERING:kotlin.Int), [PLAYSTATE_ERROR](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_ERROR:kotlin.Int). |
| `timeInMs` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):a 0 or positive value for the current media position expressed in ms (same unit as for when sending the media duration, if applicable, with [android.media.MediaMetadataRetriever#METADATA_KEY_DURATION](https://developer.android.com/reference/kotlin/android/media/MediaMetadataRetriever#METADATA_KEY_DURATION:kotlin.Int) in the [RemoteControlClient.MetadataEditor](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient.MetadataEditor)). Negative values imply that position is not known (e.g. listening to a live stream of a radio) or not applicable (e.g. when state is [PLAYSTATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_BUFFERING:kotlin.Int) and nothing had played yet). |
| `playbackSpeed` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):a value expressed as a ratio of 1x playback: 1.0f is normal playback, 2.0f is 2x, 0.5f is half-speed, -2.0f is rewind at 2x speed. 0.0f means nothing is playing (e.g. when state is [PLAYSTATE_ERROR](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#PLAYSTATE_ERROR:kotlin.Int)). |
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
| `transportControlFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):A combination of the following flags: [FLAG_KEY_MEDIA_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PREVIOUS:kotlin.Int), [FLAG_KEY_MEDIA_REWIND](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_REWIND:kotlin.Int), [FLAG_KEY_MEDIA_PLAY](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PLAY:kotlin.Int), [FLAG_KEY_MEDIA_PLAY_PAUSE](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PLAY_PAUSE:kotlin.Int), [FLAG_KEY_MEDIA_PAUSE](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_PAUSE:kotlin.Int), [FLAG_KEY_MEDIA_STOP](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_STOP:kotlin.Int), [FLAG_KEY_MEDIA_FAST_FORWARD](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_FAST_FORWARD:kotlin.Int), [FLAG_KEY_MEDIA_NEXT](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_NEXT:kotlin.Int), [FLAG_KEY_MEDIA_POSITION_UPDATE](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_POSITION_UPDATE:kotlin.Int), [FLAG_KEY_MEDIA_RATING](https://developer.android.com/reference/kotlin/android/media/RemoteControlClient#FLAG_KEY_MEDIA_RATING:kotlin.Int). |
