# NetworkScanRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkScanRequest

Kotlin| [Java](https://developer.android.com/reference/android/telephony/NetworkScanRequest "View this page in Java") 

```
class NetworkScanRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.telephony.NetworkScanRequest](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#) |

Defines a request to perform a network scan. This class defines whether the network scan will be performed only once or periodically until cancelled, when the scan is performed periodically, the time interval is not controlled by the user but defined by the modem vendor.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_ONE_SHOT](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#SCAN_TYPE_ONE_SHOT:kotlin.Int) Performs the scan only once |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_PERIODIC](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#SCAN_TYPE_PERIODIC:kotlin.Int) Performs the scan periodically until cancelled The modem will start new scans periodically, and the interval between two scans is usually multiple minutes. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkScanRequest](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#NetworkScanRequest(kotlin.Int,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int,%20kotlin.Boolean,%20kotlin.Int,%20java.util.ArrayList))`(`scanType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `specifiers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RadioAccessSpecifier](https://developer.android.com/reference/kotlin/android/telephony/RadioAccessSpecifier)!>!`, `searchPeriodicity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxSearchTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `incrementalResults:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `incrementalResultsPeriodicity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mccMncs:` ` [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Creates a new NetworkScanRequest with mScanType and network mSpecifiers |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getIncrementalResults](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getIncrementalResults())`()` Returns whether incremental result is enabled. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIncrementalResultsPeriodicity](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getIncrementalResultsPeriodicity())`()` Returns the periodicity in seconds of incremental results. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSearchTime](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getMaxSearchTime())`()` Returns maximum duration of the periodic search in seconds. |
| [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPlmns](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getPlmns())`()` Returns the List of PLMN ids (MCC-MNC) for early termination of scan. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScanType](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getScanType())`()` Returns the type of the scan. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSearchPeriodicity](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getSearchPeriodicity())`()` Returns the search periodicity in seconds. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RadioAccessSpecifier](https://developer.android.com/reference/kotlin/android/telephony/RadioAccessSpecifier)!\>! | [getSpecifiers](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#getSpecifiers())`()` Returns the radio access technologies with bands or channels that need to be scanned. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NetworkScanRequest](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### SCAN_TYPE_ONE_SHOT

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_TYPE_ONE_SHOT: Int
```

Performs the scan only once 

 Value: 0

### SCAN_TYPE_PERIODIC

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_TYPE_PERIODIC: Int
```

Performs the scan periodically until cancelled The modem will start new scans periodically, and the interval between two scans is usually multiple minutes. 

 Value: 1

## Public constructors

### NetworkScanRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NetworkScanRequest(
    scanType: Int, 
    specifiers: Array<RadioAccessSpecifier!>!, 
    searchPeriodicity: Int, 
    maxSearchTime: Int, 
    incrementalResults: Boolean, 
    incrementalResultsPeriodicity: Int, 
    mccMncs: ArrayList<String!>!)
```

Creates a new NetworkScanRequest with mScanType and network mSpecifiers

| Parameters ||
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `scanType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of the scan, can be either one shot or periodic |
| `specifiers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RadioAccessSpecifier](https://developer.android.com/reference/kotlin/android/telephony/RadioAccessSpecifier)!\>!:the radio network with bands / channels to be scanned |
| `searchPeriodicity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modem will restart the scan every searchPeriodicity seconds if no network has been found, until it reaches the maxSearchTime. Only valid when scan type is periodic scan. |
| `maxSearchTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum duration of the search (in seconds) |
| `incrementalResults` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Indicates whether the modem should report incremental results of the network scan to the client |
| `incrementalResultsPeriodicity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Indicates the periodicity with which the modem should report incremental results to the client (in seconds), only valid when incrementalResults is true |
| `mccMncs` | [ArrayList](https://developer.android.com/reference/kotlin/java/util/ArrayList.html#)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Describes the list of PLMN ids (MCC-MNC), once any network in the list has been found, the scan will be terminated by the modem. |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getIncrementalResults

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIncrementalResults(): Boolean
```

Returns whether incremental result is enabled. FALSE -- Incremental results is not enabled. TRUE -- Incremental results is reported. 

### getIncrementalResultsPeriodicity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getIncrementalResultsPeriodicity(): Int
```

Returns the periodicity in seconds of incremental results. 

### getMaxSearchTime

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMaxSearchTime(): Int
```

Returns maximum duration of the periodic search in seconds. 

### getPlmns

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPlmns(): ArrayList<String!>!
```

Returns the List of PLMN ids (MCC-MNC) for early termination of scan. If any PLMN of this list is found, search should end at that point and results with all PLMN found till that point should be sent as response. 

### getScanType

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScanType(): Int
```

Returns the type of the scan.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.NetworkScanRequest#SCAN_TYPE_ONE_SHOT](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#SCAN_TYPE_ONE_SHOT:kotlin.Int), or [android.telephony.NetworkScanRequest#SCAN_TYPE_PERIODIC](https://developer.android.com/reference/kotlin/android/telephony/NetworkScanRequest#SCAN_TYPE_PERIODIC:kotlin.Int) |

### getSearchPeriodicity

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSearchPeriodicity(): Int
```

Returns the search periodicity in seconds. 

### getSpecifiers

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSpecifiers(): Array<RadioAccessSpecifier!>!
```

Returns the radio access technologies with bands or channels that need to be scanned. 

### hashCode

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NetworkScanRequest!>
```
