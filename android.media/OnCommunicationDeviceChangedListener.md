# AudioManager.OnCommunicationDeviceChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCommunicationDeviceChangedListener

Kotlin| [Java](../android/media/AudioManager.OnCommunicationDeviceChangedListener.md) 
| --- | --- |

```
interface OnCommunicationDeviceChangedListener
```

| [android.media.AudioManager.OnCommunicationDeviceChangedListener](../android/media/AudioManager.OnCommunicationDeviceChangedListener.md) |

Listener registered by client to be notified upon communication audio device change. See [setCommunicationDevice(android.media.AudioDeviceInfo)](../android/media/AudioManager.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCommunicationDeviceChanged](../android/media/AudioManager.OnCommunicationDeviceChangedListener.md))`(`device:` ` [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)?`)` Callback method called upon communication audio device change. |

## Public methods

### onCommunicationDeviceChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCommunicationDeviceChanged(device: AudioDeviceInfo?): Unit
```

Callback method called upon communication audio device change.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)?:the audio device requested for communication use cases. Can be null on platforms not supporting [android.content.pm.PackageManager#FEATURE_TELEPHONY](../android/content/pm/PackageManager.md). |
