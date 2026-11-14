Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EmergencyNumber

```
class EmergencyNumber : Comparable<EmergencyNumber!>, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.emergency.EmergencyNumber](../android/telephony/emergency/EmergencyNumber.md) |

A parcelable class that wraps and retrieves the information of number, service category(s) and country code for a specific emergency number.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_CALL_ROUTING_EMERGENCY:kotlin.Int` Indicates the radio or IMS implementation must handle the call through emergency routing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_CALL_ROUTING_NORMAL:kotlin.Int` Indicates the radio or IMS implementation must handle the call through normal call routing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_CALL_ROUTING_UNKNOWN:kotlin.Int` Indicated the framework does not know whether an emergency call should be placed using emergency or normal call routing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DATABASE:kotlin.Int` Bit-field which indicates the number is from the platform-maintained database. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DEFAULT:kotlin.Int` Bit-field which indicates the number is available as default. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_MODEM_CONFIG:kotlin.Int` Bit-field which indicates the number is from the modem config. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_NETWORK_SIGNALING:kotlin.Int` Bit-field which indicates the number is from the network signaling. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_SIM:kotlin.Int` Bit-field which indicates the number is from the sim. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AIEC:kotlin.Int` Bit-field that indicates Emergency Service Category for Automatically Initiated eCall (AIeC) Reference: 3gpp 22. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AMBULANCE:kotlin.Int` Bit-field that indicates Emergency Service Category for Ambulance. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_FIRE_BRIGADE:kotlin.Int` Bit-field that indicates Emergency Service Category for Fire Brigade. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MARINE_GUARD:kotlin.Int` Bit-field that indicates Emergency Service Category for Marine Guard. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MIEC:kotlin.Int` Bit-field that indicates Emergency Service Category for Manually Initiated eCall (MIeC) Reference: 3gpp 22. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MOUNTAIN_RESCUE:kotlin.Int` Bit-field that indicates Emergency Service Category for Mountain Rescue. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_POLICE:kotlin.Int` Bit-field that indicates Emergency Service Category for Police. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int` Emergency Service Category UNSPECIFIED (General emergency call, all categories) bit-field indicates that no specific services are associated with this emergency number; if the emergency number is specified, it has one or more defined emergency service categories. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#compareTo(android.telephony.emergency.EmergencyNumber)(other: https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#)` Compare the display priority for this emergency number and the supplied emergency number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getCountryIso()()` Get the country code string (lowercase character) in ISO 3166 format of the emergency number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getEmergencyCallRouting()()` Returns the emergency call routing information. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getEmergencyNumberSources()()` Returns a list of sources of the emergency number. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getEmergencyServiceCategories()()` Returns the emergency service categories of the emergency number. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getEmergencyUrns()()` Returns the list of emergency Uniform Resources Names (URN) of the emergency number. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getMnc()()` Get the Mobile Network Code of the emergency number. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#getNumber()()` Get the dialing number of the emergency number. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#isFromSources(kotlin.Int)(sources: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the emergency number is from the specified emergency number source(s). |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#isInEmergencyServiceCategories(kotlin.Int)(categories: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Checks if the emergency number is in the supplied emergency service category(s). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [EmergencyNumber](../android/telephony/emergency/EmergencyNumber.md)!\> | `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### EMERGENCY_CALL_ROUTING_EMERGENCY

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_CALL_ROUTING_EMERGENCY: Int
```

Indicates the radio or IMS implementation must handle the call through emergency routing.

 Value: 1

### EMERGENCY_CALL_ROUTING_NORMAL

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_CALL_ROUTING_NORMAL: Int
```

Indicates the radio or IMS implementation must handle the call through normal call routing.

 Value: 2

### EMERGENCY_CALL_ROUTING_UNKNOWN

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_CALL_ROUTING_UNKNOWN: Int
```

Indicated the framework does not know whether an emergency call should be placed using emergency or normal call routing. This means the underlying radio or IMS implementation is free to determine for itself how to route the call.

 Value: 0

### EMERGENCY_NUMBER_SOURCE_DATABASE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_NUMBER_SOURCE_DATABASE: Int
```

Bit-field which indicates the number is from the platform-maintained database.

 Value: 16

### EMERGENCY_NUMBER_SOURCE_DEFAULT

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_NUMBER_SOURCE_DEFAULT: Int
```

Bit-field which indicates the number is available as default. 112, 911 must always be available; additionally, 000, 08, 110, 999, 118 and 119 must be available when sim is not present. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 8

### EMERGENCY_NUMBER_SOURCE_MODEM_CONFIG

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_NUMBER_SOURCE_MODEM_CONFIG: Int
```

Bit-field which indicates the number is from the modem config.

 Value: 4

### EMERGENCY_NUMBER_SOURCE_NETWORK_SIGNALING

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_NUMBER_SOURCE_NETWORK_SIGNALING: Int
```

Bit-field which indicates the number is from the network signaling. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 1

### EMERGENCY_NUMBER_SOURCE_SIM

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_NUMBER_SOURCE_SIM: Int
```

Bit-field which indicates the number is from the sim. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 2

### EMERGENCY_SERVICE_CATEGORY_AIEC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_AIEC: Int
```

Bit-field that indicates Emergency Service Category for Automatically Initiated eCall (AIeC) Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 64

### EMERGENCY_SERVICE_CATEGORY_AMBULANCE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_AMBULANCE: Int
```

