# AudioMetadata

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AudioMetadata

Kotlin| [Java](AudioMetadata.md) 
| --- | --- |

```
class AudioMetadata
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.AudioMetadata](AudioMetadata.md) |

AudioMetadata class is used to manage typed key-value pairs for configuration and capability requests within the Audio Framework.

## Summary

| Nested classes ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| | [Format](../android/media/AudioMetadata.Format.md) A container class for AudioMetadata Format keys. |
| abstract | [Key](../android/media/AudioMetadata.Key.md) Key interface for the`AudioMetadata`map. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [AudioMetadataMap](AudioMetadataMap.md) | [createMap](AudioMetadata.md))`()` Creates a [AudioMetadataMap](AudioMetadataMap.md) suitable for adding keys. |

## Public methods

### createMap

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun createMap(): AudioMetadataMap
```

Creates a [AudioMetadataMap](AudioMetadataMap.md) suitable for adding keys.

| Return ||
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [AudioMetadataMap](AudioMetadataMap.md) | an empty [AudioMetadataMap](AudioMetadataMap.md) instance. This value cannot be`null`. |
