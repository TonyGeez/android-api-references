# TableResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TableResponse

Kotlin | [Java](TableResponse.md) 
| --- | --- |

```
class TableResponse : BroadcastInfoResponse, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoResponse](BroadcastInfoResponse.md) ||
| | ↳ | [android.media.tv.TableResponse](TableResponse.md) |

A response for Table from broadcast signal.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/media/tv/TableResponse.Builder.md) Builder for [TableResponse](TableResponse.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoResponse](BroadcastInfoResponse.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) Response result: cancel. This means the request has been cancelled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md) Response result: error. This means the request can not be set up successfully. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_OK](BroadcastInfoResponse.md) Response result: OK. This means the request is set up successfully and the related responses are normal responses. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TableResponse](TableResponse.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequence:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `tableUri:` ` [Uri](../android.net/Uri.md)?`, `version:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Constructs a TableResponse with a table URI. |

| Public methods ||
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](TableResponse.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](TableResponse.md))`()` Gets the Size number of table. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getTableByteArray](TableResponse.md))`()` Gets the data of the table as a byte array. |
| --- | --- |
| [SharedMemory](../android.os/SharedMemory.md)? | [getTableSharedMemory](TableResponse.md))`()` Gets the data of the table as a [SharedMemory](../android.os/SharedMemory.md) object. |
| [Uri](../android.net/Uri.md)? | [getTableUri](TableResponse.md))`()` Gets the URI in TvProvider database. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getVersion](TableResponse.md))`()` Gets the version number of requested table. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](TableResponse.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoResponse](BroadcastInfoResponse.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](BroadcastInfoResponse.md))`()` Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseResult](BroadcastInfoResponse.md))`()` Gets the result for the response. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](BroadcastInfoResponse.md))`()` Gets the sequence number which indicates the order of related responses. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](BroadcastInfoResponse.md))`()` Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TableResponse](TableResponse.md)!\> | [CREATOR](TableResponse.md) <br /> |

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

**Deprecated:** *use [Builder](../android/media/tv/TableResponse.Builder.md) instead.*

Constructs a TableResponse with a table URI.

| Parameters ||
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The ID is used to associate the response with the request. |
| `sequence` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The sequence number which indicates the order of related responses. |
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The result for the response. It's one of [RESPONSE_RESULT_OK](BroadcastInfoResponse.md), [RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md), [RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md). Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](BroadcastInfoResponse.md), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) |
| --- | --- |
| `tableUri` | [Uri](../android.net/Uri.md)?: The URI of the table in the database. This value may be `null`. |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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

Gets the data of the table as a [SharedMemory](../android.os/SharedMemory.md) object.

This data lives in a [SharedMemory](../android.os/SharedMemory.md) instance because of the potentially large amount of data needed to store the table. This optimizes the data communication between the table data source and the receiver.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SharedMemory](../android.os/SharedMemory.md)? | the table data as a [SharedMemory](../android.os/SharedMemory.md) object, or `null` if the data is not stored in shared memory. |

**See Also**

- [android.os.SharedMemory#map(int, int, int)](../android.os/SharedMemory.md)) 

### getTableUri

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTableUri(): Uri?
```

Gets the URI in TvProvider database.

| Return ||
|------------------------------------------------------------------------------|---------------------------|
| [Uri](../android.net/Uri.md)? | This value may be `null`. |

### getVersion

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getVersion(): Int
```

Gets the version number of requested table. If it is null, value will be -1.

The consistency of version numbers between request and response depends on [BroadcastInfoRequest.getOption()](BroadcastInfoRequest.md)). If the request has RequestOption value REQUEST_OPTION_AUTO_UPDATE, then the response may be set to the latest version which may be different from the version of the request. Otherwise, response with a different version from its request will be considered invalid. 

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TableResponse!>
```
