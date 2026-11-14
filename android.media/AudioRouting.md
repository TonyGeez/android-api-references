# AudioRouting

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRouting

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioRouting "View this page in Java") 
| --- | --- |

```
interface AudioRouting
```

| [android.media.AudioRouting](https://developer.android.com/reference/kotlin/android/media/AudioRouting#) |

| Known Direct Subclasses [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord), [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack), [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer), [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [AudioRecord](https://developer.android.com/reference/kotlin/android/media/AudioRecord) | The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. | | [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack) | The AudioTrack class manages and plays a single audio resource for Java applications. | | [MediaPlayer](https://developer.android.com/reference/kotlin/android/media/MediaPlayer) | MediaPlayer class can be used to control playback of audio/video files and streams. | | [MediaRecorder](https://developer.android.com/reference/kotlin/android/media/MediaRecorder) | Used to record audio and video. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

AudioRouting defines an interface for controlling routing and routing notifications in AudioTrack and AudioRecord objects.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) Defines the interface by which applications can receive notifications of routing changes for the associated [AudioRouting](https://developer.android.com/reference/kotlin/android/media/AudioRouting#). |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting#addOnRoutingChangedListener(android.media.AudioRouting.OnRoutingChangedListener,%20android.os.Handler))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Adds an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) to receive notifications of routing changes on this AudioTrack/AudioRecord. |
| abstract [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRouting#getPreferredDevice())`()` Returns the selected output/input specified by [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRouting#setPreferredDevice(android.media.AudioDeviceInfo)). |
| abstract [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)! | [getRoutedDevice](https://developer.android.com/reference/kotlin/android/media/AudioRouting#getRoutedDevice())`()` Returns an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioTrack/AudioRecord. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!\> | [getRoutedDevices](https://developer.android.com/reference/kotlin/android/media/AudioRouting#getRoutedDevices())`()` Returns a List of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioTrack/AudioRecord. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting#removeOnRoutingChangedListener(android.media.AudioRouting.OnRoutingChangedListener))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!`)` Removes an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) which has been previously added to receive rerouting notifications. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRouting#setPreferredDevice(android.media.AudioDeviceInfo))`(`deviceInfo:` ` [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!`)` Specifies an audio device (via an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) object) to route the output/input to/from. |
| --- | --- |

## Public methods

### addOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun addOnRoutingChangedListener(
    listener: AudioRouting.OnRoutingChangedListener!, 
    handler: Handler!
): Unit
```

Adds an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) to receive notifications of routing changes on this AudioTrack/AudioRecord.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!:The [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) interface to receive notifications of rerouting events. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Specifies the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) object for the thread on which to execute the callback. If`null`, the [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#) associated with the main [Looper](https://developer.android.com/reference/kotlin/android/os/Looper.html#) will be used. |

### getPreferredDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPreferredDevice(): AudioDeviceInfo!
```

Returns the selected output/input specified by [setPreferredDevice](https://developer.android.com/reference/kotlin/android/media/AudioRouting#setPreferredDevice(android.media.AudioDeviceInfo)). Note that this is not guaranteed to correspond to the actual device being used for playback/recording. 

### getRoutedDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioTrack/AudioRecord. Note: The query is only valid if the AudioTrack/AudioRecord is currently playing. If it is not,`getRoutedDevice()`will return null. 

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) identifying the current routing of this AudioTrack/AudioRecord. Note: The query is only valid if the AudioTrack/AudioRecord is currently playing. If it is not,`getRoutedDevices()`will return an empty List.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!> | This value cannot be`null`. |

### removeOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener)!:The previously added [AudioRouting.OnRoutingChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioRouting.OnRoutingChangedListener) interface to remove. |

### setPreferredDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) object) to route the output/input to/from.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!:The [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) specifying the audio sink or source. If deviceInfo is null, default routing is restored. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if succesful, false if the specified [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) is non-null and does not correspond to a valid audio device. |
