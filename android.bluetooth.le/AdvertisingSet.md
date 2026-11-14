# AdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AdvertisingSet

Kotlin | [Java](https://developer.android.com/reference/android/bluetooth/le/AdvertisingSet "View this page in Java") 
| --- | --- |

```
class AdvertisingSet
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#) |

This class provides a way to control single Bluetooth LE advertising instance.

To get an instance of [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#), call the android.bluetooth.le.BluetoothLeAdvertiser#startAdvertisingSet method.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [enableAdvertising](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#enableAdvertising(kotlin.Boolean,%20kotlin.Int,%20kotlin.Int))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxExtendedAdvertisingEvents:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Enables Advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingData(android.bluetooth.le.AdvertiseData))`(`advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`)` Set/update data being Advertised. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setAdvertisingParameters(android.bluetooth.le.AdvertisingSetParameters))`(`parameters:` ` [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!`)` Update advertising parameters associated with this AdvertisingSet. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPeriodicAdvertisingData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingData(android.bluetooth.le.AdvertiseData))`(`periodicData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`)` Used to set periodic advertising data, must be called after setPeriodicAdvertisingParameters, or after advertising was started with periodic advertising data set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPeriodicAdvertisingEnabled](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingEnabled(kotlin.Boolean))`(`enable:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Used to enable/disable periodic advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setPeriodicAdvertisingParameters(android.bluetooth.le.PeriodicAdvertisingParameters))`(`parameters:` ` [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!`)` Update periodic advertising parameters associated with this set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setScanResponseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet#setScanResponseData(android.bluetooth.le.AdvertiseData))`(`scanResponse:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`)` Set/update scan response data. |

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
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)

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
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!: Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the advertisement is connectable, three bytes will be added for flags. If the update takes place when the advertising set is enabled, the data can be maximum 251 bytes long. |

### setAdvertisingParameters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAdvertisingParameters(parameters: AdvertisingSetParameters!): Unit
```

Update advertising parameters associated with this AdvertisingSet. Must be called when advertising is not active. This method returns immediately, the operation status is delivered through `callback.onAdvertisingParametersUpdated`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission when `parameters.getOwnAddressType()` is different from `AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT` or `parameters.isDirected()` is true. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!: advertising set parameters. |

### setPeriodicAdvertisingData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPeriodicAdvertisingData(periodicData: AdvertiseData!): Unit
```

Used to set periodic advertising data, must be called after setPeriodicAdvertisingParameters, or after advertising was started with periodic advertising data set. This method returns immediately, the operation status is delivered through `callback.onPeriodicAdvertisingDataSet()`. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `periodicData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!: Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the update takes place when the periodic advertising is enabled for this set, the data can be maximum 251 bytes long. |

### setPeriodicAdvertisingEnabled

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPeriodicAdvertisingEnabled(enable: Boolean): Unit
```

Used to enable/disable periodic advertising. This method returns immediately, the operation status is delivered through `callback.onPeriodicAdvertisingEnable()`. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `enable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): whether the periodic advertising should be enabled (true), or disabled (false). |

### setPeriodicAdvertisingParameters

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPeriodicAdvertisingParameters(parameters: PeriodicAdvertisingParameters!): Unit
```

Update periodic advertising parameters associated with this set. Must be called when periodic advertising is not enabled. This method returns immediately, the operation status is delivered through `callback.onPeriodicAdvertisingParametersUpdated()`. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) 

### setScanResponseData

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setScanResponseData(scanResponse: AdvertiseData!): Unit
```

Set/update scan response data. Make sure that data doesn't exceed the size limit for specified AdvertisingSetParameters. This method returns immediately, the operation status is delivered through `callback.onScanResponseDataSet()`. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)

| Parameters ||
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `scanResponse` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!: Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the update takes place when the advertising set is enabled, the data can be maximum 251 bytes long. |
