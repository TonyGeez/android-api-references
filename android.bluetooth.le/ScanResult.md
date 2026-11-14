# ScanResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanResult

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/ScanResult "View this page in Java") 
| --- | --- |

```
class ScanResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#) |

ScanResult for Bluetooth LE scan.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_COMPLETE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#DATA_COMPLETE:kotlin.Int) For chained advertisements, indicates that the data contained in this scan result is complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_TRUNCATED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#DATA_TRUNCATED:kotlin.Int) For chained advertisements, indicates that the controller was unable to receive all chained packets and the scan result contains incomplete truncated data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERIODIC_INTERVAL_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#PERIODIC_INTERVAL_NOT_PRESENT:kotlin.Int) Periodic advertising interval is not present in the packet. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHY_UNUSED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#PHY_UNUSED:kotlin.Int) Indicates that the secondary physical layer was not used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SID_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#SID_NOT_PRESENT:kotlin.Int) Advertising Set ID is not present in the packet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TX_POWER_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#TX_POWER_NOT_PRESENT:kotlin.Int) TX power is not present in the packet. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#ScanResult(android.bluetooth.BluetoothDevice,%20android.bluetooth.le.ScanRecord,%20kotlin.Int,%20kotlin.Long))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)!`, `scanRecord:` ` [ScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord)!`, `rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timestampNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new ScanResult. |
| [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#ScanResult(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.le.ScanRecord,%20kotlin.Long))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)!`, `eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `primaryPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `secondaryPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `advertisingSid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `txPower:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `periodicAdvertisingInterval:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scanRecord:` ` [ScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord)!`, `timestampNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new ScanResult. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvertisingSid](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getAdvertisingSid())`()` Returns the advertising set id. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataStatus](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getDataStatus())`()` Returns the data status. |
| [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)! | [getDevice](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getDevice())`()` Returns the remote Bluetooth device identified by the Bluetooth device address. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeriodicAdvertisingInterval](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getPeriodicAdvertisingInterval())`()` Returns the periodic advertising interval in units of 1. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrimaryPhy](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getPrimaryPhy())`()` Returns the primary Physical Layer on which this advertisement was received. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getRssi())`()` Returns the received signal strength in dBm. |
| [ScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord)? | [getScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getScanRecord())`()` Returns the scan record, which is a combination of advertisement and scan response. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecondaryPhy](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getSecondaryPhy())`()` Returns the secondary Physical Layer on which this advertisement was received. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampNanos](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getTimestampNanos())`()` Returns timestamp since boot when the scan record was observed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTxPower](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#getTxPower())`()` Returns the transmit power in dBm. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#hashCode())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnectable](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#isConnectable())`()` Returns true if this object represents connectable scan result. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLegacy](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#isLegacy())`()` Returns true if this object represents legacy scan result. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### DATA_COMPLETE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_COMPLETE: Int
```

For chained advertisements, indicates that the data contained in this scan result is complete. 

 Value: 0

### DATA_TRUNCATED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DATA_TRUNCATED: Int
```

For chained advertisements, indicates that the controller was unable to receive all chained packets and the scan result contains incomplete truncated data. 

 Value: 2

### PERIODIC_INTERVAL_NOT_PRESENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PERIODIC_INTERVAL_NOT_PRESENT: Int
```

Periodic advertising interval is not present in the packet. 

 Value: 0

### PHY_UNUSED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PHY_UNUSED: Int
```

Indicates that the secondary physical layer was not used. 

 Value: 0

### SID_NOT_PRESENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SID_NOT_PRESENT: Int
```

Advertising Set ID is not present in the packet. 

 Value: 255

### TX_POWER_NOT_PRESENT

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TX_POWER_NOT_PRESENT: Int
```

TX power is not present in the packet. 

 Value: 127

## Public constructors

### ScanResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScanResult(
    device: BluetoothDevice!, 
    scanRecord: ScanRecord!, 
    rssi: Int, 
    timestampNanos: Long)
```

**Deprecated:** *use [ScanResult(android.bluetooth.BluetoothDevice,int,int,int,int,int,int,int,android.bluetooth.le.ScanRecord,long)](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#ScanResult(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.le.ScanRecord,%20kotlin.Long))*

Constructs a new ScanResult.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)!:Remote Bluetooth device found. |
| `scanRecord` | [ScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord)!:Scan record including both advertising data and scan response data. |
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Received signal strength. |
| --- | --- |
| `timestampNanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Timestamp at which the scan result was observed. |

