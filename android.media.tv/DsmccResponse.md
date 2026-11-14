# DsmccResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DsmccResponse

Kotlin | [Java](DsmccResponse.md) 
| --- | --- |

```
class DsmccResponse : BroadcastInfoResponse, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoResponse](BroadcastInfoResponse.md) ||
| | ↳ | [android.media.tv.DsmccResponse](DsmccResponse.md) |

A response for DSM-CC from broadcast signal.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BIOP_MESSAGE_TYPE_DIRECTORY](DsmccResponse.md) BIOP directory message |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BIOP_MESSAGE_TYPE_FILE](DsmccResponse.md) BIOP file message |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BIOP_MESSAGE_TYPE_SERVICE_GATEWAY](DsmccResponse.md) BIOP service gateway message |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [BIOP_MESSAGE_TYPE_STREAM](DsmccResponse.md) BIOP stream message |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoResponse](BroadcastInfoResponse.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) Response result: cancel. This means the request has been cancelled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md) Response result: error. This means the request can not be set up successfully. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_OK](BroadcastInfoResponse.md) Response result: OK. This means the request is set up successfully and the related responses are normal responses. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DsmccResponse](DsmccResponse.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequence:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `file:` ` [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)?`)` Constructs a BIOP file message response. |
| [DsmccResponse](DsmccResponse.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequence:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `isServiceGateway:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `childList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Constructs a BIOP service gateway or directory message response. |
| [DsmccResponse](DsmccResponse.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequence:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `eventIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?`, `eventNames:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Constructs a BIOP stream message response. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](DsmccResponse.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getBiopMessageType](DsmccResponse.md))`()` Returns the BIOP message type. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getChildList](DsmccResponse.md))`()` Returns a list of subobject names for the given service gateway or directory message response. |
| --- | --- |
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) | [getFile](DsmccResponse.md))`()` Returns the file descriptor for a given file message response. |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getStreamEventIds](DsmccResponse.md))`()` Returns all event IDs carried in a given stream message response. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getStreamEventNames](DsmccResponse.md))`()` Returns all event names carried in a given stream message response. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](DsmccResponse.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoResponse](BroadcastInfoResponse.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](BroadcastInfoResponse.md))`()` Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseResult](BroadcastInfoResponse.md))`()` Gets the result for the response. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](BroadcastInfoResponse.md))`()` Gets the sequence number which indicates the order of related responses. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](BroadcastInfoResponse.md))`()` Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [DsmccResponse](DsmccResponse.md)!\> | [CREATOR](DsmccResponse.md) <br /> |

## Constants

### BIOP_MESSAGE_TYPE_DIRECTORY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOP_MESSAGE_TYPE_DIRECTORY: String
```

BIOP directory message 

 Value: "directory"

### BIOP_MESSAGE_TYPE_FILE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOP_MESSAGE_TYPE_FILE: String
```

BIOP file message 

 Value: "file"

### BIOP_MESSAGE_TYPE_SERVICE_GATEWAY

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOP_MESSAGE_TYPE_SERVICE_GATEWAY: String
```

BIOP service gateway message 

 Value: "service_gateway"

### BIOP_MESSAGE_TYPE_STREAM

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BIOP_MESSAGE_TYPE_STREAM: String
```

BIOP stream message 

 Value: "stream"

## Public constructors

### DsmccResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DsmccResponse(
    requestId: Int, 
    sequence: Int, 
    responseResult: Int, 
    file: ParcelFileDescriptor?)
```

Constructs a BIOP file message response.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](BroadcastInfoResponse.md), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) |
| `file` | [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md)?: This value may be `null`. |

### DsmccResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DsmccResponse(
    requestId: Int, 
    sequence: Int, 
    responseResult: Int, 
    isServiceGateway: Boolean, 
    childList: MutableList<String!>?)
```

Constructs a BIOP service gateway or directory message response.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](BroadcastInfoResponse.md), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) |
| `childList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |

### DsmccResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DsmccResponse(
    requestId: Int, 
    sequence: Int, 
    responseResult: Int, 
    eventIds: IntArray?, 
    eventNames: Array<String!>?)
```

Constructs a BIOP stream message response.

The current stream message response does not support other stream messages types than stream event message type.

| Parameters ||
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](BroadcastInfoResponse.md), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) |
| `eventIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)?: This value may be `null`. |
| `eventNames` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: This value may be `null`. |
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

### getBiopMessageType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBiopMessageType(): String
```

Returns the BIOP message type.

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be `null`. Value is [android.media.tv.DsmccResponse#BIOP_MESSAGE_TYPE_DIRECTORY](DsmccResponse.md), [android.media.tv.DsmccResponse#BIOP_MESSAGE_TYPE_FILE](DsmccResponse.md), [android.media.tv.DsmccResponse#BIOP_MESSAGE_TYPE_STREAM](DsmccResponse.md), or [android.media.tv.DsmccResponse#BIOP_MESSAGE_TYPE_SERVICE_GATEWAY](DsmccResponse.md) |

### getChildList

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getChildList(): MutableList<String!>
```

Returns a list of subobject names for the given service gateway or directory message response.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be `null`. |

### getFile

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFile(): ParcelFileDescriptor
```

Returns the file descriptor for a given file message response.

| Return ||
|--------------------------------------------------------------------------------------------------------------|------------------------------|
| [ParcelFileDescriptor](../android.os/ParcelFileDescriptor.md) | This value cannot be `null`. |

### getStreamEventIds

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStreamEventIds(): IntArray
```

Returns all event IDs carried in a given stream message response.

| Return ||
|---------------------------------------------------------------------------------------|------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | This value cannot be `null`. |

### getStreamEventNames

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStreamEventNames(): Array<String!>
```

Returns all event names carried in a given stream message response.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be `null`. |

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
static val CREATOR: Parcelable.Creator<DsmccResponse!>
```
