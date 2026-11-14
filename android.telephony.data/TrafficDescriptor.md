Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TrafficDescriptor

Kotlin | [Java](https://developer.android.com/reference/android/telephony/data/TrafficDescriptor "View this page in Java")

```
class TrafficDescriptor : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.data.TrafficDescriptor](https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#) |

A traffic descriptor, as defined in 3GPP TS 24.526 Section 5.2. It is used for UE Route Selection Policy(URSP) traffic matching as described in 3GPP TS 24.526 Section 4.2.2. It includes optional components like Data Network Name (DNN), an OS/App ID, and/or Connection Capabilities, which, if present, must be used for traffic matching. This descriptor does not specify the end point to be used for the data call.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor.Builder` Provides a convenient way to set the fields of a `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#` when creating a new instance. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_BACKGROUND:kotlin.Int` Any traffic that is not time-sensitive, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_DOWNLINK_STREAMING:kotlin.Int` Downlink streaming, characterized as downlink high data rates content and low latency. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_IMS:kotlin.Int` IMS Voice + Video comprising voice, video telephony and multimedia communications over IP networks. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_INTERNET:kotlin.Int` Internet data traffic with wide availability but no critical requirements on latency or data rates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_IOT_DELAY_TOLERANT:kotlin.Int` Delay-tolerant, low sustained data rate IoT traffic. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_IOT_NON_DELAY_TOLERANT:kotlin.Int` Non-delay-tolerant, low sustained data rate IoT traffic |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_LCS_USER_PLANE_POSITIONING:kotlin.Int` LCS user plane positioning |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_LOW_LATENCY_LOSS_TOLERANT_UNACK:kotlin.Int` Traffic which has low latency requirements and is tolerant to some loss, hence using un-acknowledged mode at the Radio Link Control (RLC) layer. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_MISSION_CRITICAL_COMMUNICATIONS:kotlin.Int` Mission-critical communications, may include MC-PTT, MC video, and MC data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_MMS:kotlin.Int` MMS (Multimedia Messaging Service) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_REAL_TIME_INTERACTIVE:kotlin.Int` Real time interactive traffic, for example, for gaming or AR/VR. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_SUPL:kotlin.Int` SUPL (Secure User Plane Location) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_TIME_CRITICAL_COMMUNICATIONS:kotlin.Int` Time Critical Communications, with bounded, low to very low latency requirements, and high availability. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UNIFIED_COMMUNICATIONS:kotlin.Int` Unified communications traffic, which comprise communications through a single user interface at the UE, for instance instant messaging, VoIP, and video collaboration through the same application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UNKNOWN:kotlin.Int` Unknown connection capability. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UPLINK_STREAMING:kotlin.Int` Uplink streaming, characterized as uplink high data rates content and low latency |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_VEHICULAR_COMMUNICATIONS:kotlin.Int` Vehicle-to-Everything (V2X) traffic comprising V2X messages, characterized by low latency, high reliability, and high availability. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#getConnectionCapability()()` Get the connection capability of the traffic. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#getDataNetworkName()()` DNN stands for Data Network Name and represents an APN as defined in 3GPP TS 23. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#getOsAppId()()` OsAppId identifies a broader traffic category. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#hashCode()()` Returns a hash code value for the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TrafficDescriptor](https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#)!\> | `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### CONNECTION_CAPABILITY_BACKGROUND

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_BACKGROUND: Int
```

Any traffic that is not time-sensitive, e.g., firmware/software updates over the air. This traffic has no critical requirements from latency or data rates perspective. This traffic should/can be subject of scheduling (e.g., at specific time of day) by the applications/networks.

 Value: 168

### CONNECTION_CAPABILITY_DOWNLINK_STREAMING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_DOWNLINK_STREAMING: Int
```

Downlink streaming, characterized as downlink high data rates content and low latency.

 Value: 163

### CONNECTION_CAPABILITY_IMS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_IMS: Int
```

IMS Voice + Video comprising voice, video telephony and multimedia communications over IP networks. Voice, Video and SMS over IMS DNN, as well as RCS (Rich Communication Services) are included in this traffic category.

 Value: 1

### CONNECTION_CAPABILITY_INTERNET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_INTERNET: Int
```

Internet data traffic with wide availability but no critical requirements on latency or data rates.

 Value: 8

### CONNECTION_CAPABILITY_IOT_DELAY_TOLERANT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_IOT_DELAY_TOLERANT: Int
```

Delay-tolerant, low sustained data rate IoT traffic.

 Value: 161

### CONNECTION_CAPABILITY_IOT_NON_DELAY_TOLERANT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_IOT_NON_DELAY_TOLERANT: Int
```

Non-delay-tolerant, low sustained data rate IoT traffic

 Value: 162

### CONNECTION_CAPABILITY_LCS_USER_PLANE_POSITIONING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_LCS_USER_PLANE_POSITIONING: Int
```

LCS user plane positioning

 Value: 16

### CONNECTION_CAPABILITY_LOW_LATENCY_LOSS_TOLERANT_UNACK

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_LOW_LATENCY_LOSS_TOLERANT_UNACK: Int
```

Traffic which has low latency requirements and is tolerant to some loss, hence using un-acknowledged mode at the Radio Link Control (RLC) layer. E.g., for certain real time voice or video traffic.

 Value: 171

### CONNECTION_CAPABILITY_MISSION_CRITICAL_COMMUNICATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_MISSION_CRITICAL_COMMUNICATIONS: Int
```

Mission-critical communications, may include MC-PTT, MC video, and MC data.

 Value: 169

### CONNECTION_CAPABILITY_MMS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_MMS: Int
```

MMS (Multimedia Messaging Service)

 Value: 2

### CONNECTION_CAPABILITY_REAL_TIME_INTERACTIVE

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_REAL_TIME_INTERACTIVE: Int
```

Real time interactive traffic, for example, for gaming or AR/VR.

 Value: 166

### CONNECTION_CAPABILITY_SUPL

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_SUPL: Int
```

SUPL (Secure User Plane Location)

 Value: 4

### CONNECTION_CAPABILITY_TIME_CRITICAL_COMMUNICATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_TIME_CRITICAL_COMMUNICATIONS: Int
```

Time Critical Communications, with bounded, low to very low latency requirements, and high availability.

 Value: 170

### CONNECTION_CAPABILITY_UNIFIED_COMMUNICATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_UNIFIED_COMMUNICATIONS: Int
```

Unified communications traffic, which comprise communications through a single user interface at the UE, for instance instant messaging, VoIP, and video collaboration through the same application.

 Value: 167

### CONNECTION_CAPABILITY_UNKNOWN

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_UNKNOWN: Int
```

Unknown connection capability.

 Value: 0

### CONNECTION_CAPABILITY_UPLINK_STREAMING

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_UPLINK_STREAMING: Int
```

Uplink streaming, characterized as uplink high data rates content and low latency

 Value: 164

### CONNECTION_CAPABILITY_VEHICULAR_COMMUNICATIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CONNECTION_CAPABILITY_VEHICULAR_COMMUNICATIONS: Int
```

Vehicle-to-Everything (V2X) traffic comprising V2X messages, characterized by low latency, high reliability, and high availability.

 Value: 165

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getConnectionCapability

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getConnectionCapability(): Int
```

Get the connection capability of the traffic.

The connection capability indicates the type of traffic. The values are defined in 3GPP TS 24.526, Table 5.2.1. This is used by the network for UE Route Selection Policy (URSP) traffic matching.

When used to request a data connection, the framework may only use one specific connection capability to match a network capability, even if the underlying APN supports multiple (e.g., both internet and MMS). In such cases, only the single matched connection capability from the network request will be sent to the modem.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The connection capability, as one of the `CONNECTION_CAPABILITY_*` constants. Returns `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UNKNOWN:kotlin.Int` if not specified. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_IMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_MMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_SUPL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_INTERNET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_LCS_USER_PLANE_POSITIONING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_IOT_DELAY_TOLERANT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_IOT_NON_DELAY_TOLERANT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_DOWNLINK_STREAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UPLINK_STREAMING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_VEHICULAR_COMMUNICATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_REAL_TIME_INTERACTIVE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_UNIFIED_COMMUNICATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_BACKGROUND:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_MISSION_CRITICAL_COMMUNICATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_TIME_CRITICAL_COMMUNICATIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor#CONNECTION_CAPABILITY_LOW_LATENCY_LOSS_TOLERANT_UNACK:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/data/TrafficDescriptor.Builder#setConnectionCapability(kotlin.Int)`

### getDataNetworkName

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDataNetworkName(): String?
```

DNN stands for Data Network Name and represents an APN as defined in 3GPP TS 23.003.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the DNN of this traffic descriptor if one is included by the network, null otherwise. |

### getOsAppId

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getOsAppId(): ByteArray?
```

OsAppId identifies a broader traffic category. Although it names Os/App id, it only includes OS version with a general/broader category id used as app id.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html?` | The id in byte format. `null` if not available. |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<TrafficDescriptor!>
```
