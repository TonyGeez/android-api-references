Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TsResponse

Kotlin | [Java](TsResponse.md)
| --- | --- |

```
class TsResponse : BroadcastInfoResponse, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.media.tv.BroadcastInfoResponse](BroadcastInfoResponse.md) ||
| | ↳ | [android.media.tv.TsResponse](TsResponse.md) |

A response for TS (transport stream) from broadcast signal.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int` Response result: cancel. This means the request has been cancelled. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int` Response result: error. This means the request can not be set up successfully. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int` Response result: OK. This means the request is set up successfully and the related responses are normal responses. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/media/tv/TsResponse#TsResponse(kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.String)(requestId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sequence: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, responseResult: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sharedFilterToken: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TsResponse#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/media/tv/TsResponse#getSharedFilterToken()()` Gets a token of SharedFilter. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/media/tv/TsResponse#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getRequestId()()` Gets the ID of the request. The ID is used to associate the response with the request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getResponseResult()()` Gets the result for the response. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getSequence()()` Gets the sequence number which indicates the order of related responses. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#getType()()` Gets the broadcast info type. The type indicates what broadcast information is requested, such as broadcast table, PES (packetized Elementary Stream), TS (transport stream), etc. The type of the request and the related responses should be the same. <br /> | ||

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TsResponse](TsResponse.md)!\> | `https://developer.android.com/reference/kotlin/android/media/tv/TsResponse#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### TsResponse

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TsResponse(
    requestId: Int, 
    sequence: Int, 
    responseResult: Int, 
    sharedFilterToken: String?)
```

| Parameters ||
|---|---|
| `responseResult` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_OK:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/media/tv/BroadcastInfoResponse#RESPONSE_RESULT_CANCEL:kotlin.Int` |
| `sharedFilterToken` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: This value may be `null`. |

## Public methods

### describeContents

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getSharedFilterToken

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSharedFilterToken(): String?
```

Gets a token of SharedFilter.

The token can be used to retrieve the transport stream from the filter.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

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
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TsResponse!>
```
