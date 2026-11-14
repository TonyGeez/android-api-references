# PlaybackState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PlaybackState

Kotlin| [Java](https://developer.android.com/reference/android/media/session/PlaybackState "View this page in Java") 
| --- | --- |

```
class PlaybackState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.session.PlaybackState](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#) |

Playback state for a [MediaSession](https://developer.android.com/reference/kotlin/android/media/session/MediaSession). This includes a state like [PlaybackState.STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PLAYING:kotlin.Int), the current playback position, and the current control capabilities.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder) Builder for [PlaybackState](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#) objects. |
| | [CustomAction](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.CustomAction) [CustomActions](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.CustomAction) can be used to extend the capabilities of the standard transport controls by exposing app specific actions to [MediaControllers](https://developer.android.com/reference/kotlin/android/media/session/MediaController). |

| Constants ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_FAST_FORWARD](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_FAST_FORWARD:kotlin.Long) Indicates this session supports the fast forward command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PAUSE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PAUSE:kotlin.Long) Indicates this session supports the pause command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PLAY](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY:kotlin.Long) Indicates this session supports the play command. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PLAY_FROM_MEDIA_ID](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_MEDIA_ID:kotlin.Long) Indicates this session supports the play from media id command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PLAY_FROM_SEARCH](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_SEARCH:kotlin.Long) Indicates this session supports the play from search command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PLAY_FROM_URI](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_URI:kotlin.Long) Indicates this session supports the play from URI command. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PLAY_PAUSE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_PAUSE:kotlin.Long) Indicates this session supports the play/pause toggle command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PREPARE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE:kotlin.Long) Indicates this session supports the prepare command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PREPARE_FROM_MEDIA_ID](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_MEDIA_ID:kotlin.Long) Indicates this session supports the prepare from media id command. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PREPARE_FROM_SEARCH](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_SEARCH:kotlin.Long) Indicates this session supports the prepare from search command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_PREPARE_FROM_URI](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_URI:kotlin.Long) Indicates this session supports the prepare from URI command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_REWIND](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_REWIND:kotlin.Long) Indicates this session supports the rewind command. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_SEEK_TO](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SEEK_TO:kotlin.Long) Indicates this session supports the seek to command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_SET_PLAYBACK_SPEED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SET_PLAYBACK_SPEED:kotlin.Long) Indicates this session supports the set playback speed command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_SET_RATING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SET_RATING:kotlin.Long) Indicates this session supports the set rating command. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_SKIP_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_NEXT:kotlin.Long) Indicates this session supports the next command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_SKIP_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_PREVIOUS:kotlin.Long) Indicates this session supports the previous command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_SKIP_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_QUEUE_ITEM:kotlin.Long) Indicates this session supports the skip to queue item command. |
| --- | --- |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [ACTION_STOP](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_STOP:kotlin.Long) Indicates this session supports the stop command. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [PLAYBACK_POSITION_UNKNOWN](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#PLAYBACK_POSITION_UNKNOWN:kotlin.Long) Use this value for the position to indicate the position is not known. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_BUFFERING:kotlin.Int) State indicating this item is currently buffering and will begin playing when enough data has buffered. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_CONNECTING:kotlin.Int) State indicating the class doing playback is currently connecting to a new destination. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_ERROR:kotlin.Int) State indicating this item is currently in an error state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_FAST_FORWARDING:kotlin.Int) State indicating this item is currently fast forwarding. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_NONE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_NONE:kotlin.Int) This is the default playback state and indicates that no media has been added yet, or the performer has been reset and has no content to play. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PAUSED:kotlin.Int) State indicating this item is currently paused. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PLAYING:kotlin.Int) State indicating this item is currently playing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_REWINDING:kotlin.Int) State indicating this item is currently rewinding. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SKIPPING_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_NEXT:kotlin.Int) State indicating the player is currently skipping to the next item. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SKIPPING_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_PREVIOUS:kotlin.Int) State indicating the player is currently skipping to the previous item. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_SKIPPING_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_QUEUE_ITEM:kotlin.Int) State indicating the player is currently skipping to a specific item in the queue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_STOPPED:kotlin.Int) State indicating this item is currently stopped. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#describeContents())`()` <br /> |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActions](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getActions())`()` Get the current actions available on this session. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getActiveQueueItemId](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getActiveQueueItemId())`()` Get the id of the currently active item in the queue. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getBufferedPosition](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getBufferedPosition())`()` Get the current buffered position in ms. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PlaybackState.CustomAction](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.CustomAction)!\>! | [getCustomActions](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getCustomActions())`()` Get the list of custom actions. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getErrorMessage](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getErrorMessage())`()` Get a user readable error message. |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | [getExtras](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getExtras())`()` Get any custom extras that were set on this playback state. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLastPositionUpdateTime](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getLastPositionUpdateTime())`()` Get the elapsed real time at which position was last updated. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getPlaybackSpeed](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getPlaybackSpeed())`()` Get the current playback speed as a multiple of normal playback. |
| --- | --- |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getPosition](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getPosition())`()` Get the current playback position in ms. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getState](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#getState())`()` Get the current state of playback. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isActive](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#isActive())`()` Returns whether this is considered as an active playback state. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PlaybackState](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ACTION_FAST_FORWARD

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_FAST_FORWARD: Long
```

Indicates this session supports the fast forward command. 

 Value: 64L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PAUSE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PAUSE: Long
```

Indicates this session supports the pause command. 

 Value: 2L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PLAY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PLAY: Long
```

Indicates this session supports the play command. 

 Value: 4L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PLAY_FROM_MEDIA_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PLAY_FROM_MEDIA_ID: Long
```

Indicates this session supports the play from media id command. 

 Value: 1024L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PLAY_FROM_SEARCH

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PLAY_FROM_SEARCH: Long
```

Indicates this session supports the play from search command. 

 Value: 2048L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PLAY_FROM_URI

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PLAY_FROM_URI: Long
```

Indicates this session supports the play from URI command. 

 Value: 8192L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PLAY_PAUSE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PLAY_PAUSE: Long
```

Indicates this session supports the play/pause toggle command. 

 Value: 512L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PREPARE

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PREPARE: Long
```

Indicates this session supports the prepare command. 

 Value: 16384L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PREPARE_FROM_MEDIA_ID

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PREPARE_FROM_MEDIA_ID: Long
```

Indicates this session supports the prepare from media id command. 

 Value: 32768L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PREPARE_FROM_SEARCH

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PREPARE_FROM_SEARCH: Long
```

Indicates this session supports the prepare from search command. 

 Value: 65536L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_PREPARE_FROM_URI

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_PREPARE_FROM_URI: Long
```

Indicates this session supports the prepare from URI command. 

 Value: 131072L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_REWIND

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_REWIND: Long
```

Indicates this session supports the rewind command. 

 Value: 8L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_SEEK_TO

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SEEK_TO: Long
```

Indicates this session supports the seek to command. 

 Value: 256L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_SET_PLAYBACK_SPEED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SET_PLAYBACK_SPEED: Long
```

Indicates this session supports the set playback speed command. 

 Value: 4194304L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_SET_RATING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SET_RATING: Long
```

Indicates this session supports the set rating command. 

 Value: 128L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_SKIP_TO_NEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SKIP_TO_NEXT: Long
```

Indicates this session supports the next command. 

 Value: 32L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_SKIP_TO_PREVIOUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SKIP_TO_PREVIOUS: Long
```

Indicates this session supports the previous command. 

 Value: 16L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_SKIP_TO_QUEUE_ITEM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SKIP_TO_QUEUE_ITEM: Long
```

Indicates this session supports the skip to queue item command. 

 Value: 4096L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### ACTION_STOP

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_STOP: Long
```

Indicates this session supports the stop command. 

 Value: 1L

**See Also**

- [android.media.session.PlaybackState.Builder#setActions(long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setActions(kotlin.Long)) 

### PLAYBACK_POSITION_UNKNOWN

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PLAYBACK_POSITION_UNKNOWN: Long
```

Use this value for the position to indicate the position is not known. 

 Value: -1L

### STATE_BUFFERING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_BUFFERING: Int
```

State indicating this item is currently buffering and will begin playing when enough data has buffered. 

 Value: 6

**See Also**

### STATE_CONNECTING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CONNECTING: Int
```

State indicating the class doing playback is currently connecting to a new destination. Depending on the implementation you may return to the previous state when the connection finishes or enter [STATE_NONE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_NONE:kotlin.Int). If the connection failed [STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_ERROR:kotlin.Int) should be used. 

 Value: 8

**See Also**

### STATE_ERROR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_ERROR: Int
```

State indicating this item is currently in an error state. The error message should also be set when entering this state. 

 Value: 7

**See Also**

### STATE_FAST_FORWARDING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_FAST_FORWARDING: Int
```

State indicating this item is currently fast forwarding. 

 Value: 4

**See Also**

### STATE_NONE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_NONE: Int
```

This is the default playback state and indicates that no media has been added yet, or the performer has been reset and has no content to play. 

 Value: 0

**See Also**

- [android.media.session.PlaybackState.Builder#setState(int, long, float)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setState(kotlin.Int,%20kotlin.Long,%20kotlin.Float))
- [android.media.session.PlaybackState.Builder#setState(int, long, float, long)](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState.Builder#setState(kotlin.Int,%20kotlin.Long,%20kotlin.Float,%20kotlin.Long)) 

### STATE_PAUSED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PAUSED: Int
```

State indicating this item is currently paused. 

 Value: 2

**See Also**

### STATE_PLAYING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_PLAYING: Int
```

State indicating this item is currently playing. 

 Value: 3

**See Also**

### STATE_REWINDING

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_REWINDING: Int
```

State indicating this item is currently rewinding. 

 Value: 5

**See Also**

### STATE_SKIPPING_TO_NEXT

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SKIPPING_TO_NEXT: Int
```

State indicating the player is currently skipping to the next item. 

 Value: 10

**See Also**

### STATE_SKIPPING_TO_PREVIOUS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SKIPPING_TO_PREVIOUS: Int
```

State indicating the player is currently skipping to the previous item. 

 Value: 9

**See Also**

### STATE_SKIPPING_TO_QUEUE_ITEM

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_SKIPPING_TO_QUEUE_ITEM: Int
```

State indicating the player is currently skipping to a specific item in the queue. 

 Value: 11

**See Also**

### STATE_STOPPED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_STOPPED: Int
```

State indicating this item is currently stopped. 

 Value: 1

**See Also**

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getActions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActions(): Long
```

Get the current actions available on this session. This should use a bitmask of the available actions.

- [PlaybackState.ACTION_SKIP_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_PREVIOUS:kotlin.Long)
- [PlaybackState.ACTION_REWIND](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_REWIND:kotlin.Long)
- [PlaybackState.ACTION_PLAY](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY:kotlin.Long)
- [PlaybackState.ACTION_PAUSE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PAUSE:kotlin.Long)
- [PlaybackState.ACTION_STOP](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_STOP:kotlin.Long)
- [PlaybackState.ACTION_FAST_FORWARD](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_FAST_FORWARD:kotlin.Long)
- [PlaybackState.ACTION_SKIP_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_NEXT:kotlin.Long)
- [PlaybackState.ACTION_SEEK_TO](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SEEK_TO:kotlin.Long)
- [PlaybackState.ACTION_SET_RATING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SET_RATING:kotlin.Long)
- [PlaybackState.ACTION_PLAY_PAUSE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_PAUSE:kotlin.Long)
- [PlaybackState.ACTION_PLAY_FROM_MEDIA_ID](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_MEDIA_ID:kotlin.Long)
- [PlaybackState.ACTION_PLAY_FROM_SEARCH](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_SEARCH:kotlin.Long)
- [PlaybackState.ACTION_SKIP_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_QUEUE_ITEM:kotlin.Long)
- [PlaybackState.ACTION_PLAY_FROM_URI](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_URI:kotlin.Long)
- [PlaybackState.ACTION_PREPARE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE:kotlin.Long)
- [PlaybackState.ACTION_PREPARE_FROM_MEDIA_ID](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_MEDIA_ID:kotlin.Long)
- [PlaybackState.ACTION_PREPARE_FROM_SEARCH](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_SEARCH:kotlin.Long)
- [PlaybackState.ACTION_PREPARE_FROM_URI](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_URI:kotlin.Long)
- [PlaybackState.ACTION_SET_PLAYBACK_SPEED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SET_PLAYBACK_SPEED:kotlin.Long)

<br />

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Value is either`0`or a combination of [android.media.session.PlaybackState#ACTION_STOP](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_STOP:kotlin.Long), [android.media.session.PlaybackState#ACTION_PAUSE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PAUSE:kotlin.Long), [android.media.session.PlaybackState#ACTION_PLAY](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY:kotlin.Long), [android.media.session.PlaybackState#ACTION_REWIND](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_REWIND:kotlin.Long), [android.media.session.PlaybackState#ACTION_SKIP_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_PREVIOUS:kotlin.Long), [android.media.session.PlaybackState#ACTION_SKIP_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_NEXT:kotlin.Long), [android.media.session.PlaybackState#ACTION_FAST_FORWARD](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_FAST_FORWARD:kotlin.Long), [android.media.session.PlaybackState#ACTION_SET_RATING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SET_RATING:kotlin.Long), [android.media.session.PlaybackState#ACTION_SEEK_TO](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SEEK_TO:kotlin.Long), [android.media.session.PlaybackState#ACTION_PLAY_PAUSE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_PAUSE:kotlin.Long), [android.media.session.PlaybackState#ACTION_PLAY_FROM_MEDIA_ID](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_MEDIA_ID:kotlin.Long), [android.media.session.PlaybackState#ACTION_PLAY_FROM_SEARCH](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_SEARCH:kotlin.Long), [android.media.session.PlaybackState#ACTION_SKIP_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SKIP_TO_QUEUE_ITEM:kotlin.Long), [android.media.session.PlaybackState#ACTION_PLAY_FROM_URI](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PLAY_FROM_URI:kotlin.Long), [android.media.session.PlaybackState#ACTION_PREPARE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE:kotlin.Long), [android.media.session.PlaybackState#ACTION_PREPARE_FROM_MEDIA_ID](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_MEDIA_ID:kotlin.Long), [android.media.session.PlaybackState#ACTION_PREPARE_FROM_SEARCH](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_SEARCH:kotlin.Long), [android.media.session.PlaybackState#ACTION_PREPARE_FROM_URI](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_PREPARE_FROM_URI:kotlin.Long), and [android.media.session.PlaybackState#ACTION_SET_PLAYBACK_SPEED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#ACTION_SET_PLAYBACK_SPEED:kotlin.Long) |

### getActiveQueueItemId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getActiveQueueItemId(): Long
```

Get the id of the currently active item in the queue. If there is no queue or a queue is not supported by the session this will be [MediaSession.QueueItem.UNKNOWN_ID](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.QueueItem#UNKNOWN_ID:kotlin.Int).

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The id of the currently active item in the queue or [MediaSession.QueueItem.UNKNOWN_ID](https://developer.android.com/reference/kotlin/android/media/session/MediaSession.QueueItem#UNKNOWN_ID:kotlin.Int). |

### getBufferedPosition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBufferedPosition(): Long
```

Get the current buffered position in ms. This is the farthest playback point that can be reached from the current position using only buffered content. 

### getCustomActions

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCustomActions(): MutableList<PlaybackState.CustomAction!>!
```

Get the list of custom actions. 

### getErrorMessage

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getErrorMessage(): CharSequence!
```

Get a user readable error message. This should be set when the state is [PlaybackState.STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_ERROR:kotlin.Int). 

### getExtras

Added in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle?
```

Get any custom extras that were set on this playback state.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)? | The extras for this state or null. |

### getLastPositionUpdateTime

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLastPositionUpdateTime(): Long
```

Get the elapsed real time at which position was last updated. If the position has never been set this will return 0;

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | The last time the position was updated. |

### getPlaybackSpeed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlaybackSpeed(): Float
```

Get the current playback speed as a multiple of normal playback. This should be negative when rewinding. A value of 1 means normal playback and 0 means paused.

| Return ||
|--------------------------------------------------------------------------------|--------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The current speed of playback. |

### getPosition

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPosition(): Long
```

Get the current playback position in ms. 

### getState

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getState(): Int
```

Get the current state of playback. One of the following:

- [PlaybackState.STATE_NONE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_NONE:kotlin.Int)
- [PlaybackState.STATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_STOPPED:kotlin.Int)
- [PlaybackState.STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PLAYING:kotlin.Int)
- [PlaybackState.STATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PAUSED:kotlin.Int)
- [PlaybackState.STATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_FAST_FORWARDING:kotlin.Int)
- [PlaybackState.STATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_REWINDING:kotlin.Int)
- [PlaybackState.STATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_BUFFERING:kotlin.Int)
- [PlaybackState.STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_ERROR:kotlin.Int)
- [PlaybackState.STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_CONNECTING:kotlin.Int)
- [PlaybackState.STATE_SKIPPING_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_PREVIOUS:kotlin.Int)
- [PlaybackState.STATE_SKIPPING_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_NEXT:kotlin.Int)
- [PlaybackState.STATE_SKIPPING_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_QUEUE_ITEM:kotlin.Int)

<br />

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.session.PlaybackState#STATE_NONE](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_NONE:kotlin.Int), [android.media.session.PlaybackState#STATE_STOPPED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_STOPPED:kotlin.Int), [android.media.session.PlaybackState#STATE_PAUSED](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PAUSED:kotlin.Int), [android.media.session.PlaybackState#STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PLAYING:kotlin.Int), [android.media.session.PlaybackState#STATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_FAST_FORWARDING:kotlin.Int), [android.media.session.PlaybackState#STATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_REWINDING:kotlin.Int), [android.media.session.PlaybackState#STATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_BUFFERING:kotlin.Int), [android.media.session.PlaybackState#STATE_ERROR](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_ERROR:kotlin.Int), [android.media.session.PlaybackState#STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_CONNECTING:kotlin.Int), [android.media.session.PlaybackState#STATE_SKIPPING_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_PREVIOUS:kotlin.Int), [android.media.session.PlaybackState#STATE_SKIPPING_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_NEXT:kotlin.Int), or [android.media.session.PlaybackState#STATE_SKIPPING_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_QUEUE_ITEM:kotlin.Int) |

### isActive

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isActive(): Boolean
```

Returns whether this is considered as an active playback state.

The playback state is considered as an active if the state is one of the following:

- [STATE_BUFFERING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_BUFFERING:kotlin.Int)
- [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_CONNECTING:kotlin.Int)
- [STATE_FAST_FORWARDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_FAST_FORWARDING:kotlin.Int)
- [STATE_PLAYING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_PLAYING:kotlin.Int)
- [STATE_REWINDING](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_REWINDING:kotlin.Int)
- [STATE_SKIPPING_TO_NEXT](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_NEXT:kotlin.Int)
- [STATE_SKIPPING_TO_PREVIOUS](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_PREVIOUS:kotlin.Int)
- [STATE_SKIPPING_TO_QUEUE_ITEM](https://developer.android.com/reference/kotlin/android/media/session/PlaybackState#STATE_SKIPPING_TO_QUEUE_ITEM:kotlin.Int) 

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<PlaybackState!>
```
