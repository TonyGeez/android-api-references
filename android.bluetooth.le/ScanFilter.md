# ScanFilter

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanFilter

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/ScanFilter "View this page in Java") 
| --- | --- |

```
class ScanFilter : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#) |

Criteria for filtering result from Bluetooth LE scans. A [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#) allows clients to restrict scan results to only those that are of interest to them.

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
| | [Builder](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter.Builder) Builder class for [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getAdvertisingData())`()` Returns the advertising data of this filter. |
| --- | --- |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getAdvertisingDataMask](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getAdvertisingDataMask())`()` Returns the advertising data mask of this filter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getAdvertisingDataType](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getAdvertisingDataType())`()` Returns the advertising data type of this filter. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeviceAddress](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getDeviceAddress())`()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDeviceName](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getDeviceName())`()` Returns the filter set the device name field of Bluetooth advertisement data. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getManufacturerData](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getManufacturerData())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getManufacturerDataMask](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getManufacturerDataMask())`()` <br /> |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getManufacturerId](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getManufacturerId())`()` Returns the manufacturer id. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getServiceData](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceData())`()` <br /> |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | [getServiceDataMask](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceDataMask())`()` <br /> |
| --- | --- |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getServiceDataUuid](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceDataUuid())`()` <br /> |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getServiceSolicitationUuid](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceSolicitationUuid())`()` Returns the filter set on the service Solicitation uuid. |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getServiceSolicitationUuidMask](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceSolicitationUuidMask())`()` Returns the filter set on the service Solicitation uuid mask. |
| --- | --- |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getServiceUuid](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceUuid())`()` Returns the filter set on the service uuid. |
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | [getServiceUuidMask](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#getServiceUuidMask())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#hashCode())`()` <br /> |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [matches](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#matches(android.bluetooth.le.ScanResult))`(`scanResult:` ` [ScanResult](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanResult)!`)` Check if the scan filter matches a`scanResult`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#CREATOR:android.os.Parcelable.Creator) A [android.os.Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#) to create [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#) from parcel. |

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

Returns the advertising data type of this filter. Returns [ScanRecord.DATA_TYPE_NONE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_NONE:kotlin.Int) if the type is not set. The values of advertising data type are defined in the Bluetooth Generic Access Profile (https://www.bluetooth.com/specifications/assigned-numbers/)

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.bluetooth.le.ScanRecord#DATA_TYPE_NONE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_NONE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_FLAGS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_FLAGS:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_PARTIAL](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_PARTIAL:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_COMPLETE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_COMPLETE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_PARTIAL](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_PARTIAL:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_COMPLETE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_COMPLETE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_PARTIAL](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_PARTIAL:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_COMPLETE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_COMPLETE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LOCAL_NAME_SHORT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LOCAL_NAME_SHORT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LOCAL_NAME_COMPLETE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LOCAL_NAME_COMPLETE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_TX_POWER_LEVEL](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_TX_POWER_LEVEL:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_CLASS_OF_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_CLASS_OF_DEVICE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_DEVICE_ID](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_DEVICE_ID:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SECURITY_MANAGER_OUT_OF_BAND_FLAGS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SECURITY_MANAGER_OUT_OF_BAND_FLAGS:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SLAVE_CONNECTION_INTERVAL_RANGE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SLAVE_CONNECTION_INTERVAL_RANGE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_16_BIT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_16_BIT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_128_BIT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_128_BIT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_DATA_16_BIT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_DATA_16_BIT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_PUBLIC_TARGET_ADDRESS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_PUBLIC_TARGET_ADDRESS:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_RANDOM_TARGET_ADDRESS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_RANDOM_TARGET_ADDRESS:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_APPEARANCE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_APPEARANCE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_BLUETOOTH_DEVICE_ADDRESS](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_BLUETOOTH_DEVICE_ADDRESS:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_ROLE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_ROLE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C_256](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C_256:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R_256](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R_256:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_32_BIT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_32_BIT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_DATA_32_BIT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_DATA_32_BIT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_SERVICE_DATA_128_BIT](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_DATA_128_BIT:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_CONFIRMATION_VALUE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_CONFIRMATION_VALUE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_RANDOM_VALUE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_RANDOM_VALUE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_URI](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_URI:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_INDOOR_POSITIONING](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_INDOOR_POSITIONING:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_TRANSPORT_DISCOVERY_DATA](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_TRANSPORT_DISCOVERY_DATA:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_LE_SUPPORTED_FEATURES](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_SUPPORTED_FEATURES:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_CHANNEL_MAP_UPDATE_INDICATION](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_CHANNEL_MAP_UPDATE_INDICATION:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_PB_ADV](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_PB_ADV:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_MESH_MESSAGE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_MESH_MESSAGE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_MESH_BEACON](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_MESH_BEACON:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_BIG_INFO](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_BIG_INFO:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_BROADCAST_CODE](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_BROADCAST_CODE:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_RESOLVABLE_SET_IDENTIFIER](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_RESOLVABLE_SET_IDENTIFIER:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL_LONG](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL_LONG:kotlin.Int), [android.bluetooth.le.ScanRecord#DATA_TYPE_3D_INFORMATION_DATA](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_3D_INFORMATION_DATA:kotlin.Int), or [android.bluetooth.le.ScanRecord#DATA_TYPE_MANUFACTURER_SPECIFIC_DATA](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_MANUFACTURER_SPECIFIC_DATA:kotlin.Int) |

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
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | This value may be`null`. |

### getServiceSolicitationUuid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceSolicitationUuid(): ParcelUuid?
```

Returns the filter set on the service Solicitation uuid.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | This value may be`null`. |

### getServiceSolicitationUuidMask

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceSolicitationUuidMask(): ParcelUuid?
```

Returns the filter set on the service Solicitation uuid mask.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | This value may be`null`. |

### getServiceUuid

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceUuid(): ParcelUuid?
```

Returns the filter set on the service uuid.

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | This value may be`null`. |

### getServiceUuidMask

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceUuidMask(): ParcelUuid?
```

| Return ||
|-------------------------------------------------------------------------------------------|--------------------------|
| [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)? | This value may be`null`. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<ScanFilter!>
```

A [android.os.Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#) to create [ScanFilter](https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanFilter#) from parcel.
