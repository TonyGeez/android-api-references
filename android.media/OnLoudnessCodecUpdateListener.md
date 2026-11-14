# LoudnessCodecController.OnLoudnessCodecUpdateListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoudnessCodecUpdateListener

Kotlin| [Java](https://developer.android.com/reference/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener "View this page in Java") 
| --- | --- |

```
interface OnLoudnessCodecUpdateListener
```

| [android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener#) |

Listener used for receiving asynchronous loudness metadata updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [onLoudnessCodecUpdate](https://developer.android.com/reference/kotlin/android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener#onLoudnessCodecUpdate(android.media.MediaCodec,%20android.os.Bundle))`(`mediaCodec:` ` [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec)`, `codecValues:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)`)` Contains the MediaCodec key/values that can be set directly to configure the loudness of the handle's corresponding decoder (see [MediaCodec.setParameters(Bundle)](https://developer.android.com/reference/kotlin/android/media/MediaCodec#setParameters(android.os.Bundle))). |

## Public methods

### onLoudnessCodecUpdate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLoudnessCodecUpdate(
    mediaCodec: MediaCodec, 
    codecValues: Bundle
): Bundle
```

Contains the MediaCodec key/values that can be set directly to configure the loudness of the handle's corresponding decoder (see [MediaCodec.setParameters(Bundle)](https://developer.android.com/reference/kotlin/android/media/MediaCodec#setParameters(android.os.Bundle))).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](https://developer.android.com/reference/kotlin/android/media/MediaCodec):the mediaCodec that will receive the new parameters |
| `codecValues` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#):contains loudness key/value pairs that can be set directly on the mediaCodec. The listener can modify these values with their own edits which will be returned for the mediaCodec configuration |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | a Bundle which contains the original computed codecValues aggregated with user edits. The platform will configure the associated MediaCodecs with the returned Bundle params. |
