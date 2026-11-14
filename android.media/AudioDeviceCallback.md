# AudioDeviceCallback

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioDeviceCallback

Kotlin| [Java](AudioDeviceCallback.md) 
| --- | --- |

```
abstract class AudioDeviceCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioDeviceCallback](AudioDeviceCallback.md) |

AudioDeviceCallback defines the mechanism by which applications can receive notifications of audio device connection and disconnection events.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AudioDeviceCallback](AudioDeviceCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioDevicesAdded](AudioDeviceCallback.md))`(`addedDevices:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioDeviceInfo](AudioDeviceInfo.md)!>!`)` Called by the [AudioManager](AudioManager.md) to indicate that one or more audio devices have been connected. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAudioDevicesRemoved](AudioDeviceCallback.md))`(`removedDevices:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [AudioDeviceInfo](AudioDeviceInfo.md)!>!`)` Called by the [AudioManager](AudioManager.md) to indicate that one or more audio devices have been disconnected. |

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

Called by the [AudioManager](AudioManager.md) to indicate that one or more audio devices have been connected.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addedDevices` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\>!:An array of [AudioDeviceInfo](AudioDeviceInfo.md) objects corresponding to any newly added audio devices. |

### onAudioDevicesRemoved

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAudioDevicesRemoved(removedDevices: Array<AudioDeviceInfo!>!): Unit
```

Called by the [AudioManager](AudioManager.md) to indicate that one or more audio devices have been disconnected.

| Parameters ||
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `removedDevices` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [AudioDeviceInfo](AudioDeviceInfo.md)!\>!:An array of [AudioDeviceInfo](AudioDeviceInfo.md) objects corresponding to any newly removed audio devices. |