### ScanResult

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ScanResult(
    device: BluetoothDevice!, 
    eventType: Int, 
    primaryPhy: Int, 
    secondaryPhy: Int, 
    advertisingSid: Int, 
    txPower: Int, 
    rssi: Int, 
    periodicAdvertisingInterval: Int, 
    scanRecord: ScanRecord!, 
    timestampNanos: Long)
```

Constructs a new ScanResult.

| Parameters ||
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#)!:Remote Bluetooth device found. |
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Event type. |
| `primaryPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Primary advertising phy. |
| --- | --- |
| `secondaryPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Secondary advertising phy. |
| `advertisingSid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Advertising set ID. |
| `txPower` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Transmit power. |
| --- | --- |
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Received signal strength. |
| `periodicAdvertisingInterval` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Periodic advertising interval. |
| `scanRecord` | [ScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord)!:Scan record including both advertising data and scan response data. |
| --- | --- |
| `timestampNanos` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):Timestamp at which the scan result was observed. |

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getAdvertisingSid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvertisingSid(): Int
```

Returns the advertising set id. May return [ScanResult.SID_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#SID_NOT_PRESENT:kotlin.Int) if no set id was is present. 

### getDataStatus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataStatus(): Int
```

Returns the data status. Can be one of [ScanResult.DATA_COMPLETE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#DATA_COMPLETE:kotlin.Int) or [android.bluetooth.le.ScanResult#DATA_TRUNCATED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#DATA_TRUNCATED:kotlin.Int). 

### getDevice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevice(): BluetoothDevice!
```

Returns the remote Bluetooth device identified by the Bluetooth device address. If the device is bonded, calling [BluetoothDevice.getAddress](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#getAddress())on the object returned by this method will return the address that was originally bonded with (either identity address or random address). 

### getPeriodicAdvertisingInterval

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPeriodicAdvertisingInterval(): Int
```

Returns the periodic advertising interval in units of 1.25ms. Valid range is 6 (7.5ms) to 65536 (81918.75ms). A value of [ScanResult.PERIODIC_INTERVAL_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#PERIODIC_INTERVAL_NOT_PRESENT:kotlin.Int) means periodic advertising interval is not present. 

### getPrimaryPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrimaryPhy(): Int
```

Returns the primary Physical Layer on which this advertisement was received. Can be one of [BluetoothDevice.PHY_LE_1M](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#PHY_LE_1M:kotlin.Int) or [BluetoothDevice.PHY_LE_CODED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#PHY_LE_CODED:kotlin.Int). 

### getRssi

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRssi(): Int
```

Returns the received signal strength in dBm. The valid range is \[-127, 126\]. 

### getScanRecord

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScanRecord(): ScanRecord?
```

Returns the scan record, which is a combination of advertisement and scan response.

| Return ||
|-----------------------------------------------------------------------------------------------|--------------------------|
| [ScanRecord](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord)? | This value may be`null`. |

### getSecondaryPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecondaryPhy(): Int
```

Returns the secondary Physical Layer on which this advertisement was received. Can be one of [BluetoothDevice.PHY_LE_1M](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#PHY_LE_1M:kotlin.Int), [BluetoothDevice.PHY_LE_2M](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#PHY_LE_2M:kotlin.Int), [android.bluetooth.BluetoothDevice#PHY_LE_CODED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.html#PHY_LE_CODED:kotlin.Int) or [ScanResult.PHY_UNUSED](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#PHY_UNUSED:kotlin.Int)- if the advertisement was not received on a secondary physical channel. 

### getTimestampNanos

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestampNanos(): Long
```

Returns timestamp since boot when the scan record was observed. 

### getTxPower

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTxPower(): Int
```

Returns the transmit power in dBm. Valid range is \[-127, 126\]. A value of [android.bluetooth.le.ScanResult#TX_POWER_NOT_PRESENT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult#TX_POWER_NOT_PRESENT:kotlin.Int) indicates that the TX power is not present. 

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isConnectable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isConnectable(): Boolean
```

Returns true if this object represents connectable scan result. 

### isLegacy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLegacy(): Boolean
```

Returns true if this object represents legacy scan result. Legacy scan results do not contain advanced advertising information as specified in the Bluetooth Core Specification v5. 

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

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
static val CREATOR: Parcelable.Creator<ScanResult!>
```
