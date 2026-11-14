# SignalStrength

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalStrength

Kotlin| [Java](../android/telephony/SignalStrength.md) 
| --- | --- |

```
open class SignalStrength : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SignalStrength](../android/telephony/SignalStrength.md) |

Contains phone signal strength related information.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID](../android/telephony/SignalStrength.md) Indicates the invalid measures of signal strength. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SignalStrength](../android/telephony/SignalStrength.md))`(`s:` ` [SignalStrength](../android/telephony/SignalStrength.md)`)` This constructor is used to create a copy of an existing SignalStrength object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/SignalStrength.md))`()` [Parcelable.describeContents](../android/os/Parcelable.md)) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/telephony/SignalStrength.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaDbm](../android/telephony/SignalStrength.md))`()` Get the CDMA RSSI value in dBm |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaEcio](../android/telephony/SignalStrength.md))`()` Get the CDMA Ec/Io value in dB\*10 |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CellSignalStrength](../android/telephony/CellSignalStrength.md)!\> | [getCellSignalStrengths](../android/telephony/SignalStrength.md))`()` Returns a List of CellSignalStrength Components of this SignalStrength Report. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [getCellSignalStrengths](../android/telephony/SignalStrength.md))`(`clazz:` ` [Class](../java/lang/Class.md)<T>`)` Returns a List of CellSignalStrength Components of this SignalStrength Report. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoDbm](../android/telephony/SignalStrength.md))`()` Get the EVDO RSSI value in dBm |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoEcio](../android/telephony/SignalStrength.md))`()` Get the EVDO Ec/Io value in dB\*10 |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoSnr](../android/telephony/SignalStrength.md))`()` Get the signal to noise ratio. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGsmBitErrorRate](../android/telephony/SignalStrength.md))`()` Get the GSM bit error rate (0-7, 99) as defined in TS 27. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGsmSignalStrength](../android/telephony/SignalStrength.md))`()` Get the GSM RSSI in ASU. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](../android/telephony/SignalStrength.md))`()` Retrieve an abstract level value for the overall signal strength. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](../android/telephony/SignalStrength.md))`()` <br /> Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](../android/os/SystemClock.md))time base. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/telephony/SignalStrength.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGsm](../android/telephony/SignalStrength.md))`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/SignalStrength.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/SignalStrength.md))`(`out:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [Parcelable.writeToParcel](../android/os/Parcelable.md)) |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SignalStrength](../android/telephony/SignalStrength.md)!\> | [CREATOR](../android/telephony/SignalStrength.md) [Parcelable.Creator](../android/os/Parcelable.Creator.md) |

## Constants

### INVALID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID: Int
```

Indicates the invalid measures of signal strength. For example, this can be returned by [getEvdoDbm()](../android/telephony/SignalStrength.md))or [getCdmaDbm()](../android/telephony/SignalStrength.md)) 

 Value: 2147483647

## Public constructors

### SignalStrength

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SignalStrength(s: SignalStrength)
```

This constructor is used to create a copy of an existing SignalStrength object.

| Parameters ||
|-----|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `s` | [SignalStrength](../android/telephony/SignalStrength.md):Source SignalStrength This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

[Parcelable.describeContents](../android/os/Parcelable.md))

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the signal strengths are the same |

### getCdmaDbm

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCdmaDbm(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getCdmaDbm](../android/telephony/CellSignalStrengthCdma.md)).*

Get the CDMA RSSI value in dBm

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the CDMA RSSI value or [INVALID](../android/telephony/SignalStrength.md) if invalid |

**See Also**

- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.SignalStrength#getCellSignalStrengths()](../android/telephony/SignalStrength.md)) 

### getCdmaEcio

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCdmaEcio(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getCdmaEcio](../android/telephony/CellSignalStrengthCdma.md)).*

Get the CDMA Ec/Io value in dB\*10 
**See Also**

- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.SignalStrength#getCellSignalStrengths()](../android/telephony/SignalStrength.md)) 

### getCellSignalStrengths

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCellSignalStrengths(): MutableList<CellSignalStrength!>
```

Returns a List of CellSignalStrength Components of this SignalStrength Report. Use this API to access underlying [CellSignalStrength](../android/telephony/CellSignalStrength.md) objects that provide more granular information about the SignalStrength report. Only valid (non-empty) CellSignalStrengths will be returned. The order of any returned elements is not guaranteed, and the list may contain more than one instance of a CellSignalStrength type.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CellSignalStrength](../android/telephony/CellSignalStrength.md)!> | a List of CellSignalStrength or an empty List if there are no valid measurements. This value cannot be`null`. |

**See Also**

- [android.telephony.CellSignalStrength](../android/telephony/CellSignalStrength.md)
- [android.telephony.CellSignalStrengthNr](../android/telephony/CellSignalStrengthNr.md)
- [android.telephony.CellSignalStrengthLte](../android/telephony/CellSignalStrengthLte.md)
- [android.telephony.CellSignalStrengthTdscdma](../android/telephony/CellSignalStrengthTdscdma.md)
- [android.telephony.CellSignalStrengthWcdma](../android/telephony/CellSignalStrengthWcdma.md)
- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md) 

### getCellSignalStrengths

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : CellSignalStrength!> getCellSignalStrengths(clazz: Class<T>): MutableList<T>
```

