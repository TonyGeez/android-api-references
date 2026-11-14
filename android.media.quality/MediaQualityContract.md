# MediaQualityContract

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaQualityContract

Kotlin| [Java](MediaQualityContract.md) 
| --- | --- |

```
open class MediaQualityContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.quality.MediaQualityContract](MediaQualityContract.md) |

The contract between the media quality service and applications. Contains definitions for the commonly used parameter names.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [PictureQuality](../android/media/quality/MediaQualityContract.PictureQuality.md) Parameters picture quality. |
| | [SoundQuality](../android/media/quality/MediaQualityContract.SoundQuality.md) Parameters for sound quality. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_HIGH](MediaQualityContract.md) High level option for a parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_LOW](MediaQualityContract.md) Low level option for a parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_MEDIUM](MediaQualityContract.md) Medium level option for a parameter. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_OFF](MediaQualityContract.md) Off level for parameters. |

## Constants

### LEVEL_HIGH

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_HIGH: String
```

High level option for a parameter.

This level represents that the corresponding feature is turned on with the high level option. 

 Value: "level_high"

### LEVEL_LOW

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_LOW: String
```

Low level option for a parameter.

This level represents that the corresponding feature is turned on with the low level option. 

 Value: "level_low"

### LEVEL_MEDIUM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_MEDIUM: String
```

Medium level option for a parameter.

This level represents that the corresponding feature is turned on with the medium level option. 

 Value: "level_medium"

### LEVEL_OFF

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LEVEL_OFF: String
```

Off level for parameters.

This level represents that the corresponding feature is turned off. 

 Value: "level_off"
