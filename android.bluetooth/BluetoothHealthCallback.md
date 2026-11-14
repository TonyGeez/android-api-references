# BluetoothHealthCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHealthCallback

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothHealthCallback "View this page in Java") 

```
abstract class BluetoothHealthCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothHealthCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthCallback#) |

| **This class was deprecated in API level 29.**
|
| Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))

This abstract class is used to implement [BluetoothHealth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth) callbacks.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothHealthCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthCallback#BluetoothHealthCallback())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHealthAppConfigurationStatusChange](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthCallback#onHealthAppConfigurationStatusChange(android.bluetooth.BluetoothHealthAppConfiguration,%20kotlin.Int))`(`config:` ` [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback to inform change in registration state of the health application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHealthChannelStateChange](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthCallback#onHealthChannelStateChange(android.bluetooth.BluetoothHealthAppConfiguration,%20android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.Int,%20android.os.ParcelFileDescriptor,%20kotlin.Int))`(`config:` ` [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!`, `device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `prevState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fd:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!`, `channelId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback to inform change in channel state. |

## Public constructors

### BluetoothHealthCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BluetoothHealthCallback()
```

## Public methods

### onHealthAppConfigurationStatusChange

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHealthAppConfigurationStatusChange(
    config: BluetoothHealthAppConfiguration!, 
    status: Int
): Unit
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Callback to inform change in registration state of the health application.

This callback is called on the binder thread (not on the UI thread)

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!:Bluetooth Health app configuration |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Success or failure of the registration or unregistration calls. Can be one of [BluetoothHealth.APP_CONFIG_REGISTRATION_SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_REGISTRATION_SUCCESS:kotlin.Int) or [android.bluetooth.BluetoothHealth#APP_CONFIG_REGISTRATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_REGISTRATION_FAILURE:kotlin.Int) or [android.bluetooth.BluetoothHealth#APP_CONFIG_UNREGISTRATION_SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_UNREGISTRATION_SUCCESS:kotlin.Int) or [android.bluetooth.BluetoothHealth#APP_CONFIG_UNREGISTRATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_UNREGISTRATION_FAILURE:kotlin.Int) |

### onHealthChannelStateChange

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onHealthChannelStateChange(
    config: BluetoothHealthAppConfiguration!, 
    device: BluetoothDevice!, 
    prevState: Int, 
    newState: Int, 
    fd: ParcelFileDescriptor!, 
    channelId: Int
): Unit
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Callback to inform change in channel state.

It's the responsibility of the implementer of this callback to close the parcel file descriptor when done. This callback is called on the Binder thread (not the UI thread)

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!:The Health app configuration |
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:The Bluetooth Device |
| `prevState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous state of the channel |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new state of the channel. |
| `fd` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)!:The Parcel File Descriptor when the channel state is connected. |
| `channelId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id associated with the channel. This id will be used in future calls like when disconnecting the channel. |
