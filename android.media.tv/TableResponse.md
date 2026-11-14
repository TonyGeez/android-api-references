# TableResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TableResponse

Kotlin | [Java](https://developer.android.com/reference/android/media/tv/TableResponse "View this page in Java") 
| --- | --- |

```
class TableResponse : BroadcastInfoResponse, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoResponse](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse) ||
| | ↳ | [android.media.tv.TableResponse](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#) |

A response for Table from broadcast signal.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse.Builder) Builder for [TableResponse](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoResponse](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_CANCEL](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int) Response result: cancel. This means the request has been cancelled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int) Response result: error. This means the request can not be set up successfully. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_OK](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int) Response result: OK. This means the request is set up successfully and the related responses are normal responses. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TableResponse](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#TableResponse(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.net.Uri,%20kotlin.Int,%20kotlin.Int))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequence:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableUri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a TableResponse with a table URI. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#getSize())`()` Gets the Size number of table. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getTableByteArray](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#getTableByteArray())`()` Gets the data of the table as a byte array. |
| --- | --- |
| [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#)? | [getTableSharedMemory](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#getTableSharedMemory())`()` Gets the data of the table as a [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#) object. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | [getTableUri](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#getTableUri())`()` Gets the URI in TvProvider database. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#getVersion())`()` Gets the version number of requested table. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoResponse](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getRequestId())`()` Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseResult](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getResponseResult())`()` Gets the result for the response. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getSequence())`()` Gets the sequence number which indicates the order of related responses. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getType())`()` Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TableResponse](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### TableResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TableResponse(
    requestId: Int, 
    sequence: Int, 
    responseResult: Int, 
    tableUri: Uri?, 
    version: Int, 
    size: Int)
```

**Deprecated:** *use [Builder](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse.Builder) instead.*

Constructs a TableResponse with a table URI.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ID is used to associate the response with the request. |
| `sequence` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The sequence number which indicates the order of related responses. |
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The result for the response. It's one of [RESPONSE_RESULT_OK](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int), [RESPONSE_RESULT_CANCEL](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int), [RESPONSE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int). Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int) |
| --- | --- |
| `tableUri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The URI of the table in the database. This value may be `null`. |
| `version` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The version number of requested table. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Size number of table in bytes. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getSize

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSize(): Int
```

Gets the Size number of table. 

### getTableByteArray

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTableByteArray(): ByteArray?
```

Gets the data of the table as a byte array.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | the table data as a byte array, or `null` if the data is not stored as a byte array. |

### getTableSharedMemory

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTableSharedMemory(): SharedMemory?
```

Gets the data of the table as a [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#) object.

This data lives in a [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#) instance because of the potentially large amount of data needed to store the table. This optimizes the data communication between the table data source and the receiver.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#)? | the table data as a [SharedMemory](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#) object, or `null` if the data is not stored in shared memory. |

**See Also**

- [android.os.SharedMemory#map(int, int, int)](https://developer.android.com/reference/kotlin/android/os/SharedMemory.html#map(kotlin.Int,%20kotlin.Int,%20kotlin.Int)) 

### getTableUri

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTableUri(): Uri?
```

Gets the URI in TvProvider database.

| Return ||
|------------------------------------------------------------------------------|---------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)? | This value may be `null`. |

### getVersion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Gets the version number of requested table. If it is null, value will be -1.

The consistency of version numbers between request and response depends on [BroadcastInfoRequest.getOption()](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getOption()). If the request has RequestOption value REQUEST_OPTION_AUTO_UPDATE, then the response may be set to the latest version which may be different from the version of the request. Otherwise, response with a different version from its request will be considered invalid. 

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TableResponse!>
```
