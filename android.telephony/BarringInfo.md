# BarringInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BarringInfo

Kotlin | [Java](https://developer.android.com/reference/android/telephony/BarringInfo "View this page in Java") 
| --- | --- |

```
class BarringInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#) |

Provides the barring configuration for a particular service type. Provides indication about the barring of a particular service for use. Certain barring types are only valid for certain technology families. Any service that does not have a barring configuration is unbarred by default.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [BarringServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo.BarringServiceInfo) Describe the current barring configuration of a cell |

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_CS_FALLBACK](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_CS_FALLBACK:kotlin.Int) Barring indicator for circuit-switched fallback for voice; applicable to EUTRAN and NGRAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_CS_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_CS_SERVICE:kotlin.Int) Barring indicator for circuit-switched service; applicable to UTRAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_CS_VOICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_CS_VOICE:kotlin.Int) Barring indicator for circuit-switched voice service; applicable to UTRAN |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_EMERGENCY:kotlin.Int) Barring indicator for emergency services; applicable to UTRAN, EUTRAN, and NGRAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_MMTEL_VIDEO](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MMTEL_VIDEO:kotlin.Int) Barring indicator for MMTEL (IMS) video; applicable to EUTRAN and NGRAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_MMTEL_VOICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MMTEL_VOICE:kotlin.Int) Barring indicator for MMTEL (IMS) voice; applicable to EUTRAN and NGRAN |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_MO_DATA](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MO_DATA:kotlin.Int) Barring indicator for mobile-originated data traffic; applicable to EUTRAN and NGRAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_MO_SIGNALLING](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MO_SIGNALLING:kotlin.Int) Barring indicator for mobile-originated signalling; applicable to EUTRAN and NGRAN |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_PS_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_PS_SERVICE:kotlin.Int) Barring indicator for packet-switched service; applicable to UTRAN |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BARRING_SERVICE_TYPE_SMS](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_SMS:kotlin.Int) Barring indicator for SMS sending; applicable to UTRAN, EUTRAN, and NGRAN |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [BarringInfo.BarringServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo.BarringServiceInfo) | [getBarringServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#getBarringServiceInfo(kotlin.Int))`(`service:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the BarringServiceInfo for a specified service. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BarringInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### BARRING_SERVICE_TYPE_CS_FALLBACK

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_CS_FALLBACK: Int
```

Barring indicator for circuit-switched fallback for voice; applicable to EUTRAN and NGRAN 

 Value: 5

### BARRING_SERVICE_TYPE_CS_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_CS_SERVICE: Int
```

Barring indicator for circuit-switched service; applicable to UTRAN 

 Value: 0

### BARRING_SERVICE_TYPE_CS_VOICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_CS_VOICE: Int
```

Barring indicator for circuit-switched voice service; applicable to UTRAN 

 Value: 2

### BARRING_SERVICE_TYPE_EMERGENCY

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_EMERGENCY: Int
```

Barring indicator for emergency services; applicable to UTRAN, EUTRAN, and NGRAN 

 Value: 8

### BARRING_SERVICE_TYPE_MMTEL_VIDEO

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_MMTEL_VIDEO: Int
```

Barring indicator for MMTEL (IMS) video; applicable to EUTRAN and NGRAN 

 Value: 7

### BARRING_SERVICE_TYPE_MMTEL_VOICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_MMTEL_VOICE: Int
```

Barring indicator for MMTEL (IMS) voice; applicable to EUTRAN and NGRAN 

 Value: 6

### BARRING_SERVICE_TYPE_MO_DATA

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_MO_DATA: Int
```

Barring indicator for mobile-originated data traffic; applicable to EUTRAN and NGRAN 

 Value: 4

### BARRING_SERVICE_TYPE_MO_SIGNALLING

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_MO_SIGNALLING: Int
```

Barring indicator for mobile-originated signalling; applicable to EUTRAN and NGRAN 

 Value: 3

### BARRING_SERVICE_TYPE_PS_SERVICE

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_PS_SERVICE: Int
```

Barring indicator for packet-switched service; applicable to UTRAN 

 Value: 1

### BARRING_SERVICE_TYPE_SMS

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BARRING_SERVICE_TYPE_SMS: Int
```

Barring indicator for SMS sending; applicable to UTRAN, EUTRAN, and NGRAN 

 Value: 9

## Public methods

### describeContents

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getBarringServiceInfo

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBarringServiceInfo(service: Int): BarringInfo.BarringServiceInfo
```

Get the BarringServiceInfo for a specified service.

| Parameters ||
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `service` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_CS_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_CS_SERVICE:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_PS_SERVICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_PS_SERVICE:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_CS_VOICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_CS_VOICE:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_MO_SIGNALLING](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MO_SIGNALLING:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_MO_DATA](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MO_DATA:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_CS_FALLBACK](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_CS_FALLBACK:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_MMTEL_VOICE](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MMTEL_VOICE:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_MMTEL_VIDEO](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_MMTEL_VIDEO:kotlin.Int), [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_EMERGENCY](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_EMERGENCY:kotlin.Int), or [android.telephony.BarringInfo#BARRING_SERVICE_TYPE_SMS](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo#BARRING_SERVICE_TYPE_SMS:kotlin.Int) |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [BarringInfo.BarringServiceInfo](https://developer.android.com/reference/kotlin/android/telephony/BarringInfo.BarringServiceInfo) | a BarringServiceInfo struct describing the current barring status for a service This value cannot be `null`. |

### hashCode

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<BarringInfo!>
```
