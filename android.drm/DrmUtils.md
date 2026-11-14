# DrmUtils

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmUtils

Kotlin | [Java](../android/drm/DrmUtils.md) 
| --- | --- |

```
open class DrmUtils
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmUtils](../android/drm/DrmUtils.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android/media/MediaDrm.md)

A utility class that provides operations for parsing extended metadata embedded in DRM constraint information. If a DRM scheme has specific constraints beyond the standard constraints, the constraints will show up in the [DrmStore.ConstraintsColumns.EXTENDED_METADATA](../android/drm/DrmStore.ConstraintsColumns.md) key. You can use [DrmUtils.ExtendedMetadataParser](../android/drm/DrmUtils.ExtendedMetadataParser.md) to iterate over those values.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [ExtendedMetadataParser](../android/drm/DrmUtils.ExtendedMetadataParser.md) Utility that parses extended metadata embedded in DRM constraint information. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------|---|
| [DrmUtils](../android/drm/DrmUtils.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open static [DrmUtils.ExtendedMetadataParser](../android/drm/DrmUtils.ExtendedMetadataParser.md)! | [getExtendedMetadataParser](../android/drm/DrmUtils.md))`(`extendedMetadata:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Gets an instance of [DrmUtils.ExtendedMetadataParser](../android/drm/DrmUtils.ExtendedMetadataParser.md), which can be used to parse extended metadata embedded in DRM constraint information. |

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

Gets an instance of [DrmUtils.ExtendedMetadataParser](../android/drm/DrmUtils.ExtendedMetadataParser.md), which can be used to parse extended metadata embedded in DRM constraint information.

| Parameters ||
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `extendedMetadata` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Object in which key-value pairs of extended metadata are embedded. |
