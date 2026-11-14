# AudioMetadata

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioMetadata

Kotlin| [Java](https://developer.android.com/reference/android/media/AudioMetadata "View this page in Java") 

```
class AudioMetadata
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.AudioMetadata](https://developer.android.com/reference/kotlin/android/media/AudioMetadata#) |

AudioMetadata class is used to manage typed key-value pairs for configuration and capability requests within the Audio Framework.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| | [Format](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Format) A container class for AudioMetadata Format keys. |
| abstract | [Key](https://developer.android.com/reference/kotlin/android/media/AudioMetadata.Key) Key interface for the`AudioMetadata`map. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) | [createMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadata#createMap())`()` Creates a [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) suitable for adding keys. |

## Public methods

### createMap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createMap(): AudioMetadataMap
```

Creates a [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) suitable for adding keys.

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) | an empty [AudioMetadataMap](https://developer.android.com/reference/kotlin/android/media/AudioMetadataMap) instance. This value cannot be`null`. |
