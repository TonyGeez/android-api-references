Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DisconnectCause

```
class DisconnectCause : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telecom.DisconnectCause](../android/telecom/DisconnectCause.md) |

Describes the cause of a disconnected call. This always includes a code describing the generic cause of the disconnect. Optionally, it may include a label and/or description to display to the user. It is the responsibility of the `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` to provide localized versions of the label and description. It also may contain a reason for the disconnect, which is intended for logging and not for display to the user.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` Disconnected because the user did not locally answer the incoming call, but it was answered on another device where the call was ringing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#BUSY:kotlin.Int` Disconnected because the other party was busy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CALL_PULLED:kotlin.Int` Disconnected because the call was pulled from the current device to another device. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int` Disconnected because it has been canceled. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CONNECTION_MANAGER_NOT_SUPPORTED:kotlin.Int` Disconnected because the connection manager did not support the call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ERROR:kotlin.Int` Disconnected because there was an error, such as a problem with the network. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` Disconnected because of a local user-initiated action, such as hanging up. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int` Disconnected because there was no response to an incoming call. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#OTHER:kotlin.Int` Disconnected for reason not described by other disconnect codes. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REASON_EMERGENCY_CALL_PLACED:kotlin.String` This reason is set when a call is ended in order to place an emergency call when a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` doesn't support holding an ongoing call to place an emergency call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REASON_EMULATING_SINGLE_CALL:kotlin.String` Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`), which indicates that the connection service is setting the call's state to `https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTED:kotlin.Int` because it is internally changing the representation of an IMS conference call to simulate a single-party call. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REASON_IMS_ACCESS_BLOCKED:kotlin.String` Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`), which indicates that the call was disconnected because IMS access is blocked. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REASON_UNWANTED:kotlin.String` Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`), which indicates that the call was disconnected because it was marked as unwanted. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REASON_WIFI_ON_BUT_WFC_OFF:kotlin.String` Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`) which indicates that a call could not be completed because the cellular radio is off or out of service, the device is connected to a wifi network, but the user has not enabled wifi calling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` Disconnected because the user rejected an incoming call. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` Disconnected because the remote party hung up an ongoing call, or because an outgoing call was not answered by the remote party. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#RESTRICTED:kotlin.Int` Disconnected because of a restriction on placing the call, such as dialing in airplane mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int` Disconnected because of an unknown or unspecified reason. |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#DisconnectCause(kotlin.Int)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new DisconnectCause. |
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#DisconnectCause(kotlin.Int,%20kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.String)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, label: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, description: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new DisconnectCause. |
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#DisconnectCause(kotlin.Int,%20kotlin.CharSequence,%20kotlin.CharSequence,%20kotlin.String,%20kotlin.Int)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, label: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, description: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, toneToPlay: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new DisconnectCause. |
| `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#DisconnectCause(kotlin.Int,%20kotlin.String)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, reason: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Creates a new DisconnectCause. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getCode()()` Returns the code for the reason for this disconnect. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getDescription()()` Returns a description which explains the reason for the disconnect cause and is for display in the user interface. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getLabel()()` Returns a short label which explains the reason for the disconnect cause and is for display in the user interface. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()()` Returns an explanation of the reason for the disconnect. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getTone()()` Returns the tone to play when disconnected. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#writeToParcel(android.os.Parcel,%20kotlin.Int)(destination: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [DisconnectCause](../android/telecom/DisconnectCause.md)!\> | `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ANSWERED_ELSEWHERE

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ANSWERED_ELSEWHERE: Int
```

Disconnected because the user did not locally answer the incoming call, but it was answered on another device where the call was ringing.

 Value: 11

### BUSY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BUSY: Int
```

Disconnected because the other party was busy.

 Value: 7

### CALL_PULLED

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CALL_PULLED: Int
```

Disconnected because the call was pulled from the current device to another device.

 Value: 12

### CANCELED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CANCELED: Int
```

Disconnected because it has been canceled.

 Value: 4

### CONNECTION_MANAGER_NOT_SUPPORTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_MANAGER_NOT_SUPPORTED: Int
```

Disconnected because the connection manager did not support the call. The call will be tried again without a connection manager. See `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount#CAPABILITY_CONNECTION_MANAGER:kotlin.Int`.

 Value: 10

### ERROR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR: Int
```

Disconnected because there was an error, such as a problem with the network.

 Value: 1

### LOCAL

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LOCAL: Int
```

Disconnected because of a local user-initiated action, such as hanging up.

 Value: 2

### MISSED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val MISSED: Int
```

Disconnected because there was no response to an incoming call.

 Value: 5

### OTHER

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OTHER: Int
```

Disconnected for reason not described by other disconnect codes.

 Value: 9

### REASON_EMERGENCY_CALL_PLACED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_EMERGENCY_CALL_PLACED: String
```

This reason is set when a call is ended in order to place an emergency call when a `https://developer.android.com/reference/kotlin/android/telecom/PhoneAccount` doesn't support holding an ongoing call to place an emergency call. This reason string should only be associated with the `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` disconnect code returned from `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getCode()`.

 Value: "REASON_EMERGENCY_CALL_PLACED"

