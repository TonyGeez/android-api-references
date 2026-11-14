Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHealth

Kotlin | [Java](../android/bluetooth/BluetoothHealth.md) 
| --- | --- |

```
class BluetoothHealth : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothHealth](../android/bluetooth/BluetoothHealth.md) |

| **This class was deprecated in API level 29.**
|
| Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))

Public API for Bluetooth Health Profile.

BluetoothHealth is a proxy object for controlling the Bluetooth Service via IPC.

How to connect to a health device which is acting in the source role.
- Use [BluetoothAdapter.getProfileProxy](../android/bluetooth/BluetoothAdapter.md)) to get the BluetoothHealth proxy object.
- Create an [BluetoothHealth](../android/bluetooth/BluetoothHealth.md) callback and call [registerSinkAppConfiguration](../android/bluetooth/BluetoothHealth.md)) to register an application configuration
- Pair with the remote device. This currently needs to be done manually from Bluetooth Settings
- Connect to a health device using [connectChannelToSource](../android/bluetooth/BluetoothHealth.md)). Some devices will connect the channel automatically. The [BluetoothHealth](../android/bluetooth/BluetoothHealth.md) callback will inform the application of channel state change.
- Use the file descriptor provided with a connected channel to read and write data to the health channel.
- The received data needs to be interpreted using a health manager which implements the IEEE 11073-xxxxx specifications.
- When done, close the health channel by calling [disconnectChannel](../android/bluetooth/BluetoothHealth.md)) and unregister the application configuration calling [unregisterAppConfiguration](../android/bluetooth/BluetoothHealth.md))

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_REGISTRATION_FAILURE](../android/bluetooth/BluetoothHealth.md) Health App Configuration registration failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_REGISTRATION_SUCCESS](../android/bluetooth/BluetoothHealth.md) Health App Configuration registration success |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_UNREGISTRATION_FAILURE](../android/bluetooth/BluetoothHealth.md) Health App Configuration un-registration failure |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_UNREGISTRATION_SUCCESS](../android/bluetooth/BluetoothHealth.md) Health App Configuration un-registration success |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_TYPE_RELIABLE](../android/bluetooth/BluetoothHealth.md) Health Profile - Channel Type used - Reliable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_TYPE_STREAMING](../android/bluetooth/BluetoothHealth.md) Health Profile - Channel Type used - Streaming |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SINK_ROLE](../android/bluetooth/BluetoothHealth.md) Health Profile Sink Role the device talking to the health device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_ROLE](../android/bluetooth/BluetoothHealth.md) Health Profile Source Role - the health device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_CONNECTED](../android/bluetooth/BluetoothHealth.md) Health Channel Connection State - Connected |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_CONNECTING](../android/bluetooth/BluetoothHealth.md) Health Channel Connection State - Connecting |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_DISCONNECTED](../android/bluetooth/BluetoothHealth.md) Health Channel Connection State - Disconnected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_DISCONNECTING](../android/bluetooth/BluetoothHealth.md) Health Channel Connection State - Disconnecting |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) |----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](../android/bluetooth/BluetoothProfile.md) Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](../android/bluetooth/BluetoothProfile.md) Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](../android/bluetooth/BluetoothProfile.md) Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](../android/bluetooth/BluetoothProfile.md) Extra for the [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](../android/bluetooth/BluetoothProfile.md) Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](../android/bluetooth/BluetoothProfile.md) Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](../android/bluetooth/BluetoothProfile.md) Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](../android/bluetooth/BluetoothProfile.md) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](../android/bluetooth/BluetoothProfile.md) Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](../android/bluetooth/BluetoothProfile.md) Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](../android/bluetooth/BluetoothProfile.md) Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](../android/bluetooth/BluetoothProfile.md) Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](../android/bluetooth/BluetoothProfile.md) LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](../android/bluetooth/BluetoothProfile.md) SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md) The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md) The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md) The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) The profile is in disconnecting state <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connectChannelToSource](../android/bluetooth/BluetoothHealth.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `config:` ` [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!`)` Connect to a health device which has the [SOURCE_ROLE](../android/bluetooth/BluetoothHealth.md). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [disconnectChannel](../android/bluetooth/BluetoothHealth.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `config:` ` [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!`, `channelId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Disconnect a connected health channel. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getConnectedDevices](../android/bluetooth/BluetoothHealth.md))`()` Get connected devices for the health profile. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](../android/bluetooth/BluetoothHealth.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Get the current connection state of the profile. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getDevicesMatchingConnectionStates](../android/bluetooth/BluetoothHealth.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Get a list of devices that match any of the given connection states. |
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | [getMainChannelFd](../android/bluetooth/BluetoothHealth.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`, `config:` ` [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!`)` Get the file descriptor of the main channel associated with the remote device and application configuration. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerSinkAppConfiguration](../android/bluetooth/BluetoothHealth.md))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [BluetoothHealthCallback](../android/bluetooth/BluetoothHealthCallback.md)!`)` Register an application configuration that acts as a Health SINK. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterAppConfiguration](../android/bluetooth/BluetoothHealth.md))`(`config:` ` [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!`)` Unregister an application configuration that has been registered using [registerSinkAppConfiguration](../android/bluetooth/BluetoothHealth.md)) For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. |

## Constants

### APP_CONFIG_REGISTRATION_FAILURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_REGISTRATION_FAILURE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health App Configuration registration failure 

 Value: 1

### APP_CONFIG_REGISTRATION_SUCCESS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_REGISTRATION_SUCCESS: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health App Configuration registration success 

 Value: 0

### APP_CONFIG_UNREGISTRATION_FAILURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_UNREGISTRATION_FAILURE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health App Configuration un-registration failure 

 Value: 3

### APP_CONFIG_UNREGISTRATION_SUCCESS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_UNREGISTRATION_SUCCESS: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health App Configuration un-registration success 

 Value: 2

### CHANNEL_TYPE_RELIABLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_TYPE_RELIABLE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Profile - Channel Type used - Reliable 

 Value: 10

### CHANNEL_TYPE_STREAMING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_TYPE_STREAMING: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Profile - Channel Type used - Streaming 

 Value: 11

### SINK_ROLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SINK_ROLE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Profile Sink Role the device talking to the health device. 

 Value: 2

### SOURCE_ROLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_ROLE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Profile Source Role - the health device. 

 Value: 1

### STATE_CHANNEL_CONNECTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_CONNECTED: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Channel Connection State - Connected 

 Value: 2

### STATE_CHANNEL_CONNECTING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_CONNECTING: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Channel Connection State - Connecting 

 Value: 1

### STATE_CHANNEL_DISCONNECTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_DISCONNECTED: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Channel Connection State - Disconnected 

 Value: 0

### STATE_CHANNEL_DISCONNECTING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_DISCONNECTING: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Channel Connection State - Disconnecting 

 Value: 3

## Public methods

### connectChannelToSource

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun connectChannelToSource(
    device: BluetoothDevice!, 
    config: BluetoothHealthAppConfiguration!
): Boolean
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Connect to a health device which has the [SOURCE_ROLE](../android/bluetooth/BluetoothHealth.md). This is an asynchronous call. If this function returns true, the callback associated with the application configuration will be called. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote Bluetooth device. |
| `config` | [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!: The application configuration which has been registered using [registerSinkAppConfiguration(java.lang.String,int,android.bluetooth.BluetoothHealthCallback)](../android/bluetooth/BluetoothHealth.md)) |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true, the callback associated with the application config will be called. |

### disconnectChannel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun disconnectChannel(
    device: BluetoothDevice!, 
    config: BluetoothHealthAppConfiguration!, 
    channelId: Int
): Boolean
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Disconnect a connected health channel. This is an asynchronous call. If this function returns true, the callback associated with the application configuration will be called. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote Bluetooth device. |
| `config` | [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!: The application configuration which has been registered using [registerSinkAppConfiguration(java.lang.String,int,android.bluetooth.BluetoothHealthCallback)](../android/bluetooth/BluetoothHealth.md)) |
| `channelId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The channel id associated with the channel |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true, the callback associated with the application config will be called. |

