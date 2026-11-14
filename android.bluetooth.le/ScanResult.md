# ScanResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanResult

Kotlin| [Java](../android/bluetooth/le/ScanResult.md) 
| --- | --- |

```
class ScanResult : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanResult](../android/bluetooth/le/ScanResult.md) |

ScanResult for Bluetooth LE scan.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_COMPLETE](../android/bluetooth/le/ScanResult.md) For chained advertisements, indicates that the data contained in this scan result is complete. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DATA_TRUNCATED](../android/bluetooth/le/ScanResult.md) For chained advertisements, indicates that the controller was unable to receive all chained packets and the scan result contains incomplete truncated data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PERIODIC_INTERVAL_NOT_PRESENT](../android/bluetooth/le/ScanResult.md) Periodic advertising interval is not present in the packet. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PHY_UNUSED](../android/bluetooth/le/ScanResult.md) Indicates that the secondary physical layer was not used. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SID_NOT_PRESENT](../android/bluetooth/le/ScanResult.md) Advertising Set ID is not present in the packet. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TX_POWER_NOT_PRESENT](../android/bluetooth/le/ScanResult.md) TX power is not present in the packet. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ScanResult](../android/bluetooth/le/ScanResult.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `scanRecord:` ` [ScanRecord](../android/bluetooth/le/ScanRecord.md)!`, `rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timestampNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new ScanResult. |
| [ScanResult](../android/bluetooth/le/ScanResult.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `eventType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `primaryPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `secondaryPhy:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `advertisingSid:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `txPower:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rssi:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `periodicAdvertisingInterval:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `scanRecord:` ` [ScanRecord](../android/bluetooth/le/ScanRecord.md)!`, `timestampNanos:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Constructs a new ScanResult. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/bluetooth/le/ScanResult.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/bluetooth/le/ScanResult.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvertisingSid](../android/bluetooth/le/ScanResult.md))`()` Returns the advertising set id. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDataStatus](../android/bluetooth/le/ScanResult.md))`()` Returns the data status. |
| [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)! | [getDevice](../android/bluetooth/le/ScanResult.md))`()` Returns the remote Bluetooth device identified by the Bluetooth device address. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPeriodicAdvertisingInterval](../android/bluetooth/le/ScanResult.md))`()` Returns the periodic advertising interval in units of 1. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPrimaryPhy](../android/bluetooth/le/ScanResult.md))`()` Returns the primary Physical Layer on which this advertisement was received. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRssi](../android/bluetooth/le/ScanResult.md))`()` Returns the received signal strength in dBm. |
| [ScanRecord](../android/bluetooth/le/ScanRecord.md)? | [getScanRecord](../android/bluetooth/le/ScanResult.md))`()` Returns the scan record, which is a combination of advertisement and scan response. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSecondaryPhy](../android/bluetooth/le/ScanResult.md))`()` Returns the secondary Physical Layer on which this advertisement was received. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampNanos](../android/bluetooth/le/ScanResult.md))`()` Returns timestamp since boot when the scan record was observed. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTxPower](../android/bluetooth/le/ScanResult.md))`()` Returns the transmit power in dBm. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/bluetooth/le/ScanResult.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isConnectable](../android/bluetooth/le/ScanResult.md))`()` Returns true if this object represents connectable scan result. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLegacy](../android/bluetooth/le/ScanResult.md))`()` Returns true if this object represents legacy scan result. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/bluetooth/le/ScanResult.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/bluetooth/le/ScanResult.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ScanResult](../android/bluetooth/le/ScanResult.md)!\> | [CREATOR](../android/bluetooth/le/ScanResult.md) <br /> |

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

**Deprecated:** *use [ScanResult(android.bluetooth.BluetoothDevice,int,int,int,int,int,int,int,android.bluetooth.le.ScanRecord,long)](../android/bluetooth/le/ScanResult.md))*

Constructs a new ScanResult.

| Parameters ||
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:Remote Bluetooth device found. |
| `scanRecord` | [ScanRecord](../android/bluetooth/le/ScanRecord.md)!:Scan record including both advertising data and scan response data. |
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
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:Remote Bluetooth device found. |
| `eventType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Event type. |
| `primaryPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Primary advertising phy. |
| --- | --- |
| `secondaryPhy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Secondary advertising phy. |
| `advertisingSid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Advertising set ID. |
| `txPower` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Transmit power. |
| --- | --- |
| `rssi` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Received signal strength. |
| `periodicAdvertisingInterval` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Periodic advertising interval. |
| `scanRecord` | [ScanRecord](../android/bluetooth/le/ScanRecord.md)!:Scan record including both advertising data and scan response data. |
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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

Returns the advertising set id. May return [ScanResult.SID_NOT_PRESENT](../android/bluetooth/le/ScanResult.md) if no set id was is present. 

### getDataStatus

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDataStatus(): Int
```

Returns the data status. Can be one of [ScanResult.DATA_COMPLETE](../android/bluetooth/le/ScanResult.md) or [android.bluetooth.le.ScanResult#DATA_TRUNCATED](../android/bluetooth/le/ScanResult.md). 

### getDevice

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevice(): BluetoothDevice!
```

Returns the remote Bluetooth device identified by the Bluetooth device address. If the device is bonded, calling [BluetoothDevice.getAddress](../android/bluetooth/BluetoothDevice.md))on the object returned by this method will return the address that was originally bonded with (either identity address or random address). 

### getPeriodicAdvertisingInterval

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPeriodicAdvertisingInterval(): Int
```

Returns the periodic advertising interval in units of 1.25ms. Valid range is 6 (7.5ms) to 65536 (81918.75ms). A value of [ScanResult.PERIODIC_INTERVAL_NOT_PRESENT](../android/bluetooth/le/ScanResult.md) means periodic advertising interval is not present. 

### getPrimaryPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrimaryPhy(): Int
```

Returns the primary Physical Layer on which this advertisement was received. Can be one of [BluetoothDevice.PHY_LE_1M](../android/bluetooth/BluetoothDevice.md) or [BluetoothDevice.PHY_LE_CODED](../android/bluetooth/BluetoothDevice.md). 

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
| [ScanRecord](../android/bluetooth/le/ScanRecord.md)? | This value may be`null`. |

### getSecondaryPhy

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSecondaryPhy(): Int
```

Returns the secondary Physical Layer on which this advertisement was received. Can be one of [BluetoothDevice.PHY_LE_1M](../android/bluetooth/BluetoothDevice.md), [BluetoothDevice.PHY_LE_2M](../android/bluetooth/BluetoothDevice.md), [android.bluetooth.BluetoothDevice#PHY_LE_CODED](../android/bluetooth/BluetoothDevice.md) or [ScanResult.PHY_UNUSED](../android/bluetooth/le/ScanResult.md)- if the advertisement was not received on a secondary physical channel. 

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

Returns the transmit power in dBm. Valid range is \[-127, 126\]. A value of [android.bluetooth.le.ScanResult#TX_POWER_NOT_PRESENT](../android/bluetooth/le/ScanResult.md) indicates that the TX power is not present. 

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ScanResult!>
```
