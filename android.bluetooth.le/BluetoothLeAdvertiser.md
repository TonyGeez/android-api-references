# BluetoothLeAdvertiser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothLeAdvertiser

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/le/BluetoothLeAdvertiser "View this page in Java") 

```
class BluetoothLeAdvertiser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.le.BluetoothLeAdvertiser](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#) |

This class provides a way to perform Bluetooth LE advertise operations, such as starting and stopping advertising. An advertiser can broadcast up to 31 bytes of advertisement data represented by [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData).

To get an instance of [BluetoothLeAdvertiser](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#), call the [android.bluetooth.BluetoothAdapter#getBluetoothLeAdvertiser()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getBluetoothLeAdvertiser())method.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertising](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#startAdvertising(android.bluetooth.le.AdvertiseSettings,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseCallback))`(`settings:` ` [AdvertiseSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseSettings)!`, `advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `callback:` ` [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback)!`)` Start Bluetooth LE Advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertising](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#startAdvertising(android.bluetooth.le.AdvertiseSettings,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseCallback))`(`settings:` ` [AdvertiseSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseSettings)!`, `advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `scanResponse:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `callback:` ` [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback)!`)` Start Bluetooth LE Advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#startAdvertisingSet(android.bluetooth.le.AdvertisingSetParameters,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.PeriodicAdvertisingParameters,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertisingSetCallback))`(`parameters:` ` [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!`, `advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `scanResponse:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!`, `periodicData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `callback:` ` [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!`)` Creates a new advertising set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#startAdvertisingSet(android.bluetooth.le.AdvertisingSetParameters,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.PeriodicAdvertisingParameters,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertisingSetCallback,%20android.os.Handler))`(`parameters:` ` [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!`, `advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `scanResponse:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!`, `periodicData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `callback:` ` [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Creates a new advertising set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#startAdvertisingSet(android.bluetooth.le.AdvertisingSetParameters,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.PeriodicAdvertisingParameters,%20android.bluetooth.le.AdvertiseData,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.le.AdvertisingSetCallback))`(`parameters:` ` [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!`, `advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `scanResponse:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!`, `periodicData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxExtendedAdvertisingEvents:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!`)` Creates a new advertising set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#startAdvertisingSet(android.bluetooth.le.AdvertisingSetParameters,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.AdvertiseData,%20android.bluetooth.le.PeriodicAdvertisingParameters,%20android.bluetooth.le.AdvertiseData,%20kotlin.Int,%20kotlin.Int,%20android.bluetooth.le.AdvertisingSetCallback,%20android.os.Handler))`(`parameters:` ` [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!`, `advertiseData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `scanResponse:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!`, `periodicData:` ` [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxExtendedAdvertisingEvents:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!`, `handler:` ` [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!`)` Creates a new advertising set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAdvertising](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#stopAdvertising(android.bluetooth.le.AdvertiseCallback))`(`callback:` ` [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback)!`)` Stop Bluetooth LE advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser#stopAdvertisingSet(android.bluetooth.le.AdvertisingSetCallback))`(`callback:` ` [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!`)` Used to dispose of a [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet) object, obtained with android. |

## Public methods

### startAdvertising

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAdvertising(
    settings: AdvertiseSettings!, 
    advertiseData: AdvertiseData!, 
    callback: AdvertiseCallback!
): Unit
```

Start Bluetooth LE Advertising. On success, the`advertiseData`will be broadcasted. Returns immediately, the operation status is delivered through`callback`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission only when`settings.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [AdvertiseSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseSettings)!:Settings for Bluetooth LE advertising. |
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Advertisement data to be broadcasted. |
| `callback` | [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback)!:Callback for advertising status. |

### startAdvertising

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAdvertising(
    settings: AdvertiseSettings!, 
    advertiseData: AdvertiseData!, 
    scanResponse: AdvertiseData!, 
    callback: AdvertiseCallback!
): Unit
```

Start Bluetooth LE Advertising. The`advertiseData`will be broadcasted if the operation succeeds. The`scanResponse`is returned when a scanning device sends an active scan request. This method returns immediately, the operation status is delivered through`callback`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission only when`settings.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [AdvertiseSettings](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseSettings)!:Settings for Bluetooth LE advertising. |
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Advertisement data to be advertised in advertisement packet. |
| `scanResponse` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Scan response associated with the advertisement data. |
| `callback` | [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback)!:Callback for advertising status. |

### startAdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAdvertisingSet(
    parameters: AdvertisingSetParameters!, 
    advertiseData: AdvertiseData!, 
    scanResponse: AdvertiseData!, 
    periodicParameters: PeriodicAdvertisingParameters!, 
    periodicData: AdvertiseData!, 
    callback: AdvertisingSetCallback!
): Unit
```

Creates a new advertising set. If operation succeed, device will start advertising. This method returns immediately, the operation status is delivered through`callback.onAdvertisingSetStarted()`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!:advertising set parameters. |
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). |
| `periodicParameters` | [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!:periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). |
| `callback` | [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!:Callback for advertising set. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when any of the data parameter exceed the maximum allowable size, or unsupported advertising PHY is selected, or when attempt to use Periodic Advertising feature is made when it's not supported by the controller. |

### startAdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAdvertisingSet(
    parameters: AdvertisingSetParameters!, 
    advertiseData: AdvertiseData!, 
    scanResponse: AdvertiseData!, 
    periodicParameters: PeriodicAdvertisingParameters!, 
    periodicData: AdvertiseData!, 
    callback: AdvertisingSetCallback!, 
    handler: Handler!
): Unit
```

