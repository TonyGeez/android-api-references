# DrmInfoStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfoStatus

Kotlin| [Java](../android/drm/DrmInfoStatus.md) 
| --- | --- |

```
open class DrmInfoStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmInfoStatus](../android/drm/DrmInfoStatus.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android/media/MediaDrm.md)

An entity class that wraps the result of communication between a device and an online DRM server. Specifically, when the [DrmManagerClient.processDrmInfo()](../android/drm/DrmManagerClient.md))method is called, an instance of`DrmInfoStatus`is returned.

This class contains the [ProcessedData](../android/drm/ProcessedData.md) object, which can be used to instantiate a [DrmRights](../android/drm/DrmRights.md) object during license acquisition.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](../android/drm/DrmInfoStatus.md) Indicate failed communication. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_OK](../android/drm/DrmInfoStatus.md) Indicate successful communication. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfoStatus](../android/drm/DrmInfoStatus.md))`(`statusCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ProcessedData](../android/drm/ProcessedData.md)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfoStatus`object with the specified parameters. |

| Properties ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [ProcessedData](../android/drm/ProcessedData.md)! | [data](../android/drm/DrmInfoStatus.md) The processed data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [infoType](../android/drm/DrmInfoStatus.md) The type of DRM information processed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [mimeType](../android/drm/DrmInfoStatus.md) The MIME type of the content. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [statusCode](../android/drm/DrmInfoStatus.md) The status of the communication. |

## Constants

### STATUS_ERROR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Indicate failed communication. 

 Value: 2

### STATUS_OK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_OK: Int
```

**Deprecated:** *Deprecated in Java.*

Indicate successful communication. 

 Value: 1

## Public constructors

### DrmInfoStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmInfoStatus(
    statusCode: Int, 
    infoType: Int, 
    data: ProcessedData!, 
    mimeType: String!)
```

Creates a`DrmInfoStatus`object with the specified parameters.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The status of the communication. Must be one of the defined status constants above. |
| `infoType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of the DRM information processed. Must be a valid type for [DrmInfoRequest](../android/drm/DrmInfoRequest.md). |
| `data` | [ProcessedData](../android/drm/ProcessedData.md)!:The processed data. |
| --- | --- |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The MIME type. |

## Properties

### data

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val data: ProcessedData!
```

**Deprecated:** *Deprecated in Java.*

The processed data. It is optional and thus could be null. When it is null, it indicates that a particular call to [DrmManagerClient.processDrmInfo()](../android/drm/DrmManagerClient.md))does not return any additional useful information except for the status code. 

### infoType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val infoType: Int
```

**Deprecated:** *Deprecated in Java.*

The type of DRM information processed. Must be one of the valid type constants defined in [DrmInfoRequest](../android/drm/DrmInfoRequest.md). 

### mimeType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val mimeType: String!
```

**Deprecated:** *Deprecated in Java.*

The MIME type of the content. Must not be null or an empty string. 

### statusCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val statusCode: Int
```

**Deprecated:** *Deprecated in Java.*

The status of the communication. Must be one of the defined status constants above.
