# AdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertisingSet

Kotlin | [Java](../android/bluetooth/le/AdvertisingSet.md) 
| --- | --- |

```
class AdvertisingSet
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.AdvertisingSet](../android/bluetooth/le/AdvertisingSet.md) |

This class provides a way to control single Bluetooth LE advertising instance.

To get an instance of [AdvertisingSet](../android/bluetooth/le/AdvertisingSet.md), call the android.bluetooth.le.BluetoothLeAdvertiser#startAdvertisingSet method.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableAdvertising](../android/bluetooth/le/AdvertisingSet.md))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxExtendedAdvertisingEvents:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enables Advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdvertisingData](../android/bluetooth/le/AdvertisingSet.md))`(`advertiseData:` ` [AdvertiseData](../android/bluetooth/le/AdvertiseData.md)!`)` Set/update data being Advertised. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdvertisingParameters](../android/bluetooth/le/AdvertisingSet.md))`(`parameters:` ` [AdvertisingSetParameters](../android/bluetooth/le/AdvertisingSetParameters.md)!`)` Update advertising parameters associated with this AdvertisingSet. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPeriodicAdvertisingData](../android/bluetooth/le/AdvertisingSet.md))`(`periodicData:` ` [AdvertiseData](../android/bluetooth/le/AdvertiseData.md)!`)` Used to set periodic advertising data, must be called after setPeriodicAdvertisingParameters, or after advertising was started with periodic advertising data set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPeriodicAdvertisingEnabled](../android/bluetooth/le/AdvertisingSet.md))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Used to enable/disable periodic advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPeriodicAdvertisingParameters](../android/bluetooth/le/AdvertisingSet.md))`(`parameters:` ` [PeriodicAdvertisingParameters](../android/bluetooth/le/PeriodicAdvertisingParameters.md)!`)` Update periodic advertising parameters associated with this set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScanResponseData](../android/bluetooth/le/AdvertisingSet.md))`(`scanResponse:` ` [AdvertiseData](../android/bluetooth/le/AdvertiseData.md)!`)` Set/update scan response data. |

## Public methods

### enableAdvertising

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun enableAdvertising(
    enable: Boolean, 
    duration: Int, 
    maxExtendedAdvertisingEvents: Int
): Unit
```

Enables Advertising. This method returns immediately, the operation status is delivered through `callback.onAdvertisingEnabled()`. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)

| Parameters ||
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the advertising should be enabled (true), or disabled (false) |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): advertising duration, in 10ms unit. Valid range is from 1 (10ms) to 65535 (655,350 ms) |
| `maxExtendedAdvertisingEvents` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): maximum number of extended advertising events the controller shall attempt to send prior to terminating the extended advertising, even if the duration has not expired. Valid range is from 1 to 255. |
| --- | --- |

### setAdvertisingData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAdvertisingData(advertiseData: AdvertiseData!): Unit
```

Set/update data being Advertised. Make sure that data doesn't exceed the size limit for specified AdvertisingSetParameters. This method returns immediately, the operation status is delivered through `callback.onAdvertisingDataSet()`.

Advertising data must be empty if non-legacy scannable advertising is used. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `advertiseData` | [AdvertiseData](../android/bluetooth/le/AdvertiseData.md)!: Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android/bluetooth/BluetoothAdapter.md)). If the advertisement is connectable, three bytes will be added for flags. If the update takes place when the advertising set is enabled, the data can be maximum 251 bytes long. |

### setAdvertisingParameters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAdvertisingParameters(parameters: AdvertisingSetParameters!): Unit
```

Update advertising parameters associated with this AdvertisingSet. Must be called when advertising is not active. This method returns immediately, the operation status is delivered through `callback.onAdvertisingParametersUpdated`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission when `parameters.getOwnAddressType()` is different from `AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT` or `parameters.isDirected()` is true. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](../android/bluetooth/le/AdvertisingSetParameters.md)!: advertising set parameters. |

### setPeriodicAdvertisingData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPeriodicAdvertisingData(periodicData: AdvertiseData!): Unit
```

Used to set periodic advertising data, must be called after setPeriodicAdvertisingParameters, or after advertising was started with periodic advertising data set. This method returns immediately, the operation status is delivered through `callback.onPeriodicAdvertisingDataSet()`. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `periodicData` | [AdvertiseData](../android/bluetooth/le/AdvertiseData.md)!: Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android/bluetooth/BluetoothAdapter.md)). If the update takes place when the periodic advertising is enabled for this set, the data can be maximum 251 bytes long. |

### setPeriodicAdvertisingEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPeriodicAdvertisingEnabled(enable: Boolean): Unit
```

Used to enable/disable periodic advertising. This method returns immediately, the operation status is delivered through `callback.onPeriodicAdvertisingEnable()`. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the periodic advertising should be enabled (true), or disabled (false). |

### setPeriodicAdvertisingParameters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPeriodicAdvertisingParameters(parameters: PeriodicAdvertisingParameters!): Unit
```

Update periodic advertising parameters associated with this set. Must be called when periodic advertising is not enabled. This method returns immediately, the operation status is delivered through `callback.onPeriodicAdvertisingParametersUpdated()`. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) 

### setScanResponseData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setScanResponseData(scanResponse: AdvertiseData!): Unit
```

Set/update scan response data. Make sure that data doesn't exceed the size limit for specified AdvertisingSetParameters. This method returns immediately, the operation status is delivered through `callback.onScanResponseDataSet()`. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `scanResponse` | [AdvertiseData](../android/bluetooth/le/AdvertiseData.md)!: Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](../android/bluetooth/BluetoothAdapter.md)). If the update takes place when the advertising set is enabled, the data can be maximum 251 bytes long. |
