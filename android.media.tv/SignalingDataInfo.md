# SignalingDataInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalingDataInfo

Kotlin| [Java](SignalingDataInfo.md) 
| --- | --- |

```
class SignalingDataInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.SignalingDataInfo](SignalingDataInfo.md) |

Describes a metadata object of a [SignalingDataResponse](SignalingDataResponse.md).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_ENCODING_BASE64](SignalingDataInfo.md) A/344:2023-5 9. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_ENCODING_UTF_8](SignalingDataInfo.md) The encoding of the content is UTF-8. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LLS_NO_GROUP_ID](SignalingDataInfo.md) This value for [getGroup()](SignalingDataInfo.md))denotes that there's no group associated with this metadata. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SignalingDataInfo](SignalingDataInfo.md))`(`table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signalingDataType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [SignalingDataInfo](SignalingDataInfo.md))`(`table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signalingDataType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SignalingDataInfo.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getEncoding](SignalingDataInfo.md))`()` The content encoding of the data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroup](SignalingDataInfo.md))`()` Gets the LLS group ID. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getSignalingDataType](SignalingDataInfo.md))`()` Gets the signaling data type contained in this metadata object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTable](SignalingDataInfo.md))`()` The signaling table data, represented as a XML, JSON or BASE64 string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](SignalingDataInfo.md))`()` Gets the version of the signalling element. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SignalingDataInfo.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SignalingDataInfo](SignalingDataInfo.md)!\> | [CREATOR](SignalingDataInfo.md) <br /> |

## Constants

### CONTENT_ENCODING_BASE64

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_ENCODING_BASE64: String
```

A/344:2023-5 9.2.10 compliant string for when the encoding of the content is Base64. 

 Value: "Base64"

### CONTENT_ENCODING_UTF_8

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONTENT_ENCODING_UTF_8: String
```

The encoding of the content is UTF-8. This is the default value. 

 Value: "UTF-8"

### LLS_NO_GROUP_ID

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LLS_NO_GROUP_ID: Int
```

This value for [getGroup()](SignalingDataInfo.md))denotes that there's no group associated with this metadata. 

 Value: -1

## Public constructors

### SignalingDataInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SignalingDataInfo(
    table: String, 
    signalingDataType: String, 
    version: Int, 
    group: Int)
```

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signalingDataType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

### SignalingDataInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SignalingDataInfo(
    table: String, 
    signalingDataType: String, 
    version: Int, 
    group: Int, 
    encoding: String)
```

| Parameters ||
|---------------------|--------------------------------------------------------------------------------------------------------------|
| `table` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `signalingDataType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| `encoding` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getEncoding

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoding(): String
```

The content encoding of the data. This value defaults to [CONTENT_ENCODING_UTF_8](SignalingDataInfo.md).

Can be either [CONTENT_ENCODING_BASE64](SignalingDataInfo.md) or [CONTENT_ENCODING_UTF_8](SignalingDataInfo.md).

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The content encoding of the data. This value cannot be`null`. Value is [android.media.tv.SignalingDataInfo#CONTENT_ENCODING_UTF_8](SignalingDataInfo.md), or [android.media.tv.SignalingDataInfo#CONTENT_ENCODING_BASE64](SignalingDataInfo.md) |

### getGroup

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGroup(): Int
```

Gets the LLS group ID. Required for LLS Tables. For SLS Metadata Objects, this should be [LLS_NO_GROUP_ID](SignalingDataInfo.md).

| Return ||
|----------------------------------------------------------------------------|-------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the LLS group ID. |

### getSignalingDataType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalingDataType(): String
```

Gets the signaling data type contained in this metadata object. This may be either a LLS Metadata Object or a SLS Metadata Object name.

For more details on each type of metadata that can be requested, refer to the ATSC standard A/344:2023-5 9.2.10 - Query Signaling Data API.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the type of metadata in this metadata object This value cannot be`null`. Value is [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_APD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_USBD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_STSID](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_MPD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_USD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_PAT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_MPT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_MPIT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_CRIT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_DCIT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_HELD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_DWD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_AEI](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_VSPD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_ASD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_IED](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_CAD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_ASPD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_SSD](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_EMSG](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_EVTI](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_RSAT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_RDT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_SLT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_RRT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_STT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_AEAT](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_OSN](SignalingDataRequest.md), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_SMT](SignalingDataRequest.md), or [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_CDT](SignalingDataRequest.md) |

### getTable

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTable(): String
```

The signaling table data, represented as a XML, JSON or BASE64 string.

For more details on how this data is formatted refer to the ATSC standard A/344:2023-5 9.2.10 - Query Signaling Data API.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The signaling table data. This value cannot be`null`. |

### getVersion

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Gets the version of the signalling element. For LLS, this should be the LLS_table_version. For SLS Metadata Objects, this should be metadataEnvelope@version. For more details on where this version comes from, refer to the ATSC 3.0 standard A/344:2023-5 9.2.10 - Query Signaling Data API.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The version of the signalling element. |

### writeToParcel

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SignalingDataInfo!>
```
