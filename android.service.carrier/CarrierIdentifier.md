# CarrierIdentifier

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CarrierIdentifier

Kotlin| [Java](https://developer.android.com/reference/android/service/carrier/CarrierIdentifier "View this page in Java") 

```
open class CarrierIdentifier : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.service.carrier.CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#) |

Used to pass info to CarrierConfigService implementations so they can decide what values to return. Instead of passing mcc, mnc, gid1, gid2, spn, imsi to locate carrier information, CarrierIdentifier also include carrier id [TelephonyManager.getSimCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSimCarrierId()), a platform-wide unique identifier for each carrier. CarrierConfigService can directly use carrier id as the key to look up the carrier info.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#CarrierIdentifier(kotlin.ByteArray,%20kotlin.String,%20kotlin.String))`(`mccMnc:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `gid1:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `gid2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Creates a carrier identifier instance. |
| [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#CarrierIdentifier(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String))`(`mcc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mnc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `spn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `imsi:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `gid1:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `gid2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> |
| [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#CarrierIdentifier(kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.String,%20kotlin.Int,%20kotlin.Int))`(`mcc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `mnc:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `spn:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `imsi:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `gid1:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `gid2:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `carrierid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `specificCarrierId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCarrierId](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getCarrierId())`()` Returns the carrier id. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getGid1](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getGid1())`()` Get the group identifier level 1. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getGid2](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getGid2())`()` Get the group identifier level 2. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getImsi](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getImsi())`()` Get the international mobile subscriber identity. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMcc](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getMcc())`()` Get the mobile country code. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getMnc](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getMnc())`()` Get the mobile network code. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpecificCarrierId](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getSpecificCarrierId())`()` A specific carrier ID returns the fine-grained carrier ID of the current subscription. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSpn](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#getSpn())`()` Get the service provider name. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#hashCode())`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#CREATOR:android.os.Parcelable.Creator) Used to create a [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#) from a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

## Public constructors

### CarrierIdentifier

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CarrierIdentifier(
    mccMnc: ByteArray!, 
    gid1: String?, 
    gid2: String?)
```

Creates a carrier identifier instance.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------|
| `mccMnc` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:A 3-byte array as defined by 3GPP TS 24.008. |
| `gid1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The group identifier level 1. This value may be`null`. |
| `gid2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The group identifier level 2. This value may be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.IllegalArgumentException` | If the length of`mccMnc`is not 3. |

### CarrierIdentifier

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CarrierIdentifier(
    mcc: String!, 
    mnc: String!, 
    spn: String?, 
    imsi: String?, 
    gid1: String?, 
    gid2: String?)
```

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------|
| `spn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `imsi` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `gid1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |
| `gid2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

### CarrierIdentifier

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CarrierIdentifier(
    mcc: String, 
    mnc: String, 
    spn: String?, 
    imsi: String?, 
    gid1: String?, 
    gid2: String?, 
    carrierid: Int, 
    specificCarrierId: Int)
```

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mcc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):mobile country code This value cannot be`null`. |
| `mnc` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):mobile network code This value cannot be`null`. |
| `spn` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:service provider name This value may be`null`. |
| `imsi` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:International Mobile Subscriber Identity [TelephonyManager.getSubscriberId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSubscriberId())This value may be`null`. |
| `gid1` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:group id level 1 [TelephonyManager.getGroupIdLevel1()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getGroupIdLevel1())This value may be`null`. |
| `gid2` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:group id level 2 This value may be`null`. |
| `carrierid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):carrier unique identifier [TelephonyManager.getSimCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSimCarrierId()), used to uniquely identify the carrier and look up the carrier configurations. |
| `specificCarrierId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):specific carrier identifier [TelephonyManager.getSimSpecificCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSimSpecificCarrierId()) |

## Public methods

### describeContents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCarrierId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCarrierId(): Int
```

Returns the carrier id. 
**See Also**

- [android.telephony.TelephonyManager#getSimCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSimCarrierId()) 

### getGid1

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGid1(): String?
```

Get the group identifier level 1.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getGid2

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGid2(): String?
```

Get the group identifier level 2.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getImsi

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getImsi(): String?
```

Get the international mobile subscriber identity.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getMcc

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMcc(): String!
```

Get the mobile country code. 

### getMnc

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMnc(): String!
```

Get the mobile network code. 

### getSpecificCarrierId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpecificCarrierId(): Int
```

A specific carrier ID returns the fine-grained carrier ID of the current subscription. It can represent the fact that a carrier may be in effect an aggregation of other carriers (ie in an MVNO type scenario) where each of these specific carriers which are used to make up the actual carrier service may have different carrier configurations. A specific carrier ID could also be used, for example, in a scenario where a carrier requires different carrier configuration for different service offering such as a prepaid plan. 
**See Also**

- [android.telephony.TelephonyManager#getSimSpecificCarrierId()](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager.html#getSimSpecificCarrierId()) 

### getSpn

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpn(): String?
```

Get the service provider name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### hashCode

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<CarrierIdentifier!>
```

Used to create a [CarrierIdentifier](https://developer.android.com/reference/kotlin/android/service/carrier/CarrierIdentifier#) from a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).
