Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkRegistrationInfo

```
class NetworkRegistrationInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.NetworkRegistrationInfo](NetworkRegistrationInfo.md) |

Description of a mobile network registration info

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS:kotlin.Int` Circuit switched domain |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS_PS:kotlin.Int` Applicable to both CS and PS Domain |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_PS:kotlin.Int` Packet switched domain |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_UNKNOWN:kotlin.Int` Unknown / Unspecified domain |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#NR_STATE_CONNECTED:kotlin.Int` The device is camped on an LTE cell that supports E-UTRA-NR Dual Connectivity(EN-DC) and also connected to at least one 5G cell as a secondary serving cell. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#NR_STATE_NONE:kotlin.Int` The device isn't camped on an LTE cell or the LTE cell doesn't support E-UTRA-NR Dual Connectivity(EN-DC). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#NR_STATE_NOT_RESTRICTED:kotlin.Int` The device is camped on an LTE cell that supports E-UTRA-NR Dual Connectivity(EN-DC) and both the use of dual connectivity with NR(DCNR) is not restricted and NR is supported by the selected PLMN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#NR_STATE_RESTRICTED:kotlin.Int` The device is camped on an LTE cell that supports E-UTRA-NR Dual Connectivity(EN-DC) but either the use of dual connectivity with NR(DCNR) is restricted or NR is not supported by the selected PLMN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_DATA:kotlin.Int` Data service |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_EMERGENCY:kotlin.Int` Emergency service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_EMERGENCY_SMS:kotlin.Int` Emergency SMS service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_MMS:kotlin.Int` MMS service |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_SMS:kotlin.Int` SMS service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_UNKNOWN:kotlin.Int` Unknown service |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_VIDEO:kotlin.Int` Video service |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_VOICE:kotlin.Int` Voice service |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getAccessNetworkTechnology()()` <br /> |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getAvailableServices()()` <br /> |
| [CellIdentity](CellIdentity.md)? | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getCellIdentity()()` Require `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`, otherwise return null. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getDomain()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getRegisteredPlmn()()` Get the PLMN-ID for this Network Registration, also known as the RPLMN. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getRejectCause()()` Get the 3GPP/3GPP2 reason code indicating why registration failed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getTransportType()()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isNetworkRegistered()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isNetworkRoaming()()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isNetworkSearching()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isNonTerrestrialNetwork()()` Get whether the network is a non-terrestrial network. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isRegistered()()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isRoaming()()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isSearching()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#toString()()` Returns a string representation of the object. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NetworkRegistrationInfo](NetworkRegistrationInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DOMAIN_CS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOMAIN_CS: Int
```

Circuit switched domain

 Value: 1

### DOMAIN_CS_PS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOMAIN_CS_PS: Int
```

Applicable to both CS and PS Domain

 Value: 3

### DOMAIN_PS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOMAIN_PS: Int
```

Packet switched domain

 Value: 2

### DOMAIN_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DOMAIN_UNKNOWN: Int
```

Unknown / Unspecified domain

 Value: 0

### NR_STATE_CONNECTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NR_STATE_CONNECTED: Int
```

The device is camped on an LTE cell that supports E-UTRA-NR Dual Connectivity(EN-DC) and also connected to at least one 5G cell as a secondary serving cell.

 Value: 3

### NR_STATE_NONE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NR_STATE_NONE: Int
```

The device isn't camped on an LTE cell or the LTE cell doesn't support E-UTRA-NR Dual Connectivity(EN-DC).

 Value: 0

### NR_STATE_NOT_RESTRICTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NR_STATE_NOT_RESTRICTED: Int
```

The device is camped on an LTE cell that supports E-UTRA-NR Dual Connectivity(EN-DC) and both the use of dual connectivity with NR(DCNR) is not restricted and NR is supported by the selected PLMN.

 Value: 2

### NR_STATE_RESTRICTED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val NR_STATE_RESTRICTED: Int
```

The device is camped on an LTE cell that supports E-UTRA-NR Dual Connectivity(EN-DC) but either the use of dual connectivity with NR(DCNR) is restricted or NR is not supported by the selected PLMN.

 Value: 1

### SERVICE_TYPE_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_DATA: Int
```

Data service

 Value: 2

### SERVICE_TYPE_EMERGENCY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_EMERGENCY: Int
```

