# AudioManager.OnPreferredMixerAttributesChangedListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreferredMixerAttributesChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioManager.OnPreferredMixerAttributesChangedListener "View this page in Java") 
| --- | --- |

```
interface OnPreferredMixerAttributesChangedListener
```

| [android.media.AudioManager.OnPreferredMixerAttributesChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnPreferredMixerAttributesChangedListener#) |

Interface to be notified of changes in the preferred mixer attributes.

Note that this listener will only be invoked whenever [setPreferredMixerAttributes(android.media.AudioAttributes,android.media.AudioDeviceInfo,android.media.AudioMixerAttributes)](https://developer.android.com/reference/kotlin/android/media/AudioManager#setPreferredMixerAttributes(android.media.AudioAttributes,%20android.media.AudioDeviceInfo,%20android.media.AudioMixerAttributes))or [clearPreferredMixerAttributes(android.media.AudioAttributes,android.media.AudioDeviceInfo)](https://developer.android.com/reference/kotlin/android/media/AudioManager#clearPreferredMixerAttributes(android.media.AudioAttributes,%20android.media.AudioDeviceInfo))or device disconnection causes a change in preferred mixer attributes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreferredMixerAttributesChanged](https://developer.android.com/reference/kotlin/android/media/AudioManager.OnPreferredMixerAttributesChangedListener#onPreferredMixerAttributesChanged(android.media.AudioAttributes,%20android.media.AudioDeviceInfo,%20android.media.AudioMixerAttributes))`(`attributes:` ` [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes)`, `device:` ` [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo)`, `mixerAttributes:` ` [AudioMixerAttributes](https://developer.android.com/reference/kotlin/android/media/AudioMixerAttributes)?`)` Called on the listener to indicate that the preferred mixer attributes for the audio attributes over the given device has changed. |

## Public methods

### onPreferredMixerAttributesChanged

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPreferredMixerAttributesChanged(
    attributes: AudioAttributes, 
    device: AudioDeviceInfo, 
    mixerAttributes: AudioMixerAttributes?
): Unit
```

Called on the listener to indicate that the preferred mixer attributes for the audio attributes over the given device has changed.

| Parameters ||
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `attributes` | [AudioAttributes](https://developer.android.com/reference/kotlin/android/media/AudioAttributes):the audio attributes for playback This value cannot be`null`. |
| `device` | [AudioDeviceInfo](https://developer.android.com/reference/kotlin/android/media/AudioDeviceInfo):the targeted device This value cannot be`null`. |
| `mixerAttributes` | [AudioMixerAttributes](https://developer.android.com/reference/kotlin/android/media/AudioMixerAttributes)?:the [AudioMixerAttributes](https://developer.android.com/reference/kotlin/android/media/AudioMixerAttributes) that contains information for preferred mixer attributes or null if preferred mixer attributes is cleared |
| --- | --- |
