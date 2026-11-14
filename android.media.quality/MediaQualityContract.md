# MediaQualityContract

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaQualityContract

Kotlin| [Java](https://developer.android.com/reference/android/media/quality/MediaQualityContract "View this page in Java") 

```
open class MediaQualityContract
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.quality.MediaQualityContract](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract#) |

The contract between the media quality service and applications. Contains definitions for the commonly used parameter names.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [PictureQuality](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract.PictureQuality) Parameters picture quality. |
| | [SoundQuality](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract.SoundQuality) Parameters for sound quality. |

| Constants ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_HIGH](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract#LEVEL_HIGH:kotlin.String) High level option for a parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_LOW](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract#LEVEL_LOW:kotlin.String) Low level option for a parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_MEDIUM](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract#LEVEL_MEDIUM:kotlin.String) Medium level option for a parameter. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [LEVEL_OFF](https://developer.android.com/reference/kotlin/android/media/quality/MediaQualityContract#LEVEL_OFF:kotlin.String) Off level for parameters. |

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
