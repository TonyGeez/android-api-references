# SignalingDataInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalingDataInfo

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/SignalingDataInfo "View this page in Java") 
| --- | --- |

```
class SignalingDataInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.SignalingDataInfo](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#) |

Describes a metadata object of a [SignalingDataResponse](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataResponse).

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_ENCODING_BASE64](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_BASE64:kotlin.String) A/344:2023-5 9. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONTENT_ENCODING_UTF_8](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_UTF_8:kotlin.String) The encoding of the content is UTF-8. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LLS_NO_GROUP_ID](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#LLS_NO_GROUP_ID:kotlin.Int) This value for [getGroup()](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getGroup())denotes that there's no group associated with this metadata. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SignalingDataInfo](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#SignalingDataInfo(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signalingDataType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [SignalingDataInfo](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#SignalingDataInfo(kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int,%20kotlin.String))`(`table:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `signalingDataType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `group:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `encoding:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#describeContents())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getEncoding](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getEncoding())`()` The content encoding of the data. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGroup](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getGroup())`()` Gets the LLS group ID. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getSignalingDataType](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getSignalingDataType())`()` Gets the signaling data type contained in this metadata object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTable](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getTable())`()` The signaling table data, represented as a XML, JSON or BASE64 string. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getVersion())`()` Gets the version of the signalling element. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SignalingDataInfo](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

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

This value for [getGroup()](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#getGroup())denotes that there's no group associated with this metadata. 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getEncoding

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEncoding(): String
```

The content encoding of the data. This value defaults to [CONTENT_ENCODING_UTF_8](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_UTF_8:kotlin.String).

Can be either [CONTENT_ENCODING_BASE64](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_BASE64:kotlin.String) or [CONTENT_ENCODING_UTF_8](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_UTF_8:kotlin.String).

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The content encoding of the data. This value cannot be`null`. Value is [android.media.tv.SignalingDataInfo#CONTENT_ENCODING_UTF_8](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_UTF_8:kotlin.String), or [android.media.tv.SignalingDataInfo#CONTENT_ENCODING_BASE64](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#CONTENT_ENCODING_BASE64:kotlin.String) |

### getGroup

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGroup(): Int
```

Gets the LLS group ID. Required for LLS Tables. For SLS Metadata Objects, this should be [LLS_NO_GROUP_ID](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataInfo#LLS_NO_GROUP_ID:kotlin.Int).

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
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the type of metadata in this metadata object This value cannot be`null`. Value is [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_APD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_APD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_USBD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_USBD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_STSID](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_STSID:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_MPD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_MPD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_USD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_USD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_PAT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_PAT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_MPT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_MPT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_MPIT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_MPIT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_CRIT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_CRIT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_DCIT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_DCIT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_HELD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_HELD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_DWD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_DWD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_AEI](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_AEI:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_VSPD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_VSPD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_ASD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_ASD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_IED](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_IED:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_CAD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_CAD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_ASPD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_ASPD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_SSD](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_SSD:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_EMSG](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_EMSG:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_EVTI](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_EVTI:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_RSAT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_RSAT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_RDT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_RDT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_SLT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_SLT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_RRT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_RRT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_STT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_STT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_AEAT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_AEAT:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_OSN](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_OSN:kotlin.String), [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_SMT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_SMT:kotlin.String), or [android.media.tv.SignalingDataRequest#SIGNALING_METADATA_CDT](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest#SIGNALING_METADATA_CDT:kotlin.String) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SignalingDataInfo!>
```
