# ImsRegistrationAttributes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsRegistrationAttributes

Kotlin| [Java](https://developer.android.com/reference/android/telephony/ims/ImsRegistrationAttributes "View this page in Java") 

```
class ImsRegistrationAttributes : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.ims.ImsRegistrationAttributes](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#) |

Contains the attributes associated with the current IMS registration.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTR_EPDG_OVER_CELL_INTERNET](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#ATTR_EPDG_OVER_CELL_INTERNET:kotlin.Int) Attribute to specify if an EPDG tunnel is setup over the cellular internet APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTR_REGISTRATION_TYPE_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#ATTR_REGISTRATION_TYPE_EMERGENCY:kotlin.Int) Attribute to specify if ims registration is of type normal or emergency. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL:kotlin.Int) Attribute to specify if virtual registration is required. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAttributeFlags](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#getAttributeFlags())`()` <br /> |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getFeatureTags](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#getFeatureTags())`()` Gets the Set of feature tags associated with the current IMS registration, if the IMS service supports supplying this information. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFlagRegistrationTypeEmergency](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#getFlagRegistrationTypeEmergency())`()` Get the attribute flag ATTR_REGISTRATION_TYPE_EMERGENCY. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFlagVirtualRegistrationForEmergencyCall](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#getFlagVirtualRegistrationForEmergencyCall())`()` Get the attribute flag ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL. |
| [SipDetails](https://developer.android.com/reference/kotlin/android/telephony/ims/SipDetails)? | [getSipDetails](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#getSipDetails())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportType](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#getTransportType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ImsRegistrationAttributes](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ATTR_EPDG_OVER_CELL_INTERNET

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTR_EPDG_OVER_CELL_INTERNET: Int
```

Attribute to specify if an EPDG tunnel is setup over the cellular internet APN.

If IMS is registered through an EPDG tunnel is setup over the cellular internet APN then this bit will be set. If IMS is registered through the IMS APN, then this bit will not be set. 

 Value: 1

### ATTR_REGISTRATION_TYPE_EMERGENCY

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTR_REGISTRATION_TYPE_EMERGENCY: Int
```

Attribute to specify if ims registration is of type normal or emergency.

For emergency registration bit will be set. For normal registration bit will not be set. This flag is only applicable when listening to emergency IMS registration state updates via the ImsMmTelManager#registerImsEmergencyRegistrationCallback API 

 Value: 2

### ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL: Int
```

Attribute to specify if virtual registration is required.

If emergency registration is not required for making emergency call, in such cases bit will be set and callback will represent virtual registration status update. This flag is only applicable when listening to emergency IMS registration state updates via the ImsMmTelManager#registerImsEmergencyRegistrationCallback API 

 Value: 4

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAttributeFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAttributeFlags(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bit-mask containing attributes associated with the IMS registration. Value is either`0`or a combination of [android.telephony.ims.ImsRegistrationAttributes#ATTR_EPDG_OVER_CELL_INTERNET](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#ATTR_EPDG_OVER_CELL_INTERNET:kotlin.Int), [android.telephony.ims.ImsRegistrationAttributes#ATTR_REGISTRATION_TYPE_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#ATTR_REGISTRATION_TYPE_EMERGENCY:kotlin.Int), and [android.telephony.ims.ImsRegistrationAttributes#ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL](https://developer.android.com/reference/kotlin/android/telephony/ims/ImsRegistrationAttributes#ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL:kotlin.Int) |

### getFeatureTags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFeatureTags(): MutableSet<String!>
```

Gets the Set of feature tags associated with the current IMS registration, if the IMS service supports supplying this information.

The format of the set of feature tags will be one feature tag key and value per entry and will potentially contain MMTEL and RCS feature tags, depending the configuration of the IMS service associated with the registration indications. Each feature tag will contain the feature tag name and string value (if applicable), even if they have the same feature tag name. For example,`+g.3gpp.icsi-ref="urn%3Aurn-7%3A3gpp-service.ims.icsi.oma.cpm.msg, urn%3Aurn-7%3A3gpp-service.ims.icsi.oma.cpm.session", +g.gsma.callcomposer`will be split into three feature tag entries:`{+g.3gpp.icsi-ref="urn%3Aurn-7%3A3gpp-service.ims.icsi.oma.cpm.msg", +g.3gpp.icsi-ref="urn%3Aurn-7%3A3gpp-service.ims.icsi.oma.cpm.session", +g.gsma.callcomposer}`.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | The Set of feature tags associated with the current IMS registration. This value cannot be`null`. |

### getFlagRegistrationTypeEmergency

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlagRegistrationTypeEmergency(): Boolean
```

Get the attribute flag ATTR_REGISTRATION_TYPE_EMERGENCY.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the ATTR_REGISTRATION_TYPE_EMERGENCY attribute has been set, or`false`if it has not been set. |

### getFlagVirtualRegistrationForEmergencyCall

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlagVirtualRegistrationForEmergencyCall(): Boolean
```

Get the attribute flag ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL attribute has been set, or`false`if it has not been set. |

### getSipDetails

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSipDetails(): SipDetails?
```

| Return ||
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [SipDetails](https://developer.android.com/reference/kotlin/android/telephony/ims/SipDetails)? | The SIP information associated with the IMS registration. This value may be`null`. |

### getTransportType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransportType(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The access network transport type that IMS has been registered over. Value is android.telephony.AccessNetworkConstants.TRANSPORT_TYPE_INVALID, [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WWAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WWAN:kotlin.Int), or [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WLAN](https://developer.android.com/reference/kotlin/android/telephony/AccessNetworkConstants.html#TRANSPORT_TYPE_WLAN:kotlin.Int) |

### hashCode

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ImsRegistrationAttributes!>
```
