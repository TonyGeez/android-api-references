# NetworkScanRequest

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkScanRequest

Kotlin| [Java](NetworkScanRequest.md) 
| --- | --- |

```
class NetworkScanRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.telephony.NetworkScanRequest](NetworkScanRequest.md) |

Defines a request to perform a network scan. This class defines whether the network scan will be performed only once or periodically until cancelled, when the scan is performed periodically, the time interval is not controlled by the user but defined by the modem vendor.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_ONE_SHOT](NetworkScanRequest.md) Performs the scan only once |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_PERIODIC](NetworkScanRequest.md) Performs the scan periodically until cancelled The modem will start new scans periodically, and the interval between two scans is usually multiple minutes. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [NetworkScanRequest](NetworkScanRequest.md))`(`scanType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `specifiers:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [RadioAccessSpecifier](RadioAccessSpecifier.md)!>!`, `searchPeriodicity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxSearchTime:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `incrementalResults:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `incrementalResultsPeriodicity:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `mccMncs:` ` [ArrayList](../java.util/ArrayList.md)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`)` Creates a new NetworkScanRequest with mScanType and network mSpecifiers |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](NetworkScanRequest.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](NetworkScanRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getIncrementalResults](NetworkScanRequest.md))`()` Returns whether incremental result is enabled. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIncrementalResultsPeriodicity](NetworkScanRequest.md))`()` Returns the periodicity in seconds of incremental results. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMaxSearchTime](NetworkScanRequest.md))`()` Returns maximum duration of the periodic search in seconds. |
| [ArrayList](../java.util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getPlmns](NetworkScanRequest.md))`()` Returns the List of PLMN ids (MCC-MNC) for early termination of scan. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScanType](NetworkScanRequest.md))`()` Returns the type of the scan. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSearchPeriodicity](NetworkScanRequest.md))`()` Returns the search periodicity in seconds. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RadioAccessSpecifier](RadioAccessSpecifier.md)!\>! | [getSpecifiers](NetworkScanRequest.md))`()` Returns the radio access technologies with bands or channels that need to be scanned. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](NetworkScanRequest.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](NetworkScanRequest.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NetworkScanRequest](NetworkScanRequest.md)!\> | [CREATOR](NetworkScanRequest.md) <br /> |

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
| `specifiers` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [RadioAccessSpecifier](RadioAccessSpecifier.md)!\>!:the radio network with bands / channels to be scanned |
| `searchPeriodicity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The modem will restart the scan every searchPeriodicity seconds if no network has been found, until it reaches the maxSearchTime. Only valid when scan type is periodic scan. |
| --- | --- |
| `maxSearchTime` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Maximum duration of the search (in seconds) |
| `incrementalResults` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):Indicates whether the modem should report incremental results of the network scan to the client |
| `incrementalResultsPeriodicity` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Indicates the periodicity with which the modem should report incremental results to the client (in seconds), only valid when incrementalResults is true |
| --- | --- |
| `mccMncs` | [ArrayList](../java.util/ArrayList.md)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Describes the list of PLMN ids (MCC-MNC), once any network in the list has been found, the scan will be terminated by the modem. |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.telephony.NetworkScanRequest#SCAN_TYPE_ONE_SHOT](NetworkScanRequest.md), or [android.telephony.NetworkScanRequest#SCAN_TYPE_PERIODIC](NetworkScanRequest.md) |

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
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NetworkScanRequest!>
```
