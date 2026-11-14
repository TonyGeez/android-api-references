# BroadcastInfoRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BroadcastInfoRequest

Kotlin| [Java](https://developer.android.com/reference/android/media/tv/BroadcastInfoRequest "View this page in Java") 
| --- | --- |

```
abstract class BroadcastInfoRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.media.tv.BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#) |

| Known Direct Subclasses [CommandRequest](https://developer.android.com/reference/kotlin/android/media/tv/CommandRequest), [DsmccRequest](https://developer.android.com/reference/kotlin/android/media/tv/DsmccRequest), [PesRequest](https://developer.android.com/reference/kotlin/android/media/tv/PesRequest), [SectionRequest](https://developer.android.com/reference/kotlin/android/media/tv/SectionRequest), [SignalingDataRequest](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest), [StreamEventRequest](https://developer.android.com/reference/kotlin/android/media/tv/StreamEventRequest), [TableRequest](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest), [TimelineRequest](https://developer.android.com/reference/kotlin/android/media/tv/TimelineRequest), [TsRequest](https://developer.android.com/reference/kotlin/android/media/tv/TsRequest) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [CommandRequest](https://developer.android.com/reference/kotlin/android/media/tv/CommandRequest) | A request for command from broadcast signal. | | [DsmccRequest](https://developer.android.com/reference/kotlin/android/media/tv/DsmccRequest) | A request for DSM-CC from broadcast signal. | | [PesRequest](https://developer.android.com/reference/kotlin/android/media/tv/PesRequest) | A request for PES from broadcast signal. | | [SectionRequest](https://developer.android.com/reference/kotlin/android/media/tv/SectionRequest) | A request for Section from broadcast signal. | | [SignalingDataRequest](https://developer.android.com/reference/kotlin/android/media/tv/SignalingDataRequest) | Request to retrieve the Low-level Signalling Tables (LLS) and Service-layer Signalling (SLS) metadata. | | [StreamEventRequest](https://developer.android.com/reference/kotlin/android/media/tv/StreamEventRequest) | A request for Stream Event from broadcast signal. | | [TableRequest](https://developer.android.com/reference/kotlin/android/media/tv/TableRequest) | A request for Table from broadcast signal. | | [TimelineRequest](https://developer.android.com/reference/kotlin/android/media/tv/TimelineRequest) | A request for Timeline from broadcast signal. | | [TsRequest](https://developer.android.com/reference/kotlin/android/media/tv/TsRequest) | A request for TS (transport stream) from broadcast signal. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A request for the information retrieved from broadcast signal.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_AUTO_UPDATE](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int) Request option: auto update. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONESHOT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONESHOT:kotlin.Int) Request option: one-shot |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONEWAY](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONEWAY:kotlin.Int) Request option: one-way |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_REPEAT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int) Request option: repeat. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOption](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getOption())`()` Gets the request option of the request. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getRequestId())`()` Gets the ID of the request. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#getType())`()` Gets the broadcast info type. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BroadcastInfoRequest](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getOption

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getOption(): Int
```

Gets the request option of the request.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_REPEAT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONEWAY](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONEWAY:kotlin.Int), or [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONESHOT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_ONESHOT:kotlin.Int) |

**See Also**

- [#REQUEST_OPTION_REPEAT](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_REPEAT:kotlin.Int)
- [#REQUEST_OPTION_AUTO_UPDATE](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE:kotlin.Int) 

### getRequestId

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRequestId(): Int
```

Gets the ID of the request.

The ID is used to associate the response with the request. 
**See Also**

- [android.media.tv.BroadcastInfoResponse#getRequestId()](https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getRequestId()) 

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
static val CREATOR: Parcelable.Creator<BroadcastInfoRequest!>
```
