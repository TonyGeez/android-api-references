# BluetoothHealthCallback

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHealthCallback

Kotlin| [Java](../android/bluetooth/BluetoothHealthCallback.md) 
| --- | --- |

```
abstract class BluetoothHealthCallback
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHealthCallback](../android/bluetooth/BluetoothHealthCallback.md) |

| **This class was deprecated in API level 29.**
|
| Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))

This abstract class is used to implement [BluetoothHealth](../android/bluetooth/BluetoothHealth.md) callbacks.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [BluetoothHealthCallback](../android/bluetooth/BluetoothHealthCallback.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHealthAppConfigurationStatusChange](../android/bluetooth/BluetoothHealthCallback.md))`(`config:` ` [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!`, `status:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback to inform change in registration state of the health application. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onHealthChannelStateChange](../android/bluetooth/BluetoothHealthCallback.md))`(`config:` ` [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!`, `device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `prevState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `fd:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!`, `channelId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Callback to inform change in channel state. |

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

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Callback to inform change in registration state of the health application.

This callback is called on the binder thread (not on the UI thread)

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!:Bluetooth Health app configuration |
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Success or failure of the registration or unregistration calls. Can be one of [BluetoothHealth.APP_CONFIG_REGISTRATION_SUCCESS](../android/bluetooth/BluetoothHealth.md) or [android.bluetooth.BluetoothHealth#APP_CONFIG_REGISTRATION_FAILURE](../android/bluetooth/BluetoothHealth.md) or [android.bluetooth.BluetoothHealth#APP_CONFIG_UNREGISTRATION_SUCCESS](../android/bluetooth/BluetoothHealth.md) or [android.bluetooth.BluetoothHealth#APP_CONFIG_UNREGISTRATION_FAILURE](../android/bluetooth/BluetoothHealth.md) |

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

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Callback to inform change in channel state.

It's the responsibility of the implementer of this callback to close the parcel file descriptor when done. This callback is called on the Binder thread (not the UI thread)

| Parameters ||
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!:The Health app configuration |
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:The Bluetooth Device |
| `prevState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The previous state of the channel |
| --- | --- |
| `newState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new state of the channel. |
| `fd` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)!:The Parcel File Descriptor when the channel state is connected. |
| `channelId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The id associated with the channel. This id will be used in future calls like when disconnecting the channel. |
| --- | --- |
