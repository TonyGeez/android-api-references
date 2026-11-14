# AudioTrack.OnCodecFormatChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCodecFormatChangedListener

Kotlin| [Java](../android/media/AudioTrack.OnCodecFormatChangedListener.md) 
| --- | --- |

```
interface OnCodecFormatChangedListener
```

| [android.media.AudioTrack.OnCodecFormatChangedListener](../android/media/AudioTrack.OnCodecFormatChangedListener.md) |

Interface definition for a listener for codec format changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCodecFormatChanged](../android/media/AudioTrack.OnCodecFormatChangedListener.md))`(`audioTrack:` ` [AudioTrack](AudioTrack.md)`, `info:` ` [AudioMetadataReadMap](AudioMetadataReadMap.md)?`)` Called when the compressed codec format changes. |

## Public methods

### onCodecFormatChanged

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCodecFormatChanged(
    audioTrack: AudioTrack, 
    info: AudioMetadataReadMap?
): Unit
```

Called when the compressed codec format changes.

| Parameters ||
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `audioTrack` | [AudioTrack](AudioTrack.md):is the`AudioTrack`instance associated with the codec. This value cannot be`null`. |
| `info` | [AudioMetadataReadMap](AudioMetadataReadMap.md)?:is a [AudioMetadataReadMap](AudioMetadataReadMap.md) of values which contains decoded format changes reported by the codec. Not all hardware codecs indicate codec format changes. Acceptable keys are taken from`AudioMetadata.Format.KEY_*`range, with the associated value type. This value may be`null`. |
