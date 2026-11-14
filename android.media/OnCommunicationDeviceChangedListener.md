# AudioManager.OnCommunicationDeviceChangedListener

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCommunicationDeviceChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioManager.OnCommunicationDeviceChangedListener "View this page in Java") 

```
interface OnCommunicationDeviceChangedListener
```

| [android.media.AudioManager.OnCommunicationDeviceChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnCommunicationDeviceChangedListener#) |

Listener registered by client to be notified upon communication audio device change. See [setCommunicationDevice(android.media.AudioDeviceInfo)](https://developer.android.com/reference/kotlin/android/media/AudioManager#setCommunicationDevice(android.media.AudioDeviceInfo)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCommunicationDeviceChanged](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnCommunicationDeviceChangedListener#onCommunicationDeviceChanged(android.media.AudioDeviceInfo))`(`device:` ` [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)?`)` Callback method called upon communication audio device change. |

## Public methods

### onCommunicationDeviceChanged

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCommunicationDeviceChanged(device: AudioDeviceInfo?): Unit
```

Callback method called upon communication audio device change.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)?:the audio device requested for communication use cases. Can be null on platforms not supporting [android.content.pm.PackageManager#FEATURE_TELEPHONY](https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_TELEPHONY:kotlin.String). |
