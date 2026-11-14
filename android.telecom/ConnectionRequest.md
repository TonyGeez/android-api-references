Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ConnectionRequest

Kotlin | [Java](https://developer.android.com/reference/android/telecom/ConnectionRequest "View this page in Java")
| --- | --- |

```
class ConnectionRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.ConnectionRequest](https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#) |

Simple data container encapsulating a request to some entity to create a new `https://developer.android.com/reference/kotlin/android/telecom/Connection`.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#ConnectionRequest(android.telecom.PhoneAccountHandle,%20android.net.Uri,%20android.os.Bundle)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, handle: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#ConnectionRequest(android.telecom.PhoneAccountHandle,%20android.net.Uri,%20android.os.Bundle,%20kotlin.Int)(accountHandle: https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle!, handle: https://developer.android.com/reference/kotlin/android/net/Uri.html#!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!, videoState: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getAccountHandle()()` The account which should be used to place the call. |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getAddress()()` The handle (e.g., phone number) to which the |
| --- | --- |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getExtras()()` Application-specific extra data. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!\>? | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getParticipants()()` The participants to which the `https://developer.android.com/reference/kotlin/android/telecom/Connection` is to connect. |
| [Connection.RttTextStream](https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream)! | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getRttTextStream()()` Gets the `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream` object that should be used to send and receive RTT text to/from the in-call app. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#getVideoState()()` Describes the video states supported by the client requesting the connection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#isAdhocConferenceCall()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#isRequestingRtt()()` Convenience method for determining whether the ConnectionRequest is requesting an RTT session |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#writeToParcel(android.os.Parcel,%20kotlin.Int)(destination: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ConnectionRequest](https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#)!\> | `https://developer.android.com/reference/kotlin/android/telecom/ConnectionRequest#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### ConnectionRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConnectionRequest(
    accountHandle: PhoneAccountHandle!, 
    handle: Uri!, 
    extras: Bundle!)
```

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The accountHandle which should be used to place the call. |
| `handle` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The handle (e.g., phone number) to which the `https://developer.android.com/reference/kotlin/android/telecom/Connection` is to connect. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Application-specific extra data. |
| --- | --- |

### ConnectionRequest

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ConnectionRequest(
    accountHandle: PhoneAccountHandle!, 
    handle: Uri!, 
    extras: Bundle!, 
    videoState: Int)
```

| Parameters ||
|---|---|
| `accountHandle` | [PhoneAccountHandle](https://developer.android.com/reference/kotlin/android/telecom/PhoneAccountHandle)!: The accountHandle which should be used to place the call. |
| `handle` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)!: The handle (e.g., phone number) to which the `https://developer.android.com/reference/kotlin/android/telecom/Connection` is to connect. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Application-specific extra data. |
| --- | --- |
| `videoState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Determines the video state for the connection. |

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getAccountHandle

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccountHandle(): PhoneAccountHandle!
```

The account which should be used to place the call.

### getAddress

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): Uri!
```

The handle (e.g., phone number) to which the `https://developer.android.com/reference/kotlin/android/telecom/Connection` is to connect.

### getExtras

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getExtras(): Bundle!
```

Application-specific extra data. Used for passing back information from an incoming call `Intent`, and for any proprietary extensions arranged between a client and servant `ConnectionService` which agree on a vocabulary for such data.

### getParticipants

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getParticipants(): MutableList<Uri!>?
```

The participants to which the `https://developer.android.com/reference/kotlin/android/telecom/Connection` is to connect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/net/Uri.html#!>?` | This value may be `null`. |

### getRttTextStream

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRttTextStream(): Connection.RttTextStream!
```

Gets the `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream` object that should be used to send and receive RTT text to/from the in-call app.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream!` | An instance of `https://developer.android.com/reference/kotlin/android/telecom/Connection.RttTextStream`, or `null` if this connection request is not requesting an RTT session upon connection establishment. |

### getVideoState

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVideoState(): Int
```

Describes the video states supported by the client requesting the connection. Valid values: `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_AUDIO_ONLY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_BIDIRECTIONAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_TX_ENABLED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/telecom/VideoProfile#STATE_RX_ENABLED:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The video state for the connection. |

### isAdhocConferenceCall

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isAdhocConferenceCall(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the call is a adhoc conference call else @return `false` |

### isRequestingRtt

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRequestingRtt(): Boolean
```

Convenience method for determining whether the ConnectionRequest is requesting an RTT session

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if RTT is requested, `false` otherwise. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    destination: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ConnectionRequest!>
```
