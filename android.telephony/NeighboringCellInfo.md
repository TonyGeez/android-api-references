# NeighboringCellInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NeighboringCellInfo

Kotlin| [Java](https://developer.android.com/reference/android/telephony/NeighboringCellInfo "View this page in Java") 
| --- | --- |

```
open class NeighboringCellInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#) |

| **This class was deprecated in API level 29.**
|
| This class should not be used by any app targeting [Android Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) or higher. Instead callers should use [CellInfo](https://developer.android.com/reference/kotlin/android/telephony/CellInfo).

Represents the neighboring cell information, including Received Signal Strength and Cell ID location.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_CID](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#UNKNOWN_CID:kotlin.Int) Cell location is not available |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [UNKNOWN_RSSI](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#UNKNOWN_RSSI:kotlin.Int) Signal strength is not available |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo())`()` Empty constructor. |
| [NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(android.os.Parcel))`(`in:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` Initialize the object from a parcel. |
| [NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(kotlin.Int,%20kotlin.Int))`(`rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `cid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initialize the object from rssi and cid. |
| [NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(kotlin.Int,%20kotlin.String,%20kotlin.Int))`(`rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `location:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `radioType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Initialize the object from rssi, location string, and radioType radioType is one of following [TelephonyManager.NETWORK_TYPE_GPRS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int), [TelephonyManager.NETWORK_TYPE_EDGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int), [TelephonyManager.NETWORK_TYPE_UMTS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int), [TelephonyManager.NETWORK_TYPE_HSDPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int), [TelephonyManager.NETWORK_TYPE_HSUPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int), and [TelephonyManager.NETWORK_TYPE_HSPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int). |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#describeContents())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCid](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getCid())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLac](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getLac())`()` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getNetworkType](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getNetworkType())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPsc](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getPsc())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getRssi())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setCid](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#setCid(kotlin.Int))`(`cid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the cell id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRssi](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#setRssi(kotlin.Int))`(`rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set the signal strength of the cell. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#toString())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NeighboringCellInfo](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

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

**Deprecated:** *by [NeighboringCellInfo(int,java.lang.String,int)](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(kotlin.Int,%20kotlin.String,%20kotlin.Int))*

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

**Deprecated:** *by [NeighboringCellInfo(int,java.lang.String,int)](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(kotlin.Int,%20kotlin.String,%20kotlin.Int))*

Initialize the object from rssi and cid. NeighboringCellInfo is one time shot for the neighboring cells based on the radio network type at that moment. Its constructor needs radio network type. 

### NeighboringCellInfo

Added in [API level 7](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NeighboringCellInfo(
    rssi: Int, 
    location: String!, 
    radioType: Int)
```

Initialize the object from rssi, location string, and radioType radioType is one of following [TelephonyManager.NETWORK_TYPE_GPRS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int), [TelephonyManager.NETWORK_TYPE_EDGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int), [TelephonyManager.NETWORK_TYPE_UMTS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int), [TelephonyManager.NETWORK_TYPE_HSDPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int), [TelephonyManager.NETWORK_TYPE_HSUPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int), and [TelephonyManager.NETWORK_TYPE_HSPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int).

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

**Deprecated:** *Deprecated in Java.*

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Radio network type while neighboring cell location is stored. Return [TelephonyManager.NETWORK_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UNKNOWN:kotlin.Int) means that the location information is unavailable. Return [TelephonyManager.NETWORK_TYPE_GPRS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_GPRS:kotlin.Int) or [TelephonyManager.NETWORK_TYPE_EDGE](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_EDGE:kotlin.Int) means that Neighboring Cell information is stored for GSM network, in which [NeighboringCellInfo.getLac](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getLac())and [NeighboringCellInfo.getCid](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getCid())should be called to access location. Return [TelephonyManager.NETWORK_TYPE_UMTS](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_UMTS:kotlin.Int), [TelephonyManager.NETWORK_TYPE_HSDPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSDPA:kotlin.Int), [TelephonyManager.NETWORK_TYPE_HSUPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSUPA:kotlin.Int), or [TelephonyManager.NETWORK_TYPE_HSPA](https://developer.android.com/reference/kotlin/android/telephony/TelephonyManager#NETWORK_TYPE_HSPA:kotlin.Int) means that Neighboring Cell information is stored for UMTS network, in which [NeighboringCellInfo.getPsc](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#getPsc())should be called to access location. |

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

**Deprecated:** *cid value passed as in location parameter passed to constructor [NeighboringCellInfo(int,java.lang.String,int)](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(kotlin.Int,%20kotlin.String,%20kotlin.Int))*

Set the cell id. NeighboringCellInfo is a one time shot for the neighboring cells based on the radio network type at that moment. It shouldn't be changed after creation. 

### setRssi

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setRssi(rssi: Int): Unit
```

**Deprecated:** *initial rssi value passed as parameter to constructor [NeighboringCellInfo(int,java.lang.String,int)](https://developer.android.com/reference/kotlin/android/telephony/NeighboringCellInfo#NeighboringCellInfo(kotlin.Int,%20kotlin.String,%20kotlin.Int))*

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NeighboringCellInfo!>
```

**Deprecated:** *Deprecated in Java.*
