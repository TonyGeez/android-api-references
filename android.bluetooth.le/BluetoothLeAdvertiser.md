# BluetoothLeAdvertiser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothLeAdvertiser

Kotlin| [Java](BluetoothLeAdvertiser.md) 
| --- | --- |

```
class BluetoothLeAdvertiser
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.le.BluetoothLeAdvertiser](BluetoothLeAdvertiser.md) |

This class provides a way to perform Bluetooth LE advertise operations, such as starting and stopping advertising. An advertiser can broadcast up to 31 bytes of advertisement data represented by [AdvertiseData](AdvertiseData.md).

To get an instance of [BluetoothLeAdvertiser](BluetoothLeAdvertiser.md), call the [android.bluetooth.BluetoothAdapter#getBluetoothLeAdvertiser()](../android.bluetooth/BluetoothAdapter.md))method.

## Summary

| Public methods ||
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertising](BluetoothLeAdvertiser.md))`(`settings:` ` [AdvertiseSettings](AdvertiseSettings.md)!`, `advertiseData:` ` [AdvertiseData](AdvertiseData.md)!`, `callback:` ` [AdvertiseCallback](AdvertiseCallback.md)!`)` Start Bluetooth LE Advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertising](BluetoothLeAdvertiser.md))`(`settings:` ` [AdvertiseSettings](AdvertiseSettings.md)!`, `advertiseData:` ` [AdvertiseData](AdvertiseData.md)!`, `scanResponse:` ` [AdvertiseData](AdvertiseData.md)!`, `callback:` ` [AdvertiseCallback](AdvertiseCallback.md)!`)` Start Bluetooth LE Advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](BluetoothLeAdvertiser.md))`(`parameters:` ` [AdvertisingSetParameters](AdvertisingSetParameters.md)!`, `advertiseData:` ` [AdvertiseData](AdvertiseData.md)!`, `scanResponse:` ` [AdvertiseData](AdvertiseData.md)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!`, `periodicData:` ` [AdvertiseData](AdvertiseData.md)!`, `callback:` ` [AdvertisingSetCallback](AdvertisingSetCallback.md)!`)` Creates a new advertising set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](BluetoothLeAdvertiser.md))`(`parameters:` ` [AdvertisingSetParameters](AdvertisingSetParameters.md)!`, `advertiseData:` ` [AdvertiseData](AdvertiseData.md)!`, `scanResponse:` ` [AdvertiseData](AdvertiseData.md)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!`, `periodicData:` ` [AdvertiseData](AdvertiseData.md)!`, `callback:` ` [AdvertisingSetCallback](AdvertisingSetCallback.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Creates a new advertising set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](BluetoothLeAdvertiser.md))`(`parameters:` ` [AdvertisingSetParameters](AdvertisingSetParameters.md)!`, `advertiseData:` ` [AdvertiseData](AdvertiseData.md)!`, `scanResponse:` ` [AdvertiseData](AdvertiseData.md)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!`, `periodicData:` ` [AdvertiseData](AdvertiseData.md)!`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxExtendedAdvertisingEvents:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [AdvertisingSetCallback](AdvertisingSetCallback.md)!`)` Creates a new advertising set. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAdvertisingSet](BluetoothLeAdvertiser.md))`(`parameters:` ` [AdvertisingSetParameters](AdvertisingSetParameters.md)!`, `advertiseData:` ` [AdvertiseData](AdvertiseData.md)!`, `scanResponse:` ` [AdvertiseData](AdvertiseData.md)!`, `periodicParameters:` ` [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!`, `periodicData:` ` [AdvertiseData](AdvertiseData.md)!`, `duration:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `maxExtendedAdvertisingEvents:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [AdvertisingSetCallback](AdvertisingSetCallback.md)!`, `handler:` ` [Handler](../android.os/Handler.md)!`)` Creates a new advertising set. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAdvertising](BluetoothLeAdvertiser.md))`(`callback:` ` [AdvertiseCallback](AdvertiseCallback.md)!`)` Stop Bluetooth LE advertising. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopAdvertisingSet](BluetoothLeAdvertiser.md))`(`callback:` ` [AdvertisingSetCallback](AdvertisingSetCallback.md)!`)` Used to dispose of a [AdvertisingSet](AdvertisingSet.md) object, obtained with android. |

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

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission only when`settings.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [AdvertiseSettings](AdvertiseSettings.md)!:Settings for Bluetooth LE advertising. |
| `advertiseData` | [AdvertiseData](AdvertiseData.md)!:Advertisement data to be broadcasted. |
| `callback` | [AdvertiseCallback](AdvertiseCallback.md)!:Callback for advertising status. |
| --- | --- |

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

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission only when`settings.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `settings` | [AdvertiseSettings](AdvertiseSettings.md)!:Settings for Bluetooth LE advertising. |
| `advertiseData` | [AdvertiseData](AdvertiseData.md)!:Advertisement data to be advertised in advertisement packet. |
| `scanResponse` | [AdvertiseData](AdvertiseData.md)!:Scan response associated with the advertisement data. |
| --- | --- |
| `callback` | [AdvertiseCallback](AdvertiseCallback.md)!:Callback for advertising status. |

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

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](AdvertisingSetParameters.md)!:advertising set parameters. |
| `advertiseData` | [AdvertiseData](AdvertiseData.md)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](AdvertiseData.md)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). |
| --- | --- |
| `periodicParameters` | [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!:periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](AdvertiseData.md)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). |
| `callback` | [AdvertisingSetCallback](AdvertisingSetCallback.md)!:Callback for advertising set. |
| --- | --- |

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

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](AdvertisingSetParameters.md)!:advertising set parameters. |
| `advertiseData` | [AdvertiseData](AdvertiseData.md)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](AdvertiseData.md)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). |
| --- | --- |
| `periodicParameters` | [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!:periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](AdvertiseData.md)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). |
| `callback` | [AdvertisingSetCallback](AdvertisingSetCallback.md)!:Callback for advertising set. |
| --- | --- |
| `handler` | [Handler](../android.os/Handler.md)!:thread upon which the callbacks will be invoked. |

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

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](AdvertisingSetParameters.md)!:advertising set parameters. |
| `advertiseData` | [AdvertiseData](AdvertiseData.md)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](AdvertiseData.md)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). |
| --- | --- |
| `periodicParameters` | [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!:periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](AdvertiseData.md)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):advertising duration, in 10ms unit. Valid range is from 1 (10ms) to 65535 (655,350 ms). 0 means advertising should continue until stopped. |
| --- | --- |
| `maxExtendedAdvertisingEvents` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum number of extended advertising events the controller shall attempt to send prior to terminating the extended advertising, even if the duration has not expired. Valid range is from 1 to 255. 0 means no maximum. |
| `callback` | [AdvertisingSetCallback](AdvertisingSetCallback.md)!:Callback for advertising set. |

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

Requires the [android.Manifest.permission#BLUETOOTH_PRIVILEGED](../android/Manifest.permission.md) permission when`parameters.getOwnAddressType()`is different from`AdvertisingSetParameters.ADDRESS_TYPE_DEFAULT`or`parameters.isDirected()`is true.

The [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission is always enforced. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)).

| Parameters ||
|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `parameters` | [AdvertisingSetParameters](AdvertisingSetParameters.md)!:Advertising set parameters. |
| `advertiseData` | [AdvertiseData](AdvertiseData.md)!:Advertisement data to be broadcasted. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)). If the advertisement is connectable, three bytes will be added for flags. |
| `scanResponse` | [AdvertiseData](AdvertiseData.md)!:Scan response associated with the advertisement data. Size must not exceed [BluetoothAdapter.getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)) |
| --- | --- |
| `periodicParameters` | [PeriodicAdvertisingParameters](PeriodicAdvertisingParameters.md)!:Periodic advertising parameters. If null, periodic advertising will not be started. |
| `periodicData` | [AdvertiseData](AdvertiseData.md)!:Periodic advertising data. Size must not exceed [android.bluetooth.BluetoothAdapter#getLeMaximumAdvertisingDataLength](../android.bluetooth/BluetoothAdapter.md)) |
| `duration` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):advertising duration, in 10ms unit. Valid range is from 1 (10ms) to 65535 (655,350 ms). 0 means advertising should continue until stopped. |
| --- | --- |
| `maxExtendedAdvertisingEvents` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):maximum number of extended advertising events the controller shall attempt to send prior to terminating the extended advertising, even if the duration has not expired. Valid range is from 1 to 255. 0 means no maximum. |
| `callback` | [AdvertisingSetCallback](AdvertisingSetCallback.md)!:Callback for advertising set. |
| `handler` | [Handler](../android.os/Handler.md)!:Thread upon which the callbacks will be invoked. |
| --- | --- |

| Exceptions ||
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | When any of the data parameter exceed the maximum allowable size, or unsupported advertising PHY is selected, or when attempt to use Periodic Advertising feature is made when it's not supported by the controller, or when maxExtendedAdvertisingEvents is used on a controller that doesn't support the LE Extended Advertising |

### stopAdvertising

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopAdvertising(callback: AdvertiseCallback!): Unit
```

Stop Bluetooth LE advertising. The`callback`must be the same one use in android.bluetooth.le.BluetoothLeAdvertiser#startAdvertising. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `callback` | [AdvertiseCallback](AdvertiseCallback.md)!: [AdvertiseCallback](AdvertiseCallback.md) identifies the advertising instance to stop. |

### stopAdvertisingSet

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun stopAdvertisingSet(callback: AdvertisingSetCallback!): Unit
```

Used to dispose of a [AdvertisingSet](AdvertisingSet.md) object, obtained with android.bluetooth.le.BluetoothLeAdvertiser#startAdvertisingSet. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH_ADMIN](../android/Manifest.permission.md) permission which can be gained with a simple`<uses-permission>`manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_ADVERTISE](../android/Manifest.permission.md) permission which can be gained with[android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_ADVERTISE](../android/Manifest.permission.md)
