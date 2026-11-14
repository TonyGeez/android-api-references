# BluetoothProfile

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothProfile

Kotlin| [Java](https://developer.android.com/reference/android/bluetooth/BluetoothProfile "View this page in Java") 
| --- | --- |

```
interface BluetoothProfile
```

| [android.bluetooth.BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#) |

| Known Direct Subclasses [BluetoothA2dp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothA2dp), [BluetoothCsipSetCoordinator](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCsipSetCoordinator), [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [BluetoothGattServer](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer), [BluetoothHeadset](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset), [BluetoothHealth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth), [BluetoothHearingAid](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHearingAid), [BluetoothHidDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice), [BluetoothLeAudio](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudio) |-----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------| | [BluetoothA2dp](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothA2dp) | This class provides the public APIs to control the Bluetooth A2DP profile. | | [BluetoothCsipSetCoordinator](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothCsipSetCoordinator) | This class provides the public APIs to control the Bluetooth CSIP set coordinator. | | [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt) | Public API for the Bluetooth GATT Profile. | | [BluetoothGattServer](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattServer) | Public API for the Bluetooth GATT Profile server role. | | [BluetoothHeadset](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHeadset) | Public API for controlling the Bluetooth Headset Service. | | [BluetoothHealth](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHealth) | Public API for Bluetooth Health Profile. | | [BluetoothHearingAid](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHearingAid) | This class provides the public APIs to control the Hearing Aid profile. | | [BluetoothHidDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothHidDevice) | Provides the public APIs to control the Bluetooth HID Device profile. | | [BluetoothLeAudio](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothLeAudio) | This class provides the public APIs to control the LeAudio profile. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Public APIs for the Bluetooth Profiles.

Clients should call [BluetoothAdapter.getProfileProxy](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int)), to get the Profile Proxy. Each public profile implements this interface.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [ServiceListener](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.ServiceListener) An interface for notifying BluetoothProfile IPC clients when they have been connected or disconnected to the service. |

| Constants ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [A2DP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int) Advanced Audio Distribution Profile (A2DP) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CSIP_SET_COORDINATOR](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#CSIP_SET_COORDINATOR:kotlin.Int) Coordinated Set Identification Profile (CSIP) set coordinator |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PREVIOUS_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PREVIOUS_STATE:kotlin.String) Extra for the connection state intents of the individual profiles. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_PROFILE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_PROFILE:kotlin.String) Extra for the [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#) that the intent applies to. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [EXTRA_STATE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#EXTRA_STATE:kotlin.String) Extra for the connection state intents of the individual profiles. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT:kotlin.Int) Generic Attribute Profile (GATT) |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GATT_SERVER](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#GATT_SERVER:kotlin.Int) Generic Attribute Profile (GATT) Server |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HAP_CLIENT](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HAP_CLIENT:kotlin.Int) <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEADSET](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int) Headset and Handsfree profile |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEALTH](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEALTH:kotlin.Int) Health Profile |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HEARING_AID](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEARING_AID:kotlin.Int) Hearing Aid Device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [HID_DEVICE](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HID_DEVICE:kotlin.Int) Human Interface Device (HID) Device |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LE_AUDIO](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#LE_AUDIO:kotlin.Int) LE Audio Device |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SAP](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#SAP:kotlin.Int) SIM Access Profile (SAP) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int) The profile is in connected state |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int) The profile is in connecting state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int) The profile is in disconnected state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) The profile is in disconnecting state |
| --- | --- |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getConnectedDevices](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#getConnectedDevices())`()` Get connected devices for this specific profile. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionState](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#getConnectionState(android.bluetooth.BluetoothDevice))`(`device:` ` [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!`)` Get the current connection state of the profile |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | [getDevicesMatchingConnectionStates](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#getDevicesMatchingConnectionStates(kotlin.IntArray))`(`states:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Get a list of devices that match any of the given connection states. |
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

Extra for the [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#) that the intent applies to.

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

**Deprecated:** *Health Device Profile (HDP) and MCAP protocol are no longer used. New apps should use Bluetooth Low Energy based solutions such as [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt), [android.bluetooth.BluetoothAdapter#listenUsingL2capChannel()](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()), or [android.bluetooth.BluetoothDevice#createL2capChannel(int)](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int))*

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

Return the set of devices which are in state [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int)

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |

### getConnectionState

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getConnectionState(device: BluetoothDevice!): Int
```

Get the current connection state of the profile

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| `device` | [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!:Remote bluetooth device. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | State of the profile connection. One of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) Value is [android.bluetooth.BluetoothProfile#STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [android.bluetooth.BluetoothProfile#STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [android.bluetooth.BluetoothProfile#STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), or [android.bluetooth.BluetoothProfile#STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int) |

### getDevicesMatchingConnectionStates

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getDevicesMatchingConnectionStates(states: IntArray!): MutableList<BluetoothDevice!>!
```

Get a list of devices that match any of the given connection states.

If none of the devices match any of the given states, an empty list will be returned.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `states` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:Array of states. States can be one of [STATE_CONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTED:kotlin.Int), [STATE_CONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_CONNECTING:kotlin.Int), [STATE_DISCONNECTED](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTED:kotlin.Int), [STATE_DISCONNECTING](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#STATE_DISCONNECTING:kotlin.Int), |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!>! | List of devices. The list will be empty on error. |
