Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ScanRecord

Kotlin | [Java](ScanRecord.md)
| --- | --- |

```
class ScanRecord
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.ScanRecord](ScanRecord.md) |

Represents a scan record from Bluetooth LE scan.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_3D_INFORMATION_DATA:kotlin.Int` Data type is 3D Information Data, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL:kotlin.Int` Data type is Advertising Interval, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_ADVERTISING_INTERVAL_LONG:kotlin.Int` Data type is Advertising Interval - long, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_APPEARANCE:kotlin.Int` Data type is Appearance, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_BIG_INFO:kotlin.Int` Data type is BIGInfo, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_BROADCAST_CODE:kotlin.Int` Data type is Broadcast_Code, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_CHANNEL_MAP_UPDATE_INDICATION:kotlin.Int` Data type is Channel Map Update Indication, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_CLASS_OF_DEVICE:kotlin.Int` Data type is Class of Device, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_DEVICE_ID:kotlin.Int` Data type is Device ID, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_FLAGS:kotlin.Int` Data type is Flags, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_INDOOR_POSITIONING:kotlin.Int` Data type is Indoor Positioning, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_BLUETOOTH_DEVICE_ADDRESS:kotlin.Int` Data type is LE Bluetooth Device Address, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_ROLE:kotlin.Int` Data type is LE Role, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_CONFIRMATION_VALUE:kotlin.Int` Data type is LE Secure Connections Confirmation Value, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_SECURE_CONNECTIONS_RANDOM_VALUE:kotlin.Int` Data type is LE Secure Connections Random Value, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LE_SUPPORTED_FEATURES:kotlin.Int` Data type is LE Supported Features, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LOCAL_NAME_COMPLETE:kotlin.Int` Data type is Complete Local Name, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_LOCAL_NAME_SHORT:kotlin.Int` Data type is Shortened Local Name, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_MANUFACTURER_SPECIFIC_DATA:kotlin.Int` Data type is Manufacturer Specific Data, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_MESH_BEACON:kotlin.Int` Data type is Mesh Beacon, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_MESH_MESSAGE:kotlin.Int` Data type is Mesh Message, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_NONE:kotlin.Int` Data type is not set for the filter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_PB_ADV:kotlin.Int` Data type is PB-ADV, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_PUBLIC_TARGET_ADDRESS:kotlin.Int` Data type is Public Target Address, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_RANDOM_TARGET_ADDRESS:kotlin.Int` Data type is Random Target Address, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_RESOLVABLE_SET_IDENTIFIER:kotlin.Int` Data type is Resolvable Set Identifier, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SECURITY_MANAGER_OUT_OF_BAND_FLAGS:kotlin.Int` Data type is Security Manager Out of Band Flags, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_DATA_128_BIT:kotlin.Int` Data type is Service Data - 128-bit UUID, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_DATA_16_BIT:kotlin.Int` Data type is Service Data - 16-bit UUID, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_DATA_32_BIT:kotlin.Int` Data type is Service Data - 32-bit UUID, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_128_BIT:kotlin.Int` Data type is List of 128-bit Service Solicitation UUIDs, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_16_BIT:kotlin.Int` Data type is List of 16-bit Service Solicitation UUIDs, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_SOLICITATION_UUIDS_32_BIT:kotlin.Int` Data type is List of 32-bit Service Solicitation UUIDs, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_COMPLETE:kotlin.Int` Data type is Complete List of 128-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_128_BIT_PARTIAL:kotlin.Int` Data type is Incomplete List of 128-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for the details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_COMPLETE:kotlin.Int` Data type is Complete List of 16-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_16_BIT_PARTIAL:kotlin.Int` Data type is Incomplete List of 16-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for the details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_COMPLETE:kotlin.Int` Data type is Complete List of 32-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SERVICE_UUIDS_32_BIT_PARTIAL:kotlin.Int` Data type is Incomplete List of 32-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for the details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C:kotlin.Int` Data type is Simple Pairing Hash C, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_HASH_C_256:kotlin.Int` Data type is Simple Pairing Hash C-256, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R:kotlin.Int` Data type is Simple Pairing Randomizer R, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R_256:kotlin.Int` Data type is Simple Pairing Randomizer R-256, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_SLAVE_CONNECTION_INTERVAL_RANGE:kotlin.Int` Data type is Slave Connection Interval Range, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_TRANSPORT_DISCOVERY_DATA:kotlin.Int` Data type is Transport Discovery Data, see the Bluetooth Generic Access Profile for more details. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_TX_POWER_LEVEL:kotlin.Int` Data type is Tx Power Level, see the Bluetooth Generic Access Profile for more details. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#DATA_TYPE_URI:kotlin.Int` Data type is URI, see the Bluetooth Generic Access Profile for more details. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getAdvertiseFlags()()` Returns the advertising flags indicating the discoverable mode and capability of the device. |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getAdvertisingDataMap()()` Returns a map of advertising data type and its corresponding advertising data. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getBytes()()` Returns raw bytes of scan record. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getDeviceName()()` Returns the local name of the BLE device. |
| [SparseArray](../android.util/SparseArray.md)\< [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getManufacturerSpecificData()()` Returns a sparse array of manufacturer identifier and its corresponding manufacturer specific data. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getManufacturerSpecificData(kotlin.Int)(manufacturerId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the manufacturer specific data associated with the manufacturer id. |
| --- | --- |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [ParcelUuid](../android.os/ParcelUuid.md)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getServiceData()()` Returns a map of service UUID and its corresponding service data. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)? | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getServiceData(android.os.ParcelUuid)(serviceDataUuid: https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#!)` Returns the service data byte array associated with the `serviceUuid`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ParcelUuid](../android.os/ParcelUuid.md)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getServiceSolicitationUuids()()` Returns a list of service solicitation UUIDs within the advertisement that are used to identify the Bluetooth GATT services. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ParcelUuid](../android.os/ParcelUuid.md)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getServiceUuids()()` Returns a list of service UUIDs within the advertisement that are used to identify the bluetooth GATT services. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#getTxPowerLevel()()` Returns the transmission power level of the packet in dBm. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/le/ScanRecord#toString()()` Returns a string representation of the object. |
| --- | --- |

## Constants

### DATA_TYPE_3D_INFORMATION_DATA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_3D_INFORMATION_DATA: Int
```

Data type is 3D Information Data, see the Bluetooth Generic Access Profile for more details.

 Value: 61

### DATA_TYPE_ADVERTISING_INTERVAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_ADVERTISING_INTERVAL: Int
```

Data type is Advertising Interval, see the Bluetooth Generic Access Profile for more details.

 Value: 26

### DATA_TYPE_ADVERTISING_INTERVAL_LONG

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_ADVERTISING_INTERVAL_LONG: Int
```

Data type is Advertising Interval - long, see the Bluetooth Generic Access Profile for more details.

 Value: 47

### DATA_TYPE_APPEARANCE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_APPEARANCE: Int
```

Data type is Appearance, see the Bluetooth Generic Access Profile for more details.

 Value: 25

### DATA_TYPE_BIG_INFO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_BIG_INFO: Int
```

Data type is BIGInfo, see the Bluetooth Generic Access Profile for more details.

 Value: 44

### DATA_TYPE_BROADCAST_CODE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_BROADCAST_CODE: Int
```

Data type is Broadcast_Code, see the Bluetooth Generic Access Profile for more details.

 Value: 45

### DATA_TYPE_CHANNEL_MAP_UPDATE_INDICATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_CHANNEL_MAP_UPDATE_INDICATION: Int
```

Data type is Channel Map Update Indication, see the Bluetooth Generic Access Profile for more details.

 Value: 40

### DATA_TYPE_CLASS_OF_DEVICE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_CLASS_OF_DEVICE: Int
```

Data type is Class of Device, see the Bluetooth Generic Access Profile for more details.

 Value: 13

### DATA_TYPE_DEVICE_ID

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_DEVICE_ID: Int
```

Data type is Device ID, see the Bluetooth Generic Access Profile for more details.

 Value: 16

### DATA_TYPE_FLAGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_FLAGS: Int
```

Data type is Flags, see the Bluetooth Generic Access Profile for more details.

 Value: 1

### DATA_TYPE_INDOOR_POSITIONING

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_INDOOR_POSITIONING: Int
```

Data type is Indoor Positioning, see the Bluetooth Generic Access Profile for more details.

 Value: 37

### DATA_TYPE_LE_BLUETOOTH_DEVICE_ADDRESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LE_BLUETOOTH_DEVICE_ADDRESS: Int
```

Data type is LE Bluetooth Device Address, see the Bluetooth Generic Access Profile for more details.

 Value: 27

### DATA_TYPE_LE_ROLE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LE_ROLE: Int
```

Data type is LE Role, see the Bluetooth Generic Access Profile for more details.

 Value: 28

### DATA_TYPE_LE_SECURE_CONNECTIONS_CONFIRMATION_VALUE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LE_SECURE_CONNECTIONS_CONFIRMATION_VALUE: Int
```

Data type is LE Secure Connections Confirmation Value, see the Bluetooth Generic Access Profile for more details.

 Value: 34

### DATA_TYPE_LE_SECURE_CONNECTIONS_RANDOM_VALUE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LE_SECURE_CONNECTIONS_RANDOM_VALUE: Int
```

Data type is LE Secure Connections Random Value, see the Bluetooth Generic Access Profile for more details.

 Value: 35

### DATA_TYPE_LE_SUPPORTED_FEATURES

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LE_SUPPORTED_FEATURES: Int
```

Data type is LE Supported Features, see the Bluetooth Generic Access Profile for more details.

 Value: 39

### DATA_TYPE_LOCAL_NAME_COMPLETE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LOCAL_NAME_COMPLETE: Int
```

Data type is Complete Local Name, see the Bluetooth Generic Access Profile for more details.

 Value: 9

### DATA_TYPE_LOCAL_NAME_SHORT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_LOCAL_NAME_SHORT: Int
```

Data type is Shortened Local Name, see the Bluetooth Generic Access Profile for more details.

 Value: 8

### DATA_TYPE_MANUFACTURER_SPECIFIC_DATA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_MANUFACTURER_SPECIFIC_DATA: Int
```

Data type is Manufacturer Specific Data, see the Bluetooth Generic Access Profile for more details.

 Value: 255

### DATA_TYPE_MESH_BEACON

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_MESH_BEACON: Int
```

Data type is Mesh Beacon, see the Bluetooth Generic Access Profile for more details.

 Value: 43

### DATA_TYPE_MESH_MESSAGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_MESH_MESSAGE: Int
```

Data type is Mesh Message, see the Bluetooth Generic Access Profile for more details.

 Value: 42

### DATA_TYPE_NONE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_NONE: Int
```

Data type is not set for the filter. Will not filter advertising data type.

 Value: -1

### DATA_TYPE_PB_ADV

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_PB_ADV: Int
```

Data type is PB-ADV, see the Bluetooth Generic Access Profile for more details.

 Value: 41

### DATA_TYPE_PUBLIC_TARGET_ADDRESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_PUBLIC_TARGET_ADDRESS: Int
```

Data type is Public Target Address, see the Bluetooth Generic Access Profile for more details.

 Value: 23

### DATA_TYPE_RANDOM_TARGET_ADDRESS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_RANDOM_TARGET_ADDRESS: Int
```

Data type is Random Target Address, see the Bluetooth Generic Access Profile for more details.

 Value: 24

### DATA_TYPE_RESOLVABLE_SET_IDENTIFIER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_RESOLVABLE_SET_IDENTIFIER: Int
```

Data type is Resolvable Set Identifier, see the Bluetooth Generic Access Profile for more details.

 Value: 46

### DATA_TYPE_SECURITY_MANAGER_OUT_OF_BAND_FLAGS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SECURITY_MANAGER_OUT_OF_BAND_FLAGS: Int
```

Data type is Security Manager Out of Band Flags, see the Bluetooth Generic Access Profile for more details.

 Value: 17

### DATA_TYPE_SERVICE_DATA_128_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_DATA_128_BIT: Int
```

Data type is Service Data - 128-bit UUID, see the Bluetooth Generic Access Profile for more details.

 Value: 33

### DATA_TYPE_SERVICE_DATA_16_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_DATA_16_BIT: Int
```

Data type is Service Data - 16-bit UUID, see the Bluetooth Generic Access Profile for more details.

 Value: 22

### DATA_TYPE_SERVICE_DATA_32_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_DATA_32_BIT: Int
```

Data type is Service Data - 32-bit UUID, see the Bluetooth Generic Access Profile for more details.

 Value: 32

### DATA_TYPE_SERVICE_SOLICITATION_UUIDS_128_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_SOLICITATION_UUIDS_128_BIT: Int
```

Data type is List of 128-bit Service Solicitation UUIDs, see the Bluetooth Generic Access Profile for more details.

 Value: 21

### DATA_TYPE_SERVICE_SOLICITATION_UUIDS_16_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_SOLICITATION_UUIDS_16_BIT: Int
```

Data type is List of 16-bit Service Solicitation UUIDs, see the Bluetooth Generic Access Profile for more details.

 Value: 20

### DATA_TYPE_SERVICE_SOLICITATION_UUIDS_32_BIT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_SOLICITATION_UUIDS_32_BIT: Int
```

Data type is List of 32-bit Service Solicitation UUIDs, see the Bluetooth Generic Access Profile for more details.

 Value: 31

### DATA_TYPE_SERVICE_UUIDS_128_BIT_COMPLETE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_UUIDS_128_BIT_COMPLETE: Int
```

Data type is Complete List of 128-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for more details.

 Value: 7

### DATA_TYPE_SERVICE_UUIDS_128_BIT_PARTIAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_UUIDS_128_BIT_PARTIAL: Int
```

Data type is Incomplete List of 128-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for the details.

 Value: 6

### DATA_TYPE_SERVICE_UUIDS_16_BIT_COMPLETE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_UUIDS_16_BIT_COMPLETE: Int
```

Data type is Complete List of 16-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for more details.

 Value: 3

### DATA_TYPE_SERVICE_UUIDS_16_BIT_PARTIAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_UUIDS_16_BIT_PARTIAL: Int
```

Data type is Incomplete List of 16-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for the details.

 Value: 2

### DATA_TYPE_SERVICE_UUIDS_32_BIT_COMPLETE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_UUIDS_32_BIT_COMPLETE: Int
```

Data type is Complete List of 32-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for more details.

 Value: 5

### DATA_TYPE_SERVICE_UUIDS_32_BIT_PARTIAL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SERVICE_UUIDS_32_BIT_PARTIAL: Int
```

Data type is Incomplete List of 32-bit Service Class UUIDs, see the Bluetooth Generic Access Profile for the details.

 Value: 4

### DATA_TYPE_SIMPLE_PAIRING_HASH_C

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SIMPLE_PAIRING_HASH_C: Int
```

Data type is Simple Pairing Hash C, see the Bluetooth Generic Access Profile for more details.

 Value: 14

### DATA_TYPE_SIMPLE_PAIRING_HASH_C_256

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SIMPLE_PAIRING_HASH_C_256: Int
```

Data type is Simple Pairing Hash C-256, see the Bluetooth Generic Access Profile for more details.

 Value: 29

### DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R: Int
```

Data type is Simple Pairing Randomizer R, see the Bluetooth Generic Access Profile for more details.

 Value: 15

### DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R_256

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SIMPLE_PAIRING_RANDOMIZER_R_256: Int
```

Data type is Simple Pairing Randomizer R-256, see the Bluetooth Generic Access Profile for more details.

 Value: 30

### DATA_TYPE_SLAVE_CONNECTION_INTERVAL_RANGE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_SLAVE_CONNECTION_INTERVAL_RANGE: Int
```

Data type is Slave Connection Interval Range, see the Bluetooth Generic Access Profile for more details.

 Value: 18

### DATA_TYPE_TRANSPORT_DISCOVERY_DATA

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_TRANSPORT_DISCOVERY_DATA: Int
```

Data type is Transport Discovery Data, see the Bluetooth Generic Access Profile for more details.

 Value: 38

### DATA_TYPE_TX_POWER_LEVEL

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_TX_POWER_LEVEL: Int
```

Data type is Tx Power Level, see the Bluetooth Generic Access Profile for more details.

 Value: 10

### DATA_TYPE_URI

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DATA_TYPE_URI: Int
```

Data type is URI, see the Bluetooth Generic Access Profile for more details.

 Value: 36

## Public methods

### getAdvertiseFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAdvertiseFlags(): Int
```

Returns the advertising flags indicating the discoverable mode and capability of the device. Returns -1 if the flag field is not set.

### getAdvertisingDataMap

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAdvertisingDataMap(): MutableMap<Int!, ByteArray!>
```

Returns a map of advertising data type and its corresponding advertising data. The values of advertising data type are defined in the Bluetooth Generic Access Profile (https://www.bluetooth.com/specifications/assigned-numbers/)

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!>` | This value cannot be `null`. |

### getBytes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBytes(): ByteArray!
```

Returns raw bytes of scan record.

### getDeviceName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDeviceName(): String?
```

Returns the local name of the BLE device. This is a UTF-8 encoded string.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getManufacturerSpecificData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getManufacturerSpecificData(): SparseArray<ByteArray!>!
```

Returns a sparse array of manufacturer identifier and its corresponding manufacturer specific data.

### getManufacturerSpecificData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getManufacturerSpecificData(manufacturerId: Int): ByteArray?
```

Returns the manufacturer specific data associated with the manufacturer id. Returns `null` if the `manufacturerId` is not found.

### getServiceData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceData(): MutableMap<ParcelUuid!, ByteArray!>!
```

Returns a map of service UUID and its corresponding service data.

### getServiceData

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceData(serviceDataUuid: ParcelUuid!): ByteArray?
```

Returns the service data byte array associated with the `serviceUuid`. Returns `null` if the `serviceDataUuid` is not found.

### getServiceSolicitationUuids

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceSolicitationUuids(): MutableList<ParcelUuid!>
```

Returns a list of service solicitation UUIDs within the advertisement that are used to identify the Bluetooth GATT services.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#!>` | This value cannot be `null`. |

### getServiceUuids

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getServiceUuids(): MutableList<ParcelUuid!>!
```

Returns a list of service UUIDs within the advertisement that are used to identify the bluetooth GATT services.

### getTxPowerLevel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTxPowerLevel(): Int
```

Returns the transmission power level of the packet in dBm. Returns `https://developer.android.com/reference/kotlin/java/lang/Integer.html#MIN_VALUE:kotlin.Int` if the field is not set. This value can be used to calculate the path loss of a received packet using the following equation:

`pathloss = txPowerLevel - rssi`

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |
