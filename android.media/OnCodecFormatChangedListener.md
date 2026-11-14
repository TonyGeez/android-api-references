# AudioTrack.OnCodecFormatChangedListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCodecFormatChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioTrack.OnCodecFormatChangedListener "View this page in Java") 

```
interface OnCodecFormatChangedListener
```

| [android.media.AudioTrack.OnCodecFormatChangedListener](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener#) |

Interface definition for a listener for codec format changes.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCodecFormatChanged](https://developer.android.com/reference/kotlin/android/media/AudioTrack.OnCodecFormatChangedListener#onCodecFormatChanged(android.media.AudioTrack,%20android.media.AudioMetadataReadMap))`(`audioTrack:` ` [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack)`, `info:` ` [AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap)?`)` Called when the compressed codec format changes. |

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
| `audioTrack` | [AudioTrack](https://developer.android.com/reference/kotlin/android/media/AudioTrack):is the`AudioTrack`instance associated with the codec. This value cannot be`null`. |
| `info` | [AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap)?:is a [AudioMetadataReadMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataReadMap) of values which contains decoded format changes reported by the codec. Not all hardware codecs indicate codec format changes. Acceptable keys are taken from`AudioMetadata.Format.KEY_*`range, with the associated value type. This value may be`null`. |