Returns a List of CellSignalStrength Components of this SignalStrength Report. Use this API to access underlying [CellSignalStrength](../android/telephony/CellSignalStrength.md) objects that provide more granular information about the SignalStrength report. Only valid (non-empty) CellSignalStrengths will be returned. The order of any returned elements is not guaranteed, and the list may contain more than one instance of a CellSignalStrength type.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clazz` | [Class](../java/lang/Class.md)\<T\>:a class type that extends [CellSignalStrength](../android/telephony/CellSignalStrength.md) to filter possible return values. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | a List of CellSignalStrength or an empty List if there are no valid measurements. This value cannot be`null`. |

**See Also**

- [android.telephony.CellSignalStrength](../android/telephony/CellSignalStrength.md)
- [android.telephony.CellSignalStrengthNr](../android/telephony/CellSignalStrengthNr.md)
- [android.telephony.CellSignalStrengthLte](../android/telephony/CellSignalStrengthLte.md)
- [android.telephony.CellSignalStrengthTdscdma](../android/telephony/CellSignalStrengthTdscdma.md)
- [android.telephony.CellSignalStrengthWcdma](../android/telephony/CellSignalStrengthWcdma.md)
- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md) 

### getEvdoDbm

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvdoDbm(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getEvdoDbm](../android/telephony/CellSignalStrengthCdma.md)).*

Get the EVDO RSSI value in dBm

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the EVDO RSSI value or [INVALID](../android/telephony/SignalStrength.md) if invalid |

**See Also**

- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.SignalStrength#getCellSignalStrengths()](../android/telephony/SignalStrength.md)) 

### getEvdoEcio

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvdoEcio(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getEvdoEcio](../android/telephony/CellSignalStrengthCdma.md)).*

Get the EVDO Ec/Io value in dB\*10 
**See Also**

- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.SignalStrength#getCellSignalStrengths()](../android/telephony/SignalStrength.md)) 

### getEvdoSnr

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvdoSnr(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getEvdoSnr](../android/telephony/CellSignalStrengthCdma.md)).*

Get the signal to noise ratio. Valid values are 0-8. 8 is the highest. 
**See Also**

- [android.telephony.CellSignalStrengthCdma](../android/telephony/CellSignalStrengthCdma.md)
- [android.telephony.SignalStrength#getCellSignalStrengths()](../android/telephony/SignalStrength.md)) 

### getGsmBitErrorRate

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGsmBitErrorRate(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthGsm.getBitErrorRate](../android/telephony/CellSignalStrengthGsm.md)).*

Get the GSM bit error rate (0-7, 99) as defined in TS 27.007 8.5 
**See Also**

- [android.telephony.CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md)
- [android.telephony.SignalStrength#getCellSignalStrengths()](../android/telephony/SignalStrength.md)) 

### getGsmSignalStrength

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGsmSignalStrength(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthGsm.getAsuLevel](../android/telephony/CellSignalStrengthGsm.md)).*

Get the GSM RSSI in ASU. Asu is calculated based on 3GPP RSRP. Refer to 3GPP 27.007 (Ver 10.3.0) Sec 8.69

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | RSSI in ASU 0..31, 99, or UNAVAILABLE |

**See Also**

- [android.telephony.CellSignalStrengthGsm](../android/telephony/CellSignalStrengthGsm.md) 

### getLevel

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLevel(): Int
```

Retrieve an abstract level value for the overall signal strength.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a single integer from 0 to 4 representing the general signal quality. This may take into account many different radio technology inputs. 0 represents very poor signal strength while 4 represents a very strong signal strength. |

### getTimestampMillis

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTimestampMillis(): Long
```

<br />

Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](../android/os/SystemClock.md))time base.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | timestamp in milliseconds since boot for [SignalStrength](../android/telephony/SignalStrength.md). This timestamp reports the approximate time that the signal was measured and reported by the modem. It can be used to compare the recency of [SignalStrength](../android/telephony/SignalStrength.md) instances. Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](../android/os/SystemClock.md))time base. |

### hashCode

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|-----------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hash code |

### isGsm

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isGsm(): Boolean
```

**Deprecated:** *This method returns true if there are any 3gpp type SignalStrength elements in this SignalStrength report or if the report contains no valid SignalStrength information. Instead callers should use android.telephony.SignalStrength#getCellSignalStrengths to determine which types of information are contained in the SignalStrength report.*

| Return ||
|------------------------------------------------------------------------------------|-------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this is for GSM |

### toString

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | string representation. |

### writeToParcel

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

[Parcelable.writeToParcel](../android/os/Parcelable.md))

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SignalStrength!>
```

[Parcelable.Creator](../android/os/Parcelable.Creator.md)