Creates a new advertising set. If operation succeed, device will start advertising. This method returns immediately, the operation status is delivered through`callback.onAdvertisingSetStarted()`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!:advertising set parameters. |
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). |
| `periodicParameters` | [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!:periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). |
| `callback` | [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!:Callback for advertising set. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:thread upon which the callbacks will be invoked. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when any of the data parameter exceed the maximum allowable size, or unsupported advertising PHY is selected, or when attempt to use Periodic Advertising feature is made when it's not supported by the controller. |

### startAdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAdvertisingSet(
    parameters: AdvertisingSetParameters!, 
    advertiseData: AdvertiseData!, 
    scanResponse: AdvertiseData!, 
    periodicParameters: PeriodicAdvertisingParameters!, 
    periodicData: AdvertiseData!, 
    duration: Int, 
    maxExtendedAdvertisingEvents: Int, 
    callback: AdvertisingSetCallback!
): Unit
```

Creates a new advertising set. If operation succeed, device will start advertising. This method returns immediately, the operation status is delivered through`callback.onAdvertisingSetStarted()`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!:advertising set parameters. |
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). |
| `periodicParameters` | [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!:periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):advertising duration, in 10ms unit. Valid range is from 1 (10ms) to 65535 (655,350 ms). 0 means advertising should continue until stopped. |
| `maxExtendedAdvertisingEvents` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum number of extended advertising events the controller shall attempt to send prior to terminating the extended advertising, even if the duration has not expired. Valid range is from 1 to 255. 0 means no maximum. |
| `callback` | [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!:Callback for advertising set. |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | when any of the data parameter exceed the maximum allowable size, or unsupported advertising PHY is selected, or when attempt to use Periodic Advertising feature is made when it's not supported by the controller. |

### startAdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAdvertisingSet(
    parameters: AdvertisingSetParameters!, 
    advertiseData: AdvertiseData!, 
    scanResponse: AdvertiseData!, 
    periodicParameters: PeriodicAdvertisingParameters!, 
    periodicData: AdvertiseData!, 
    duration: Int, 
    maxExtendedAdvertisingEvents: Int, 
    callback: AdvertisingSetCallback!, 
    handler: Handler!
): Unit
```

Creates a new advertising set. If operation succeed, device will start advertising. This method returns immediately, the operation status is delivered through`callback.onAdvertisingSetStarted()`.

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetParameters)!:Advertising set parameters. |
| `advertiseData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()) |
| `periodicParameters` | [PeriodicAdvertisingParameters](https://developer.android.com/reference/kotlin/android/bluetooth/le/PeriodicAdvertisingParameters)!:Periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseData)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.html#getLeMaximumAdvertisingDataLength()) |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):advertising duration, in 10ms unit. Valid range is from 1 (10ms) to 65535 (655,350 ms). 0 means advertising should continue until stopped. |
| `maxExtendedAdvertisingEvents` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum number of extended advertising events the controller shall attempt to send prior to terminating the extended advertising, even if the duration has not expired. Valid range is from 1 to 255. 0 means no maximum. |
| `callback` | [AdvertisingSetCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSetCallback)!:Callback for advertising set. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!:Thread upon which the callbacks will be invoked. |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When any of the data parameter exceed the maximum allowable size, or unsupported advertising PHY is selected, or when attempt to use Periodic Advertising feature is made when it's not supported by the controller, or when maxExtendedAdvertisingEvents is used on a controller that doesn't support the LE Extended Advertising |

### stopAdvertising

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopAdvertising(callback: AdvertiseCallback!): Unit
```

Stop Bluetooth LE advertising. The`callback`must be the same one use in android.bluetooth.le.BluetoothLeAdvertiser#startAdvertising. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback)!: [AdvertiseCallback](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertiseCallback) identifies the advertising instance to stop. |

### stopAdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopAdvertisingSet(callback: AdvertisingSetCallback!): Unit
```

Used to dispose of a [AdvertisingSet](https://developer.android.com/reference/kotlin/android/bluetooth/le/AdvertisingSet) object, obtained with android.bluetooth.le.BluetoothLeAdvertiser#startAdvertisingSet. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String)