Bit-field that indicates Emergency Service Category for Ambulance. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 2

### EMERGENCY_SERVICE_CATEGORY_FIRE_BRIGADE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_FIRE_BRIGADE: Int
```

Bit-field that indicates Emergency Service Category for Fire Brigade. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 4

### EMERGENCY_SERVICE_CATEGORY_MARINE_GUARD

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_MARINE_GUARD: Int
```

Bit-field that indicates Emergency Service Category for Marine Guard. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 8

### EMERGENCY_SERVICE_CATEGORY_MIEC

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_MIEC: Int
```

Bit-field that indicates Emergency Service Category for Manually Initiated eCall (MIeC) Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 32

### EMERGENCY_SERVICE_CATEGORY_MOUNTAIN_RESCUE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_MOUNTAIN_RESCUE: Int
```

Bit-field that indicates Emergency Service Category for Mountain Rescue. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 16

### EMERGENCY_SERVICE_CATEGORY_POLICE

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_POLICE: Int
```

Bit-field that indicates Emergency Service Category for Police. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 1

### EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED: Int
```

Emergency Service Category UNSPECIFIED (General emergency call, all categories) bit-field indicates that no specific services are associated with this emergency number; if the emergency number is specified, it has one or more defined emergency service categories. Reference: 3gpp 22.101, Section 10 - Emergency Calls

 Value: 0

## Public methods

### compareTo

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun compareTo(other: EmergencyNumber): Int
```

Compare the display priority for this emergency number and the supplied emergency number.

| Parameters ||
|---|---|
| `o` | the object to be compared. |
| `emergencyNumber` | the supplied emergency number. This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a negative value if the supplied emergency number has a lower display priority; a positive value if the supplied emergency number has a higher display priority; 0 if both have equal display priority. |

| Exceptions ||
|---|---|
| `java.lang.ClassCastException` | if the specified object's type prevents it from being compared to this object. |
| `java.lang.NullPointerException` | if the specified object is null |

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### getCountryIso

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCountryIso(): String
```

Get the country code string (lowercase character) in ISO 3166 format of the emergency number.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the country code string (lowercase character) in ISO 3166 format. This value cannot be `null`. |

### getEmergencyCallRouting

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEmergencyCallRouting(): Int
```

Returns the emergency call routing information.

Some regions require some emergency numbers which are not routed using typical emergency call processing, but are instead placed as regular phone calls. The emergency call routing field provides information about how an emergency call will be routed when it is placed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the emergency call routing requirement. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_CALL_ROUTING_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_CALL_ROUTING_EMERGENCY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_CALL_ROUTING_NORMAL:kotlin.Int` |

### getEmergencyNumberSources

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEmergencyNumberSources(): MutableList<Int!>
```

Returns a list of sources of the emergency number.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | a list of emergency number sources. This value cannot be `null`. |

### getEmergencyServiceCategories

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEmergencyServiceCategories(): MutableList<Int!>
```

Returns the emergency service categories of the emergency number. Note: if the emergency number is in `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int`, only `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int` is returned and it means the number is in all categories.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!>` | a list of the emergency service categories. This value cannot be `null`. |

### getEmergencyUrns

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEmergencyUrns(): MutableList<String!>
```

Returns the list of emergency Uniform Resources Names (URN) of the emergency number. For example, `urn:service:sos` is the generic URN for contacting emergency services of all type. Reference: 3gpp 24.503, Section 5.1.6.8.1 - General; RFC 5031

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>` | list of emergency Uniform Resources Names (URN) or an empty list if the emergency number does not have a specified emergency Uniform Resource Name. This value cannot be `null`. |

### getMnc

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMnc(): String
```

Get the Mobile Network Code of the emergency number.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the Mobile Network Code of the emergency number. This value cannot be `null`. |

### getNumber

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getNumber(): String
```

Get the dialing number of the emergency number. The character in the number string is only the dial pad character('0'-'9', '\*', '+', or '#'). For example: 911. If the number starts with carrier prefix, the carrier prefix is configured in `https://developer.android.com/reference/kotlin/android/telephony/CarrierConfigManager.html#KEY_EMERGENCY_NUMBER_PREFIX_STRING_ARRAY:kotlin.String`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | the dialing number. This value cannot be `null`. |

### hashCode

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

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

### isFromSources

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isFromSources(sources: Int): Boolean
```

Checks if the emergency number is from the specified emergency number source(s).

| Parameters ||
|---|---|
| `sources` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): - the supplied emergency number sources. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_NETWORK_SIGNALING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_SIM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DATABASE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_MODEM_CONFIG:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_NUMBER_SOURCE_DEFAULT:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the emergency number is from the specified emergency number source(s); `false` otherwise. |

### isInEmergencyServiceCategories

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isInEmergencyServiceCategories(categories: Int): Boolean
```

Checks if the emergency number is in the supplied emergency service category(s).

| Parameters ||
|---|---|
| `categories` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): - the supplied emergency service categories. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_POLICE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AMBULANCE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_FIRE_BRIGADE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MARINE_GUARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MOUNTAIN_RESCUE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_MIEC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_AIEC:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the emergency number is in the specified emergency service category(s) or if its emergency service category is `https://developer.android.com/reference/kotlin/android/telephony/emergency/EmergencyNumber#EMERGENCY_SERVICE_CATEGORY_UNSPECIFIED:kotlin.Int`; `false` otherwise. |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<EmergencyNumber!>
```
