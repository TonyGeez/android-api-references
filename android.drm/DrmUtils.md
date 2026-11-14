# DrmUtils

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmUtils

Kotlin | [Java](https://developer.android.com/reference/android/drm/DrmUtils "View this page in Java") 

```
open class DrmUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.drm.DrmUtils](https://developer.android.com/reference/kotlin/android/drm/DrmUtils#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

A utility class that provides operations for parsing extended metadata embedded in DRM constraint information. If a DRM scheme has specific constraints beyond the standard constraints, the constraints will show up in the [DrmStore.ConstraintsColumns.EXTENDED_METADATA](https://developer.android.com/reference/kotlin/android/drm/DrmStore.ConstraintsColumns#EXTENDED_METADATA:kotlin.String) key. You can use [DrmUtils.ExtendedMetadataParser](https://developer.android.com/reference/kotlin/android/drm/DrmUtils.ExtendedMetadataParser) to iterate over those values.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ExtendedMetadataParser](https://developer.android.com/reference/kotlin/android/drm/DrmUtils.ExtendedMetadataParser) Utility that parses extended metadata embedded in DRM constraint information. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------|---|
| [DrmUtils](https://developer.android.com/reference/kotlin/android/drm/DrmUtils#DrmUtils())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [DrmUtils.ExtendedMetadataParser](https://developer.android.com/reference/kotlin/android/drm/DrmUtils.ExtendedMetadataParser)! | [getExtendedMetadataParser](https://developer.android.com/reference/kotlin/android/drm/DrmUtils#getExtendedMetadataParser(kotlin.ByteArray))`(`extendedMetadata:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Gets an instance of [DrmUtils.ExtendedMetadataParser](https://developer.android.com/reference/kotlin/android/drm/DrmUtils.ExtendedMetadataParser), which can be used to parse extended metadata embedded in DRM constraint information. |

## Public constructors

### DrmUtils

```
DrmUtils()
```

## Public methods

### getExtendedMetadataParser

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getExtendedMetadataParser(extendedMetadata: ByteArray!): DrmUtils.ExtendedMetadataParser!
```

**Deprecated:** *Deprecated in Java.*

Gets an instance of [DrmUtils.ExtendedMetadataParser](https://developer.android.com/reference/kotlin/android/drm/DrmUtils.ExtendedMetadataParser), which can be used to parse extended metadata embedded in DRM constraint information.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extendedMetadata` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Object in which key-value pairs of extended metadata are embedded. |
