# HomeSp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HomeSp

Kotlin| [Java](../android/net/wifi/hotspot2/pps/HomeSp.md) 
| --- | --- |

```
class HomeSp : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.hotspot2.pps.HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md) |

Class representing HomeSP subtree in PerProviderSubscription (PPS) Management Object (MO) tree. For more info, refer to Hotspot 2.0 PPS MO defined in section 9.1 of the Hotspot 2.0 Release 2 Technical Specification.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Constructor for creating HomeSp with default values. |
| [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`source:` ` [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md)!`)` Copy constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFqdn](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Get the FQDN (Fully Qualified Domain Name) associated with this home service provider. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFriendlyName](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Get the friendly name associated with this home service provider. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getMatchAllOis](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Get the list of HomeOIs such that all OIs in the list must match an OI in the Roaming Consortium advertised by a hotspot operator. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getMatchAnyOis](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Get a list of HomeOIs such that any OI in the list matches an OI in the Roaming Consortium advertised by a hotspot operator. |
| --- | --- |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getOtherHomePartnersList](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Get the list of FQDN (Fully Qualified Domain Name) of other Home partner providers set in the profile. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [getRoamingConsortiumOis](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` Get the Organization Identifiers (OIs) identifying a roaming consortium of which this provider is a member. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFqdn](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`fqdn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the FQDN (Fully Qualified Domain Name) associated with this home service provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFriendlyName](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`friendlyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the friendly name associated with this home service provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatchAllOis](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`matchAllOis:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?`)` Set a list of HomeOIs such that all OIs in the list must match an OI in the Roaming Consortium advertised by a hotspot operator. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatchAnyOis](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`matchAnyOis:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?`)` Set a list of HomeOIs such that any OI in the list matches an OI in the Roaming Consortium advertised by a hotspot operator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOtherHomePartnersList](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`otherHomePartners:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Set the list of FQDN (Fully Qualified Domain Name) of other Home partner providers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoamingConsortiumOis](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`roamingConsortiumOis:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Set the Organization Identifiers (OIs) identifying a roaming consortium of which this provider is a member. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/wifi/hotspot2/pps/HomeSp.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/wifi/hotspot2/pps/HomeSp.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md)!\> | [CREATOR](../android/net/wifi/hotspot2/pps/HomeSp.md) <br /> |

## Public constructors

### HomeSp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HomeSp()
```

Constructor for creating HomeSp with default values. 

### HomeSp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
HomeSp(source: HomeSp!)
```

Copy constructor.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------|
| `source` | [HomeSp](../android/net/wifi/hotspot2/pps/HomeSp.md)!:The source to copy from |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getFqdn

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFqdn(): String!
```

Get the FQDN (Fully Qualified Domain Name) associated with this home service provider.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the FQDN associated with this home service provider |

### getFriendlyName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFriendlyName(): String!
```

Get the friendly name associated with this home service provider.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the friendly name associated with this home service provider |

### getMatchAllOis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchAllOis(): LongArray?
```

Get the list of HomeOIs such that all OIs in the list must match an OI in the Roaming Consortium advertised by a hotspot operator.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | An array of longs containing the HomeOIs This value may be`null`. |

### getMatchAnyOis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatchAnyOis(): LongArray?
```

Get a list of HomeOIs such that any OI in the list matches an OI in the Roaming Consortium advertised by a hotspot operator.

| Return ||
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | An array of longs containing the HomeOIs This value may be`null`. |

### getOtherHomePartnersList

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOtherHomePartnersList(): MutableCollection<String!>
```

Get the list of FQDN (Fully Qualified Domain Name) of other Home partner providers set in the profile.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | Collection of Strings containing the FQDNs of other Home partner providers set in the profile This value cannot be`null`. |

### getRoamingConsortiumOis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoamingConsortiumOis(): LongArray!
```

Get the Organization Identifiers (OIs) identifying a roaming consortium of which this provider is a member.

| Return ||
|------------------------------------------------------------------------------------------|---------------------------------|
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | array of roaming consortium OIs |

### hashCode

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setFqdn

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFqdn(fqdn: String!): Unit
```

Set the FQDN (Fully Qualified Domain Name) associated with this home service provider.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------|
| `fqdn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The FQDN to set to |

### setFriendlyName

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setFriendlyName(friendlyName: String!): Unit
```

Set the friendly name associated with this home service provider.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------|
| `friendlyName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The friendly name to set to |

### setMatchAllOis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMatchAllOis(matchAllOis: LongArray?): Unit
```

Set a list of HomeOIs such that all OIs in the list must match an OI in the Roaming Consortium advertised by a hotspot operator. The list set by this API will have precedence over[setMatchAnyOis(long[])](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setMatchAnyOis(kotlin.LongArray)), meaning the list set in[setMatchAnyOis(long[])](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setMatchAnyOis(kotlin.LongArray))will only be used for matching if the list set by this API is null or empty.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `matchAllOis` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?:An array of longs containing the HomeOIs This value may be`null`. |

### setMatchAnyOis

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMatchAnyOis(matchAnyOis: LongArray?): Unit
```

Set a list of HomeOIs such that any OI in the list matches an OI in the Roaming Consortium advertised by a hotspot operator. The list set by[setMatchAllOis(long[])](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setMatchAllOis(kotlin.LongArray))will have precedence over this API, meaning this list will only be used for matching if the list set by[setMatchAllOis(long[])](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setMatchAllOis(kotlin.LongArray))is null or empty.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `matchAnyOis` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?:An array of longs containing the HomeOIs This value may be`null`. |

### setOtherHomePartnersList

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOtherHomePartnersList(otherHomePartners: MutableCollection<String!>): Unit
```

Set the list of FQDN (Fully Qualified Domain Name) of other Home partner providers.

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `otherHomePartners` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:Collection of Strings containing the FQDNs of other Home partner providers This value cannot be`null`. |

### setRoamingConsortiumOis

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setRoamingConsortiumOis(roamingConsortiumOis: LongArray!): Unit
```

Set the Organization Identifiers (OIs) identifying a roaming consortium of which this provider is a member.

| Parameters ||
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `roamingConsortiumOis` | [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!:Array of roaming consortium OIs |

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<HomeSp!>
```
