# DrmInfoStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmInfoStatus

Kotlin| [Java](https://developer.android.com/reference/android/drm/DrmInfoStatus "View this page in Java") 
| --- | --- |

```
open class DrmInfoStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmInfoStatus](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](https://developer.android.com/reference/kotlin/android/media/MediaDrm.html#)

An entity class that wraps the result of communication between a device and an online DRM server. Specifically, when the [DrmManagerClient.processDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo))method is called, an instance of`DrmInfoStatus`is returned.

This class contains the [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData) object, which can be used to instantiate a [DrmRights](https://developer.android.com/reference/kotlin/android/drm/DrmRights) object during license acquisition.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#STATUS_ERROR:kotlin.Int) Indicate failed communication. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_OK](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#STATUS_OK:kotlin.Int) Indicate successful communication. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmInfoStatus](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#DrmInfoStatus(kotlin.Int,%20kotlin.Int,%20android.drm.ProcessedData,%20kotlin.String))`(`statusCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `infoType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData)!`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Creates a`DrmInfoStatus`object with the specified parameters. |

| Properties ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData)! | [data](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#data:android.drm.ProcessedData) The processed data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [infoType](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#infoType:kotlin.Int) The type of DRM information processed. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [mimeType](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#mimeType:kotlin.String) The MIME type of the content. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [statusCode](https://developer.android.com/reference/kotlin/android/drm/DrmInfoStatus#statusCode:kotlin.Int) The status of the communication. |

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
| `infoType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of the DRM information processed. Must be a valid type for [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest). |
| `data` | [ProcessedData](https://developer.android.com/reference/kotlin/android/drm/ProcessedData)!:The processed data. |
| --- | --- |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The MIME type. |

## Properties

### data

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val data: ProcessedData!
```

**Deprecated:** *Deprecated in Java.*

The processed data. It is optional and thus could be null. When it is null, it indicates that a particular call to [DrmManagerClient.processDrmInfo()](https://developer.android.com/reference/kotlin/android/drm/DrmManagerClient#processDrmInfo(android.drm.DrmInfo))does not return any additional useful information except for the status code. 

### infoType

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val infoType: Int
```

**Deprecated:** *Deprecated in Java.*

The type of DRM information processed. Must be one of the valid type constants defined in [DrmInfoRequest](https://developer.android.com/reference/kotlin/android/drm/DrmInfoRequest). 

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