### REASON_EMULATING_SINGLE_CALL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_EMULATING_SINGLE_CALL: String
```

Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`), which indicates that the connection service is setting the call's state to `https://developer.android.com/reference/kotlin/android/telecom/Call#STATE_DISCONNECTED:kotlin.Int` because it is internally changing the representation of an IMS conference call to simulate a single-party call. This reason code is only used for communication between a `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` and Telecom and should not be surfaced to the user.

 Value: "EMULATING_SINGLE_CALL"

### REASON_IMS_ACCESS_BLOCKED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_IMS_ACCESS_BLOCKED: String
```

Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`), which indicates that the call was disconnected because IMS access is blocked.

 Value: "REASON_IMS_ACCESS_BLOCKED"

### REASON_UNWANTED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_UNWANTED: String
```

Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`), which indicates that the call was disconnected because it was marked as unwanted.

 Value: "REASON_UNWANTED"

### REASON_WIFI_ON_BUT_WFC_OFF

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REASON_WIFI_ON_BUT_WFC_OFF: String
```

Reason code (returned via `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getReason()`) which indicates that a call could not be completed because the cellular radio is off or out of service, the device is connected to a wifi network, but the user has not enabled wifi calling.

 Value: "REASON_WIFI_ON_BUT_WFC_OFF"

### REJECTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REJECTED: Int
```

Disconnected because the user rejected an incoming call.

 Value: 6

### REMOTE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val REMOTE: Int
```

Disconnected because the remote party hung up an ongoing call, or because an outgoing call was not answered by the remote party.

 Value: 3

### RESTRICTED

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESTRICTED: Int
```

Disconnected because of a restriction on placing the call, such as dialing in airplane mode.

 Value: 8

### UNKNOWN

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN: Int
```

Disconnected because of an unknown or unspecified reason.

 Value: 0

## Public constructors

### DisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DisconnectCause(code: Int)
```

Creates a new DisconnectCause.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The code for the disconnect cause. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CONNECTION_MANAGER_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CALL_PULLED:kotlin.Int` |

### DisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DisconnectCause(
    code: Int, 
    label: CharSequence!, 
    description: CharSequence!, 
    reason: String!)
```

Creates a new DisconnectCause.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The code for the disconnect cause. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CONNECTION_MANAGER_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CALL_PULLED:kotlin.Int` |
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The localized label to show to the user to explain the disconnect. |
| `description` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The localized description to show to the user to explain the disconnect. |
| --- | --- |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The reason for the disconnect. |

### DisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DisconnectCause(
    code: Int, 
    label: CharSequence!, 
    description: CharSequence!, 
    reason: String!, 
    toneToPlay: Int)
```

Creates a new DisconnectCause.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The code for the disconnect cause. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CONNECTION_MANAGER_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CALL_PULLED:kotlin.Int` |
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The localized label to show to the user to explain the disconnect. |
| `description` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!: The localized description to show to the user to explain the disconnect. |
| --- | --- |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The reason for the disconnect. |
| `toneToPlay` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The tone to play on disconnect, as defined in `https://developer.android.com/reference/kotlin/android/media/ToneGenerator.html#`. |

### DisconnectCause

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DisconnectCause(
    code: Int, 
    reason: String!)
```

Creates a new DisconnectCause.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The code for the disconnect cause. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CONNECTION_MANAGER_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CALL_PULLED:kotlin.Int` |
| `reason` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The reason for the disconnect. |

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

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCode(): Int
```

Returns the code for the reason for this disconnect.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The disconnect code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#LOCAL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REMOTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CANCELED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#MISSED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#REJECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#BUSY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#RESTRICTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#OTHER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CONNECTION_MANAGER_NOT_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#ANSWERED_ELSEWHERE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#CALL_PULLED:kotlin.Int` |

### getDescription

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDescription(): CharSequence!
```

Returns a description which explains the reason for the disconnect cause and is for display in the user interface. This optional text is generally a longer and more descriptive version of `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getLabel()`, however it can exist even if `https://developer.android.com/reference/kotlin/android/telecom/DisconnectCause#getLabel()` is empty. The In-Call UI should display this relatively prominently; the traditional implementation displays this as an alert dialog. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` is responsible for providing and localizing this message. If there is no string provided, returns null.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The disconnect description. |

### getLabel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLabel(): CharSequence!
```

Returns a short label which explains the reason for the disconnect cause and is for display in the user interface. If not null, it is expected that the In-Call UI should display this text where it would normally display the call state ("Dialing", "Disconnected") and is therefore expected to be relatively small. The `https://developer.android.com/reference/kotlin/android/telecom/ConnectionService` is responsible for providing and localizing this label. If there is no string provided, returns null.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | The disconnect label. |

### getReason

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getReason(): String!
```

Returns an explanation of the reason for the disconnect. This is not intended for display to the user and is used mainly for logging.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | The disconnect reason. |

### getTone

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTone(): Int
```

Returns the tone to play when disconnected.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the tone as defined in `https://developer.android.com/reference/kotlin/android/media/ToneGenerator.html#` to play when disconnected. |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

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
static val CREATOR: Parcelable.Creator<DisconnectCause!>
```
