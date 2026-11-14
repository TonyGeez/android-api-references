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

Note that this listener will only be invoked whenever [setPreferredMixerAttributes(android.media.AudioAttributes,android.media.AudioDeviceInfo,android.media.AudioMixerAttributes)](AudioManager.md))or [clearPreferredMixerAttributes(android.media.AudioAttributes,android.media.AudioDeviceInfo)](AudioManager.md))or device disconnection causes a change in preferred mixer attributes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPreferredMixerAttributesChanged](../android/media/AudioManager.OnPreferredMixerAttributesChangedListener.md))`(`attributes:` ` [AudioAttributes](AudioAttributes.md)`, `device:` ` [AudioDeviceInfo](AudioDeviceInfo.md)`, `mixerAttributes:` ` [AudioMixerAttributes](AudioMixerAttributes.md)?`)` Called on the listener to indicate that the preferred mixer attributes for the audio attributes over the given device has changed. |

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
| `attributes` | [AudioAttributes](AudioAttributes.md):the audio attributes for playback This value cannot be`null`. |
| `device` | [AudioDeviceInfo](AudioDeviceInfo.md):the targeted device This value cannot be`null`. |
| `mixerAttributes` | [AudioMixerAttributes](AudioMixerAttributes.md)?:the [AudioMixerAttributes](AudioMixerAttributes.md) that contains information for preferred mixer attributes or null if preferred mixer attributes is cleared |
| --- | --- |