Emergency service

 Value: 5

### SERVICE_TYPE_EMERGENCY_SMS

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_EMERGENCY_SMS: Int
```

Emergency SMS service

 Value: 7

### SERVICE_TYPE_MMS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_MMS: Int
```

MMS service

 Value: 6

### SERVICE_TYPE_SMS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_SMS: Int
```

SMS service

 Value: 3

### SERVICE_TYPE_UNKNOWN

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_UNKNOWN: Int
```

Unknown service

 Value: 0

### SERVICE_TYPE_VIDEO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_VIDEO: Int
```

Video service

 Value: 4

### SERVICE_TYPE_VOICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SERVICE_TYPE_VOICE: Int
```

Voice service

 Value: 1

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getAccessNetworkTechnology

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAccessNetworkTechnology(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The access network technology network type.. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_CDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_0:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_A:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_1xRTT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IDEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EVDO_B:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_LTE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EHRPD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPAP:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GSM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_TD_SCDMA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_IWLAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_NR:kotlin.Int` |

### getAvailableServices

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAvailableServices(): MutableList<Int!>
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | List of available service types. This value cannot be `null`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_VOICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_DATA:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_SMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_VIDEO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_EMERGENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_MMS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#SERVICE_TYPE_EMERGENCY_SMS:kotlin.Int` |

### getCellIdentity

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCellIdentity(): CellIdentity?
```

Require `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String`, otherwise return null.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/telephony/CellIdentity?` | The cell information. |

### getDomain

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDomain(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The network domain. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_PS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS_PS:kotlin.Int` |

### getRegisteredPlmn

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRegisteredPlmn(): String?
```

Get the PLMN-ID for this Network Registration, also known as the RPLMN.

If the device is registered, this will return the registered PLMN-ID. If registration has failed, then this will return the PLMN ID of the last attempted registration. If the device is not registered, or if is registered to a non-3GPP radio technology, then this will return null.

See 3GPP TS 23.122 for further information about the Registered PLMN.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the registered PLMN-ID or null. |

### getRejectCause

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRejectCause(): Int
```

Get the 3GPP/3GPP2 reason code indicating why registration failed. Returns the reason code for non-transient registration failures. Typically this method will only return the last reason code received during a network selection procedure. The reason code is system-specific; however, the reason codes for both 3GPP and 3GPP2 systems are largely equivalent across generations.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | registration reject cause if available, otherwise 0. Depending on `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#getAccessNetworkTechnology()`, the values are defined in 3GPP TS 24.008 10.5.3.6 for WCDMA/UMTS, 3GPP TS 24.301 9.9.3.9 for LTE/EPS, 3GPP 24.501 Annex A for NR/5GS, or 3GPP2 A.S0001 6.2.2.44 for CDMA. |

### getTransportType

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTransportType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The transport type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants#TRANSPORT_TYPE_WWAN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants#TRANSPORT_TYPE_WLAN:kotlin.Int` |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isNetworkRegistered

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNetworkRegistered(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if registered on roaming or home network, `false` otherwise. (This value is not affected by any carrier config or resource overlay override). |

### isNetworkRoaming

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNetworkRoaming(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if registered on roaming network. (This value is not affected by any carrier config or resource overlay override). |

### isNetworkSearching

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNetworkSearching(): Boolean
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if searching for service, `false` otherwise. (This value is not affected by any carrier config or resource overlay override). |

### isNonTerrestrialNetwork

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isNonTerrestrialNetwork(): Boolean
```

Get whether the network is a non-terrestrial network.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if network is a non-terrestrial network else `false`. |

### isRegistered

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRegistered(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isNetworkRegistered()`, which is not affected by any carrier config or resource overlay, instead.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if registered on roaming or home network. Note this value can be affected by the carrier config override. |

### isRoaming

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isRoaming(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/TelephonyDisplayInfo#isRoaming()` instead.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if registered on roaming network overridden by config. Note this value can be affected by the carrier config override. |

### isSearching

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isSearching(): Boolean
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#isNetworkRegistered()`, which is not affected by any carrier config or resource overlay, instead.*

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if searching for service, `false` otherwise. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### writeToParcel

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<NetworkRegistrationInfo!>
```
