Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ServiceState

Kotlin | [Java](ServiceState.md)
| --- | --- |

```
open class ServiceState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ServiceState](ServiceState.md) |

Contains phone state and service related information. The following phone information is included in returned ServiceState:

- Service state: IN_SERVICE, OUT_OF_SERVICE, EMERGENCY_ONLY, POWER_OFF
- Duplex mode: UNKNOWN, FDD, TDD
- Roaming indicator
- Operator name, short name and numeric id
- Network selection mode

For historical reasons this class is not declared as final; however, it should be treated as though it were final.

<br />

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_FDD:kotlin.Int` Duplex mode for the phone is frequency-division duplexing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_TDD:kotlin.Int` Duplex mode for the phone is time-division duplexing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_UNKNOWN:kotlin.Int` Duplex mode for the phone is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_EMERGENCY_ONLY:kotlin.Int` The phone is registered and locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_IN_SERVICE:kotlin.Int` Normal operation condition, the phone is registered with an operator either in home network or in roaming. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_OUT_OF_SERVICE:kotlin.Int` Phone is not registered with any operator, the phone can be currently searching a new operator to register to, or not searching to registration at all, or registration is denied, or radio signal is not available. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#STATE_POWER_OFF:kotlin.Int` Radio of telephony is explicitly powered off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#UNKNOWN_ID:kotlin.Int` Unknown ID. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| ServiceState Empty constructor |
| ServiceState Construct a ServiceState object from the given parcel. |
| ServiceState Copy constructors |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCdmaNetworkId Get the CDMA NID (Network Identification Number), a number uniquely identifying a network within a wireless system. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getCdmaSystemId Get the CDMA SID (System Identification Number), a number uniquely identifying a wireless system. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | getCellBandwidths Get an array of cell bandwidths (kHz) for the current serving cells |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getChannelNumber Get the channel number of the current primary serving cell, or -1 if unknown |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getDuplexMode Get the current duplex mode |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getIsManualSelection Get current network selection mode. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [NetworkRegistrationInfo](NetworkRegistrationInfo.md)!\> | getNetworkRegistrationInfoList Get all of the available network registration info. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getOperatorAlphaLong Get current registered operator name in long alphanumeric format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getOperatorAlphaShort Get current registered operator name in short alphanumeric format. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getOperatorNumeric Get current registered operator numeric id. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | getRoaming Get current roaming indicator of phone. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getState Get current voice service state |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isSearching This indicates whether the device is searching for service. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isUsingNonTerrestrialNetwork Get whether device is connected to a non-terrestrial network. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setIsManualSelection <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setOperatorName <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRoaming <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setState <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStateOff <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setStateOutOfService <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | toString Returns a string representation of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |

| Protected methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | copyFrom <br /> |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ServiceState](ServiceState.md)!\> | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### DUPLEX_MODE_FDD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLEX_MODE_FDD: Int
```

Duplex mode for the phone is frequency-division duplexing.

 Value: 1

### DUPLEX_MODE_TDD

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLEX_MODE_TDD: Int
```

Duplex mode for the phone is time-division duplexing.

 Value: 2

### DUPLEX_MODE_UNKNOWN

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUPLEX_MODE_UNKNOWN: Int
```

Duplex mode for the phone is unknown.

 Value: 0

### STATE_EMERGENCY_ONLY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_EMERGENCY_ONLY: Int
```

The phone is registered and locked. Only emergency numbers are allowed. {@more}

 Value: 2

### STATE_IN_SERVICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_IN_SERVICE: Int
```

Normal operation condition, the phone is registered with an operator either in home network or in roaming.

 Value: 0

### STATE_OUT_OF_SERVICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_OUT_OF_SERVICE: Int
```

Phone is not registered with any operator, the phone can be currently searching a new operator to register to, or not searching to registration at all, or registration is denied, or radio signal is not available.

 Value: 1

### STATE_POWER_OFF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_POWER_OFF: Int
```

Radio of telephony is explicitly powered off.

 Value: 3

### UNKNOWN_ID

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val UNKNOWN_ID: Int
```

Unknown ID. Could be returned by getCdmaNetworkId or getCdmaSystemId

 Value: -1

## Public constructors

### ServiceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ServiceState()
```

Empty constructor

### ServiceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ServiceState(in: Parcel!)
```

**Deprecated:** *The constructor takes parcel should not be public at the beginning. Use ServiceState instead.*

Construct a ServiceState object from the given parcel.

### ServiceState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ServiceState(s: ServiceState!)
```

Copy constructors

| Parameters ||
|---|---|
| `s` | [ServiceState](ServiceState.md)!: Source service state |

## Public methods

### describeContents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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

### getCdmaNetworkId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCdmaNetworkId(): Int
```

