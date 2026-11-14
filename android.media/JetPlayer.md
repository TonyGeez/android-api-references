# JetPlayer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JetPlayer

Kotlin| [Java](https://developer.android.com/reference/android/media/JetPlayer "View this page in Java") 
| --- | --- |

```
open class JetPlayer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.JetPlayer](https://developer.android.com/reference/kotlin/android/media/JetPlayer#) |

JetPlayer provides access to JET content playback and control.

Please refer to the [JET Creator User Manual](https://developer.android.com/guide/topics/media/jet/jetcreator_manual) for a presentation of the JET interactive music concept and how to use the JetCreator tool to create content to be player by JetPlayer.

Use of the JetPlayer class is based around the playback of a number of JET segments sequentially added to a playback FIFO queue. The rendering of the MIDI content stored in each segment can be dynamically affected by two mechanisms:

- Tracks in a segment can be muted or unmuted at any moment, individually or through a mask (to change the mute state of multiple tracks at once).
- Parts of tracks in a segment can be played at predefined points in the segment, in order to maintain synchronization with the other tracks in the segment. This is achieved through the notion of "clips", which can be triggered at any time, but that will play only at the right time, as authored in the corresponding JET file.

As a result of the rendering and playback of the JET segments, the user of the JetPlayer instance can receive notifications from the JET engine relative to:

- Playback state
- Number of segments left to play in the queue
- Application controller events (CC80-83) to mark points in the MIDI segments

Use [getJetPlayer()](https://developer.android.com/reference/kotlin/android/media/JetPlayer#getJetPlayer())to construct a JetPlayer instance. JetPlayer is a singleton class.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnJetEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener) Handles the notification when the JET engine generates an event. |

| Public methods ||
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [clearQueue](https://developer.android.com/reference/kotlin/android/media/JetPlayer#clearQueue())`()` Empties the segment queue, and clears all clips that are scheduled for playback. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | [clone](https://developer.android.com/reference/kotlin/android/media/JetPlayer#clone())`()` Cloning a JetPlayer instance is not supported. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [closeJetFile](https://developer.android.com/reference/kotlin/android/media/JetPlayer#closeJetFile())`()` Closes the resource containing the JET content. |
| --- | --- |
| openstatic [JetPlayer](https://developer.android.com/reference/kotlin/android/media/JetPlayer#)! | [getJetPlayer](https://developer.android.com/reference/kotlin/android/media/JetPlayer#getJetPlayer())`()` Factory method for the JetPlayer class. |
| openstatic [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxTracks](https://developer.android.com/reference/kotlin/android/media/JetPlayer#getMaxTracks())`()` Gets the maximum number of simultaneous MIDI tracks supported by JetPlayer. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [loadJetFile](https://developer.android.com/reference/kotlin/android/media/JetPlayer#loadJetFile(android.content.res.AssetFileDescriptor))`(`afd:` ` [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)!`)` Loads a . |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [loadJetFile](https://developer.android.com/reference/kotlin/android/media/JetPlayer#loadJetFile(kotlin.String))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Loads a . |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pause](https://developer.android.com/reference/kotlin/android/media/JetPlayer#pause())`()` Pauses the playback of the JET segment queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [play](https://developer.android.com/reference/kotlin/android/media/JetPlayer#play())`()` Starts playing the JET segment queue. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [queueJetSegment](https://developer.android.com/reference/kotlin/android/media/JetPlayer#queueJetSegment(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Byte))`(`segmentNum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `libNum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `transpose:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `muteFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `userID:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Queues the specified segment in the JET queue. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [queueJetSegmentMuteArray](https://developer.android.com/reference/kotlin/android/media/JetPlayer#queueJetSegmentMuteArray(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.BooleanArray,%20kotlin.Byte))`(`segmentNum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `libNum:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `repeatCount:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `transpose:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `muteArray:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`, `userID:` ` [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html)`)` Queues the specified segment in the JET queue. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/media/JetPlayer#release())`()` Stops the current JET playback, and releases all associated native resources. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer#setEventListener(android.media.JetPlayer.OnJetEventListener))`(`listener:` ` [JetPlayer.OnJetEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener)!`)` Sets the listener JetPlayer notifies when a JET event is generated by the rendering and playback engine. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer#setEventListener(android.media.JetPlayer.OnJetEventListener,%20android.os.Handler))`(`listener:` ` [JetPlayer.OnJetEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Sets the listener JetPlayer notifies when a JET event is generated by the rendering and playback engine. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setMuteArray](https://developer.android.com/reference/kotlin/android/media/JetPlayer#setMuteArray(kotlin.BooleanArray,%20kotlin.Boolean))`(`muteArray:` ` [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!`, `sync:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Modifies the mute flags for the current active segment. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setMuteFlag](https://developer.android.com/reference/kotlin/android/media/JetPlayer#setMuteFlag(kotlin.Int,%20kotlin.Boolean,%20kotlin.Boolean))`(`trackId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `muteFlag:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `sync:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Mutes or unmutes a single track. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setMuteFlags](https://developer.android.com/reference/kotlin/android/media/JetPlayer#setMuteFlags(kotlin.Int,%20kotlin.Boolean))`(`muteFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sync:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Modifies the mute flags. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [triggerClip](https://developer.android.com/reference/kotlin/android/media/JetPlayer#triggerClip(kotlin.Int))`(`clipId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Schedules the playback of a clip. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](https://developer.android.com/reference/kotlin/android/media/JetPlayer#finalize())`()` <br /> |

## Public methods

### clearQueue

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearQueue(): Boolean
```

Empties the segment queue, and clears all clips that are scheduled for playback.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the queue was successfully cleared, false otherwise. |

### clone

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clone(): Any!
```

Cloning a JetPlayer instance is not supported. Calling clone() will generate an exception.

| Return ||
|-----------------------------------------------------------------------------|---------------------------|
| [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | a clone of this instance. |

| Exceptions ||
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.CloneNotSupportedException` | if the object's class does not support the`Cloneable`interface. Subclasses that override the`clone`method can also throw this exception to indicate that an instance cannot be cloned. |

### closeJetFile

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun closeJetFile(): Boolean
```

Closes the resource containing the JET content.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if successfully closed, false otherwise. |

### getJetPlayer

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getJetPlayer(): JetPlayer!
```

Factory method for the JetPlayer class.

| Return ||
|---------------------------------------------------------------------------------------|-----------------------------------|
| [JetPlayer](https://developer.android.com/reference/kotlin/android/media/JetPlayer#)! | the singleton JetPlayer instance. |

### getMaxTracks

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getMaxTracks(): Int
```

Gets the maximum number of simultaneous MIDI tracks supported by JetPlayer.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the maximum number of simultaneous MIDI tracks supported by JetPlayer. |

### loadJetFile

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadJetFile(afd: AssetFileDescriptor!): Boolean
```

Loads a .jet file from an asset file descriptor.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `afd` | [AssetFileDescriptor](https://developer.android.com/reference/kotlin/android/content/res/AssetFileDescriptor.html#)!:the asset file descriptor. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if loading the .jet file was successful, false if loading failed. |

### loadJetFile

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun loadJetFile(path: String!): Boolean
```

Loads a .jet file from a given path.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path to the .jet file, for instance "/sdcard/mygame/music.jet". |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if loading the .jet file was successful, false if loading failed. |

### pause

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pause(): Boolean
```

Pauses the playback of the JET segment queue.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if rendering and playback is successfully paused, false otherwise. |

### play

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun play(): Boolean
```

Starts playing the JET segment queue.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if rendering and playback is successfully started, false otherwise. |

### queueJetSegment

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queueJetSegment(
    segmentNum: Int, 
    libNum: Int, 
    repeatCount: Int, 
    transpose: Int, 
    muteFlags: Int, 
    userID: Byte
): Boolean
```

Queues the specified segment in the JET queue.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `segmentNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identifier of the segment. |
| `libNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the sound bank associated with the segment. Use -1 to indicate that no sound bank (DLS file) is associated with this segment, in which case JET will use the General MIDI library. |
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of times the segment will be repeated. 0 means the segment will only play once. -1 means the segment will repeat indefinitely. |
| --- | --- |
| `transpose` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of pitch transposition. Set to 0 for normal playback. Range is -12 to +12. |
| `muteFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bitmask to specify which MIDI tracks will be muted during playback. Bit 0 affects track 0, bit 1 affects track 1 etc. |
| `userID` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):a value specified by the application that uniquely identifies the segment. this value is received in the [OnJetEventListener.onJetUserIdUpdate(JetPlayer, int, int)](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener#onJetUserIdUpdate(android.media.JetPlayer,%20kotlin.Int,%20kotlin.Int))event listener method. Normally, the application will keep a byte value that is incremented each time a new segment is queued up. This can be used to look up any special characteristics of that track including trigger clips and mute flags. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the segment was successfully queued, false if the queue is full or if the parameters are invalid. |

### queueJetSegmentMuteArray

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queueJetSegmentMuteArray(
    segmentNum: Int, 
    libNum: Int, 
    repeatCount: Int, 
    transpose: Int, 
    muteArray: BooleanArray!, 
    userID: Byte
): Boolean
```

Queues the specified segment in the JET queue.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `segmentNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identifier of the segment. |
| `libNum` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the soundbank associated with the segment. Use -1 to indicate that no sound bank (DLS file) is associated with this segment, in which case JET will use the General MIDI library. |
| `repeatCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of times the segment will be repeated. 0 means the segment will only play once. -1 means the segment will repeat indefinitely. |
| --- | --- |
| `transpose` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the amount of pitch transposition. Set to 0 for normal playback. Range is -12 to +12. |
| `muteArray` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:an array of booleans to specify which MIDI tracks will be muted during playback. The value at index 0 affects track 0, value at index 1 affects track 1 etc. The length of the array must be [getMaxTracks()](https://developer.android.com/reference/kotlin/android/media/JetPlayer#getMaxTracks())for the call to succeed. |
| `userID` | [Byte](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte/index.html):a value specified by the application that uniquely identifies the segment. this value is received in the [OnJetEventListener.onJetUserIdUpdate(JetPlayer, int, int)](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener#onJetUserIdUpdate(android.media.JetPlayer,%20kotlin.Int,%20kotlin.Int))event listener method. Normally, the application will keep a byte value that is incremented each time a new segment is queued up. This can be used to look up any special characteristics of that track including trigger clips and mute flags. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the segment was successfully queued, false if the queue is full or if the parameters are invalid. |

### release

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```

Stops the current JET playback, and releases all associated native resources. The object can no longer be used and the reference should be set to null after a call to release(). 

### setEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEventListener(listener: JetPlayer.OnJetEventListener!): Unit
```

Sets the listener JetPlayer notifies when a JET event is generated by the rendering and playback engine. Notifications are received in the same thread as the one in which the JetPlayer instance was created.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [JetPlayer.OnJetEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener)!:the listener that will be notified when a JET event is generated. |

### setEventListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setEventListener(
    listener: JetPlayer.OnJetEventListener!, 
    handler: Handler!
): Unit
```

Sets the listener JetPlayer notifies when a JET event is generated by the rendering and playback engine. Use this method to receive JET events in the Handler associated with another thread than the one in which you created the JetPlayer instance.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [JetPlayer.OnJetEventListener](https://developer.android.com/reference/kotlin/android/media/JetPlayer.OnJetEventListener)!:the listener that will be notified when a JET event is generated. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:the Handler that will receive the event notification messages. |

### setMuteArray

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMuteArray(
    muteArray: BooleanArray!, 
    sync: Boolean
): Boolean
```

Modifies the mute flags for the current active segment.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `muteArray` | [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)!:an array of booleans to specify which MIDI tracks are muted. The value at index 0 affects track 0, value at index 1 affects track 1 etc. The length of the array must be [getMaxTracks()](https://developer.android.com/reference/kotlin/android/media/JetPlayer#getMaxTracks())for the call to succeed. |
| `sync` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if false, the new mute flags will be applied as soon as possible by the JET render and playback engine. If true, the mute flags will be updated at the start of the next segment. If the segment is repeated, the flags will take effect the next time segment is repeated. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the mute flags were successfully updated, false otherwise. |

### setMuteFlag

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMuteFlag(
    trackId: Int, 
    muteFlag: Boolean, 
    sync: Boolean
): Boolean
```

Mutes or unmutes a single track.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `trackId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the track to mute. |
| `muteFlag` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):set to true to mute, false to unmute. |
| `sync` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if false, the new mute flags will be applied as soon as possible by the JET render and playback engine. If true, the mute flag will be updated at the start of the next segment. If the segment is repeated, the flag will take effect the next time segment is repeated. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the mute flag was successfully updated, false otherwise. |

### setMuteFlags

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setMuteFlags(
    muteFlags: Int, 
    sync: Boolean
): Boolean
```

Modifies the mute flags.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `muteFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):a bitmask to specify which MIDI tracks are muted. Bit 0 affects track 0, bit 1 affects track 1 etc. |
| `sync` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if false, the new mute flags will be applied as soon as possible by the JET render and playback engine. If true, the mute flags will be updated at the start of the next segment. If the segment is repeated, the flags will take effect the next time segment is repeated. |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the mute flags were successfully updated, false otherwise. |

### triggerClip

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun triggerClip(clipId: Int): Boolean
```

Schedules the playback of a clip. This will automatically update the mute flags in sync with the JET Clip Marker (controller 103). The parameter clipID must be in the range of 0-63. After the call to triggerClip, when JET next encounters a controller event 103 with bits 0-5 of the value equal to clipID and bit 6 set to 1, it will automatically unmute the track containing the controller event. When JET encounters the complementary controller event 103 with bits 0-5 of the value equal to clipID and bit 6 set to 0, it will mute the track again.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------|
| `clipId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the identifier of the clip to trigger. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the clip was successfully triggered, false otherwise. |

## Protected methods

### finalize

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
