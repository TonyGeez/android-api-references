# AudioRouting

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioRouting

Kotlin| [Java](../android/media/AudioRouting.md) 
| --- | --- |

```
interface AudioRouting
```

| [android.media.AudioRouting](../android/media/AudioRouting.md) |

| Known Direct Subclasses [AudioRecord](../android/media/AudioRecord.md), [AudioTrack](../android/media/AudioTrack.md), [MediaPlayer](../android/media/MediaPlayer.md), [MediaRecorder](../android/media/MediaRecorder.md) |---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------| | [AudioRecord](../android/media/AudioRecord.md) | The AudioRecord class manages the audio resources for Java applications to record audio from the audio input hardware of the platform. | | [AudioTrack](../android/media/AudioTrack.md) | The AudioTrack class manages and plays a single audio resource for Java applications. | | [MediaPlayer](../android/media/MediaPlayer.md) | MediaPlayer class can be used to control playback of audio/video files and streams. | | [MediaRecorder](../android/media/MediaRecorder.md) | Used to record audio and video. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

AudioRouting defines an interface for controlling routing and routing notifications in AudioTrack and AudioRecord objects.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) Defines the interface by which applications can receive notifications of routing changes for the associated [AudioRouting](../android/media/AudioRouting.md). |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addOnRoutingChangedListener](../android/media/AudioRouting.md))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!`, `handler:` ` [Handler](../android/os/Handler.md)!`)` Adds an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) to receive notifications of routing changes on this AudioTrack/AudioRecord. |
| abstract [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)! | [getPreferredDevice](../android/media/AudioRouting.md))`()` Returns the selected output/input specified by [setPreferredDevice](../android/media/AudioRouting.md)). |
| abstract [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)! | [getRoutedDevice](../android/media/AudioRouting.md))`()` Returns an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this AudioTrack/AudioRecord. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!\> | [getRoutedDevices](../android/media/AudioRouting.md))`()` Returns a List of [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this AudioTrack/AudioRecord. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeOnRoutingChangedListener](../android/media/AudioRouting.md))`(`listener:` ` [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!`)` Removes an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [setPreferredDevice](../android/media/AudioRouting.md))`(`deviceInfo:` ` [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!`)` Specifies an audio device (via an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) object) to route the output/input to/from. |
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

Adds an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) to receive notifications of routing changes on this AudioTrack/AudioRecord.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!:The [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) interface to receive notifications of rerouting events. |
| `handler` | [Handler](../android/os/Handler.md)!:Specifies the [Handler](../android/os/Handler.md) object for the thread on which to execute the callback. If`null`, the [Handler](../android/os/Handler.md) associated with the main [Looper](../android/os/Looper.md) will be used. |

### getPreferredDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getPreferredDevice(): AudioDeviceInfo!
```

Returns the selected output/input specified by [setPreferredDevice](../android/media/AudioRouting.md)). Note that this is not guaranteed to correspond to the actual device being used for playback/recording. 

### getRoutedDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getRoutedDevice(): AudioDeviceInfo!
```

Returns an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this AudioTrack/AudioRecord. Note: The query is only valid if the AudioTrack/AudioRecord is currently playing. If it is not,`getRoutedDevice()`will return null. 

### getRoutedDevices

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRoutedDevices(): MutableList<AudioDeviceInfo!>
```

Returns a List of [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) identifying the current routing of this AudioTrack/AudioRecord. Note: The query is only valid if the AudioTrack/AudioRecord is currently playing. If it is not,`getRoutedDevices()`will return an empty List.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!> | This value cannot be`null`. |

### removeOnRoutingChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun removeOnRoutingChangedListener(listener: AudioRouting.OnRoutingChangedListener!): Unit
```

Removes an [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) which has been previously added to receive rerouting notifications.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md)!:The previously added [AudioRouting.OnRoutingChangedListener](../android/media/AudioRouting.OnRoutingChangedListener.md) interface to remove. |

### setPreferredDevice

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setPreferredDevice(deviceInfo: AudioDeviceInfo!): Boolean
```

Specifies an audio device (via an [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) object) to route the output/input to/from.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceInfo` | [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)!:The [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) specifying the audio sink or source. If deviceInfo is null, default routing is restored. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if succesful, false if the specified [AudioDeviceInfo](../android/media/AudioDeviceInfo.md) is non-null and does not correspond to a valid audio device. |