Get the CDMA NID (Network Identification Number), a number uniquely identifying a network within a wireless system. (Defined in 3GPP2 C.S0023 3.4.8)

Require at least `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. Otherwise return `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#UNKNOWN_ID:kotlin.Int`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#UNKNOWN_ID:kotlin.Int` as CDMA is no longer supported. |

### getCdmaSystemId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCdmaSystemId(): Int
```

Get the CDMA SID (System Identification Number), a number uniquely identifying a wireless system. (Defined in 3GPP2 C.S0023 3.4.8)

Require at least `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. Otherwise return `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#UNKNOWN_ID:kotlin.Int`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#UNKNOWN_ID:kotlin.Int` as CDMA is no longer supported. |

### getCellBandwidths

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getCellBandwidths(): IntArray!
```

Get an array of cell bandwidths (kHz) for the current serving cells

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!` | Current serving cell bandwidths |

### getChannelNumber

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getChannelNumber(): Int
```

Get the channel number of the current primary serving cell, or -1 if unknown

This is NRARFCN for NR, EARFCN for LTE, UARFCN for UMTS, and ARFCN for GSM.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Channel number of primary serving cell |

### getDuplexMode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getDuplexMode(): Int
```

Get the current duplex mode

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Current `DuplexMode` for the phone. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_FDD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_TDD:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_FDD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/telephony/ServiceState#DUPLEX_MODE_TDD:kotlin.Int`

### getIsManualSelection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getIsManualSelection(): Boolean
```

Get current network selection mode.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if manual mode, false if automatic mode |

### getNetworkRegistrationInfoList

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getNetworkRegistrationInfoList(): MutableList<NetworkRegistrationInfo!>
```

Get all of the available network registration info.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo!>` | List of NetworkRegistrationInfo This value cannot be `null`. |

### getOperatorAlphaLong

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOperatorAlphaLong(): String!
```

Get current registered operator name in long alphanumeric format. In GSM/UMTS, long format can be up to 16 characters long. In CDMA, returns the ERI text, if set. Otherwise, returns the ONS. Require at least `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. Otherwise return null if the caller does not hold neither `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` nor `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | long name of operator, null if unregistered or unknown |

### getOperatorAlphaShort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOperatorAlphaShort(): String!
```

Get current registered operator name in short alphanumeric format. In GSM/UMTS, short format can be up to 8 characters long. Require at least `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. Otherwise return null if the caller does not hold neither `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` nor `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | short name of operator, null if unregistered or unknown |

### getOperatorNumeric

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getOperatorNumeric(): String!
```

Get current registered operator numeric id. In GSM/UMTS, numeric format is 3 digit country code plus 2 or 3 digit network code. Require at least `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. Otherwise return null if the caller does not hold neither `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` nor `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` or `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_COARSE_LOCATION:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | numeric format of operator, null if unregistered or unknown |

### getRoaming

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRoaming(): Boolean
```

Get current roaming indicator of phone. This roaming state could be overridden by the carrier config. (note: not just decoding from TS 27.007 7.2)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if TS 27.007 7.2 roaming is true and ONS is different from SPN |

**See Also**

- isRoaming
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_FORCE_HOME_NETWORK_BOOL:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_GSM_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_ROAMING_NETWORKS_STRING_ARRAY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager#KEY_CDMA_NONROAMING_NETWORKS_STRING_ARRAY:kotlin.String`

### getState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getState(): Int
```

Get current voice service state

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isSearching

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isSearching(): Boolean
```

This indicates whether the device is searching for service. This API reports the modem searching status for `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants#TRANSPORT_TYPE_WWAN:kotlin.Int` (cellular) service in either `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_CS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/telephony/NetworkRegistrationInfo#DOMAIN_PS:kotlin.Int`. This API will not report searching status for `https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants#TRANSPORT_TYPE_WLAN:kotlin.Int`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` whenever the modem is searching for service. |

### isUsingNonTerrestrialNetwork

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isUsingNonTerrestrialNetwork(): Boolean
```

Get whether device is connected to a non-terrestrial network.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if device is connected to a non-terrestrial network else `false`. |

### setIsManualSelection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setIsManualSelection(isManual: Boolean): Unit
```

### setOperatorName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOperatorName(
    longName: String!, 
    shortName: String!, 
    numeric: String!
): Unit
```

### setRoaming

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRoaming(roaming: Boolean): Unit
```

### setState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setState(state: Int): Unit
```

### setStateOff

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStateOff(): Unit
```

### setStateOutOfService

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStateOutOfService(): Unit
```

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Protected methods

### copyFrom

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun copyFrom(s: ServiceState!): Unit
```

## Properties

### CREATOR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<ServiceState!>
```
