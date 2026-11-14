# ScanSettings

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanSettings

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/ScanSettings "View this page in Java") 
| --- | --- |

```
class ScanSettings : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#) |

Bluetooth LE scan settings are passed to android.bluetooth.le.BluetoothLeScanner#startScan to define the parameters for the scan.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings.Builder) Builder for [ScanSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#). |

| Constants ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [AUTO_BATCH_MIN_REPORT_DELAY_MILLIS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#AUTO_BATCH_MIN_REPORT_DELAY_MILLIS:kotlin.Long) Minimum report delay for [ScanSettings.CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_TYPE_ALL_MATCHES](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_ALL_MATCHES:kotlin.Int) Trigger a callback for every Bluetooth advertisement found that matches the filter criteria. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH:kotlin.Int) A result callback for every Bluetooth advertisement found that matches the filter criteria is only triggered when screen is turned on. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_TYPE_FIRST_MATCH](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_FIRST_MATCH:kotlin.Int) A result callback is only triggered for the first advertisement packet received that matches the filter criteria. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CALLBACK_TYPE_MATCH_LOST](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_MATCH_LOST:kotlin.Int) Receive a callback when advertisements are no longer received from a device that has been previously reported by a first match callback. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_MODE_AGGRESSIVE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#MATCH_MODE_AGGRESSIVE:kotlin.Int) In Aggressive mode, hw will determine a match sooner even with feeble signal strength and few number of sightings/match in a duration. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_MODE_STICKY](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#MATCH_MODE_STICKY:kotlin.Int) For sticky mode, higher threshold of signal strength and sightings is required before reporting by hw. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_NUM_FEW_ADVERTISEMENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#MATCH_NUM_FEW_ADVERTISEMENT:kotlin.Int) Match few advertisement per filter, depends on current capability and availability of the resources in hw. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_NUM_MAX_ADVERTISEMENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#MATCH_NUM_MAX_ADVERTISEMENT:kotlin.Int) Match as many advertisement per filter as hw could allow, depends on current capability and availability of the resources in hw. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MATCH_NUM_ONE_ADVERTISEMENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#MATCH_NUM_ONE_ADVERTISEMENT:kotlin.Int) Determines how many advertisements to match per filter, as this is scarce hw resource. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHY_LE_ALL_SUPPORTED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#PHY_LE_ALL_SUPPORTED:kotlin.Int) Use all supported PHYs for scanning. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_MODE_BALANCED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_MODE_BALANCED:kotlin.Int) Perform Bluetooth LE scan in balanced power mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_MODE_LOW_LATENCY](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_MODE_LOW_LATENCY:kotlin.Int) Scan using highest duty cycle. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_MODE_LOW_POWER](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_MODE_LOW_POWER:kotlin.Int) Perform Bluetooth LE scan in low power mode. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_MODE_OPPORTUNISTIC](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_MODE_OPPORTUNISTIC:kotlin.Int) A special Bluetooth LE scan mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_ACTIVE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_TYPE_ACTIVE:kotlin.Int) Does active scanning, scan results are delivered upon scan responses arrive. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_PASSIVE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_TYPE_PASSIVE:kotlin.Int) Does passive scanning, scan responses are ignored. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SCAN_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_TYPE_UNKNOWN:kotlin.Int) Scan type is unknown. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallbackType](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getCallbackType())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getLegacy](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getLegacy())`()` Returns whether only legacy advertisements will be returned. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPhy](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getPhy())`()` Returns the physical layer used during a scan. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getReportDelayMillis](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getReportDelayMillis())`()` Returns report delay timestamp based on the device clock. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssiThreshold](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getRssiThreshold())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScanMode](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getScanMode())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScanResultType](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getScanResultType())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScanType](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#getScanType())`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ScanSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### AUTO_BATCH_MIN_REPORT_DELAY_MILLIS

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val AUTO_BATCH_MIN_REPORT_DELAY_MILLIS: Long
```

Minimum report delay for [ScanSettings.CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH:kotlin.Int). 

 Value: 600000L

### CALLBACK_TYPE_ALL_MATCHES

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLBACK_TYPE_ALL_MATCHES: Int
```

Trigger a callback for every Bluetooth advertisement found that matches the filter criteria. If no filter is active, all advertisement packets are reported. 

 Value: 1

### CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLBACK_TYPE_ALL_MATCHES_AUTO_BATCH: Int
```

A result callback for every Bluetooth advertisement found that matches the filter criteria is only triggered when screen is turned on. While the screen is turned off, the advertisements are batched and the batched result callbacks are triggered every report delay. When the batch scan with this callback type is activated, the batched result callbacks are also triggered while turning on screen or disabling the scan. This callback type must be used with a report delay of [ScanSettings.AUTO_BATCH_MIN_REPORT_DELAY_MILLIS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#AUTO_BATCH_MIN_REPORT_DELAY_MILLIS:kotlin.Long) or greater. 

 Value: 8

### CALLBACK_TYPE_FIRST_MATCH

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLBACK_TYPE_FIRST_MATCH: Int
```

A result callback is only triggered for the first advertisement packet received that matches the filter criteria. 

 Value: 2

### CALLBACK_TYPE_MATCH_LOST

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CALLBACK_TYPE_MATCH_LOST: Int
```

Receive a callback when advertisements are no longer received from a device that has been previously reported by a first match callback. 

 Value: 4

### MATCH_MODE_AGGRESSIVE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_MODE_AGGRESSIVE: Int
```

In Aggressive mode, hw will determine a match sooner even with feeble signal strength and few number of sightings/match in a duration. 

 Value: 1

### MATCH_MODE_STICKY

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_MODE_STICKY: Int
```

For sticky mode, higher threshold of signal strength and sightings is required before reporting by hw. 

 Value: 2

### MATCH_NUM_FEW_ADVERTISEMENT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_NUM_FEW_ADVERTISEMENT: Int
```

Match few advertisement per filter, depends on current capability and availability of the resources in hw. 

 Value: 2

### MATCH_NUM_MAX_ADVERTISEMENT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_NUM_MAX_ADVERTISEMENT: Int
```

Match as many advertisement per filter as hw could allow, depends on current capability and availability of the resources in hw. 

 Value: 3

### MATCH_NUM_ONE_ADVERTISEMENT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MATCH_NUM_ONE_ADVERTISEMENT: Int
```

Determines how many advertisements to match per filter, as this is scarce hw resource. Match one advertisement per filter. 

 Value: 1

### PHY_LE_ALL_SUPPORTED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHY_LE_ALL_SUPPORTED: Int
```

Use all supported PHYs for scanning. This will check the controller capabilities, and start the scan on 1Mbit and LE Coded PHYs if supported, or on the 1Mbit PHY only. 

 Value: 255

### SCAN_MODE_BALANCED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_MODE_BALANCED: Int
```

Perform Bluetooth LE scan in balanced power mode. Scan results are returned at a rate that provides a good trade-off between scan frequency and power consumption. 

 Value: 1

### SCAN_MODE_LOW_LATENCY

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_MODE_LOW_LATENCY: Int
```

Scan using highest duty cycle. It's recommended to only use this mode when the application is running in the foreground. 

 Value: 2

### SCAN_MODE_LOW_POWER

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_MODE_LOW_POWER: Int
```

Perform Bluetooth LE scan in low power mode. This is the default scan mode as it consumes the least power. This mode is enforced if the scanning application is not in foreground. 

 Value: 0

### SCAN_MODE_OPPORTUNISTIC

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_MODE_OPPORTUNISTIC: Int
```

A special Bluetooth LE scan mode. Applications using this scan mode will passively listen for other scan results without starting BLE scans themselves. 

 Value: -1

### SCAN_TYPE_ACTIVE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_TYPE_ACTIVE: Int
```

Does active scanning, scan results are delivered upon scan responses arrive. 

 Value: 2

### SCAN_TYPE_PASSIVE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_TYPE_PASSIVE: Int
```

Does passive scanning, scan responses are ignored. 

 Value: 1

### SCAN_TYPE_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SCAN_TYPE_UNKNOWN: Int
```

Scan type is unknown. 

 Value: 0

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getCallbackType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCallbackType(): Int
```  

### getLegacy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLegacy(): Boolean
```

Returns whether only legacy advertisements will be returned. Legacy advertisements include advertisements as specified by the Bluetooth core specification 4.2 and below. 

### getPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPhy(): Int
```

Returns the physical layer used during a scan. 

### getReportDelayMillis

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getReportDelayMillis(): Long
```

Returns report delay timestamp based on the device clock. 

### getRssiThreshold

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRssiThreshold(): Int
```  

### getScanMode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScanMode(): Int
```  

### getScanResultType

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScanResultType(): Int
```  

### getScanType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScanType(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.le.ScanSettings#SCAN_TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_TYPE_UNKNOWN:kotlin.Int), [android.bluetooth.le.ScanSettings#SCAN_TYPE_PASSIVE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_TYPE_PASSIVE:kotlin.Int), or [android.bluetooth.le.ScanSettings#SCAN_TYPE_ACTIVE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanSettings#SCAN_TYPE_ACTIVE:kotlin.Int) |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ScanSettings!>
```
