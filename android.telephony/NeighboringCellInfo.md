# NeighboringCellInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NeighboringCellInfo

Kotlin| [Java](../android/telephony/NeighboringCellInfo.md) 
| --- | --- |

```
open class NeighboringCellInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md) |

| **This class was deprecated in API level 29.**
|
| This class should not be used by any app targeting [Android Q](../android/os/Build.VERSION_CODES.md) or higher. Instead callers should use [CellInfo](../android/telephony/CellInfo.md).

Represents the neighboring cell information, including Received Signal Strength and Cell ID location.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_CID](../android/telephony/NeighboringCellInfo.md) Cell location is not available |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_RSSI](../android/telephony/NeighboringCellInfo.md) Signal strength is not available |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md))`()` Empty constructor. |
| [NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md))`(`in:` ` [Parcel](../android/os/Parcel.md)!`)` Initialize the object from a parcel. |
| [NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md))`(`rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initialize the object from rssi and cid. |
| [NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md))`(`rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `location:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `radioType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initialize the object from rssi, location string, and radioType radioType is one of following [TelephonyManager.NETWORK_TYPE_GPRS](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_EDGE](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_UMTS](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_HSDPA](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_HSUPA](../android/telephony/TelephonyManager.md), and [TelephonyManager.NETWORK_TYPE_HSPA](../android/telephony/TelephonyManager.md). |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCid](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLac](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkType](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPsc](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCid](../android/telephony/NeighboringCellInfo.md))`(`cid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the cell id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRssi](../android/telephony/NeighboringCellInfo.md))`(`rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the signal strength of the cell. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/telephony/NeighboringCellInfo.md))`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/telephony/NeighboringCellInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NeighboringCellInfo](../android/telephony/NeighboringCellInfo.md)!\> | [CREATOR](../android/telephony/NeighboringCellInfo.md) <br /> |

## Constants

### UNKNOWN_CID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_CID: Int
```

**Deprecated:** *Deprecated in Java.*

Cell location is not available 

 Value: -1

### UNKNOWN_RSSI

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val UNKNOWN_RSSI: Int
```

**Deprecated:** *Deprecated in Java.*

Signal strength is not available 

 Value: 99

## Public constructors

### NeighboringCellInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NeighboringCellInfo()
```

**Deprecated:** *by [NeighboringCellInfo(int,java.lang.String,int)](../android/telephony/NeighboringCellInfo.md))*

Empty constructor. Initializes the RSSI and CID. NeighboringCellInfo is one time shot for the neighboring cells based on the radio network type at that moment. Its constructor needs radio network type. 

### NeighboringCellInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NeighboringCellInfo(in: Parcel!)
```

Initialize the object from a parcel. 

### NeighboringCellInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NeighboringCellInfo(
    rssi: Int, 
    cid: Int)
```

**Deprecated:** *by [NeighboringCellInfo(int,java.lang.String,int)](../android/telephony/NeighboringCellInfo.md))*

Initialize the object from rssi and cid. NeighboringCellInfo is one time shot for the neighboring cells based on the radio network type at that moment. Its constructor needs radio network type. 

### NeighboringCellInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NeighboringCellInfo(
    rssi: Int, 
    location: String!, 
    radioType: Int)
```

Initialize the object from rssi, location string, and radioType radioType is one of following [TelephonyManager.NETWORK_TYPE_GPRS](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_EDGE](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_UMTS](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_HSDPA](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_HSUPA](../android/telephony/TelephonyManager.md), and [TelephonyManager.NETWORK_TYPE_HSPA](../android/telephony/TelephonyManager.md).

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getCid

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCid(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | cell id in GSM, 0xffff max legal value UNKNOWN_CID if in UMTS or CDMA or unknown |

### getLac

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLac(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | LAC in GSM, 0xffff max legal value UNKNOWN_CID if in UMTS or CMDA or unknown |

### getNetworkType

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkType(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Radio network type while neighboring cell location is stored. Return [TelephonyManager.NETWORK_TYPE_UNKNOWN](../android/telephony/TelephonyManager.md) means that the location information is unavailable. Return [TelephonyManager.NETWORK_TYPE_GPRS](../android/telephony/TelephonyManager.md) or [TelephonyManager.NETWORK_TYPE_EDGE](../android/telephony/TelephonyManager.md) means that Neighboring Cell information is stored for GSM network, in which [NeighboringCellInfo.getLac](../android/telephony/NeighboringCellInfo.md))and [NeighboringCellInfo.getCid](../android/telephony/NeighboringCellInfo.md))should be called to access location. Return [TelephonyManager.NETWORK_TYPE_UMTS](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_HSDPA](../android/telephony/TelephonyManager.md), [TelephonyManager.NETWORK_TYPE_HSUPA](../android/telephony/TelephonyManager.md), or [TelephonyManager.NETWORK_TYPE_HSPA](../android/telephony/TelephonyManager.md) means that Neighboring Cell information is stored for UMTS network, in which [NeighboringCellInfo.getPsc](../android/telephony/NeighboringCellInfo.md))should be called to access location. |

### getPsc

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPsc(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Primary Scrambling Code in 9 bits format in UMTS, 0x1ff max value UNKNOWN_CID if in GSM or CMDA or unknown |

### getRssi

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRssi(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | received signal strength or UNKNOWN_RSSI if unknown For GSM, it is in "asu" ranging from 0 to 31 (dBm = -113 + 2\*asu) 0 means "-113 dBm or less" and 31 means "-51 dBm or greater" For UMTS, it is the Level index of CPICH RSCP defined in TS 25.125 |

### setCid

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setCid(cid: Int): Unit
```

**Deprecated:** *cid value passed as in location parameter passed to constructor [NeighboringCellInfo(int,java.lang.String,int)](../android/telephony/NeighboringCellInfo.md))*

Set the cell id. NeighboringCellInfo is a one time shot for the neighboring cells based on the radio network type at that moment. It shouldn't be changed after creation. 

### setRssi

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRssi(rssi: Int): Unit
```

**Deprecated:** *initial rssi value passed as parameter to constructor [NeighboringCellInfo(int,java.lang.String,int)](../android/telephony/NeighboringCellInfo.md))*

Set the signal strength of the cell. NeighboringCellInfo is a one time shot for the neighboring cells based on the radio network type at that moment. It shouldn't be changed after creation. 

### toString

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NeighboringCellInfo!>
```

**Deprecated:** *Deprecated in Java.*
