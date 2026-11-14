# BroadcastInfoResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BroadcastInfoResponse

Kotlin| [Java](BroadcastInfoResponse.md) 
| --- | --- |

```
abstract class BroadcastInfoResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.BroadcastInfoResponse](BroadcastInfoResponse.md) |

| Known Direct Subclasses [CommandResponse](CommandResponse.md), [DsmccResponse](DsmccResponse.md), [PesResponse](PesResponse.md), [SectionResponse](SectionResponse.md), [SignalingDataResponse](SignalingDataResponse.md), [StreamEventResponse](StreamEventResponse.md), [TableResponse](TableResponse.md), [TimelineResponse](TimelineResponse.md), [TsResponse](TsResponse.md) |----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------| | [CommandResponse](CommandResponse.md) | A response for command from broadcast signal. | | [DsmccResponse](DsmccResponse.md) | A response for DSM-CC from broadcast signal. | | [PesResponse](PesResponse.md) | A response for PES from broadcast signal. | | [SectionResponse](SectionResponse.md) | A response for Section from broadcast signal. | | [SignalingDataResponse](SignalingDataResponse.md) | A response for the signaling data from the broadcast signal. | | [StreamEventResponse](StreamEventResponse.md) | A response for Stream Event from broadcast signal. | | [TableResponse](TableResponse.md) | A response for Table from broadcast signal. | | [TimelineResponse](TimelineResponse.md) | A response for Timeline from broadcast signal. | | [TsResponse](TsResponse.md) | A response for TS (transport stream) from broadcast signal. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A response of [BroadcastInfoRequest](BroadcastInfoRequest.md) for information retrieved from broadcast signal.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) Response result: cancel. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md) Response result: error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_OK](BroadcastInfoResponse.md) Response result: OK. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](BroadcastInfoResponse.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](BroadcastInfoResponse.md))`()` Gets the ID of the request. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseResult](BroadcastInfoResponse.md))`()` Gets the result for the response. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](BroadcastInfoResponse.md))`()` Gets the sequence number which indicates the order of related responses. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](BroadcastInfoResponse.md))`()` Gets the broadcast info type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](BroadcastInfoResponse.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BroadcastInfoResponse](BroadcastInfoResponse.md)!\> | [CREATOR](BroadcastInfoResponse.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getRequestId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestId(): Int
```

Gets the ID of the request.

The ID is used to associate the response with the request. 
**See Also**

- [android.media.tv.BroadcastInfoRequest#getRequestId()](BroadcastInfoRequest.md)) 

### getResponseResult

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getResponseResult(): Int
```

Gets the result for the response.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](BroadcastInfoResponse.md), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) |

**See Also**

- [#RESPONSE_RESULT_OK](BroadcastInfoResponse.md)
- [#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md)
- [#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) 

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TS](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TABLE](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_SECTION](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_PES](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_STREAM_EVENT](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_DSMCC](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_COMMAND](TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TIMELINE](TvInputManager.md), or android.media.tv.TvInputManager.BROADCAST_INFO_TYPE_SIGNALING_DATA |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BroadcastInfoResponse!>
```
