# AudioManager.OnPreferredMixerAttributesChangedListener

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnPreferredMixerAttributesChangedListener

Kotlin| [Java](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md) 
| --- | --- |

```
interface OnPreferredMixerAttributesChangedListener
```

| [android.media.AudioManager.OnPreferredMixerAttributesChangedListener](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md) |

Interface to be notified of changes in the preferred mixer attributes.

Note that this listener will only be invoked whenever [setPreferredMixerAttributes(android.media.AudioAttributes,android.media.AudioDeviceInfo,android.media.AudioMixerAttributes)](../android/media/AudioManager.md))or [clearPreferredMixerAttributes(android.media.AudioAttributes,android.media.AudioDeviceInfo)](../android/media/AudioManager.md))or device disconnection causes a change in preferred mixer attributes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreferredMixerAttributesChanged](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md))`(`attributes:` ` [AudioAttributes](../android/media/AudioAttributes.md)`, `device:` ` [AudioDeviceInfo](../android/media/AudioDeviceInfo.md)`, `mixerAttributes:` ` [AudioMixerAttributes](../android/media/AudioMixerAttributes.md)?`)` Called on the listener to indicate that the preferred mixer attributes for the audio attributes over the given device has changed. |

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
| `attributes` | [AudioAttributes](../android/media/AudioAttributes.md):the audio attributes for playback This value cannot be`null`. |
| `device` | [AudioDeviceInfo](../android/media/AudioDeviceInfo.md):the targeted device This value cannot be`null`. |
| `mixerAttributes` | [AudioMixerAttributes](../android/media/AudioMixerAttributes.md)?:the [AudioMixerAttributes](../android/media/AudioMixerAttributes.md) that contains information for preferred mixer attributes or null if preferred mixer attributes is cleared |
| --- | --- |
