Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssistantQueryResponse

```
class AssistantQueryResponse : EgressResponse, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.privatecompute.EgressResponse](https://developer.android.com/reference/kotlin/android/app/privatecompute/EgressResponse) ||
| | ↳ | [android.app.privatecompute.AssistantQueryResponse](https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#) |

Specialized response for Assistant Query use-cases. Includes the specific query ID and the generated response payload.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#`. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#getMetadata()()` Returns the metadata bytes associated with this egress response. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#getQueryId()()` Returns the unique identifier of the query associated with this egress response. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#getQueryResponse()()` Returns the raw query response payload generated for the query. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [AssistantQueryResponse](https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#)!\> | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#CREATOR:android.os.Parcelable.Creator` Creator for `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#` instance. |

## Public methods

### describeContents

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getMetadata

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMetadata(): ByteArray?
```

Returns the metadata bytes associated with this egress response.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | The metadata bytes, or `null` if unavailable. |

### getQueryId

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQueryId(): String?
```

Returns the unique identifier of the query associated with this egress response.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | A string representing the unique query ID, or `null` if unavailable. |

### getQueryResponse

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQueryResponse(): String?
```

Returns the raw query response payload generated for the query.

May be `null` if the response is empty.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The raw query response string, or `null` if unavailable. |

### writeToParcel

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AssistantQueryResponse!>
```

Creator for `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse#` instance.
