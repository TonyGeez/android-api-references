# BluetoothProfile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothProfile

Kotlin| [Java](../android/bluetooth/BluetoothProfile.md) 
| --- | --- |

```
interface BluetoothProfile
```

| [android.bluetooth.BluetoothProfile](../android/bluetooth/BluetoothProfile.md) |

| Known Direct Subclasses [BluetoothA2dp](../android/bluetooth/BluetoothA2dp.md), [BluetoothCsipSetCoordinator](../android/bluetooth/BluetoothCsipSetCoordinator.md), [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [BluetoothGattServer](../android/bluetooth/BluetoothGattServer.md), [BluetoothHeadset](../android/bluetooth/BluetoothHeadset.md), [BluetoothHealth](../android/bluetooth/BluetoothHealth.md), [BluetoothHearingAid](../android/bluetooth/BluetoothHearingAid.md), [BluetoothHidDevice](../android/bluetooth/BluetoothHidDevice.md), [BluetoothLeAudio](../android/bluetooth/BluetoothLeAudio.md) |-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [BluetoothA2dp](../android/bluetooth/BluetoothA2dp.md) | This class provides the public APIs to control the Bluetooth A2DP profile. | | [BluetoothCsipSetCoordinator](../android/bluetooth/BluetoothCsipSetCoordinator.md) | This class provides the public APIs to control the Bluetooth CSIP set coordinator. | | [BluetoothGatt](../android/bluetooth/BluetoothGatt.md) | Public API for the Bluetooth GATT Profile. | | [BluetoothGattServer](../android/bluetooth/BluetoothGattServer.md) | Public API for the Bluetooth GATT Profile server role. | | [BluetoothHeadset](../android/bluetooth/BluetoothHeadset.md) | Public API for controlling the Bluetooth Headset Service. | | [BluetoothHealth](../android/bluetooth/BluetoothHealth.md) | Public API for Bluetooth Health Profile. | | [BluetoothHearingAid](../android/bluetooth/BluetoothHearingAid.md) | This class provides the public APIs to control the Hearing Aid profile. | | [BluetoothHidDevice](../android/bluetooth/BluetoothHidDevice.md) | Provides the public APIs to control the Bluetooth HID Device profile. | | [BluetoothLeAudio](../android/bluetooth/BluetoothLeAudio.md) | This class provides the public APIs to control the LeAudio profile. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Public APIs for the Bluetooth Profiles.

Clients should call [BluetoothAdapter.getProfileProxy](../android/bluetooth/BluetoothAdapter.md)), to get the Profile Proxy. Each public profile implements this interface.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ServiceListener](../android/bluetooth/BluetoothProfile.ServiceListener.md) An interface for notifying BluetoothProfile IPC clients when they have been connected or disconnected to the service. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](../android/bluetooth/BluetoothProfile.md) Advanced Audio Distribution Profile (A2DP) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](../android/bluetooth/BluetoothProfile.md) Coordinated Set Identification Profile (CSIP) set coordinator |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](../android/bluetooth/BluetoothProfile.md) Extra for the connection state intents of the individual profiles. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](../android/bluetooth/BluetoothProfile.md) Extra for the [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) that the intent applies to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](../android/bluetooth/BluetoothProfile.md) Extra for the connection state intents of the individual profiles. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](../android/bluetooth/BluetoothProfile.md) Generic Attribute Profile (GATT) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](../android/bluetooth/BluetoothProfile.md) Generic Attribute Profile (GATT) Server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](../android/bluetooth/BluetoothProfile.md) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](../android/bluetooth/BluetoothProfile.md) Headset and Handsfree profile |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](../android/bluetooth/BluetoothProfile.md) Health Profile |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](../android/bluetooth/BluetoothProfile.md) Hearing Aid Device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](../android/bluetooth/BluetoothProfile.md) Human Interface Device (HID) Device |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](../android/bluetooth/BluetoothProfile.md) LE Audio Device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](../android/bluetooth/BluetoothProfile.md) SIM Access Profile (SAP) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md) The profile is in connected state |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md) The profile is in connecting state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md) The profile is in disconnected state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) The profile is in disconnecting state |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getConnectedDevices](../android/bluetooth/BluetoothProfile.md))`()` Get connected devices for this specific profile. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](../android/bluetooth/BluetoothProfile.md))`(`device:` ` [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!`)` Get the current connection state of the profile |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!\>! | [getDevicesMatchingConnectionStates](../android/bluetooth/BluetoothProfile.md))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Get a list of devices that match any of the given connection states. |
| --- | --- |

## Constants

### A2DP

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val A2DP: Int
```

Advanced Audio Distribution Profile (A2DP) 

 Value: 2

### CSIP_SET_COORDINATOR

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CSIP_SET_COORDINATOR: Int
```

Coordinated Set Identification Profile (CSIP) set coordinator 

 Value: 25

### EXTRA_PREVIOUS_STATE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PREVIOUS_STATE: String
```

Extra for the connection state intents of the individual profiles.

This extra represents the previous connection state of the profile of the Bluetooth device. 

 Value: "android.bluetooth.profile.extra.PREVIOUS_STATE"

### EXTRA_PROFILE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_PROFILE: String
```

Extra for the [BluetoothProfile](../android/bluetooth/BluetoothProfile.md) that the intent applies to.

This extra represents the Bluetooth profile that the intent applies to. 

 Value: "android.bluetooth.profile.extra.PROFILE"

### EXTRA_STATE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EXTRA_STATE: String
```

Extra for the connection state intents of the individual profiles.

This extra represents the current connection state of the profile of the Bluetooth device. 

 Value: "android.bluetooth.profile.extra.STATE"

### GATT

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GATT: Int
```

Generic Attribute Profile (GATT) 

 Value: 7

### GATT_SERVER

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val GATT_SERVER: Int
```

Generic Attribute Profile (GATT) Server 

 Value: 8

### HAP_CLIENT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HAP_CLIENT: Int
```  

 Value: 28

### HEADSET

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEADSET: Int
```

Headset and Handsfree profile 

 Value: 1

### HEALTH

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEALTH: Int
```

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](../android/bluetooth/BluetoothGatt.md), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](../android/bluetooth/BluetoothAdapter.md)), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](../android/bluetooth/BluetoothDevice.md))*

Health Profile 

 Value: 3

### HEARING_AID

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEARING_AID: Int
```

Hearing Aid Device 

 Value: 21

### HID_DEVICE

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HID_DEVICE: Int
```

Human Interface Device (HID) Device 

 Value: 19

### LE_AUDIO

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val LE_AUDIO: Int
```

LE Audio Device 

 Value: 22

### SAP

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SAP: Int
```

SIM Access Profile (SAP) 

 Value: 10

### STATE_CONNECTED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CONNECTED: Int
```

The profile is in connected state 

 Value: 2

### STATE_CONNECTING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_CONNECTING: Int
```

The profile is in connecting state 

 Value: 1

### STATE_DISCONNECTED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DISCONNECTED: Int
```

The profile is in disconnected state 

 Value: 0

### STATE_DISCONNECTING

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STATE_DISCONNECTING: Int
```

The profile is in disconnecting state 

 Value: 3

## Public methods

### getConnectedDevices

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnectedDevices(): MutableList<BluetoothDevice!>!
```

Get connected devices for this specific profile.

Return the set of devices which are in state [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnectionState(device: BluetoothDevice!): Int
```

Get the current connection state of the profile

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!:Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md) |

### getDevicesMatchingConnectionStates

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Array of states. States can be one of [STATE_CONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_CONNECTING](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTED](../android/bluetooth/BluetoothProfile.md), [STATE_DISCONNECTING](../android/bluetooth/BluetoothProfile.md), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](../android/bluetooth/BluetoothDevice.md)!>! | List of devices. The list will be empty on error. |
