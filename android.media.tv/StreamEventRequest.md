# StreamEventRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StreamEventRequest

Kotlin| [Java](StreamEventRequest.md) 
| --- | --- |

```
class StreamEventRequest : BroadcastInfoRequest, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoRequest](BroadcastInfoRequest.md) ||
| | ↳ | [android.media.tv.StreamEventRequest](StreamEventRequest.md) |

A request for Stream Event from broadcast signal.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoRequest](BroadcastInfoRequest.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_AUTO_UPDATE](BroadcastInfoRequest.md) <br /> Request option: auto update. With this option, a response is sent only when broadcast information is detected for the first time, new values are detected. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONESHOT](BroadcastInfoRequest.md) <br /> Request option: one-shot With this option, only one response will be given per request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_ONEWAY](BroadcastInfoRequest.md) <br /> Request option: one-way With this option, no response is expected after sending the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_OPTION_REPEAT](BroadcastInfoRequest.md) <br /> Request option: repeat. With this option, a response is sent when related broadcast information is detected, even if the same information has been sent previously. <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [StreamEventRequest](StreamEventRequest.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `option:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `targetUri:` ` [Uri](../android.net/Uri.md)`, `eventName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](StreamEventRequest.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getEventName](StreamEventRequest.md))`()` Gets the name of the event. |
| [Uri](../android.net/Uri.md) | [getTargetUri](StreamEventRequest.md))`()` Gets the URI for the DSM-CC Object or the event description file describing the event. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](StreamEventRequest.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoRequest](BroadcastInfoRequest.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOption](BroadcastInfoRequest.md))`()` <br /> Gets the request option of the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](BroadcastInfoRequest.md))`()` <br /> Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](BroadcastInfoRequest.md))`()` <br /> Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [StreamEventRequest](StreamEventRequest.md)!\> | [CREATOR](StreamEventRequest.md) <br /> |

## Public constructors

### StreamEventRequest

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
StreamEventRequest(
    requestId: Int, 
    option: Int, 
    targetUri: Uri, 
    eventName: String)
```

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `option` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_REPEAT](BroadcastInfoRequest.md), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_AUTO_UPDATE](BroadcastInfoRequest.md), [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONEWAY](BroadcastInfoRequest.md), or [android.media.tv.BroadcastInfoRequest#REQUEST_OPTION_ONESHOT](BroadcastInfoRequest.md) |
| `targetUri` | [Uri](../android.net/Uri.md):This value cannot be`null`. |
| `eventName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| --- | --- |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getEventName

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEventName(): String
```

Gets the name of the event.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. |

### getTargetUri

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTargetUri(): Uri
```

Gets the URI for the DSM-CC Object or the event description file describing the event.

| Return ||
|-----------------------------------------------------------------------------|-----------------------------|
| [Uri](../android.net/Uri.md) | This value cannot be`null`. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<StreamEventRequest!>
```
