Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothHealth

Kotlin | [Java](https://developer.android.com/reference/android/bluetooth/BluetoothHealth "View this page in Java") 

```
class BluetoothHealth : BluetoothProfile
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothHealth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#) |

| **This class was deprecated in API level 29.**
|
| Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))

Public API for Bluetooth Health Profile.

BluetoothHealth is a proxy object for controlling the Bluetooth Service via IPC.

How to connect to a health device which is acting in the source role.
- Use [BluetoothAdapter.getProfileProxy](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int)) to get the BluetoothHealth proxy object.
- Create an [BluetoothHealth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#) callback and call [registerSinkAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#registerSinkAppConfiguration(kotlin.String,%20kotlin.Int,%20android.bluetooth.BluetoothHealthCallback)) to register an application configuration
- Pair with the remote device. This currently needs to be done manually from Bluetooth Settings
- Connect to a health device using [connectChannelToSource](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#connectChannelToSource(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothHealthAppConfiguration)). Some devices will connect the channel automatically. The [BluetoothHealth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#) callback will inform the application of channel state change.
- Use the file descriptor provided with a connected channel to read and write data to the health channel.
- The received data needs to be interpreted using a health manager which implements the IEEE 11073-xxxxx specifications.
- When done, close the health channel by calling [disconnectChannel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#disconnectChannel(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothHealthAppConfiguration,%20kotlin.Int)) and unregister the application configuration calling [unregisterAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#unregisterAppConfiguration(android.bluetooth.BluetoothHealthAppConfiguration))

## Summary

| Constants ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_REGISTRATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_REGISTRATION_FAILURE:kotlin.Int) Health App Configuration registration failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_REGISTRATION_SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_REGISTRATION_SUCCESS:kotlin.Int) Health App Configuration registration success |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_UNREGISTRATION_FAILURE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_UNREGISTRATION_FAILURE:kotlin.Int) Health App Configuration un-registration failure |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APP_CONFIG_UNREGISTRATION_SUCCESS](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#APP_CONFIG_UNREGISTRATION_SUCCESS:kotlin.Int) Health App Configuration un-registration success |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_TYPE_RELIABLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#CHANNEL_TYPE_RELIABLE:kotlin.Int) Health Profile - Channel Type used - Reliable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CHANNEL_TYPE_STREAMING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#CHANNEL_TYPE_STREAMING:kotlin.Int) Health Profile - Channel Type used - Streaming |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SINK_ROLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SINK_ROLE:kotlin.Int) Health Profile Sink Role the device talking to the health device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SOURCE_ROLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SOURCE_ROLE:kotlin.Int) Health Profile Source Role - the health device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#STATE_CHANNEL_CONNECTED:kotlin.Int) Health Channel Connection State - Connected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#STATE_CHANNEL_CONNECTING:kotlin.Int) Health Channel Connection State - Connecting |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#STATE_CHANNEL_DISCONNECTED:kotlin.Int) Health Channel Connection State - Disconnected |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CHANNEL_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#STATE_CHANNEL_DISCONNECTING:kotlin.Int) Health Channel Connection State - Disconnecting |

| Inherited constants ||
|---|---|
| From class [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile) |----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int) Advanced Audio Distribution Profile (A2DP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#CSIP_SET_COORDINATOR:kotlin.Int) Coordinated Set Identification Profile (CSIP) set coordinator <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String) Extra for the connection state intents of the individual profiles. This extra represents the previous connection state of the profile of the Bluetooth device. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PROFILE:kotlin.String) Extra for the [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile) that the intent applies to. This extra represents the Bluetooth profile that the intent applies to. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String) Extra for the connection state intents of the individual profiles. This extra represents the current connection state of the profile of the Bluetooth device. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) Generic Attribute Profile (GATT) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT_SERVER:kotlin.Int) Generic Attribute Profile (GATT) Server <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HAP_CLIENT:kotlin.Int) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int) Headset and Handsfree profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEALTH:kotlin.Int) Health Profile <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEARING_AID:kotlin.Int) Hearing Aid Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HID_DEVICE:kotlin.Int) Human Interface Device (HID) Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#LE_AUDIO:kotlin.Int) LE Audio Device <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#SAP:kotlin.Int) SIM Access Profile (SAP) <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int) The profile is in connected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int) The profile is in connecting state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int) The profile is in disconnected state <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) The profile is in disconnecting state <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [connectChannelToSource](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#connectChannelToSource(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothHealthAppConfiguration))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `config:` ` [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!`)` Connect to a health device which has the [SOURCE_ROLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SOURCE_ROLE:kotlin.Int). |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [disconnectChannel](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#disconnectChannel(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothHealthAppConfiguration,%20kotlin.Int))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `config:` ` [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!`, `channelId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Disconnect a connected health channel. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getConnectedDevices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#getConnectedDevices())`()` Get connected devices for the health profile. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#getConnectionState(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Get the current connection state of the profile. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getDevicesMatchingConnectionStates](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#getDevicesMatchingConnectionStates(kotlin.IntArray))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Get a list of devices that match any of the given connection states. |
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | [getMainChannelFd](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#getMainChannelFd(android.bluetooth.BluetoothDevice,%20android.bluetooth.BluetoothHealthAppConfiguration))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`, `config:` ` [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!`)` Get the file descriptor of the main channel associated with the remote device and application configuration. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [registerSinkAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#registerSinkAppConfiguration(kotlin.String,%20kotlin.Int,%20android.bluetooth.BluetoothHealthCallback))`(`name:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `dataType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `callback:` ` [BluetoothHealthCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthCallback)!`)` Register an application configuration that acts as a Health SINK. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unregisterAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#unregisterAppConfiguration(android.bluetooth.BluetoothHealthAppConfiguration))`(`config:` ` [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!`)` Unregister an application configuration that has been registered using [registerSinkAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#registerSinkAppConfiguration(kotlin.String,%20kotlin.Int,%20android.bluetooth.BluetoothHealthCallback)) For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. |

## Constants

### APP_CONFIG_REGISTRATION_FAILURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_REGISTRATION_FAILURE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health App Configuration registration failure 

 Value: 1

### APP_CONFIG_REGISTRATION_SUCCESS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_REGISTRATION_SUCCESS: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health App Configuration registration success 

 Value: 0

### APP_CONFIG_UNREGISTRATION_FAILURE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_UNREGISTRATION_FAILURE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health App Configuration un-registration failure 

 Value: 3

### APP_CONFIG_UNREGISTRATION_SUCCESS

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APP_CONFIG_UNREGISTRATION_SUCCESS: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health App Configuration un-registration success 

 Value: 2

### CHANNEL_TYPE_RELIABLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_TYPE_RELIABLE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Profile - Channel Type used - Reliable 

 Value: 10

### CHANNEL_TYPE_STREAMING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHANNEL_TYPE_STREAMING: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Profile - Channel Type used - Streaming 

 Value: 11

### SINK_ROLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SINK_ROLE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Profile Sink Role the device talking to the health device. 

 Value: 2

### SOURCE_ROLE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOURCE_ROLE: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Profile Source Role - the health device. 

 Value: 1

### STATE_CHANNEL_CONNECTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_CONNECTED: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Channel Connection State - Connected 

 Value: 2

### STATE_CHANNEL_CONNECTING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_CONNECTING: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Channel Connection State - Connecting 

 Value: 1

### STATE_CHANNEL_DISCONNECTED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_DISCONNECTED: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Health Channel Connection State - Disconnected 

 Value: 0

### STATE_CHANNEL_DISCONNECTING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CHANNEL_DISCONNECTING: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

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

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Connect to a health device which has the [SOURCE_ROLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SOURCE_ROLE:kotlin.Int). This is an asynchronous call. If this function returns true, the callback associated with the application configuration will be called. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!: The remote Bluetooth device. |
| `config` | [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!: The application configuration which has been registered using [registerSinkAppConfiguration(java.lang.String,int,android.bluetooth.BluetoothHealthCallback)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#registerSinkAppConfiguration(kotlin.String,%20kotlin.Int,%20android.bluetooth.BluetoothHealthCallback)) |

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

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Disconnect a connected health channel. This is an asynchronous call. If this function returns true, the callback associated with the application configuration will be called. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!: The remote Bluetooth device. |
| `config` | [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!: The application configuration which has been registered using [registerSinkAppConfiguration(java.lang.String,int,android.bluetooth.BluetoothHealthCallback)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#registerSinkAppConfiguration(kotlin.String,%20kotlin.Int,%20android.bluetooth.BluetoothHealthCallback)) |
| `channelId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The channel id associated with the channel |

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

Return the set of devices which are in state [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int)

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter for this profile. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConnectionState(device: BluetoothDevice!): Int
```

**Deprecated:** *Deprecated in Java.*

Get the current connection state of the profile.

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter with the remote device. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!: Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) |

### getDevicesMatchingConnectionStates

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

**Deprecated:** *Deprecated in Java.*

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned.

This is not specific to any application configuration but represents the connection state of the local Bluetooth adapter for this profile. This can be used by applications like status bar which would just like to know the state of the local adapter. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: Array of states. States can be one of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

### getMainChannelFd

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMainChannelFd(
    device: BluetoothDevice!, 
    config: BluetoothHealthAppConfiguration!
): ParcelFileDescriptor!
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Get the file descriptor of the main channel associated with the remote device and application configuration.

It's the responsibility of the caller to close the ParcelFileDescriptor when done. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!: The remote Bluetooth health device |
| `config` | [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!: The application configuration |

| Return ||
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)! | null on failure, ParcelFileDescriptor on success. |

### registerSinkAppConfiguration

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun registerSinkAppConfiguration(
    name: String!, 
    dataType: Int, 
    callback: BluetoothHealthCallback!
): Boolean
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Register an application configuration that acts as a Health SINK. This is the configuration that will be used to communicate with health devices which will act as the [SOURCE_ROLE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#SOURCE_ROLE:kotlin.Int). This is an asynchronous call and so the callback is used to notify success or failure if the function returns true. 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The friendly name associated with the application or configuration. |
| `dataType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The dataType of the Source role of Health Profile to which the sink wants to connect to. |
| `callback` | [BluetoothHealthCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthCallback)!: A callback to indicate success or failure of the registration and all operations done on this application configuration. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | If true, callback will be called. |

### unregisterAppConfiguration

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun unregisterAppConfiguration(config: BluetoothHealthAppConfiguration!): Boolean
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

Unregister an application configuration that has been registered using [registerSinkAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth#registerSinkAppConfiguration(kotlin.String,%20kotlin.Int,%20android.bluetooth.BluetoothHealthCallback)) 
For apps targeting [Build.VERSION_CODES.R](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int) or lower, this requires the [Manifest.permission.BLUETOOTH](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String) permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting [Build.VERSION_CODES.S](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int) or or higher, this requires the [Manifest.permission.BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String) permission which can be gained with [android.app.Activity#requestPermissions(String[], int)](https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)). 
Requires [android.Manifest.permission#BLUETOOTH_CONNECT](https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String)

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `config` | [BluetoothHealthAppConfiguration](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealthAppConfiguration)!: The health app configuration |

| Return ||
|------------------------------------------------------------------------------------|---------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Success or failure. |
