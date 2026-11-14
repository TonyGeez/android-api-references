Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothAdapter

```
class BluetoothAdapter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.bluetooth.BluetoothAdapter](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#) |

Represents the local device Bluetooth adapter. The `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#` lets you perform fundamental Bluetooth tasks, such as initiate device discovery, query a list of bonded (paired) devices, instantiate a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` using a known MAC address, and create a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` to listen for connection requests from other devices, and start a scan for Bluetooth LE devices.

To get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#` representing the local Bluetooth adapter, call the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager#getAdapter()` function on `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothManager`. On JELLY_BEAN_MR1 and below you will need to use the static `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getDefaultAdapter()` method instead.

Fundamentally, this is your starting point for all Bluetooth actions. Once you have the local adapter, you can get a set of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` objects representing all paired devices with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getBondedDevices()`; start device discovery with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#startDiscovery()`; or create a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` to listen for incoming RFComm connection requests with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)`; listen for incoming L2CAP Connection-oriented Channels (CoC) connection requests with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`; or start a scan for Bluetooth LE devices with `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(android.bluetooth.le.ScanCallback)` using the scanner from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getBluetoothLeScanner()`.

This class is thread safe.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using Bluetooth, read the [Bluetooth](https://developer.android.com/guide/topics/connectivity/bluetooth.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback` Callback interface used to deliver LE scan results. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` Intent used to broadcast the change in connection state of the local Bluetooth adapter to a profile of the remote device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_DISCOVERY_FINISHED:kotlin.String` Broadcast Action: The local Bluetooth adapter has finished the device discovery process. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_DISCOVERY_STARTED:kotlin.String` Broadcast Action: The local Bluetooth adapter has started the remote device discovery process. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_LOCAL_NAME_CHANGED:kotlin.String` Broadcast Action: The local Bluetooth adapter has changed its friendly Bluetooth name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_REQUEST_DISCOVERABLE:kotlin.String` Activity Action: Show a system activity that requests discoverable mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_REQUEST_ENABLE:kotlin.String` Activity Action: Show a system activity that allows the user to turn on Bluetooth. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_SCAN_MODE_CHANGED:kotlin.String` Broadcast Action: Indicates the Bluetooth scan mode of the local Adapter has changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` Broadcast Action: The state of the local Bluetooth adapter has been changed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ERROR:kotlin.Int` Sentinel error value for this class. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_CONNECTION_STATE:kotlin.String` Extra used by `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_DISCOVERABLE_DURATION:kotlin.String` Used as an optional int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_REQUEST_DISCOVERABLE:kotlin.String` intents to request a specific duration for discoverability in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_LOCAL_NAME:kotlin.String` Used as a String extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_LOCAL_NAME_CHANGED:kotlin.String` intents to request the local Bluetooth name. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_CONNECTION_STATE:kotlin.String` Extra used by `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_CONNECTION_STATE_CHANGED:kotlin.String` |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_SCAN_MODE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_SCAN_MODE_CHANGED:kotlin.String` intents to request the previous scan mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_STATE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` intents to request the previous power state. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_SCAN_MODE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_SCAN_MODE_CHANGED:kotlin.String` intents to request the current scan mode. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_STATE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` intents to request the current power state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE:kotlin.Int` Indicates that inquiry scan is disabled, but page scan is enabled on the local Bluetooth adapter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int` Indicates that both inquiry scan and page scan are enabled on the local Bluetooth adapter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_NONE:kotlin.Int` Indicates that both inquiry scan and page scan are disabled on the local Bluetooth adapter. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_CONNECTED:kotlin.Int` The profile is in connected state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_CONNECTING:kotlin.Int` The profile is in connecting state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_DISCONNECTED:kotlin.Int` The profile is in disconnected state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_DISCONNECTING:kotlin.Int` The profile is in disconnecting state |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int` Indicates the local Bluetooth adapter is off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` Indicates the local Bluetooth adapter is on, and ready for use. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_OFF:kotlin.Int` Indicates the local Bluetooth adapter is turning off. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_ON:kotlin.Int` Indicates the local Bluetooth adapter is turning on. |

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery()()` Cancel the current device discovery process. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#checkBluetoothAddress(kotlin.String)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Validate a String Bluetooth address, such as "00:43:A8:23:10:F0" |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#closeProfileProxy(kotlin.Int,%20android.bluetooth.BluetoothProfile)(unusedProfile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, proxy: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile!)` Close the connection of the profile proxy to the Service. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#disable()()` Turn off the local Bluetooth adapter---do not use without explicit user action to turn off Bluetooth. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#enable()()` Turn on the local Bluetooth adapter---do not use without explicit user action to turn on Bluetooth. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getAddress()()` Returns the hardware address of the local Bluetooth adapter. |
| [BluetoothLeAdvertiser](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getBluetoothLeAdvertiser()()` Returns a `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser` object for Bluetooth LE Advertising operations. |
| [BluetoothLeScanner](https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getBluetoothLeScanner()()` Returns a `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner` object for Bluetooth LE scan operations. |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getBondedDevices()()` Return the set of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` objects that are bonded (paired) to the local adapter. |
| static [BluetoothAdapter](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getDefaultAdapter()()` Get a handle to the default local Bluetooth adapter. |
| [Duration](https://developer.android.com/reference/kotlin/java/time/Duration.html#)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getDiscoverableTimeout()()` Get the timeout duration of the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getLeMaximumAdvertisingDataLength()()` Return the maximum LE advertising data length in bytes, if LE Extended Advertising feature is supported, 0 otherwise. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getMaxConnectedAudioDevices()()` Get the maximum number of connected devices per audio profile for this device. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getName()()` Get the friendly Bluetooth name of the local Bluetooth adapter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileConnectionState(kotlin.Int)(profile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the current connection state of a profile. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, listener: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.ServiceListener!, profile: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the profile proxy object associated with the profile. |
| [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getRemoteDevice(kotlin.ByteArray)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` object for the given Bluetooth hardware address. |
| [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getRemoteDevice(kotlin.String)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` object for the given Bluetooth hardware address. |
| [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getRemoteLeDevice(kotlin.String,%20kotlin.Int)(address: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, addressType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` object for the given Bluetooth hardware address and addressType. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getScanMode()()` Get the current Bluetooth scan mode of the local Bluetooth adapter. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getState()()` Get the current state of the local Bluetooth adapter. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isDiscovering()()` Return true if the local Bluetooth adapter is currently in the device discovery process. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isEnabled()()` Return true if Bluetooth is currently enabled and ready for use. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLe2MPhySupported()()` Return true if LE 2M PHY feature is supported. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLeAudioBroadcastAssistantSupported()()` Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` if the LE audio broadcast assistant feature is supported, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` if the feature is not supported, or an error code. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLeAudioBroadcastSourceSupported()()` Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` if the LE audio broadcast source feature is supported, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` if the feature is not supported, or an error code. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLeAudioSupported()()` Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` if the LE audio feature is supported, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` if the feature is not supported, or an error code. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLeCodedPhySupported()()` Return true if LE Coded PHY feature is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLeExtendedAdvertisingSupported()()` Return true if LE Extended Advertising feature is supported. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLeHighDataThroughputPhySupported()()` Checks if LE High Data Throughput (HDT) PHY is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isLePeriodicAdvertisingSupported()()` Return true if LE Periodic Advertising feature is supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isMultipleAdvertisementSupported()()` Return true if the multi advertisement is supported by the chipset. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isOffloadedFilteringSupported()()` Return true if offloaded filters are supported. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isOffloadedScanBatchingSupported()()` Return true if offloaded scan batching is supported. |
| [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingInsecureL2capChannel()()` Create an insecure L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` and assign a dynamic PSM value. |
| [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingInsecureRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uuid: https://developer.android.com/reference/kotlin/java/util/UUID.html#!)` Create a listening, insecure RFCOMM Bluetooth socket with Service Record. |
| [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()()` Create a secure L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` and assign a dynamic protocol/service multiplexer (PSM) value. |
| [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, uuid: https://developer.android.com/reference/kotlin/java/util/UUID.html#!)` Create a listening, secure RFCOMM Bluetooth socket with Service Record. |
| [BluetoothServerSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingSocketSettings(android.bluetooth.BluetoothSocketSettings)(settings: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings)` Creates a listening server channel for Bluetooth connections with the specified socket settings `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings`. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#setName(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set the friendly Bluetooth name of the local Bluetooth adapter. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#startDiscovery()()` Start the remote device discovery process. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#startLeScan(android.bluetooth.BluetoothAdapter.LeScanCallback)(callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback!)` Starts a scan for Bluetooth LE devices. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#startLeScan(kotlin.Array,%20android.bluetooth.BluetoothAdapter.LeScanCallback)(serviceUuids: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/util/UUID.html#!>!, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback!)` Starts a scan for Bluetooth LE devices, looking for devices that advertise given services. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#stopLeScan(android.bluetooth.BluetoothAdapter.LeScanCallback)(callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback!)` Stops an ongoing Bluetooth LE device scan. |

| Protected methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |

## Constants

### ACTION_CONNECTION_STATE_CHANGED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CONNECTION_STATE_CHANGED: String
```

Intent used to broadcast the change in connection state of the local Bluetooth adapter to a profile of the remote device. When the adapter is not connected to any profiles of any remote devices and it attempts a connection to a profile this intent will be sent. Once connected, this intent will not be sent for any more connection attempts to any profiles of any remote device. When the adapter disconnects from the last profile its connected to of any remote device, this intent will be sent.

This intent is useful for applications that are only concerned about whether the local adapter is connected to any profile of any device and are not really concerned about which profile. For example, an application which displays an icon to display whether Bluetooth is connected or not can use this intent.

This intent will have 3 extras: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_CONNECTION_STATE:kotlin.String` - The current connection state. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_CONNECTION_STATE:kotlin.String`- The previous connection state. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` - The remote device.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_CONNECTION_STATE:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_CONNECTION_STATE:kotlin.String` can be any of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_DISCONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_CONNECTING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_CONNECTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_DISCONNECTING:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.adapter.action.CONNECTION_STATE_CHANGED"

### ACTION_DISCOVERY_FINISHED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DISCOVERY_FINISHED: String
```

Broadcast Action: The local Bluetooth adapter has finished the device discovery process. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

 Value: "android.bluetooth.adapter.action.DISCOVERY_FINISHED"

### ACTION_DISCOVERY_STARTED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_DISCOVERY_STARTED: String
```

Broadcast Action: The local Bluetooth adapter has started the remote device discovery process.

This usually involves an inquiry scan of about 12 seconds, followed by a page scan of each new device to retrieve its Bluetooth name.

Register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` to be notified as remote Bluetooth devices are found.

Device discovery is a heavyweight procedure. New connections to remote Bluetooth devices should not be attempted while discovery is in progress, and existing connections will experience limited bandwidth and high latency. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery()` to cancel an ongoing discovery. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

 Value: "android.bluetooth.adapter.action.DISCOVERY_STARTED"

### ACTION_LOCAL_NAME_CHANGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LOCAL_NAME_CHANGED: String
```

Broadcast Action: The local Bluetooth adapter has changed its friendly Bluetooth name.

This name is visible to remote Bluetooth devices.

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_LOCAL_NAME:kotlin.String` containing the name. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.adapter.action.LOCAL_NAME_CHANGED"

### ACTION_REQUEST_DISCOVERABLE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_DISCOVERABLE: String
```

Activity Action: Show a system activity that requests discoverable mode. This activity will also request the user to turn on Bluetooth if it is not currently enabled.

Discoverable mode is equivalent to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int`. It allows remote devices to see this Bluetooth adapter when they perform a discovery.

For privacy, Android is not discoverable by default.

The sender of this Intent can optionally use extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_DISCOVERABLE_DURATION:kotlin.String` to request the duration of discoverability. Currently the default duration is 120 seconds, and maximum duration is capped at 300 seconds for each request.

Notification of the result of this activity is posted using the android.app.Activity#onActivityResult callback. The `resultCode` will be the duration (in seconds) of discoverability or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` if the user rejected discoverability or an error has occurred.

Applications can also listen for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_SCAN_MODE_CHANGED:kotlin.String` for global notification whenever the scan mode changes. For example, an application can be notified when the device has ended discoverability. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADVERTISE:kotlin.String`

 Value: "android.bluetooth.adapter.action.REQUEST_DISCOVERABLE"

### ACTION_REQUEST_ENABLE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_REQUEST_ENABLE: String
```

Activity Action: Show a system activity that allows the user to turn on Bluetooth.

This system activity will return once Bluetooth has completed turning on, or the user has decided not to turn Bluetooth on.

Notification of the result of this activity is posted using the android.app.Activity#onActivityResult callback. The `resultCode` will be `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` if Bluetooth has been turned on or `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` if the user has rejected the request or an error has occurred.

Applications can also listen for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` for global notification whenever Bluetooth is turned on or off. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.adapter.action.REQUEST_ENABLE"

### ACTION_SCAN_MODE_CHANGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_SCAN_MODE_CHANGED: String
```

Broadcast Action: Indicates the Bluetooth scan mode of the local Adapter has changed.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_SCAN_MODE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_SCAN_MODE:kotlin.String` containing the new and old scan modes respectively. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

 Value: "android.bluetooth.adapter.action.SCAN_MODE_CHANGED"

### ACTION_STATE_CHANGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_STATE_CHANGED: String
```

Broadcast Action: The state of the local Bluetooth adapter has been changed.

For example, Bluetooth has been turned on or off.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_STATE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#EXTRA_PREVIOUS_STATE:kotlin.String` containing the new and old states respectively. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

 Value: "android.bluetooth.adapter.action.STATE_CHANGED"

### ERROR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR: Int
```

Sentinel error value for this class. Guaranteed to not equal any other integer constant in this class. Provided as a convenience for functions that require a sentinel error value, for example:

`Intent.getIntExtra(BluetoothAdapter.EXTRA_STATE, BluetoothAdapter.ERROR)`

 Value: -2147483648

### EXTRA_CONNECTION_STATE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CONNECTION_STATE: String
```

Extra used by `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_CONNECTION_STATE_CHANGED:kotlin.String`

This extra represents the current connection state.

 Value: "android.bluetooth.adapter.extra.CONNECTION_STATE"

### EXTRA_DISCOVERABLE_DURATION

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISCOVERABLE_DURATION: String
```

Used as an optional int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_REQUEST_DISCOVERABLE:kotlin.String` intents to request a specific duration for discoverability in seconds. The current default is 120 seconds, and requests over 300 seconds will be capped. These values could change.

 Value: "android.bluetooth.adapter.extra.DISCOVERABLE_DURATION"

### EXTRA_LOCAL_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LOCAL_NAME: String
```

Used as a String extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_LOCAL_NAME_CHANGED:kotlin.String` intents to request the local Bluetooth name.

 Value: "android.bluetooth.adapter.extra.LOCAL_NAME"

### EXTRA_PREVIOUS_CONNECTION_STATE

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREVIOUS_CONNECTION_STATE: String
```

Extra used by `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_CONNECTION_STATE_CHANGED:kotlin.String`

This extra represents the previous connection state.

 Value: "android.bluetooth.adapter.extra.PREVIOUS_CONNECTION_STATE"

### EXTRA_PREVIOUS_SCAN_MODE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREVIOUS_SCAN_MODE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_SCAN_MODE_CHANGED:kotlin.String` intents to request the previous scan mode. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int`,

 Value: "android.bluetooth.adapter.extra.PREVIOUS_SCAN_MODE"

### EXTRA_PREVIOUS_STATE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREVIOUS_STATE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` intents to request the previous power state. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_OFF:kotlin.Int`

 Value: "android.bluetooth.adapter.extra.PREVIOUS_STATE"

### EXTRA_SCAN_MODE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_SCAN_MODE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_SCAN_MODE_CHANGED:kotlin.String` intents to request the current scan mode. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int`,

 Value: "android.bluetooth.adapter.extra.SCAN_MODE"

### EXTRA_STATE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_STATE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` intents to request the current power state. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_OFF:kotlin.Int`,

 Value: "android.bluetooth.adapter.extra.STATE"

### SCAN_MODE_CONNECTABLE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCAN_MODE_CONNECTABLE: Int
```

Indicates that inquiry scan is disabled, but page scan is enabled on the local Bluetooth adapter. Therefore this device is not discoverable from remote Bluetooth devices, but is connectable from remote devices that have previously discovered this device.

 Value: 21

### SCAN_MODE_CONNECTABLE_DISCOVERABLE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCAN_MODE_CONNECTABLE_DISCOVERABLE: Int
```

Indicates that both inquiry scan and page scan are enabled on the local Bluetooth adapter. Therefore this device is both discoverable and connectable from remote Bluetooth devices.

 Value: 23

### SCAN_MODE_NONE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val SCAN_MODE_NONE: Int
```

Indicates that both inquiry scan and page scan are disabled on the local Bluetooth adapter. Therefore this device is neither discoverable nor connectable from remote Bluetooth devices.

 Value: 20

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

### STATE_OFF

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_OFF: Int
```

Indicates the local Bluetooth adapter is off.

 Value: 10

### STATE_ON

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_ON: Int
```

Indicates the local Bluetooth adapter is on, and ready for use.

 Value: 12

### STATE_TURNING_OFF

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TURNING_OFF: Int
```

Indicates the local Bluetooth adapter is turning off. Local clients should immediately attempt graceful disconnection of any remote links.

 Value: 13

### STATE_TURNING_ON

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val STATE_TURNING_ON: Int
```

Indicates the local Bluetooth adapter is turning on. However local clients should wait for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` before attempting to use the adapter.

 Value: 11

## Public methods

### cancelDiscovery

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancelDiscovery(): Boolean
```

Cancel the current device discovery process.

Because discovery is a heavyweight procedure for the Bluetooth adapter, this method should always be called before attempting to connect to a remote device with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect()`. Discovery is not managed by the Activity, but is run as a system service, so an application should always call cancel discovery even if it did not directly request a discovery, just to be sure.

If Bluetooth state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, this API will return false. After turning on Bluetooth, wait for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` to get the updated value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on error |

### checkBluetoothAddress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun checkBluetoothAddress(address: String!): Boolean
```

Validate a String Bluetooth address, such as "00:43:A8:23:10:F0"

Alphabetic characters must be uppercase to be valid.

| Parameters ||
|---|---|
| `address` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: Bluetooth address as string |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the address is valid, false otherwise |

### closeProfileProxy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun closeProfileProxy(
    unusedProfile: Int, 
    proxy: BluetoothProfile!
): Unit
```

Close the connection of the profile proxy to the Service.

Clients should call this when they are no longer using the proxy obtained from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getProfileProxy(android.content.Context,%20android.bluetooth.BluetoothProfile.ServiceListener,%20kotlin.Int)`. Profile can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int`

| Parameters ||
|---|---|
| `proxy` | [BluetoothProfile](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile)!: Profile proxy object |

### disable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disable(): Boolean
```

**Deprecated:** *Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, applications are not allowed to enable/disable Bluetooth. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or above, this API will always fail and return `false`. If apps are targeting an older SDK (`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or below), they can continue to use this API.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Turn off the local Bluetooth adapter---do not use without explicit user action to turn off Bluetooth.

This gracefully shuts down all Bluetooth connections, stops Bluetooth system services, and powers down the underlying Bluetooth hardware.

**Bluetooth should never be disabled without direct user consent** . The `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#disable()` method is provided only for applications that include a user interface for changing system settings, such as a "power manager" app.

This is an asynchronous call: it will return immediately, and clients should listen for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` to be notified of subsequent adapter state changes. If this call returns true, then the adapter state will immediately transition from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_OFF:kotlin.Int`, and some time later transition to either `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`. If this call returns false then there was an immediate problem that will prevent the adapter from being turned off - such as the adapter already being turned off. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true to indicate adapter shutdown has begun, or false on immediate error |

### enable

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun enable(): Boolean
```

**Deprecated:** *Starting with `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int`, applications are not allowed to enable/disable Bluetooth. **Compatibility Note:** For applications targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#TIRAMISU:kotlin.Int` or above, this API will always fail and return `false`. If apps are targeting an older SDK (`https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or below), they can continue to use this API.*

*Deprecation Exemptions:*
*- Device Owner (DO), Profile Owner (PO) and system apps.*

<br />

Turn on the local Bluetooth adapter---do not use without explicit user action to turn on Bluetooth.

This powers on the underlying Bluetooth hardware, and starts all Bluetooth system services.

**Bluetooth should never be enabled without direct user consent** . If you want to turn on Bluetooth in order to create a wireless connection, you should use the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_REQUEST_ENABLE:kotlin.String` Intent, which will raise a dialog that requests user permission to turn on Bluetooth. The `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#enable()` method is provided only for applications that include a user interface for changing system settings, such as a "power manager" app.

This is an asynchronous call: it will return immediately, and clients should listen for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` to be notified of subsequent adapter state changes. If this call returns true, then the adapter state will immediately transition from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int` to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_ON:kotlin.Int`, and some time later transition to either `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`. If this call returns false then there was an immediate problem that will prevent the adapter from being turned on - such as Airplane mode, or the adapter is already turned on. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true to indicate adapter startup has begun, or false on immediate error |

### getAddress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): String!
```

Returns the hardware address of the local Bluetooth adapter.

For example, "00:11:22:AA:BB:CC". 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` and android.Manifest.permission#LOCAL_MAC_ADDRESS

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Bluetooth hardware address as string |

### getBluetoothLeAdvertiser

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBluetoothLeAdvertiser(): BluetoothLeAdvertiser?
```

Returns a `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeAdvertiser` object for Bluetooth LE Advertising operations. Will return null if Bluetooth is turned off or if Bluetooth LE Advertising is not supported on this device.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isEnabled()` to check if Bluetooth is currently enabled. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isMultipleAdvertisementSupported()` to check whether LE Advertising is supported on this device before calling this method.

### getBluetoothLeScanner

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBluetoothLeScanner(): BluetoothLeScanner?
```

Returns a `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner` object for Bluetooth LE scan operations. Will return null if Bluetooth is turned off.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#isEnabled()` to check if Bluetooth is currently enabled.

### getBondedDevices

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBondedDevices(): MutableSet<BluetoothDevice!>!
```

Return the set of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` objects that are bonded (paired) to the local adapter.

If Bluetooth state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, this API will return an empty set. After turning on Bluetooth, wait for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` to get the updated value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice!>!` | unmodifiable set of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` |

### getDefaultAdapter

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static fun getDefaultAdapter(): BluetoothAdapter!
```

**Deprecated:** *Use `context.getSystemService(BluetoothManager.class).getAdapter()` instead to allows context override such as `https://developer.android.com/reference/kotlin/android/content/Context.html#createAttributionContext(kotlin.String)` or android.content.Context#createContextAsUser.*

Get a handle to the default local Bluetooth adapter.

Currently Android only supports one Bluetooth adapter, but the API could be extended to support more. This will always return the default adapter.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#!` | the default local adapter, or null if Bluetooth is not supported on this hardware platform |

### getDiscoverableTimeout

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getDiscoverableTimeout(): Duration?
```

Get the timeout duration of the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Duration.html#?` | the duration of the discoverable timeout or null if an error has occurred |

### getLeMaximumAdvertisingDataLength

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeMaximumAdvertisingDataLength(): Int
```

Return the maximum LE advertising data length in bytes, if LE Extended Advertising feature is supported, 0 otherwise. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the maximum LE advertising data length. |

### getMaxConnectedAudioDevices

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMaxConnectedAudioDevices(): Int
```

Get the maximum number of connected devices per audio profile for this device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the number of allowed simultaneous connected devices for each audio profile for this device, or -1 if the Bluetooth service can't be reached |

### getName

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

Get the friendly Bluetooth name of the local Bluetooth adapter.

This name is visible to remote Bluetooth devices. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the Bluetooth name, or null on error |

### getProfileConnectionState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProfileConnectionState(profile: Int): Int
```

Get the current connection state of a profile. This function can be used to check whether the local Bluetooth adapter is connected to any remote device for a specific profile. Profile can be one of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#HEADSET:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile#A2DP:kotlin.Int`.

Return the profile connection state. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_DISCONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_CONNECTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_CONNECTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_DISCONNECTING:kotlin.Int` |

### getProfileProxy

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getProfileProxy(
    context: Context!, 
    listener: BluetoothProfile.ServiceListener!, 
    profile: Int
): Boolean
```

Get the profile proxy object associated with the profile.

The ServiceListener's methods will be invoked on the application's main looper

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: Context of the application |
| `listener` | [BluetoothProfile.ServiceListener](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothProfile.ServiceListener)!: The service listener for connection callbacks. |
| `profile` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The Bluetooth profile to listen for status change |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on error |

### getRemoteDevice

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRemoteDevice(address: ByteArray!): BluetoothDevice!
```

Get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` object for the given Bluetooth hardware address.

Valid Bluetooth hardware addresses must be 6 bytes. This method expects the address in network byte order (MSB first).

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` will always be returned for a valid hardware address, even if this adapter has never seen that device.

| Parameters ||
|---|---|
| `address` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!: Bluetooth MAC address (6 bytes) |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if address is invalid |

### getRemoteDevice

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRemoteDevice(address: String!): BluetoothDevice!
```

Get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` object for the given Bluetooth hardware address.

Valid Bluetooth hardware addresses must be upper case, in big endian byte order, and in a format such as "00:11:22:33:AA:BB". The helper `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#checkBluetoothAddress(kotlin.String)` is available to validate a Bluetooth address.

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` will always be returned for a valid hardware address, even if this adapter has never seen that device.

| Parameters ||
|---|---|
| `address` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: valid Bluetooth MAC address |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if address is invalid |

### getRemoteLeDevice

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getRemoteLeDevice(
    address: String, 
    addressType: Int
): BluetoothDevice
```

Get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` object for the given Bluetooth hardware address and addressType.

Valid Bluetooth hardware addresses must be upper case, in big endian byte order, and in a format such as "00:11:22:33:AA:BB". The helper `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#checkBluetoothAddress(kotlin.String)` is available to validate a Bluetooth address.

A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` will always be returned for a valid hardware address and type, even if this adapter has never seen that device.

| Parameters ||
|---|---|
| `address` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): valid Bluetooth MAC address. This value cannot be `null`. |
| `addressType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Bluetooth address type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_PUBLIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_RANDOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_ANONYMOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_UNKNOWN:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if address is invalid |

### getScanMode

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getScanMode(): Int
```

Get the current Bluetooth scan mode of the local Bluetooth adapter.

The Bluetooth scan mode determines if the local adapter is connectable and/or discoverable from remote Bluetooth devices.

Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int`.

If Bluetooth state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, this API will return `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_NONE:kotlin.Int`. After turning on Bluetooth, wait for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` to get the updated value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | scan mode. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_NONE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#SCAN_MODE_CONNECTABLE_DISCOVERABLE:kotlin.Int` |

### getState

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getState(): Int
```

Get the current state of the local Bluetooth adapter.

Possible return values are `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_OFF:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | current state of Bluetooth adapter. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_OFF:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_TURNING_OFF:kotlin.Int` |

### isDiscovering

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isDiscovering(): Boolean
```

Return true if the local Bluetooth adapter is currently in the device discovery process.

Device discovery is a heavyweight procedure. New connections to remote Bluetooth devices should not be attempted while discovery is in progress, and existing connections will experience limited bandwidth and high latency. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery()` to cancel an ongoing discovery.

Applications can also register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_DISCOVERY_STARTED:kotlin.String` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_DISCOVERY_FINISHED:kotlin.String` to be notified when discovery starts or completes.

If Bluetooth state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, this API will return false. After turning on Bluetooth, wait for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` to get the updated value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if discovering |

### isEnabled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isEnabled(): Boolean
```

Return true if Bluetooth is currently enabled and ready for use.

Equivalent to: `getBluetoothState() == STATE_ON`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the local adapter is turned on |

### isLe2MPhySupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLe2MPhySupported(): Boolean
```

Return true if LE 2M PHY feature is supported. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if chipset supports LE 2M PHY feature |

### isLeAudioBroadcastAssistantSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeAudioBroadcastAssistantSupported(): Int
```

Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` if the LE audio broadcast assistant feature is supported, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` if the feature is not supported, or an error code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | whether the LE audio broadcast assistant is supported. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` |

### isLeAudioBroadcastSourceSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeAudioBroadcastSourceSupported(): Int
```

Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` if the LE audio broadcast source feature is supported, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` if the feature is not supported, or an error code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | whether the LE audio broadcast source is supported. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` |

### isLeAudioSupported

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeAudioSupported(): Int
```

Returns `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` if the LE audio feature is supported, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` if the feature is not supported, or an error code.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | whether the LE audio is supported. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` |

### isLeCodedPhySupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeCodedPhySupported(): Boolean
```

Return true if LE Coded PHY feature is supported. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if chipset supports LE Coded PHY feature |

### isLeExtendedAdvertisingSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeExtendedAdvertisingSupported(): Boolean
```

Return true if LE Extended Advertising feature is supported. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if chipset supports LE Extended Advertising feature |

### isLeHighDataThroughputPhySupported

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLeHighDataThroughputPhySupported(): Int
```

Checks if LE High Data Throughput (HDT) PHY is supported.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the support status of the feature. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_SUPPORTED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#FEATURE_NOT_SUPPORTED:kotlin.Int` |

### isLePeriodicAdvertisingSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isLePeriodicAdvertisingSupported(): Boolean
```

Return true if LE Periodic Advertising feature is supported. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if chipset supports LE Periodic Advertising feature |

### isMultipleAdvertisementSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isMultipleAdvertisementSupported(): Boolean
```

Return true if the multi advertisement is supported by the chipset. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if Multiple Advertisement feature is supported |

### isOffloadedFilteringSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOffloadedFilteringSupported(): Boolean
```

Return true if offloaded filters are supported. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if chipset supports on-chip filtering |

### isOffloadedScanBatchingSupported

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isOffloadedScanBatchingSupported(): Boolean
```

Return true if offloaded scan batching is supported. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if chipset supports on-chip scan batching |

### listenUsingInsecureL2capChannel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun listenUsingInsecureL2capChannel(): BluetoothServerSocket
```

Create an insecure L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` and assign a dynamic PSM value. This socket can be used to listen for incoming connections. The supported Bluetooth transport is LE only.

The link key is not required to be authenticated, i.e. the communication may be vulnerable to person-in-the-middle attacks. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()`, if an encrypted and authenticated communication channel is desired.

Use android.bluetooth.BluetoothServerSocket#accept to retrieve incoming connections from a listening `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket`.

The system will assign a dynamic protocol/service multiplexer (PSM) value. This PSM value can be read from the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#getPsm()` and this value will be released when this server socket is closed, Bluetooth is turned off, or the application exits unexpectedly.

The mechanism of disclosing the assigned dynamic PSM value to the initiating peer is defined and performed by the application.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createInsecureL2capChannel(kotlin.Int)` to connect to this server socket from another Android device that is given the PSM value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` | an L2CAP CoC BluetoothServerSocket. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available or unable to start this CoC |

### listenUsingInsecureRfcommWithServiceRecord

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun listenUsingInsecureRfcommWithServiceRecord(
    name: String!, 
    uuid: UUID!
): BluetoothServerSocket!
```

Create a listening, insecure RFCOMM Bluetooth socket with Service Record.

The link key is not required to be authenticated, i.e. the communication may be vulnerable to Person In the Middle attacks. For Bluetooth 2.1 devices, the link will be encrypted, as encryption is mandatory. For legacy devices (pre Bluetooth 2.1 devices) the link will not be encrypted. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)`, if an encrypted and authenticated communication channel is desired.

Use android.bluetooth.BluetoothServerSocket#accept to retrieve incoming connections from a listening `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket`.

The system will assign an unused RFCOMM channel to listen on.

The system will also register a Service Discovery Protocol (SDP) record with the local SDP server containing the specified UUID, service name, and auto-assigned channel. Remote Bluetooth devices can use the same UUID to query our SDP server and discover which channel to connect to. This SDP record will be removed when this socket is closed, or if this application closes unexpectedly.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createInsecureRfcommSocketToServiceRecord(java.util.UUID)` to connect to this socket from another device using the same `https://developer.android.com/reference/kotlin/java/util/UUID.html#`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: service name for SDP record |
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!: uuid for SDP record |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket!` | a listening RFCOMM BluetoothServerSocket |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available, or insufficient permissions, or channel in use. |

### listenUsingL2capChannel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun listenUsingL2capChannel(): BluetoothServerSocket
```

Create a secure L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` and assign a dynamic protocol/service multiplexer (PSM) value. This socket can be used to listen for incoming connections. The supported Bluetooth transport is LE only.

A remote device connecting to this socket will be authenticated and communication on this socket will be encrypted.

Use android.bluetooth.BluetoothServerSocket#accept to retrieve incoming connections from a listening `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket`.

The system will assign a dynamic PSM value. This PSM value can be read from the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#getPsm()` and this value will be released when this server socket is closed, Bluetooth is turned off, or the application exits unexpectedly.

The mechanism of disclosing the assigned dynamic PSM value to the initiating peer is defined and performed by the application.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)` to connect to this server socket from another Android device that is given the PSM value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` | an L2CAP CoC BluetoothServerSocket. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available or unable to start this CoC |

### listenUsingRfcommWithServiceRecord

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun listenUsingRfcommWithServiceRecord(
    name: String!, 
    uuid: UUID!
): BluetoothServerSocket!
```

Create a listening, secure RFCOMM Bluetooth socket with Service Record.

A remote device connecting to this socket will be authenticated and communication on this socket will be encrypted.

Use android.bluetooth.BluetoothServerSocket#accept to retrieve incoming connections from a listening `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket`.

The system will assign an unused RFCOMM channel to listen on.

The system will also register a Service Discovery Protocol (SDP) record with the local SDP server containing the specified UUID, service name, and auto-assigned channel. Remote Bluetooth devices can use the same UUID to query our SDP server and discover which channel to connect to. This SDP record will be removed when this socket is closed, or if this application closes unexpectedly.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createRfcommSocketToServiceRecord(java.util.UUID)` to connect to this socket from another device using the same `https://developer.android.com/reference/kotlin/java/util/UUID.html#`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: service name for SDP record |
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!: uuid for SDP record |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket!` | a listening RFCOMM BluetoothServerSocket |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available, or insufficient permissions, or channel in use. |

### listenUsingSocketSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun listenUsingSocketSettings(settings: BluetoothSocketSettings): BluetoothServerSocket
```

Creates a listening server channel for Bluetooth connections with the specified socket settings `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings`.

Use android.bluetooth.BluetoothServerSocket#accept to retrieve incoming connections from a listening `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket`.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createUsingSocketSettings(android.bluetooth.BluetoothSocketSettings)` to connect to this server socket from another Android device using the L2cap protocol/service multiplexer(PSM) value or the RFCOMM service UUID as input.

This API requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` permission only when `settings.getDataPath()` is different from android.bluetooth.BluetoothSocketSettings#DATA_PATH_NO_OFFLOAD.

This API supports `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_RFCOMM:kotlin.Int` and {`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#TYPE_LE:kotlin.Int` only, which can be set using android.bluetooth.BluetoothSocketSettings#setSocketType().
- For \`BluetoothSocket.TYPE_RFCOMM\`: The RFCOMM UUID must be provided using android.bluetooth.BluetoothSocketSettings#setRfcommUuid().
- For \`BluetoothSocket.TYPE_LE\`: The system assigns a dynamic protocol/service multiplexer (PSM) value. This value can be read from `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket#getPsm()`. This value is released when the server socket is closed, Bluetooth is turned off, or the application exits unexpectedly. The mechanism for disclosing the PSM value to the client is application-defined.
- For \`BluetoothSocket.TYPE_LE\`: It is possible for a privileged application to host the L2cap server on a designated PSM channel. This is intended for peripheral devices that reserve a range of PSM values to be used to host dedicated L2cap socket servers. 
 For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `settings` | [BluetoothSocketSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings): Bluetooth socket settings `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` | a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothServerSocket` This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available or unable to start this LE Connection-oriented Channel (CoC). |
| `java.lang.IllegalArgumentException` | if BluetoothSocket#TYPE_RFCOMM socket is requested with no UUID. |

### setName

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setName(name: String!): Boolean
```

Set the friendly Bluetooth name of the local Bluetooth adapter.

This name is visible to remote Bluetooth devices.

Valid Bluetooth names are a maximum of 248 bytes using UTF-8 encoding(see \[Vol 2\] Part C, Section 4.3.5), although many remote devices can only display the first 40 characters, and some may be limited to just 20.

Note: The factory name is the result of

1. System property 'bluetooth.device.default_name'
2. Settings.Global.DEVICE_NAME
3. System property 'ro.product.model'
4. Hardcoded value 'Android'

. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: a valid Bluetooth name or null to reset to factory default |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true |

### startDiscovery

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startDiscovery(): Boolean
```

Start the remote device discovery process.

The discovery process usually involves an inquiry scan of about 12 seconds, followed by a page scan of each new device to retrieve its Bluetooth name. If BLE is supported, a simultaneous LE scan runs until discovery ends.

This is an asynchronous call, it will return immediately. Register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_DISCOVERY_STARTED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_DISCOVERY_FINISHED:kotlin.String` intents to determine exactly when the discovery starts and completes. Register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` to be notified as remote Bluetooth devices are found.

Device discovery is a heavyweight procedure. New connections to remote Bluetooth devices should not be attempted while discovery is in progress, and existing connections will experience limited bandwidth and high latency. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery()` to cancel an ongoing discovery. Discovery is not managed by the Activity, but is run as a system service, so an application should always call `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#cancelDiscovery()` even if it did not directly request a discovery, just to be sure.

Device discovery will only find remote devices that are currently *discoverable* (inquiry scan enabled). Many Bluetooth devices are not discoverable by default, and need to be entered into a special mode.

If Bluetooth state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`, this API will return false. After turning on Bluetooth, wait for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#ACTION_STATE_CHANGED:kotlin.String` with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int` to get the updated value.

If a device is currently bonding, this request will be queued and executed once that device has finished bonding. If a request is already queued, this request will be ignored. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on error |

### startLeScan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startLeScan(callback: BluetoothAdapter.LeScanCallback!): Boolean
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(kotlin.collections.MutableList,%20android.bluetooth.le.ScanSettings,%20android.bluetooth.le.ScanCallback)` instead.*

Starts a scan for Bluetooth LE devices.

Results of the scan are reported using the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback#onLeScan(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.ByteArray)` callback.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission. Additionally, an app must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` if it is used for BLE scan only mode (when the adapter state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with.

| Parameters ||
|---|---|
| `callback` | [BluetoothAdapter.LeScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback)!: the callback LE scan results are delivered |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the scan was started successfully |

### startLeScan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun startLeScan(
    serviceUuids: Array<UUID!>!, 
    callback: BluetoothAdapter.LeScanCallback!
): Boolean
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#startScan(kotlin.collections.MutableList,%20android.bluetooth.le.ScanSettings,%20android.bluetooth.le.ScanCallback)` instead.*

Starts a scan for Bluetooth LE devices, looking for devices that advertise given services.

Devices which advertise all specified services are reported using the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback#onLeScan(android.bluetooth.BluetoothDevice,%20kotlin.Int,%20kotlin.ByteArray)` callback.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission. Additionally, an app must have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` if it is used for BLE scan only mode (when the adapter state is not `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#STATE_ON:kotlin.Int`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with.

| Parameters ||
|---|---|
| `serviceUuids` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!\>!: Array of services to look for |
| `callback` | [BluetoothAdapter.LeScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback)!: the callback LE scan results are delivered |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true, if the scan was started successfully |

### stopLeScan

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun stopLeScan(callback: BluetoothAdapter.LeScanCallback!): Unit
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/le/BluetoothLeScanner#stopScan(android.bluetooth.le.ScanCallback)` instead.*

Stops an ongoing Bluetooth LE device scan. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

| Parameters ||
|---|---|
| `callback` | [BluetoothAdapter.LeScanCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter.LeScanCallback)!: used to identify which scan to stop must be the same handle used to start the scan |

## Protected methods

### finalize

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |
