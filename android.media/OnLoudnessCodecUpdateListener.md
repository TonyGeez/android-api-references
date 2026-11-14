# LoudnessCodecController.OnLoudnessCodecUpdateListener

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnLoudnessCodecUpdateListener

Kotlin| [Java](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md) 
| --- | --- |

```
interface OnLoudnessCodecUpdateListener
```

| [android.media.LoudnessCodecController.OnLoudnessCodecUpdateListener](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md) |

Listener used for receiving asynchronous loudness metadata updates.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Bundle](../android.os/Bundle.md) | [onLoudnessCodecUpdate](../android/media/LoudnessCodecController.OnLoudnessCodecUpdateListener.md))`(`mediaCodec:` ` [MediaCodec](MediaCodec.md)`, `codecValues:` ` [Bundle](../android.os/Bundle.md)`)` Contains the MediaCodec key/values that can be set directly to configure the loudness of the handle's corresponding decoder (see [MediaCodec.setParameters(Bundle)](MediaCodec.md))). |

## Public methods

### onLoudnessCodecUpdate

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onLoudnessCodecUpdate(
    mediaCodec: MediaCodec, 
    codecValues: Bundle
): Bundle
```

Contains the MediaCodec key/values that can be set directly to configure the loudness of the handle's corresponding decoder (see [MediaCodec.setParameters(Bundle)](MediaCodec.md))).

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mediaCodec` | [MediaCodec](MediaCodec.md):the mediaCodec that will receive the new parameters |
| `codecValues` | [Bundle](../android.os/Bundle.md):contains loudness key/value pairs that can be set directly on the mediaCodec. The listener can modify these values with their own edits which will be returned for the mediaCodec configuration |

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bundle](../android.os/Bundle.md) | a Bundle which contains the original computed codecValues aggregated with user edits. The platform will configure the associated MediaCodecs with the returned Bundle params. |
