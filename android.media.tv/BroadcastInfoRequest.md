# BroadcastInfoRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BroadcastInfoRequest

Kotlin| [Java](../android/media/tv/BroadcastInfoRequest.md) 
| --- | --- |

```
abstract class BroadcastInfoRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.BroadcastInfoRequest](../android/media/tv/BroadcastInfoRequest.md) |

| Known Direct Subclasses [CommandRequest](../android/media/tv/CommandRequest.md), [DsmccRequest](../android/media/tv/DsmccRequest.md), [PesRequest](../android/media/tv/PesRequest.md), [SectionRequest](../android/media/tv/SectionRequest.md), [SignalingDataRequest](../android/media/tv/SignalingDataRequest.md), [StreamEventRequest](../android/media/tv/StreamEventRequest.md), [TableRequest](../android/media/tv/TableRequest.md), [TimelineRequest](../android/media/tv/TimelineRequest.md), [TsRequest](../android/media/tv/TsRequest.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [CommandRequest](../android/media/tv/CommandRequest.md) | A request for command from broadcast signal. | | [DsmccRequest](../android/media/tv/DsmccRequest.md) | A request for DSM-CC from broadcast signal. | | [PesRequest](../android/media/tv/PesRequest.md) | A request for PES from broadcast signal. | | [SectionRequest](../android/media/tv/SectionRequest.md) | A request for Section from broadcast signal. | | [SignalingDataRequest](../android/media/tv/SignalingDataRequest.md) | Request to retrieve the Low-level Signalling Tables (LLS) and Service-layer Signalling (SLS) metadata. | | [StreamEventRequest](../android/media/tv/StreamEventRequest.md) | A request for Stream Event from broadcast signal. | | [TableRequest](../android/media/tv/TableRequest.md) | A request for Table from broadcast signal. | | [TimelineRequest](../android/media/tv/TimelineRequest.md) | A request for Timeline from broadcast signal. | | [TsRequest](../android/media/tv/TsRequest.md) | A request for TS (transport stream) from broadcast signal. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A request for the information retrieved from broadcast signal.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_AUTO_UPDATE](../android/media/tv/BroadcastInfoRequest.md) Request option: auto update. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONESHOT](../android/media/tv/BroadcastInfoRequest.md) Request option: one-shot |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONEWAY](../android/media/tv/BroadcastInfoRequest.md) Request option: one-way |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_REPEAT](../android/media/tv/BroadcastInfoRequest.md) Request option: repeat. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/media/tv/BroadcastInfoRequest.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOption](../android/media/tv/BroadcastInfoRequest.md))`()` Gets the request option of the request. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](../android/media/tv/BroadcastInfoRequest.md))`()` Gets the ID of the request. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](../android/media/tv/BroadcastInfoRequest.md))`()` Gets the broadcast info type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/media/tv/BroadcastInfoRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [BroadcastInfoRequest](../android/media/tv/BroadcastInfoRequest.md)!\> | [CREATOR](../android/media/tv/BroadcastInfoRequest.md) <br /> |

## Constants

### REQUEST_OPTION_AUTO_UPDATE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_OPTION_AUTO_UPDATE: Int
```

Request option: auto update.

With this option, a response is sent only when broadcast information is detected for the first time, new values are detected. 

 Value: 1

### REQUEST_OPTION_ONESHOT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_OPTION_ONESHOT: Int
```

Request option: one-shot

With this option, only one response will be given per request. 

 Value: 3

### REQUEST_OPTION_ONEWAY

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_OPTION_ONEWAY: Int
```

Request option: one-way

With this option, no response is expected after sending the request. 

 Value: 2

### REQUEST_OPTION_REPEAT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_OPTION_REPEAT: Int
```

Request option: repeat.

With this option, a response is sent when related broadcast information is detected, even if the same information has been sent previously. 

 Value: 0

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOption(): Int
```

Gets the request option of the request.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_REPEAT](../android/media/tv/BroadcastInfoRequest.md), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE](../android/media/tv/BroadcastInfoRequest.md), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONEWAY](../android/media/tv/BroadcastInfoRequest.md), or [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONESHOT](../android/media/tv/BroadcastInfoRequest.md) |

**See Also**

- [#REQUEST_OPTION_REPEAT](../android/media/tv/BroadcastInfoRequest.md)
- [#REQUEST_OPTION_AUTO_UPDATE](../android/media/tv/BroadcastInfoRequest.md) 

### getRequestId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestId(): Int
```

Gets the ID of the request.

The ID is used to associate the response with the request. 
**See Also**

- [android.media.tv.BroadcastInfoResponse#getRequestId()](../android/media/tv/BroadcastInfoResponse.md)) 

### getType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getType(): Int
```

Gets the broadcast info type.

The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TS](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TABLE](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_SECTION](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_PES](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_STREAM_EVENT](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_DSMCC](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_COMMAND](../android/media/tv/TvInputManager.md), [android.media.tv.TvInputManager#BROADCAST_INFO_TYPE_TIMELINE](../android/media/tv/TvInputManager.md), or android.media.tv.TvInputManager.BROADCAST_INFO_TYPE_SIGNALING_DATA |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BroadcastInfoRequest!>
```
