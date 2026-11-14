# SignalingDataResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalingDataResponse

Kotlin| [Java](SignalingDataResponse.md) 
| --- | --- |

```
class SignalingDataResponse : BroadcastInfoResponse, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoResponse](BroadcastInfoResponse.md) ||
| | ↳ | [android.media.tv.SignalingDataResponse](SignalingDataResponse.md) |

A response for the signaling data from the broadcast signal.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [BroadcastInfoResponse](BroadcastInfoResponse.md) |----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) <br /> Response result: cancel. This means the request has been cancelled. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md) <br /> Response result: error. This means the request can not be set up successfully. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RESPONSE_RESULT_OK](BroadcastInfoResponse.md) <br /> Response result: OK. This means the request is set up successfully and the related responses are normal responses. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SignalingDataResponse](SignalingDataResponse.md))`(`requestId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `sequence:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `responseResult:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `signalingDataTypes:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`, `signalingDataInfoList:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SignalingDataInfo](SignalingDataInfo.md)!>`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SignalingDataResponse.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SignalingDataInfo](SignalingDataInfo.md)!\> | [getSignalingDataInfoList](SignalingDataResponse.md))`()` Gets a list of [SignalingDataInfo](SignalingDataInfo.md) contained in this response. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSignalingDataTypes](SignalingDataResponse.md))`()` Gets a list of types of metadata that are contained in this response. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SignalingDataResponse.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Inherited functions ||
|---|---|
| From class [BroadcastInfoResponse](BroadcastInfoResponse.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRequestId](BroadcastInfoResponse.md))`()` <br /> Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResponseResult](BroadcastInfoResponse.md))`()` <br /> Gets the result for the response. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSequence](BroadcastInfoResponse.md))`()` <br /> Gets the sequence number which indicates the order of related responses. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getType](BroadcastInfoResponse.md))`()` <br /> Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SignalingDataResponse](SignalingDataResponse.md)!\> | [CREATOR](SignalingDataResponse.md) <br /> |

## Public constructors

### SignalingDataResponse

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SignalingDataResponse(
    requestId: Int, 
    sequence: Int, 
    responseResult: Int, 
    signalingDataTypes: MutableList<String!>, 
    signalingDataInfoList: MutableList<SignalingDataInfo!>)
```

| Parameters ||
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_ERROR](BroadcastInfoResponse.md), [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_OK](BroadcastInfoResponse.md), or [android.media.tv.BroadcastInfoResponse#RESPONSE_RESULT_CANCEL](BroadcastInfoResponse.md) |
| `signalingDataTypes` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:This value cannot be`null`. |
| `signalingDataInfoList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [SignalingDataInfo](SignalingDataInfo.md)!\>:This value cannot be`null`. |
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

### getSignalingDataInfoList

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalingDataInfoList(): MutableList<SignalingDataInfo!>
```

Gets a list of [SignalingDataInfo](SignalingDataInfo.md) contained in this response.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [SignalingDataInfo](SignalingDataInfo.md)!> | A list of [SignalingDataInfo](SignalingDataInfo.md) contained in this response. This value cannot be`null`. |

### getSignalingDataTypes

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSignalingDataTypes(): MutableList<String!>
```

Gets a list of types of metadata that are contained in this response.

This list correlates to all the available types that can be found within [getSignalingDataInfoList()](SignalingDataResponse.md)). This list is determined by the types specified in [SignalingDataRequest.getSignalingDataTypes()](SignalingDataRequest.md)).

A list of types available are defined in [SignalingDataRequest](SignalingDataRequest.md). For more information about these types, see A/344:2023-5 9.2.10 - Query Signaling Data API.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | A list of types of metadata that are contained in this response. This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<SignalingDataResponse!>
```
