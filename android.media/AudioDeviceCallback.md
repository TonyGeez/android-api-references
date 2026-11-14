# AudioDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioDeviceCallback

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioDeviceCallback "View this page in Java") 
| --- | --- |

```
abstract class AudioDeviceCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioDeviceCallback](https://developer.android.com/reference/kotlin/android/media/AudioDeviceCallback#) |

AudioDeviceCallback defines the mechanism by which applications can receive notifications of audio device connection and disconnection events.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioDeviceCallback](https://developer.android.com/reference/kotlin/android/media/AudioDeviceCallback#AudioDeviceCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioDevicesAdded](https://developer.android.com/reference/kotlin/android/media/AudioDeviceCallback#onAudioDevicesAdded(kotlin.Array))`(`addedDevices:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!>!`)` Called by the [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager) to indicate that one or more audio devices have been connected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioDevicesRemoved](https://developer.android.com/reference/kotlin/android/media/AudioDeviceCallback#onAudioDevicesRemoved(kotlin.Array))`(`removedDevices:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!>!`)` Called by the [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager) to indicate that one or more audio devices have been disconnected. |

## Public constructors

### AudioDeviceCallback

```
AudioDeviceCallback()
```

## Public methods

### onAudioDevicesAdded

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAudioDevicesAdded(addedDevices: Array<AudioDeviceInfo!>!): Unit
```

Called by the [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager) to indicate that one or more audio devices have been connected.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addedDevices` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!\>!:An array of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) objects corresponding to any newly added audio devices. |

### onAudioDevicesRemoved

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAudioDevicesRemoved(removedDevices: Array<AudioDeviceInfo!>!): Unit
```

Called by the [AudioManager](https://developer.android.com/reference/kotlin/android/media/AudioManager) to indicate that one or more audio devices have been disconnected.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `removedDevices` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)!\>!:An array of [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo) objects corresponding to any newly removed audio devices. |
