# ImsRegistrationAttributes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ImsRegistrationAttributes

Kotlin| [Java](../android/telephony/ims/ImsRegistrationAttributes.md) 
| --- | --- |

```
class ImsRegistrationAttributes : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.ims.ImsRegistrationAttributes](../android/telephony/ims/ImsRegistrationAttributes.md) |

Contains the attributes associated with the current IMS registration.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTR_EPDG_OVER_CELL_INTERNET](../android/telephony/ims/ImsRegistrationAttributes.md) Attribute to specify if an EPDG tunnel is setup over the cellular internet APN. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTR_REGISTRATION_TYPE_EMERGENCY](../android/telephony/ims/ImsRegistrationAttributes.md) Attribute to specify if ims registration is of type normal or emergency. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL](../android/telephony/ims/ImsRegistrationAttributes.md) Attribute to specify if virtual registration is required. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/ims/ImsRegistrationAttributes.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/ims/ImsRegistrationAttributes.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAttributeFlags](../android/telephony/ims/ImsRegistrationAttributes.md))`()` <br /> |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getFeatureTags](../android/telephony/ims/ImsRegistrationAttributes.md))`()` Gets the Set of feature tags associated with the current IMS registration, if the IMS service supports supplying this information. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFlagRegistrationTypeEmergency](../android/telephony/ims/ImsRegistrationAttributes.md))`()` Get the attribute flag ATTR_REGISTRATION_TYPE_EMERGENCY. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getFlagVirtualRegistrationForEmergencyCall](../android/telephony/ims/ImsRegistrationAttributes.md))`()` Get the attribute flag ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL. |
| --- | --- |
| [SipDetails](../android/telephony/ims/SipDetails.md)? | [getSipDetails](../android/telephony/ims/ImsRegistrationAttributes.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTransportType](../android/telephony/ims/ImsRegistrationAttributes.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/ims/ImsRegistrationAttributes.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/ims/ImsRegistrationAttributes.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/ims/ImsRegistrationAttributes.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ImsRegistrationAttributes](../android/telephony/ims/ImsRegistrationAttributes.md)!\> | [CREATOR](../android/telephony/ims/ImsRegistrationAttributes.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | A bit-mask containing attributes associated with the IMS registration. Value is either`0`or a combination of [android.telephony.ims.ImsRegistrationAttributes#ATTR_EPDG_OVER_CELL_INTERNET](../android/telephony/ims/ImsRegistrationAttributes.md), [android.telephony.ims.ImsRegistrationAttributes#ATTR_REGISTRATION_TYPE_EMERGENCY](../android/telephony/ims/ImsRegistrationAttributes.md), and [android.telephony.ims.ImsRegistrationAttributes#ATTR_VIRTUAL_FOR_ANONYMOUS_EMERGENCY_CALL](../android/telephony/ims/ImsRegistrationAttributes.md) |

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
| [SipDetails](../android/telephony/ims/SipDetails.md)? | The SIP information associated with the IMS registration. This value may be`null`. |

### getTransportType

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTransportType(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The access network transport type that IMS has been registered over. Value is android.telephony.AccessNetworkConstants.TRANSPORT_TYPE_INVALID, [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WWAN](../android/telephony/AccessNetworkConstants.md), or [android.telephony.AccessNetworkConstants#TRANSPORT_TYPE_WLAN](../android/telephony/AccessNetworkConstants.md) |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ImsRegistrationAttributes!>
```