### getConnectedDevices

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

**Deprecated:** *Deprecated in Java.*

Get connected devices for the health profile.

Return the set of devices which are in state [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md)

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter for this profile. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice!): Int
```

**Deprecated:** *Deprecated in Java.*

Get the current connection state of the profile.

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter with the remote device. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) |

### getDevicesMatchingConnectionStates

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

**Deprecated:** *Deprecated in Java.*

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned.

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter for this profile. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Array of states. States can be one of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

### getMainChannelFd

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMainChannelFd(
    device: BluetoothDevice!, 
    config: BluetoothHealthAppConfiguration!
): ParcelFileDescriptor!
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Get the file descriptor of the main channel associated with the remote device and application configuration.

It's the responsibility of the caller to close the ParcelFileDescriptor when done. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!: The remote Bluetooth health device |
| `config` | [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!: The application configuration |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)! | null on failure, ParcelFileDescriptor on success. |

### registerSinkAppConfiguration

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerSinkAppConfiguration(
    name: String!, 
    dataType: Int, 
    callback: BluetoothHealthCallback!
): Boolean
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Register an application configuration that acts as a Health SINK. This is the configuration that will be used to communicate with health devices which will act as the [SOURCE_ROLE](../android/bluetooth/BluetoothHealth.md). This is an asynchronous call and so the callback is used to notify success or failure if the function returns true. 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The friendly name associated with the application or configuration. |
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The dataType of the Source role of Health Profile to which the sink wants to connect to. |
| `callback` | [BluetoothHealthCallback](../android/bluetooth/BluetoothHealthCallback.md)!: A callback to indicate success or failure of the registration and all operations done on this application configuration. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true, callback will be called. |

### unregisterAppConfiguration

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterAppConfiguration(config: BluetoothHealthAppConfiguration!): Boolean
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Unregister an application configuration that has been registered using [registerSinkAppConfiguration](../android/bluetooth/BluetoothHealth.md)) 
For apps targeting [Build.VERSION_CODES.R](../android/os/Build.VERSION_CODES.md) or lower, this requires the [Manifest.permission.BLUETOOTH](../android/Manifest.permission.md) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](../android/os/Build.VERSION_CODES.md) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](../android/Manifest.permission.md) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](../android/Manifest.permission.md)

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [BluetoothHealthAppConfiguration](../android/bluetooth/BluetoothHealthAppConfiguration.md)!: The health app configuration |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Success or failure. |
