Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AssistantQueryRequest

```
class AssistantQueryRequest : EgressRequest<AssistantQueryResponse!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.app.privatecompute.EgressRequest](EgressRequest.md)\< [android.app.privatecompute.AssistantQueryResponse](AssistantQueryResponse.md)\> ||
| | ↳ | [android.app.privatecompute.AssistantQueryRequest](AssistantQueryRequest.md) |

Request object specifically for Assistant Query Egress operations. Binds this request to the `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryResponse` type.

These requests are subject to system validations, rate limits, and user consent. If the non-PCC process does not return the response in a reasonable timeframe, the platform will unbind from the non-PCC process and return `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccEgressException#ERROR_NO_RESPONSE_FROM_EGRESS_SERVICE:kotlin.Int` via the callback.

A request is considered invalid and will cause `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#egressData(android.app.privatecompute.EgressRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` to throw `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` synchronously if:

- The request or its `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Query` payload is null.
- The `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Query#getSessionId()` or `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Query#getQueryString()` is null.
- The session ID has already been used (reused/replayed).
- The query string size exceeds the maximum allowed limit (10 KB).
- The calling package does not contain the user-chosen default Assistant.

A request will cause `https://developer.android.com/reference/kotlin/android/app/privatecompute/PccSandboxManager#egressData(android.app.privatecompute.EgressRequest,%20java.util.concurrent.Executor,%20android.os.OutcomeReceiver)` to throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#` synchronously if:

- The user has not consented to egress for the Assistant service.
- The egress rate limit has been exceeded. The system enforces two limits:
 - A maximum of 100 successful egress calls in a rolling 24-hour window.
 - A maximum of 200 total egress attempts in a rolling 24-hour window.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#`. |
| | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Query` Payload containing the raw query details to be routed to the non-PCC assistant process. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [AssistantQueryRequest.Query](../android/app/privatecompute/AssistantQueryRequest.Query.md) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#getQuery()()` Returns the query payload associated with this request. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [AssistantQueryRequest](AssistantQueryRequest.md)!\> | `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#CREATOR:android.os.Parcelable.Creator` Creator for `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#` instance. |

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

### getQuery

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getQuery(): AssistantQueryRequest.Query
```

Returns the query payload associated with this request.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Query` | The `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest.Query` payload. This value cannot be `null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<AssistantQueryRequest!>
```

Creator for `https://developer.android.com/reference/kotlin/android/app/privatecompute/AssistantQueryRequest#` instance.
