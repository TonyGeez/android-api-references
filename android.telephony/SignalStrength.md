# SignalStrength

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SignalStrength

Kotlin| [Java](https://developer.android.com/reference/android/telephony/SignalStrength "View this page in Java") 
| --- | --- |

```
open class SignalStrength : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#) |

Contains phone signal strength related information.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INVALID](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#INVALID:kotlin.Int) Indicates the invalid measures of signal strength. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#SignalStrength(android.telephony.SignalStrength))`(`s:` ` [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#)`)` This constructor is used to create a copy of an existing SignalStrength object. |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#describeContents())`()` [Parcelable.describeContents](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()) |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaDbm](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCdmaDbm())`()` Get the CDMA RSSI value in dBm |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCdmaEcio](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCdmaEcio())`()` Get the CDMA Ec/Io value in dB\*10 |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength)!\> | [getCellSignalStrengths](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths())`()` Returns a List of CellSignalStrength Components of this SignalStrength Report. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\<T\> | [getCellSignalStrengths](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths(java.lang.Class))`(`clazz:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<T>`)` Returns a List of CellSignalStrength Components of this SignalStrength Report. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoDbm](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getEvdoDbm())`()` Get the EVDO RSSI value in dBm |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoEcio](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getEvdoEcio())`()` Get the EVDO Ec/Io value in dB\*10 |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEvdoSnr](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getEvdoSnr())`()` Get the signal to noise ratio. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGsmBitErrorRate](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getGsmBitErrorRate())`()` Get the GSM bit error rate (0-7, 99) as defined in TS 27. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGsmSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getGsmSignalStrength())`()` Get the GSM RSSI in ASU. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLevel](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getLevel())`()` Retrieve an abstract level value for the overall signal strength. |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getTimestampMillis())`()` <br /> Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime())time base. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#hashCode())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isGsm](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#isGsm())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#toString())`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`out:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` [Parcelable.writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)) |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#CREATOR:android.os.Parcelable.Creator) [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#) |

## Constants

### INVALID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val INVALID: Int
```

Indicates the invalid measures of signal strength. For example, this can be returned by [getEvdoDbm()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getEvdoDbm())or [getCdmaDbm()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCdmaDbm()) 

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
| `s` | [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#):Source SignalStrength This value cannot be`null`. |

## Public methods

### describeContents

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

[Parcelable.describeContents](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents())

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getCdmaDbm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma#getCdmaDbm()).*

Get the CDMA RSSI value in dBm

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the CDMA RSSI value or [INVALID](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#INVALID:kotlin.Int) if invalid |

**See Also**

- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.SignalStrength#getCellSignalStrengths()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths()) 

### getCdmaEcio

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCdmaEcio(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getCdmaEcio](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma#getCdmaEcio()).*

Get the CDMA Ec/Io value in dB\*10 
**See Also**

- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.SignalStrength#getCellSignalStrengths()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths()) 

### getCellSignalStrengths

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCellSignalStrengths(): MutableList<CellSignalStrength!>
```

Returns a List of CellSignalStrength Components of this SignalStrength Report. Use this API to access underlying [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) objects that provide more granular information about the SignalStrength report. Only valid (non-empty) CellSignalStrengths will be returned. The order of any returned elements is not guaranteed, and the list may contain more than one instance of a CellSignalStrength type.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength)!> | a List of CellSignalStrength or an empty List if there are no valid measurements. This value cannot be`null`. |

**See Also**

- [android.telephony.CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength)
- [android.telephony.CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr)
- [android.telephony.CellSignalStrengthLte](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte)
- [android.telephony.CellSignalStrengthTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthTdscdma)
- [android.telephony.CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma)
- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm) 

### getCellSignalStrengths

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun <T : CellSignalStrength!> getCellSignalStrengths(clazz: Class<T>): MutableList<T>
```

Returns a List of CellSignalStrength Components of this SignalStrength Report. Use this API to access underlying [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) objects that provide more granular information about the SignalStrength report. Only valid (non-empty) CellSignalStrengths will be returned. The order of any returned elements is not guaranteed, and the list may contain more than one instance of a CellSignalStrength type.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `clazz` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<T\>:a class type that extends [CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength) to filter possible return values. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)<T> | a List of CellSignalStrength or an empty List if there are no valid measurements. This value cannot be`null`. |

**See Also**

- [android.telephony.CellSignalStrength](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrength)
- [android.telephony.CellSignalStrengthNr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthNr)
- [android.telephony.CellSignalStrengthLte](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthLte)
- [android.telephony.CellSignalStrengthTdscdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthTdscdma)
- [android.telephony.CellSignalStrengthWcdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthWcdma)
- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm) 

### getEvdoDbm

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvdoDbm(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getEvdoDbm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma#getEvdoDbm()).*

Get the EVDO RSSI value in dBm

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the EVDO RSSI value or [INVALID](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#INVALID:kotlin.Int) if invalid |

**See Also**

- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.SignalStrength#getCellSignalStrengths()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths()) 

### getEvdoEcio

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvdoEcio(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getEvdoEcio](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma#getEvdoEcio()).*

Get the EVDO Ec/Io value in dB\*10 
**See Also**

- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.SignalStrength#getCellSignalStrengths()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths()) 

### getEvdoSnr

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvdoSnr(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthCdma.getEvdoSnr](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma#getEvdoSnr()).*

Get the signal to noise ratio. Valid values are 0-8. 8 is the highest. 
**See Also**

- [android.telephony.CellSignalStrengthCdma](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthCdma)
- [android.telephony.SignalStrength#getCellSignalStrengths()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths()) 

### getGsmBitErrorRate

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGsmBitErrorRate(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthGsm.getBitErrorRate](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getBitErrorRate()).*

Get the GSM bit error rate (0-7, 99) as defined in TS 27.007 8.5 
**See Also**

- [android.telephony.CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm)
- [android.telephony.SignalStrength#getCellSignalStrengths()](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#getCellSignalStrengths()) 

### getGsmSignalStrength

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getGsmSignalStrength(): Int
```

**Deprecated:** *this information should be retrieved from [CellSignalStrengthGsm.getAsuLevel](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm#getAsuLevel()).*

Get the GSM RSSI in ASU. Asu is calculated based on 3GPP RSRP. Refer to 3GPP 27.007 (Ver 10.3.0) Sec 8.69

| Return ||
|----------------------------------------------------------------------------|---------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | RSSI in ASU 0..31, 99, or UNAVAILABLE |

**See Also**

- [android.telephony.CellSignalStrengthGsm](https://developer.android.com/reference/kotlin/android/telephony/CellSignalStrengthGsm) 

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

Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime())time base.

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | timestamp in milliseconds since boot for [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#). This timestamp reports the approximate time that the signal was measured and reported by the modem. It can be used to compare the recency of [SignalStrength](https://developer.android.com/reference/kotlin/android/telephony/SignalStrength#) instances. Value is a non-negative timestamp in the [android.os.SystemClock#elapsedRealtime()](https://developer.android.com/reference/kotlin/android/os/SystemClock.html#elapsedRealtime())time base. |

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

[Parcelable.writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int))

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SignalStrength!>
```

[Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)
