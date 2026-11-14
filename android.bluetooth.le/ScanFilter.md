# ScanFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanFilter

Kotlin| [Java](../android/bluetooth/le/ScanFilter.md) 
| --- | --- |

```
class ScanFilter : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanFilter](../android/bluetooth/le/ScanFilter.md) |

Criteria for filtering result from Bluetooth LE scans. A [ScanFilter](../android/bluetooth/le/ScanFilter.md) allows clients to restrict scan results to only those that are of interest to them.

Current filtering on the following fields are supported:
- Service UUIDs which identify the bluetooth gatt services running on the device.
- Name of remote Bluetooth LE device.
- Mac address of the remote device.
- Service data which is the data associated with a service.
- Manufacturer specific data which is the data associated with a particular manufacturer.
- Advertising data type and corresponding data.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/bluetooth/le/ScanFilter.Builder.md) Builder class for [ScanFilter](../android/bluetooth/le/ScanFilter.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/bluetooth/le/ScanFilter.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdvertisingData](../android/bluetooth/le/ScanFilter.md))`()` Returns the advertising data of this filter. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdvertisingDataMask](../android/bluetooth/le/ScanFilter.md))`()` Returns the advertising data mask of this filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvertisingDataType](../android/bluetooth/le/ScanFilter.md))`()` Returns the advertising data type of this filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeviceAddress](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeviceName](../android/bluetooth/le/ScanFilter.md))`()` Returns the filter set the device name field of Bluetooth advertisement data. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getManufacturerData](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getManufacturerDataMask](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getManufacturerId](../android/bluetooth/le/ScanFilter.md))`()` Returns the manufacturer id. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getServiceData](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getServiceDataMask](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| --- | --- |
| [ParcelUuid](../android/os/ParcelUuid.md)? | [getServiceDataUuid](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| [ParcelUuid](../android/os/ParcelUuid.md)? | [getServiceSolicitationUuid](../android/bluetooth/le/ScanFilter.md))`()` Returns the filter set on the service Solicitation uuid. |
| [ParcelUuid](../android/os/ParcelUuid.md)? | [getServiceSolicitationUuidMask](../android/bluetooth/le/ScanFilter.md))`()` Returns the filter set on the service Solicitation uuid mask. |
| --- | --- |
| [ParcelUuid](../android/os/ParcelUuid.md)? | [getServiceUuid](../android/bluetooth/le/ScanFilter.md))`()` Returns the filter set on the service uuid. |
| [ParcelUuid](../android/os/ParcelUuid.md)? | [getServiceUuidMask](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](../android/bluetooth/le/ScanFilter.md))`(`scanResult:` ` [ScanResult](../android/bluetooth/le/ScanResult.md)!`)` Check if the scan filter matches a`scanResult`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/bluetooth/le/ScanFilter.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/bluetooth/le/ScanFilter.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [ScanFilter](../android/bluetooth/le/ScanFilter.md)!\> | [CREATOR](../android/bluetooth/le/ScanFilter.md) A [android.os.Parcelable.Creator](../android/os/Parcelable.Creator.md) to create [ScanFilter](../android/bluetooth/le/ScanFilter.md) from parcel. |

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

### getAdvertisingData

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvertisingData(): ByteArray?
```

Returns the advertising data of this filter.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getAdvertisingDataMask

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvertisingDataMask(): ByteArray?
```

Returns the advertising data mask of this filter.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getAdvertisingDataType

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAdvertisingDataType(): Int
```

Returns the advertising data type of this filter. Returns [ScanRecord.DATA_TYPE_NONE](../android/bluetooth/le/ScanRecord.md) if the type is not set. The values of advertising data type are defined in the Bluetooth Generic Access Profile (https://www.bluetooth.com/specifications/assigned-numbers/)

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.le.ScanRecord#DATA_TYPE_NONE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_FLAGS](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_PARTIAL](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_COMPLETE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_PARTIAL](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_COMPLETE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_PARTIAL](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_COMPLETE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LOCAL_NAME_SHORT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LOCAL_NAME_COMPLETE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_TX_POWER_LEVEL](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_CLASS_OF_DEVICE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_DEVICE_ID](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SECURITY_MANAGER_OUT_OF_BAND_FLAGS](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SLAVE_CONNECTION_INTERVAL_RANGE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_16_BIT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_128_BIT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_DATA_16_BIT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_PUBLIC_TARGET_ADDRESS](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_RANDOM_TARGET_ADDRESS](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_APPEARANCE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_BLUETOOTH_DEVICE_ADDRESS](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_ROLE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C_256](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R_256](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_32_BIT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_DATA_32_BIT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_DATA_128_BIT](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_CONFIRMATION_VALUE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_RANDOM_VALUE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_URI](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_INDOOR_POSITIONING](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_TRANSPORT_DISCOVERY_DATA](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_SUPPORTED_FEATURES](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_CHANNEL_MAP_UPDATE_INDICATION](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_PB_ADV](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_MESH_MESSAGE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_MESH_BEACON](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_BIG_INFO](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_BROADCAST_CODE](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_RESOLVABLE_SET_IDENTIFIER](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL_LONG](../android/bluetooth/le/ScanRecord.md), [android.bluetooth.le.ScanRecord#DATA_TYPE_3D_INFORMATION_DATA](../android/bluetooth/le/ScanRecord.md), or [android.bluetooth.le.ScanRecord#DATA_TYPE_MANUFACTURER_SPECIFIC_DATA](../android/bluetooth/le/ScanRecord.md) |

### getDeviceAddress

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceAddress(): String?
```

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getDeviceName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDeviceName(): String?
```

Returns the filter set the device name field of Bluetooth advertisement data.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getManufacturerData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getManufacturerData(): ByteArray?
```

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getManufacturerDataMask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getManufacturerDataMask(): ByteArray?
```

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getManufacturerId

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getManufacturerId(): Int
```

Returns the manufacturer id. -1 if the manufacturer filter is not set. 

### getServiceData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceData(): ByteArray?
```

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getServiceDataMask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceDataMask(): ByteArray?
```

| Return ||
|------------------------------------------------------------------------------------------|--------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | This value may be`null`. |

### getServiceDataUuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceDataUuid(): ParcelUuid?
```

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | This value may be`null`. |

### getServiceSolicitationUuid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceSolicitationUuid(): ParcelUuid?
```

Returns the filter set on the service Solicitation uuid.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | This value may be`null`. |

### getServiceSolicitationUuidMask

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceSolicitationUuidMask(): ParcelUuid?
```

Returns the filter set on the service Solicitation uuid mask.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | This value may be`null`. |

### getServiceUuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceUuid(): ParcelUuid?
```

Returns the filter set on the service uuid.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | This value may be`null`. |

### getServiceUuidMask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceUuidMask(): ParcelUuid?
```

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](../android/os/ParcelUuid.md)? | This value may be`null`. |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### matches

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun matches(scanResult: ScanResult!): Boolean
```

Check if the scan filter matches a`scanResult`. A scan result is considered as a match if it matches all the field filters. 

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
static val CREATOR: Parcelable.Creator<ScanFilter!>
```

A [android.os.Parcelable.Creator](../android/os/Parcelable.Creator.md) to create [ScanFilter](../android/bluetooth/le/ScanFilter.md) from parcel.
