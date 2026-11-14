# HomeSp

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HomeSp

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/hotspot2/pps/HomeSp "View this page in Java") 

```
class HomeSp : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.wifi.hotspot2.pps.HomeSp](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#) |

Class representing HomeSP subtree in PerProviderSubscription (PPS) Management Object (MO) tree. For more info, refer to Hotspot 2.0 PPS MO defined in section 9.1 of the Hotspot 2.0 Release 2 Technical Specification.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [HomeSp](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#HomeSp())`()` Constructor for creating HomeSp with default values. |
| [HomeSp](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#HomeSp(android.net.wifi.hotspot2.pps.HomeSp))`(`source:` ` [HomeSp](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#)!`)` Copy constructor. |

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFqdn](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#getFqdn())`()` Get the FQDN (Fully Qualified Domain Name) associated with this home service provider. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getFriendlyName](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#getFriendlyName())`()` Get the friendly name associated with this home service provider. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getMatchAllOis](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#getMatchAllOis())`()` Get the list of HomeOIs such that all OIs in the list must match an OI in the Roaming Consortium advertised by a hotspot operator. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)? | [getMatchAnyOis](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#getMatchAnyOis())`()` Get a list of HomeOIs such that any OI in the list matches an OI in the Roaming Consortium advertised by a hotspot operator. |
| [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getOtherHomePartnersList](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#getOtherHomePartnersList())`()` Get the list of FQDN (Fully Qualified Domain Name) of other Home partner providers set in the profile. |
| [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)! | [getRoamingConsortiumOis](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#getRoamingConsortiumOis())`()` Get the Organization Identifiers (OIs) identifying a roaming consortium of which this provider is a member. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFqdn](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setFqdn(kotlin.String))`(`fqdn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the FQDN (Fully Qualified Domain Name) associated with this home service provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFriendlyName](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setFriendlyName(kotlin.String))`(`friendlyName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the friendly name associated with this home service provider. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatchAllOis](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setMatchAllOis(kotlin.LongArray))`(`matchAllOis:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?`)` Set a list of HomeOIs such that all OIs in the list must match an OI in the Roaming Consortium advertised by a hotspot operator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatchAnyOis](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setMatchAnyOis(kotlin.LongArray))`(`matchAnyOis:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)?`)` Set a list of HomeOIs such that any OI in the list matches an OI in the Roaming Consortium advertised by a hotspot operator. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOtherHomePartnersList](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setOtherHomePartnersList(kotlin.collections.MutableCollection))`(`otherHomePartners:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Set the list of FQDN (Fully Qualified Domain Name) of other Home partner providers. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRoamingConsortiumOis](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#setRoamingConsortiumOis(kotlin.LongArray))`(`roamingConsortiumOis:` ` [LongArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long-array/index.html)!`)` Set the Organization Identifiers (OIs) identifying a roaming consortium of which this provider is a member. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [HomeSp](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#CREATOR:android.os.Parcelable.Creator) <br /> |

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
| `source` | [HomeSp](https://developer.android.com/reference/kotlin/android/net/wifi/hotspot2/pps/HomeSp#)!:The source to copy from |

## Public methods

### describeContents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<HomeSp!>
```
