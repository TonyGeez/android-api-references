# BroadcastInfoResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BroadcastInfoResponse

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/BroadcastInfoResponse "View this page in Java") 

```
abstract class BroadcastInfoResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.tv.BroadcastInfoResponse](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#) |

| Known Direct Subclasses [CommandResponse](https://developer.android.com/reference/kotlin/android/media/tv/CommandResponse), [DsmccResponse](https://developer.android.com/reference/kotlin/android/media/tv/DsmccResponse), [PesResponse](https://developer.android.com/reference/kotlin/android/media/tv/PesResponse), [SectionResponse](https://developer.android.com/reference/kotlin/android/media/tv/SectionResponse), [SignalingDataResponse](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataResponse), [StreamEventResponse](https://developer.android.com/reference/kotlin/android/media/tv/StreamEventResponse), [TableResponse](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse), [TimelineResponse](https://developer.android.com/reference/kotlin/android/media/tv/TimelineResponse), [TsResponse](https://developer.android.com/reference/kotlin/android/media/tv/TsResponse) |----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------| | [CommandResponse](https://developer.android.com/reference/kotlin/android/media/tv/CommandResponse) | A response for command from broadcast signal. | | [DsmccResponse](https://developer.android.com/reference/kotlin/android/media/tv/DsmccResponse) | A response for DSM-CC from broadcast signal. | | [PesResponse](https://developer.android.com/reference/kotlin/android/media/tv/PesResponse) | A response for PES from broadcast signal. | | [SectionResponse](https://developer.android.com/reference/kotlin/android/media/tv/SectionResponse) | A response for Section from broadcast signal. | | [SignalingDataResponse](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataResponse) | A response for the signaling data from the broadcast signal. | | [StreamEventResponse](https://developer.android.com/reference/kotlin/android/media/tv/StreamEventResponse) | A response for Stream Event from broadcast signal. | | [TableResponse](https://developer.android.com/reference/kotlin/android/media/tv/TableResponse) | A response for Table from broadcast signal. | | [TimelineResponse](https://developer.android.com/reference/kotlin/android/media/tv/TimelineResponse) | A response for Timeline from broadcast signal. | | [TsResponse](https://developer.android.com/reference/kotlin/android/media/tv/TsResponse) | A response for TS (transport stream) from broadcast signal. | |

A response of [BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest) for information retrieved from broadcast signal.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_CANCEL](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int) Response result: cancel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int) Response result: error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_OK](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int) Response result: OK. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getRequestId())`()` Gets the ID of the request. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseResult](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getResponseResult())`()` Gets the result for the response. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getSequence())`()` Gets the sequence number which indicates the order of related responses. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getType())`()` Gets the broadcast info type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BroadcastInfoResponse](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### RESPONSE_RESULT_CANCEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_RESULT_CANCEL: Int
```

Response result: cancel. This means the request has been cancelled. 

 Value: 3

### RESPONSE_RESULT_ERROR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_RESULT_ERROR: Int
```

Response result: error. This means the request can not be set up successfully. 

 Value: 1

### RESPONSE_RESULT_OK

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val RESPONSE_RESULT_OK: Int
```

Response result: OK. This means the request is set up successfully and the related responses are normal responses. 

 Value: 2

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getRequestId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestId(): Int
```

Gets the ID of the request.

The ID is used to associate the response with the request. 
**See Also**

- [android.media.tv.BroadcastInfoRequest#getRequestId()](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getRequestId()) 

### getResponseResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResponseResult(): Int
```

Gets the result for the response.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int) |

**See Also**

- [#RESPONSE_RESULT_OK](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int)
- [#RESPONSE_RESULT_ERROR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int)
- [#RESPONSE_RESULT_CANCEL](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int) 

### getSequence

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSequence(): Int
```

Gets the sequence number which indicates the order of related responses. 

### getType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

Gets the broadcast info type.

The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TS](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_TS:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TABLE](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_TABLE:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_SECTION](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_SECTION:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_PES](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_PES:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_STREAM_EVENT](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_STREAM_EVENT:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_DSMCC](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_DSMCC:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_COMMAND](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_COMMAND:kotlin.Int), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TIMELINE](https://developer.android.com/reference/kotlin/android/media/tv/TvInputManager#BROADCAST_INFO_TYPE_TIMELINE:kotlin.Int), or android.media.tv.TvInputManager.BROADCAST_INFO_TYPE_SIGNALING_DATA |

### writeToParcel

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
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

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BroadcastInfoResponse!>
```
