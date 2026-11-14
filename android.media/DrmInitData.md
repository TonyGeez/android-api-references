# DrmInitData

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInitData

Kotlin| [Java](https://developer.android.com/reference/android/media/DrmInitData "View this page in Java") 
| --- | --- |

```
abstract class DrmInitData
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.DrmInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData#) |

Encapsulates initialization data required by a [MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm) instance.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------|
| | [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) Scheme initialization data. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [DrmInitData.SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData)! | [get](https://developer.android.com/reference/kotlin/android/media/DrmInitData#get(java.util.UUID))`(`schemeUuid:` ` [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!`)` Retrieves initialization data for a given DRM scheme, specified by its UUID. |
| open [DrmInitData.SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) | [getSchemeInitDataAt](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataAt(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) with the given`index`. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSchemeInitDataCount](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataCount())`()` Returns the number of [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) elements available through [getSchemeInitDataAt](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataAt(kotlin.Int)). |
| --- | --- |

## Public methods

### get

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(schemeUuid: UUID!): DrmInitData.SchemeInitData!
```

**Deprecated:** *Use [getSchemeInitDataCount](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataCount())and [getSchemeInitDataAt](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataAt(kotlin.Int))instead.*

Retrieves initialization data for a given DRM scheme, specified by its UUID.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------|
| `schemeUuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!:The DRM scheme's UUID. |

| Return ||
|------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [DrmInitData.SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData)! | The initialization data for the scheme, or null if the scheme is not supported. |

### getSchemeInitDataAt

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSchemeInitDataAt(index: Int): DrmInitData.SchemeInitData
```

Returns the [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) with the given`index`.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The index of the [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) to return. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DrmInitData.SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) | The [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) associated with the given`index`. This value cannot be`null`. |

| Exceptions ||
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | If the given`index`is negative or greater than [getSchemeInitDataCount](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataCount())`- 1`. |

### getSchemeInitDataCount

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSchemeInitDataCount(): Int
```

Returns the number of [SchemeInitData](https://developer.android.com/reference/kotlin/android/media/DrmInitData.SchemeInitData) elements available through [getSchemeInitDataAt](https://developer.android.com/reference/kotlin/android/media/DrmInitData#getSchemeInitDataAt(kotlin.Int)).
