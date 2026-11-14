# DrmConvertedStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DrmConvertedStatus

Kotlin| [Java](../android/drm/DrmConvertedStatus.md) 
| --- | --- |

```
open class DrmConvertedStatus
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.drm.DrmConvertedStatus](../android/drm/DrmConvertedStatus.md) |

| **This class was deprecated in API level 30.**
|
| Please use [android.media.MediaDrm](../android/media/MediaDrm.md)

An entity class that wraps converted data, conversion status, and the offset for appending the header and body signature to the converted data. An instance of this class may be created two ways by the drm framework: a) a call to [DrmManagerClient.convertData()](../android/drm/DrmManagerClient.md))and b) a call to [DrmManagerClient.closeConvertSession()](../android/drm/DrmManagerClient.md)). An valid offset value is provided only from a success call to [DrmManagerClient.closeConvertSession()](../android/drm/DrmManagerClient.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_ERROR](../android/drm/DrmConvertedStatus.md) Indicate a general failed conversion status. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_INPUTDATA_ERROR](../android/drm/DrmConvertedStatus.md) Indicate a failed conversion status due to input data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATUS_OK](../android/drm/DrmConvertedStatus.md) Indicate the conversion status is successful. |
| --- | --- |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DrmConvertedStatus](../android/drm/DrmConvertedStatus.md))`(`statusCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `convertedData:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a`DrmConvertedStatus`object with the specified parameters. |

| Properties ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [convertedData](../android/drm/DrmConvertedStatus.md) Converted data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [offset](../android/drm/DrmConvertedStatus.md) Offset value for the body and header signature. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [statusCode](../android/drm/DrmConvertedStatus.md) Status code for the conversion. |
| --- | --- |

## Constants

### STATUS_ERROR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Indicate a general failed conversion status. 

 Value: 3

### STATUS_INPUTDATA_ERROR

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_INPUTDATA_ERROR: Int
```

**Deprecated:** *Deprecated in Java.*

Indicate a failed conversion status due to input data. 

 Value: 2

### STATUS_OK

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATUS_OK: Int
```

**Deprecated:** *Deprecated in Java.*

Indicate the conversion status is successful. 

 Value: 1

## Public constructors

### DrmConvertedStatus

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DrmConvertedStatus(
    statusCode: Int, 
    convertedData: ByteArray!, 
    offset: Int)
```

Creates a`DrmConvertedStatus`object with the specified parameters.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| `statusCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Conversion status. Must be one of the status code constants defined above. |
| `convertedData` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:Converted data. It can be null. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Offset value for appending the header and body signature. |
| --- | --- |

## Properties

### convertedData

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val convertedData: ByteArray!
```

**Deprecated:** *Deprecated in Java.*

Converted data. It is optional and thus can be null. 

### offset

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val offset: Int
```

**Deprecated:** *Deprecated in Java.*

Offset value for the body and header signature. 

### statusCode

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
val statusCode: Int
```

**Deprecated:** *Deprecated in Java.*

Status code for the conversion. Must be one of the defined status constants above.
