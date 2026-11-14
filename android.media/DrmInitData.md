# DrmInitData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInitData

Kotlin| [Java](../android/media/DrmInitData.md) 
| --- | --- |

```
abstract class DrmInitData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.DrmInitData](../android/media/DrmInitData.md) |

Encapsulates initialization data required by a [MediaDrm](../android/media/MediaDrm.md) instance.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------|
| | [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) Scheme initialization data. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DrmInitData.SchemeInitData](../android/media/DrmInitData.SchemeInitData.md)! | [get](../android/media/DrmInitData.md))`(`schemeUuid:` ` [UUID](../java/util/UUID.md)!`)` Retrieves initialization data for a given DRM scheme, specified by its UUID. |
| open [DrmInitData.SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) | [getSchemeInitDataAt](../android/media/DrmInitData.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) with the given`index`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSchemeInitDataCount](../android/media/DrmInitData.md))`()` Returns the number of [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) elements available through [getSchemeInitDataAt](../android/media/DrmInitData.md)). |
| --- | --- |

## Public methods

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(schemeUuid: UUID!): DrmInitData.SchemeInitData!
```

**Deprecated:** *Use [getSchemeInitDataCount](../android/media/DrmInitData.md))and [getSchemeInitDataAt](../android/media/DrmInitData.md))instead.*

Retrieves initialization data for a given DRM scheme, specified by its UUID.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `schemeUuid` | [UUID](../java/util/UUID.md)!:The DRM scheme's UUID. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [DrmInitData.SchemeInitData](../android/media/DrmInitData.SchemeInitData.md)! | The initialization data for the scheme, or null if the scheme is not supported. |

### getSchemeInitDataAt

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSchemeInitDataAt(index: Int): DrmInitData.SchemeInitData
```

Returns the [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) with the given`index`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) to return. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DrmInitData.SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) | The [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) associated with the given`index`. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the given`index`is negative or greater than [getSchemeInitDataCount](../android/media/DrmInitData.md))`- 1`. |

### getSchemeInitDataCount

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSchemeInitDataCount(): Int
```

Returns the number of [SchemeInitData](../android/media/DrmInitData.SchemeInitData.md) elements available through [getSchemeInitDataAt](../android/media/DrmInitData.md)).
