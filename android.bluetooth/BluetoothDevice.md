Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BluetoothDevice

```
class BluetoothDevice : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.bluetooth.BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#) |

Represents a remote Bluetooth device. A `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#` lets you create a connection with the respective device or query information about it, such as the name, address, class, and bonding state.

This class is really just a thin wrapper for a Bluetooth hardware address. Objects of this class are immutable. Operations on this class are performed on the remote Bluetooth hardware address, using the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter` that was used to create this `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#`.

To get a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#`, use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getRemoteDevice(kotlin.String)` to create one representing a device of a known MAC address (which you can get through device discovery with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter`) or get one from the set of bonded devices returned by `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#getBondedDevices()`. You can then open a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` for communication with the remote device, using `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createRfcommSocketToServiceRecord(java.util.UUID)` over Bluetooth BR/EDR or using `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)` over Bluetooth LE.

<br />

> [!NOTE]
>
> ### Developer Guides
>
> For more information about using Bluetooth, read the [Bluetooth](https://developer.android.com/guide/topics/connectivity/bluetooth.html) developer guide.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.BluetoothAddress` A data class for Bluetooth address and address type. |

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_CONNECTED:kotlin.String` Broadcast Action: Indicates a low level (ACL) connection has been established with a remote device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_DISCONNECTED:kotlin.String` Broadcast Action: Indicates a low level (ACL) disconnection from a remote device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_DISCONNECT_REQUESTED:kotlin.String` Broadcast Action: Indicates that a low level (ACL) disconnection has been requested for a remote device, and it will soon be disconnected. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ALIAS_CHANGED:kotlin.String` Broadcast Action: Indicates the alias of a remote device has been changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` Broadcast Action: Indicates a change in the bond state of a remote device. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_CLASS_CHANGED:kotlin.String` Broadcast Action: Bluetooth class of a remote device has changed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` Broadcast Action: Indicates that encryption state changed |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` Broadcast Action: Remote device discovered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_KEY_MISSING:kotlin.String` Broadcast Action: Indicates that previously bonded device couldn't provide keys to establish encryption. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_LE_APPEARANCE_CHANGED:kotlin.String` This intent will be broadcasted for bonded devices after LE connection is established, if the LE Appearance value was not known already or changed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_NAME_CHANGED:kotlin.String` Broadcast Action: Indicates the friendly name of a remote device has been retrieved for the first time, or changed since the last retrieval. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` Broadcast Action: This intent is used to broadcast a PAIRING REQUEST. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_UUID:kotlin.String` Broadcast Action: This intent is used to broadcast the `https://developer.android.com/reference/kotlin/java/util/UUID.html#` wrapped as a `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#` of the remote device after it has been fetched. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_ANONYMOUS:kotlin.Int` Address type used to indicate an anonymous advertisement. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_PUBLIC:kotlin.Int` Hardware MAC Address of the device |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_RANDOM:kotlin.Int` Address is either resolvable, non-resolvable or static. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_UNKNOWN:kotlin.Int` Address type is unknown or unavailable |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDED:kotlin.Int` Indicates the remote device is bonded (paired). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDING:kotlin.Int` Indicates bonding (pairing) is in progress with the remote device. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_BREDR_AUTH_FAILURE:kotlin.Int` Indicates the reason for the bond loss is BREDR authentication failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_BREDR_INCOMING_PAIRING:kotlin.Int` Indicates the reason for the bond loss is BREDR pairing failure. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_LE_ENCRYPT_FAILURE:kotlin.Int` Indicates the reason for the bond loss is LE encryption failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_LE_INCOMING_PAIRING:kotlin.Int` Indicates the reason for the bond loss is LE pairing failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_UNKNOWN:kotlin.Int` Indicates the reason for the bond loss is unknown. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_NONE:kotlin.Int` Indicates the remote device is not bonded (paired). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_CLASSIC:kotlin.Int` Bluetooth device type, Classic - BR/EDR devices |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_DUAL:kotlin.Int` Bluetooth device type, Dual Mode - BR/EDR/LE |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_LE:kotlin.Int` Bluetooth device type, Low Energy - LE-only |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_UNKNOWN:kotlin.Int` Bluetooth device type, Unknown |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_AES:kotlin.Int` Indicates link was encrypted using AES algorithm |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_E0:kotlin.Int` Indicates link was encrypted using E0 algorithm |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_NONE:kotlin.Int` Indicates that link was not encrypted using any algorithm |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN:kotlin.Int` Indicates link was encrypted using unknown algorithm |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ERROR:kotlin.Int` Sentinel error value for this class. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_BOND_LOSS_REASON:kotlin.String` Contains the reason for the bond loss. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_BOND_STATE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_CLASS:kotlin.String` Used as a Parcelable `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass` extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_CLASS_CHANGED:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` Used as a Parcelable `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#` extra field in every intent broadcast by this class. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DISCOVERY_RESULT_TYPE:kotlin.String` Used as an integer field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_ENCRYPTION_ALGORITHM:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intents as the algorithm used for encryption. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_ENCRYPTION_ENABLED:kotlin.String` Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intent. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_ENCRYPTION_STATUS:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intent. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_IS_COORDINATED_SET_MEMBER:kotlin.String` Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_KEY_SIZE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intents as the size of the encryption key, in number of bytes. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` Used as an integer extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_LE_APPEARANCE_CHANGED:kotlin.String` intents, and in `ACTION_*_CONNECTION_STATE_CHANGED` intents for audio related profiles. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_NAME:kotlin.String` Used as a String extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_NAME_CHANGED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_ALGORITHM:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` intents which indicates the pairing algorithm used. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_CONTEXT:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents which indicates the pairing context. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_KEY:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` intents as the value of passkey. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_VARIANT:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` intents to indicate pairing method used. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PREVIOUS_BOND_STATE:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_RSSI:kotlin.String` Used as an optional short extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_TRANSPORT:kotlin.String` Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_CONNECTED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_DISCONNECTED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intents to indicate which transport is connected. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` Contains the `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#`s of the remote device which is a parcelable version of `https://developer.android.com/reference/kotlin/java/util/UUID.html#`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID_LE:kotlin.String` Contains the `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#`s of the remote device which is a parcelable version of `https://developer.android.com/reference/kotlin/java/util/UUID.html#`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#LE_APPEARANCE_UNKNOWN:kotlin.Int` Value indicating that the LE Appearance of the device is unknown. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_BREDR_LEGACY:kotlin.Int` Indicates usage of the BR/EDR Legacy pairing algorithm. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_BREDR_SSP:kotlin.Int` Indicates usage of the BR/EDR Secure Simple Pairing (SSP) algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_LE_LEGACY:kotlin.Int` Indicates usage of the LE Legacy pairing algorithm. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_SC:kotlin.Int` Indicates usage of the Secure Connections pairing algorithm, applicable to both BR/EDR and LE transports. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_REPAIRING:kotlin.Int` Signals an autonomous, system-initiated re-pairing process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_USER_APPROVAL_REQUESTED:kotlin.Int` Indicates that the pairing process is initiated, and user approval is requested to complete the pairing process. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_USER_PARTICIPATION_REQUESTED:kotlin.Int` Signals a request for user participation to begin the LE Legacy pairing process. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PASSKEY_CONFIRMATION:kotlin.Int` The user will be prompted to confirm the passkey displayed on the screen or an app will confirm the passkey for the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PIN:kotlin.Int` The user will be prompted to enter a pin or an app will enter a pin for user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M:kotlin.Int` Bluetooth LE 1M PHY. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int` Bluetooth LE 1M PHY mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M:kotlin.Int` Bluetooth LE 2M PHY. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int` Bluetooth LE 2M PHY mask. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED:kotlin.Int` Bluetooth LE Coded PHY. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int` Bluetooth LE Coded PHY mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT:kotlin.Int` Bluetooth LE HDT PHY. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_HDT_MASK:kotlin.Int` Bluetooth LE HDT PHY mask. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_NO_PREFERRED:kotlin.Int` No preferred coding when transmitting on the LE Coded PHY. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_S2:kotlin.Int` Prefer the S=2 coding to be used when transmitting on the LE Coded PHY. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_OPTION_S8:kotlin.Int` Prefer the S=8 coding to be used when transmitting on the LE Coded PHY. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` No preference of physical transport for GATT connections to remote dual-mode devices |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` Constant representing the BR/EDR transport. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` Constant representing the Bluetooth Low Energy (BLE) Transport. |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

| Public methods ||
|---|---|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#cancelBondProcess()()` Cancel an in-progress bonding request started with #createBond. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connect()()` Connects all user enabled and supported bluetooth profiles between the local and remote device. |
| [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.bluetooth.BluetoothGattConnectionSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothGattCallback)(gattConnectionSettings: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattConnectionSettings, executor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback)` Connect to the GATT Server hosted by the given device. |
| --- | --- |
| [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.content.Context,%20kotlin.Boolean,%20android.bluetooth.BluetoothGattCallback)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, autoConnect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback!)` Connect to GATT Server hosted by this device. |
| [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.content.Context,%20kotlin.Boolean,%20android.bluetooth.BluetoothGattCallback,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, autoConnect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback!, transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connect to GATT Server hosted by this device. |
| [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.content.Context,%20kotlin.Boolean,%20android.bluetooth.BluetoothGattCallback,%20kotlin.Int,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, autoConnect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback!, transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, phy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Connect to GATT Server hosted by this device. |
| --- | --- |
| [BluetoothGatt](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.content.Context,%20kotlin.Boolean,%20android.bluetooth.BluetoothGattCallback,%20kotlin.Int,%20kotlin.Int,%20android.os.Handler)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!, autoConnect: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html, callback: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback!, transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, phy: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, handler: https://developer.android.com/reference/kotlin/android/os/Handler.html#!)` Connect to GATT Server hosted by this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createBond()()` Start the bonding (pairing) process with the remote device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createBond(kotlin.Int)(transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Start the bonding (pairing) process with the remote device using the specified transport. |
| --- | --- |
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createInsecureL2capChannel(kotlin.Int)(psm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a Bluetooth L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` that can be used to start a secure outgoing connection to the remote device with the same dynamic protocol/service multiplexer (PSM) value. |
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createInsecureRfcommSocketToServiceRecord(java.util.UUID)(uuid: https://developer.android.com/reference/kotlin/java/util/UUID.html#!)` Create an RFCOMM `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` socket ready to start an insecure outgoing connection to this remote device using SDP lookup of uuid. |
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)(psm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Create a Bluetooth L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` that can be used to start a secure outgoing connection to the remote device with the same dynamic protocol/service multiplexer (PSM) value. |
| --- | --- |
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createRfcommSocketToServiceRecord(java.util.UUID)(uuid: https://developer.android.com/reference/kotlin/java/util/UUID.html#!)` Create an RFCOMM `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` ready to start a secure outgoing connection to this remote device using SDP lookup of uuid. |
| [BluetoothSocket](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createUsingSocketSettings(android.bluetooth.BluetoothSocketSettings)(settings: https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings)` Creates a client socket to connect to a remote Bluetooth server with the specified socket settings `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings` This API is used to connect to a remote server hosted using `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingSocketSettings(android.bluetooth.BluetoothSocketSettings)`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#disconnect()()` Disconnects all connected bluetooth profiles between the local and remote device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#disconnectAcl(kotlin.Int)(transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Disconnects ACL links for this device. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#fetchUuids(kotlin.Int)(transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Performs a service discovery on the remote device to get the UUIDs supported, allowing the caller to specify the transport. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#fetchUuidsWithSdp()()` Performs a service discovery on the remote device to get the UUIDs supported. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getAddress()()` Returns the hardware address of this BluetoothDevice. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getAddressType()()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getAlias()()` Get the locally modifiable name (alias) of the remote Bluetooth device. |
| [BluetoothClass](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getBluetoothClass()()` Get the Bluetooth class of the remote device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getBondState()()` This API returns the bond state of the remote device. |
| [BondStatus](https://developer.android.com/reference/kotlin/android/bluetooth/BondStatus)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getBondStatus(kotlin.Int)(transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the bond status of this device. |
| [EncryptionStatus](https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus)? | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getEncryptionStatus(kotlin.Int)(transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the encryption status of the connected device. |
| --- | --- |
| [BluetoothDevice.BluetoothAddress](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.BluetoothAddress) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getIdentityAddressWithType()()` Returns the identity address and identity address type of this BluetoothDevice. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getKeyMissingCount()()` Get the number of times `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_KEY_MISSING:kotlin.String` intent was thrown for this device since the last successful encrypted connection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getLeAppearance()()` Get the Bluetooth LE Appearance of the remote device. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getName()()` Get the friendly Bluetooth name of the remote device. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getType()()` Get the Bluetooth device type of the remote device. |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [ParcelUuid](https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#)!\>! | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getUuids()()` Returns the supported features (UUIDs) of the remote device. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#hashCode()()` Returns a hash code value for the object. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#isConnected(kotlin.Int)(transport: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns whether there is an open connection to this device on the given transport. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#setAlias(kotlin.String)(alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Sets the locally modifiable name (alias) of the remote Bluetooth device. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#setPairingConfirmation(kotlin.Boolean)(confirm: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Confirm passkey for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PASSKEY_CONFIRMATION:kotlin.Int` pairing. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#setPin(kotlin.ByteArray)(pin: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html!)` Set the pin during pairing when the pairing method is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PIN:kotlin.Int` |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#toString()()` Returns a string representation of this BluetoothDevice. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#writeToParcel(android.os.Parcel,%20kotlin.Int)(out: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [BluetoothDevice](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#)!\> | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#CREATOR:android.os.Parcelable.Creator` <br /> |

## Constants

### ACTION_ACL_CONNECTED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ACL_CONNECTED: String
```

Broadcast Action: Indicates a low level (ACL) connection has been established with a remote device.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_TRANSPORT:kotlin.String`.

ACL connections are managed automatically by the Android Bluetooth stack. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.ACL_CONNECTED"

### ACTION_ACL_DISCONNECTED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ACL_DISCONNECTED: String
```

Broadcast Action: Indicates a low level (ACL) disconnection from a remote device.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_TRANSPORT:kotlin.String`.

ACL connections are managed automatically by the Android Bluetooth stack. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.ACL_DISCONNECTED"

### ACTION_ACL_DISCONNECT_REQUESTED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ACL_DISCONNECT_REQUESTED: String
```

Broadcast Action: Indicates that a low level (ACL) disconnection has been requested for a remote device, and it will soon be disconnected.

This is useful for graceful disconnection. Applications should use this intent as a hint to immediately terminate higher level connections (RFCOMM, L2CAP, or profile connections) to the remote device.

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.ACL_DISCONNECT_REQUESTED"

### ACTION_ALIAS_CHANGED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ALIAS_CHANGED: String
```

Broadcast Action: Indicates the alias of a remote device has been changed.

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.ALIAS_CHANGED"

### ACTION_BOND_STATE_CHANGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_BOND_STATE_CHANGED: String
```

Broadcast Action: Indicates a change in the bond state of a remote device. For example, if a device is bonded (paired).

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_BOND_STATE:kotlin.String`, and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PREVIOUS_BOND_STATE:kotlin.String`. From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_CONTEXT:kotlin.String` will be available. An extra field #EXTRA_UNBOND_REASON will be present, if the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_BOND_STATE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_NONE:kotlin.Int`. From the next SDK release post `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_TRANSPORT:kotlin.String` will be available which indicates the transport(s) for which the new bond state applies. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` will be used if the bond update is applicable for both BREDR and LE transport, while the specific transport will be used if the bond update is applicable for only one of the transports. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.BOND_STATE_CHANGED"

### ACTION_CLASS_CHANGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_CLASS_CHANGED: String
```

Broadcast Action: Bluetooth class of a remote device has changed.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_CLASS:kotlin.String`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.CLASS_CHANGED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass`

### ACTION_ENCRYPTION_CHANGE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_ENCRYPTION_CHANGE: String
```

Broadcast Action: Indicates that encryption state changed

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_TRANSPORT:kotlin.String`

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_ENCRYPTION_STATUS:kotlin.String`

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_ENCRYPTION_ENABLED:kotlin.String`

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_KEY_SIZE:kotlin.String`

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_ENCRYPTION_ALGORITHM:kotlin.String` 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.ENCRYPTION_CHANGE"

### ACTION_FOUND

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_FOUND: String
```

Broadcast Action: Remote device discovered.

Sent when a remote device is found during discovery.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_CLASS:kotlin.String`. Can contain the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_NAME:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_RSSI:kotlin.String` and/or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_IS_COORDINATED_SET_MEMBER:kotlin.String` if they are available.

From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES_FULL.html#BAKLAVA_1:kotlin.Int`, it contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DISCOVERY_RESULT_TYPE:kotlin.String`. Based on the discovery result type, it can contain extra fields for UUIDs:

- If `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DISCOVERY_RESULT_TYPE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_CLASSIC:kotlin.Int`, it can contain `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` for BR/EDR UUIDs.
- If `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DISCOVERY_RESULT_TYPE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_LE:kotlin.Int`, it can contain `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID_LE:kotlin.String` for LE UUIDs and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` for LE appearance.
- If `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DISCOVERY_RESULT_TYPE:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_DUAL:kotlin.Int`, it can contain `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` for BR/EDR UUIDs, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID_LE:kotlin.String` for LE UUIDs and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` for LE appearance.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` includes BR/EDR UUIDs in the extended inquiry response (EIR). A `null` or absent `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` indicates EIR does not include Service Class UUID list. An empty `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` indicates EIR includes Service Class UUID filed, but the list is empty.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID_LE:kotlin.String` includes BLE UUIDs in the BLE advertising data (AD). Specifically, it includes UUIDs present in SERVICE UUID data type and SERVICE DATA data type, as defined by Bluetooth Core Specification Supplement (CSS). A `null` or absent `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID_LE:kotlin.String` indicates the AD does not include Service UUID or Service DATA. An empty `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` indicates AD includes Service UUID and/or Service DATA, but the list is empty.

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` includes the LE Appearance value in the BLE advertising data (AD). Specifically, it includes the appearance data type, as defined by Bluetooth Core Specification Supplement (CSS). An `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#LE_APPEARANCE_UNKNOWN:kotlin.Int` or absent `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` indicates the AD does not include appearance data. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
In addition, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#ACCESS_FINE_LOCATION:kotlin.String` permission. For apps targeting Build.VERSION_CODES#S or higher, an alternative is a strong assertion that you will never derive the physical location of the device, made by declaring `usesPermissionFlags="neverForLocation"` on the relevant `<uses-permission>` manifest tag. However, this assertion may restrict the types of Bluetooth devices you can interact with. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_SCAN:kotlin.String`

 Value: "android.bluetooth.device.action.FOUND"

### ACTION_KEY_MISSING

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_KEY_MISSING: String
```

Broadcast Action: Indicates that previously bonded device couldn't provide keys to establish encryption. This can have numerous reasons, i.e.:

- remote was factory reset, or removed bond
- spoofing attack, someone is impersonating remote device
- in case of LE devices, very unlikely address collision

<br />

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`

From `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int`, it can contain the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_BOND_LOSS_REASON:kotlin.String` which contains the reason for the bond loss. The possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_BREDR_AUTH_FAILURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_BREDR_INCOMING_PAIRING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_LE_ENCRYPT_FAILURE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_LE_INCOMING_PAIRING:kotlin.Int`.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission. Before `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#BAKLAVA:kotlin.Int` this method also required `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String`

 Value: "android.bluetooth.device.action.KEY_MISSING"

### ACTION_LE_APPEARANCE_CHANGED

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_LE_APPEARANCE_CHANGED: String
```

This intent will be broadcasted for bonded devices after LE connection is established, if the LE Appearance value was not known already or changed.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.LE_APPEARANCE_CHANGED"

### ACTION_NAME_CHANGED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_NAME_CHANGED: String
```

Broadcast Action: Indicates the friendly name of a remote device has been retrieved for the first time, or changed since the last retrieval.

Always contains the extra fields `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_NAME:kotlin.String`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.NAME_CHANGED"

### ACTION_PAIRING_REQUEST

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_PAIRING_REQUEST: String
```

Broadcast Action: This intent is used to broadcast a PAIRING REQUEST.

It will contain the following extra fields:

- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_KEY:kotlin.String`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_CONTEXT:kotlin.String`, post `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` only
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_PAIRING_ALGORITHM:kotlin.String`, post `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#CINNAMON_BUN:kotlin.Int` only

. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.PAIRING_REQUEST"

### ACTION_UUID

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_UUID: String
```

Broadcast Action: This intent is used to broadcast the `https://developer.android.com/reference/kotlin/java/util/UUID.html#` wrapped as a `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#` of the remote device after it has been fetched. This intent is sent only when the UUIDs of the remote device are requested to be fetched using Service Discovery Protocol

`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` includes UUIDs from both BR/EDR and LE service discovery results. A `null` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` indicates a timeout. An empty `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` indicates a successful discovery, but zero UUIDs are discovered.

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_DEVICE:kotlin.String`

Always contains the extra field `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_UUID:kotlin.String` 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

 Value: "android.bluetooth.device.action.UUID"

### ADDRESS_TYPE_ANONYMOUS

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADDRESS_TYPE_ANONYMOUS: Int
```

Address type used to indicate an anonymous advertisement.

 Value: 255

### ADDRESS_TYPE_PUBLIC

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADDRESS_TYPE_PUBLIC: Int
```

Hardware MAC Address of the device

 Value: 0

### ADDRESS_TYPE_RANDOM

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADDRESS_TYPE_RANDOM: Int
```

Address is either resolvable, non-resolvable or static.

 Value: 1

### ADDRESS_TYPE_UNKNOWN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ADDRESS_TYPE_UNKNOWN: Int
```

Address type is unknown or unavailable

 Value: 65535

### BOND_BONDED

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_BONDED: Int
```

Indicates the remote device is bonded (paired).

A shared link keys exists locally for the remote device, so communication can be authenticated and encrypted.

*Being bonded (paired) with a remote device does not necessarily mean the device is currently connected. It just means that the pending procedure was completed at some earlier time, and the link key is still stored locally, ready to use on the next connection.*

 Value: 12

### BOND_BONDING

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_BONDING: Int
```

Indicates bonding (pairing) is in progress with the remote device.

 Value: 11

### BOND_LOSS_REASON_BREDR_AUTH_FAILURE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_LOSS_REASON_BREDR_AUTH_FAILURE: Int
```

Indicates the reason for the bond loss is BREDR authentication failure.

 Value: 1

### BOND_LOSS_REASON_BREDR_INCOMING_PAIRING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_LOSS_REASON_BREDR_INCOMING_PAIRING: Int
```

Indicates the reason for the bond loss is BREDR pairing failure.

 Value: 2

### BOND_LOSS_REASON_LE_ENCRYPT_FAILURE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_LOSS_REASON_LE_ENCRYPT_FAILURE: Int
```

Indicates the reason for the bond loss is LE encryption failure.

 Value: 3

### BOND_LOSS_REASON_LE_INCOMING_PAIRING

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_LOSS_REASON_LE_INCOMING_PAIRING: Int
```

Indicates the reason for the bond loss is LE pairing failure.

 Value: 4

### BOND_LOSS_REASON_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_LOSS_REASON_UNKNOWN: Int
```

Indicates the reason for the bond loss is unknown.

 Value: 0

### BOND_NONE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val BOND_NONE: Int
```

Indicates the remote device is not bonded (paired).

There is no shared link key with the remote device, so communication (if it is allowed at all) will be unauthenticated and unencrypted.

 Value: 10

### DEVICE_TYPE_CLASSIC

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_TYPE_CLASSIC: Int
```

Bluetooth device type, Classic - BR/EDR devices

 Value: 1

### DEVICE_TYPE_DUAL

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_TYPE_DUAL: Int
```

Bluetooth device type, Dual Mode - BR/EDR/LE

 Value: 3

### DEVICE_TYPE_LE

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_TYPE_LE: Int
```

Bluetooth device type, Low Energy - LE-only

 Value: 2

### DEVICE_TYPE_UNKNOWN

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DEVICE_TYPE_UNKNOWN: Int
```

Bluetooth device type, Unknown

 Value: 0

### ENCRYPTION_ALGORITHM_AES

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_AES: Int
```

Indicates link was encrypted using AES algorithm

 Value: 2

### ENCRYPTION_ALGORITHM_E0

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_E0: Int
```

Indicates link was encrypted using E0 algorithm

 Value: 1

### ENCRYPTION_ALGORITHM_NONE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_NONE: Int
```

Indicates that link was not encrypted using any algorithm

 Value: 0

### ENCRYPTION_ALGORITHM_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ENCRYPTION_ALGORITHM_UNKNOWN: Int
```

Indicates link was encrypted using unknown algorithm

 Value: 3

### ERROR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ERROR: Int
```

Sentinel error value for this class. Guaranteed to not equal any other integer constant in this class. Provided as a convenience for functions that require a sentinel error value, for example:

`Intent.getIntExtra(BluetoothDevice.EXTRA_BOND_STATE, BluetoothDevice.ERROR)`

 Value: -2147483648

### EXTRA_BOND_LOSS_REASON

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BOND_LOSS_REASON: String
```

Contains the reason for the bond loss.

Possible values are:
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_UNKNOWN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_BREDR_AUTH_FAILURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_BREDR_INCOMING_PAIRING:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_LE_ENCRYPT_FAILURE:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_LOSS_REASON_LE_INCOMING_PAIRING:kotlin.Int`

<br />

 Value: "android.bluetooth.device.extra.BOND_LOSS_REASON"

### EXTRA_BOND_STATE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_BOND_STATE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents. Contains the bond state of the remote device.

Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDED:kotlin.Int`.

 Value: "android.bluetooth.device.extra.BOND_STATE"

### EXTRA_CLASS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CLASS: String
```

Used as a Parcelable `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass` extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_CLASS_CHANGED:kotlin.String` intents.

 Value: "android.bluetooth.device.extra.CLASS"

### EXTRA_DEVICE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DEVICE: String
```

Used as a Parcelable `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#` extra field in every intent broadcast by this class. It contains the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#` that the intent applies to.

 Value: "android.bluetooth.device.extra.DEVICE"

### EXTRA_DISCOVERY_RESULT_TYPE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_DISCOVERY_RESULT_TYPE: String
```

Used as an integer field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. It contains the discovery type for how the device is found:

- If BR/EDR inquiry result is received, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_CLASSIC:kotlin.Int`.
- If BLE advertising data is received, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_LE:kotlin.Int`.
- If both are received, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_DUAL:kotlin.Int`.

<br />

 Value: "android.bluetooth.device.extra.DISCOVERY_RESULT_TYPE"

### EXTRA_ENCRYPTION_ALGORITHM

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ENCRYPTION_ALGORITHM: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intents as the algorithm used for encryption.

Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_E0:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_AES:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ENCRYPTION_ALGORITHM_UNKNOWN:kotlin.Int`.

 Value: "android.bluetooth.device.extra.EXTRA_ENCRYPTION_ALGORITHM"

### EXTRA_ENCRYPTION_ENABLED

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ENCRYPTION_ENABLED: String
```

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intent. false mean encryption is OFF, true means encryption is ON

 Value: "android.bluetooth.device.extra.ENCRYPTION_ENABLED"

### EXTRA_ENCRYPTION_STATUS

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_ENCRYPTION_STATUS: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intent. This is the status value as returned from controller in "HCI Encryption Change event" i.e. value of 0 means success.

 Value: "android.bluetooth.device.extra.ENCRYPTION_STATUS"

### EXTRA_IS_COORDINATED_SET_MEMBER

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_IS_COORDINATED_SET_MEMBER: String
```

Used as a boolean extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. It contains the information if device is discovered as member of a coordinated set or not. Pairing with device that belongs to a set would trigger pairing with the rest of set members. See Bluetooth CSIP specification for more details.

 Value: "android.bluetooth.extra.IS_COORDINATED_SET_MEMBER"

### EXTRA_KEY_SIZE

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_KEY_SIZE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intents as the size of the encryption key, in number of bytes. i.e. value of 16 means 16-byte, or 128 bit key size.

 Value: "android.bluetooth.device.extra.KEY_SIZE"

### EXTRA_LE_APPEARANCE

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_LE_APPEARANCE: String
```

Used as an integer extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_LE_APPEARANCE_CHANGED:kotlin.String` intents, and in `ACTION_*_CONNECTION_STATE_CHANGED` intents for audio related profiles. Contains the LE Appearance of the device.

 Value: "android.bluetooth.device.extra.LE_APPEARANCE"

### EXTRA_NAME

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_NAME: String
```

Used as a String extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_NAME_CHANGED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. It contains the friendly Bluetooth name.

 Value: "android.bluetooth.device.extra.NAME"

### EXTRA_PAIRING_ALGORITHM

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PAIRING_ALGORITHM: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` intents which indicates the pairing algorithm used. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_LE_LEGACY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_BREDR_LEGACY:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_BREDR_SSP:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_ALGORITHM_SC:kotlin.Int`.

 Value: "android.bluetooth.device.extra.PAIRING_ALGORITHM"

### EXTRA_PAIRING_CONTEXT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PAIRING_CONTEXT: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents which indicates the pairing context. Possible values for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_USER_PARTICIPATION_REQUESTED:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_USER_APPROVAL_REQUESTED:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_REPAIRING:kotlin.Int`, while the possible value for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_CONTEXT_REPAIRING:kotlin.Int`.

 Value: "android.bluetooth.device.extra.PAIRING_CONTEXT"

### EXTRA_PAIRING_KEY

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PAIRING_KEY: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` intents as the value of passkey. The Bluetooth Passkey is a 6-digit numerical value represented as integer value in the range 0x00000000 -- 0x000F423F (000000 to 999999).

 Value: "android.bluetooth.device.extra.PAIRING_KEY"

### EXTRA_PAIRING_VARIANT

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PAIRING_VARIANT: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_PAIRING_REQUEST:kotlin.String` intents to indicate pairing method used. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PIN:kotlin.Int`, #PAIRING_VARIANT_PASSKEY, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PASSKEY_CONFIRMATION:kotlin.Int`, #PAIRING_VARIANT_CONSENT, #PAIRING_VARIANT_DISPLAY_PASSKEY, #PAIRING_VARIANT_DISPLAY_PIN, #PAIRING_VARIANT_OOB_CONSENT, #PAIRING_VARIANT_PIN_16_DIGITS.

 Value: "android.bluetooth.device.extra.PAIRING_VARIANT"

### EXTRA_PREVIOUS_BOND_STATE

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_PREVIOUS_BOND_STATE: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents. Contains the previous bond state of the remote device.

Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDED:kotlin.Int`.

 Value: "android.bluetooth.device.extra.PREVIOUS_BOND_STATE"

### EXTRA_RSSI

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_RSSI: String
```

Used as an optional short extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_FOUND:kotlin.String` intents. Contains the RSSI value of the remote device as reported by the Bluetooth hardware.

 Value: "android.bluetooth.device.extra.RSSI"

### EXTRA_TRANSPORT

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_TRANSPORT: String
```

Used as an int extra field in `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_CONNECTED:kotlin.String`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_DISCONNECTED:kotlin.String` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ENCRYPTION_CHANGE:kotlin.String` intents to indicate which transport is connected. Possible values are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int`.

 Value: "android.bluetooth.device.extra.TRANSPORT"

### EXTRA_UUID

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_UUID: String
```

Contains the `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#`s of the remote device which is a parcelable version of `https://developer.android.com/reference/kotlin/java/util/UUID.html#`.

An empty EXTRA_UUID indicates the UUIDs are discovered, but zero UUIDs were found.

A `null` or absent EXTRA_UUID indicates the system failed obtain the UUIDs.

 Value: "android.bluetooth.device.extra.UUID"

### EXTRA_UUID_LE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_UUID_LE: String
```

Contains the `https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#`s of the remote device which is a parcelable version of `https://developer.android.com/reference/kotlin/java/util/UUID.html#`. Only services discovered for the LE transport is included here.

An empty EXTRA_UUID_LE indicates the UUIDs are discovered, but zero UUIDs were found.

A `null` or absent EXTRA_UUID_LE indicates the system failed obtain the UUIDs.

 Value: "android.bluetooth.device.extra.UUID_LE"

### LE_APPEARANCE_UNKNOWN

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LE_APPEARANCE_UNKNOWN: Int
```

Value indicating that the LE Appearance of the device is unknown.

 Value: 0

### PAIRING_ALGORITHM_BREDR_LEGACY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_ALGORITHM_BREDR_LEGACY: Int
```

Indicates usage of the BR/EDR Legacy pairing algorithm. Refer to Bluetooth Core Spec v6.2, Vol 1, Part A, Section 5 for security requirements and procedure details.

 Value: 1

### PAIRING_ALGORITHM_BREDR_SSP

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_ALGORITHM_BREDR_SSP: Int
```

Indicates usage of the BR/EDR Secure Simple Pairing (SSP) algorithm. Refer to Bluetooth Core Spec v6.2, Vol 1, Part A, Section 5 for security requirements and procedure details.

 Value: 2

### PAIRING_ALGORITHM_LE_LEGACY

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_ALGORITHM_LE_LEGACY: Int
```

Indicates usage of the LE Legacy pairing algorithm. Refer to Bluetooth Core Spec v6.2, Vol 1, Part A, Section 5 for security requirements and procedure details.

 Value: 0

### PAIRING_ALGORITHM_SC

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_ALGORITHM_SC: Int
```

Indicates usage of the Secure Connections pairing algorithm, applicable to both BR/EDR and LE transports. Refer to Bluetooth Core Spec v6.2, Vol 1, Part A, Section 5 for security requirements and procedure details.

 Value: 3

### PAIRING_CONTEXT_REPAIRING

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_CONTEXT_REPAIRING: Int
```

Signals an autonomous, system-initiated re-pairing process. Acceptance replaces the existing bond; rejection or ignoring preserves it. Failure results in immediate link disconnection and an `ACTION_KEY_MISSING` intent broadcast.

 Value: 2

### PAIRING_CONTEXT_USER_APPROVAL_REQUESTED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_CONTEXT_USER_APPROVAL_REQUESTED: Int
```

Indicates that the pairing process is initiated, and user approval is requested to complete the pairing process.

 Value: 1

### PAIRING_CONTEXT_USER_PARTICIPATION_REQUESTED

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_CONTEXT_USER_PARTICIPATION_REQUESTED: Int
```

Signals a request for user participation to begin the LE Legacy pairing process. Accepting this allows the Bluetooth stack to proceed toward the formal pairing association model; rejecting or ignoring it results in immediate pairing failure. Note: This only authorizes the process to start and does not constitute final pairing approval.

 Value: 0

### PAIRING_VARIANT_PASSKEY_CONFIRMATION

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_VARIANT_PASSKEY_CONFIRMATION: Int
```

The user will be prompted to confirm the passkey displayed on the screen or an app will confirm the passkey for the user.

 Value: 2

### PAIRING_VARIANT_PIN

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PAIRING_VARIANT_PIN: Int
```

The user will be prompted to enter a pin or an app will enter a pin for user.

 Value: 0

### PHY_LE_1M

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_1M: Int
```

Bluetooth LE 1M PHY. Used to refer to LE 1M Physical Channel for advertising, scanning or connection.

 Value: 1

### PHY_LE_1M_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_1M_MASK: Int
```

Bluetooth LE 1M PHY mask. Used to specify LE 1M Physical Channel as one of many available options in a bitmask.

 Value: 1

### PHY_LE_2M

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_2M: Int
```

Bluetooth LE 2M PHY. Used to refer to LE 2M Physical Channel for advertising, scanning or connection.

 Value: 2

### PHY_LE_2M_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_2M_MASK: Int
```

Bluetooth LE 2M PHY mask. Used to specify LE 2M Physical Channel as one of many available options in a bitmask.

 Value: 2

### PHY_LE_CODED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_CODED: Int
```

Bluetooth LE Coded PHY. Used to refer to LE Coded Physical Channel for advertising, scanning or connection.

 Value: 3

### PHY_LE_CODED_MASK

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_CODED_MASK: Int
```

Bluetooth LE Coded PHY mask. Used to specify LE Coded Physical Channel as one of many available options in a bitmask.

 Value: 4

### PHY_LE_HDT

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_HDT: Int
```

Bluetooth LE HDT PHY. Used to refer to LE High Data Throughput Physical Channel.

 Value: 5

### PHY_LE_HDT_MASK

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_LE_HDT_MASK: Int
```

Bluetooth LE HDT PHY mask. Used to specify LE High Data Throughput Physical Channel as one of many available options in a bitmask.

 Value: 16

### PHY_OPTION_NO_PREFERRED

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_OPTION_NO_PREFERRED: Int
```

No preferred coding when transmitting on the LE Coded PHY.

 Value: 0

### PHY_OPTION_S2

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_OPTION_S2: Int
```

Prefer the S=2 coding to be used when transmitting on the LE Coded PHY.

 Value: 1

### PHY_OPTION_S8

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PHY_OPTION_S8: Int
```

Prefer the S=8 coding to be used when transmitting on the LE Coded PHY.

 Value: 2

### TRANSPORT_AUTO

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_AUTO: Int
```

No preference of physical transport for GATT connections to remote dual-mode devices

 Value: 0

### TRANSPORT_BREDR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_BREDR: Int
```

Constant representing the BR/EDR transport.

 Value: 1

### TRANSPORT_LE

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TRANSPORT_LE: Int
```

Constant representing the Bluetooth Low Energy (BLE) Transport.

 Value: 2

## Public methods

### cancelBondProcess

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun cancelBondProcess(): Boolean
```

Cancel an in-progress bonding request started with #createBond.

BLUETOOTH_PRIVILEGED is enforced only if the calling app didn't initiate bonding. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true on success, false on error |

### connect

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connect(): Int
```

Connects all user enabled and supported bluetooth profiles between the local and remote device. If no profiles are user enabled (e.g. first connection), we connect all supported profiles. If the device is not already connected, this will page the device before initiating profile connections. Connection is asynchronous and you should listen to each profile's broadcast intent ACTION_CONNECTION_STATE_CHANGED to verify whether connection was successful. For example, to verify a2dp is connected, you would listen for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothA2dp#ACTION_CONNECTION_STATE_CHANGED:kotlin.String`

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission. Additionally, an app must either have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` permission or be associated with the Companion Device manager (see `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#associate(android.companion.AssociationRequest,%20android.companion.CompanionDeviceManager.Callback,%20android.os.Handler)`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` upon successful initiation of the operation, otherwise an error code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_DEVICE_NOT_BONDED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the device address is invalid |

### connectGatt

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectGatt(
    gattConnectionSettings: BluetoothGattConnectionSettings, 
    executor: Executor, 
    callback: BluetoothGattCallback
): BluetoothGatt?
```

Connect to the GATT Server hosted by the given device. Caller acts as a GATT client. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback` of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattConnectionSettings` will deliver results to the Caller, such as connection updates and GATT client operation results. The method returns a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt` instance. The application can use BluetoothGatt to conduct GATT client operations. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `gattConnectionSettings` | [BluetoothGattConnectionSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattConnectionSettings): `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattConnectionSettings` objects with required gatt settings for the GATT connection. This value cannot be `null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): The executor to use for the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use `https://developer.android.com/reference/kotlin/android/content/Context.html#getMainExecutor()`. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [BluetoothGattCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback): GATT callback handler that will receive asynchronous callbacks. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGatt?` | A BluetoothGatt instance. You can use BluetoothGatt to conduct GATT client operations. This value may be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if gattConnectionSettings, callback or executor is null. |

### connectGatt

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectGatt(
    context: Context!, 
    autoConnect: Boolean, 
    callback: BluetoothGattCallback!
): BluetoothGatt!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.bluetooth.BluetoothGattConnectionSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothGattCallback)`.*

Connect to GATT Server hosted by this device. Caller acts as GATT client. The callback is used to deliver results to Caller, such as connection status as well as any further GATT client operations. The method returns a BluetoothGatt instance. You can use BluetoothGatt to conduct GATT client operations. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `autoConnect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to directly connect to the remote device (false) or to automatically connect as soon as the remote device becomes available (true). |
| `callback` | [BluetoothGattCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback)!: GATT callback handler that will receive asynchronous callbacks. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if callback is null |

### connectGatt

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectGatt(
    context: Context!, 
    autoConnect: Boolean, 
    callback: BluetoothGattCallback!, 
    transport: Int
): BluetoothGatt!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.bluetooth.BluetoothGattConnectionSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothGattCallback)`.*

Connect to GATT Server hosted by this device. Caller acts as GATT client. The callback is used to deliver results to Caller, such as connection status as well as any further GATT client operations. The method returns a BluetoothGatt instance. You can use BluetoothGatt to conduct GATT client operations. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `autoConnect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to directly connect to the remote device (false) or to automatically connect as soon as the remote device becomes available (true). |
| `callback` | [BluetoothGattCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback)!: GATT callback handler that will receive asynchronous callbacks. |
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred transport for GATT connections to remote dual-mode devices `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |
| --- | --- |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if callback is null |

### connectGatt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectGatt(
    context: Context!, 
    autoConnect: Boolean, 
    callback: BluetoothGattCallback!, 
    transport: Int, 
    phy: Int
): BluetoothGatt!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.bluetooth.BluetoothGattConnectionSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothGattCallback)`.*

Connect to GATT Server hosted by this device. Caller acts as GATT client. The callback is used to deliver results to Caller, such as connection status as well as any further GATT client operations. The method returns a BluetoothGatt instance. You can use BluetoothGatt to conduct GATT client operations. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `autoConnect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to directly connect to the remote device (false) or to automatically connect as soon as the remote device becomes available (true). |
| `callback` | [BluetoothGattCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback)!: GATT callback handler that will receive asynchronous callbacks. |
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred transport for GATT connections to remote dual-mode devices `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |
| --- | --- |
| `phy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred PHY for connections to remote LE device. Bitwise OR of any of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int`. This option does not take effect if `autoConnect` is set to true. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if callback is null |

### connectGatt

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun connectGatt(
    context: Context!, 
    autoConnect: Boolean, 
    callback: BluetoothGattCallback!, 
    transport: Int, 
    phy: Int, 
    handler: Handler!
): BluetoothGatt!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#connectGatt(android.bluetooth.BluetoothGattConnectionSettings,%20java.util.concurrent.Executor,%20android.bluetooth.BluetoothGattCallback)`.*

Connect to GATT Server hosted by this device. Caller acts as GATT client. The callback is used to deliver results to Caller, such as connection status as well as any further GATT client operations. The method returns a BluetoothGatt instance. You can use BluetoothGatt to conduct GATT client operations. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `autoConnect` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to directly connect to the remote device (false) or to automatically connect as soon as the remote device becomes available (true). |
| `callback` | [BluetoothGattCallback](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothGattCallback)!: GATT callback handler that will receive asynchronous callbacks. |
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred transport for GATT connections to remote dual-mode devices `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |
| --- | --- |
| `phy` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): preferred PHY for connections to remote LE device. Bitwise OR of any of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_1M_MASK:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_2M_MASK:kotlin.Int`, an d`https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PHY_LE_CODED_MASK:kotlin.Int`. This option does not take effect if `autoConnect` is set to true. |
| `handler` | [Handler](https://developer.android.com/reference/kotlin/android/os/Handler.html#)!: The handler to use for the callback. If `null`, callbacks will happen on an un-specified background thread. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if callback is null |

### createBond

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createBond(): Boolean
```

Start the bonding (pairing) process with the remote device.

This is an asynchronous call, it will return immediately. Register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents to be notified when the bonding process completes, and its result.

Android system services will handle the necessary user interactions to confirm and complete the bonding process. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false on immediate error, true if bonding will begin |

### createBond

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createBond(transport: Int): Boolean
```

Start the bonding (pairing) process with the remote device using the specified transport.

This is an asynchronous call, it will return immediately. Register for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_BOND_STATE_CHANGED:kotlin.String` intents to be notified when the bonding process completes, and its result.

Android system services will handle the necessary user interactions to confirm and complete the bonding process. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The transport to use for the pairing procedure. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false on immediate error, true if bonding will begin |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if an invalid transport was specified |

### createInsecureL2capChannel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createInsecureL2capChannel(psm: Int): BluetoothSocket
```

Create a Bluetooth L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` that can be used to start a secure outgoing connection to the remote device with the same dynamic protocol/service multiplexer (PSM) value. The supported Bluetooth transport is LE only.

This is designed to be used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingInsecureL2capChannel()` for peer-peer Bluetooth applications.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect()` to initiate the outgoing connection.

Application using this API is responsible for obtaining PSM value from remote device.

The communication channel may not have an authenticated link key, i.e. it may be subject to person-in-the-middle attacks. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createL2capChannel(kotlin.Int)` if an encrypted and authenticated communication channel is possible.

| Parameters ||
|---|---|
| `psm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): dynamic PSM value from remote device |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` | a CoC #BluetoothSocket ready for an outgoing connection. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available, or insufficient permissions |

### createInsecureRfcommSocketToServiceRecord

Added in [API level 10](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createInsecureRfcommSocketToServiceRecord(uuid: UUID!): BluetoothSocket!
```

Create an RFCOMM `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` socket ready to start an insecure outgoing connection to this remote device using SDP lookup of uuid.

The communication channel will not have an authenticated link key i.e. it will be subject to person-in-the-middle attacks. For Bluetooth 2.1 devices, the link key will be encrypted, as encryption is mandatory. For legacy devices (pre Bluetooth 2.1 devices) the link key will be not be encrypted. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createRfcommSocketToServiceRecord(java.util.UUID)` if an encrypted and authenticated communication channel is desired.

This is designed to be used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingInsecureRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)` for peer-peer Bluetooth applications.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect()` to initiate the outgoing connection. This will also perform an SDP lookup of the given uuid to determine which channel to connect to.

The remote device will be authenticated and communication on this socket will be encrypted.

Hint: If you are connecting to a Bluetooth serial board then try using the well-known SPP UUID 00001101-0000-1000-8000-00805F9B34FB. However if you are connecting to an Android peer then please generate your own unique UUID.

| Parameters ||
|---|---|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!: service record uuid to lookup RFCOMM channel |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket!` | a RFCOMM BluetoothServerSocket ready for an outgoing connection |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available, or insufficient permissions |

### createL2capChannel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createL2capChannel(psm: Int): BluetoothSocket
```

Create a Bluetooth L2CAP Connection-oriented Channel (CoC) `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` that can be used to start a secure outgoing connection to the remote device with the same dynamic protocol/service multiplexer (PSM) value. The supported Bluetooth transport is LE only.

This is designed to be used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingL2capChannel()` for peer-peer Bluetooth applications.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect()` to initiate the outgoing connection.

Application using this API is responsible for obtaining PSM value from remote device.

The remote device will be authenticated and communication on this socket will be encrypted.

Use this socket if an authenticated socket link is possible. Authentication refers to the authentication of the link key to prevent person-in-the-middle type of attacks.

| Parameters ||
|---|---|
| `psm` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): dynamic PSM value from remote device |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` | a CoC #BluetoothSocket ready for an outgoing connection. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available, or insufficient permissions |

### createRfcommSocketToServiceRecord

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createRfcommSocketToServiceRecord(uuid: UUID!): BluetoothSocket!
```

Create an RFCOMM `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` ready to start a secure outgoing connection to this remote device using SDP lookup of uuid.

This is designed to be used with `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingRfcommWithServiceRecord(kotlin.String,%20java.util.UUID)` for peer-peer Bluetooth applications.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect()` to initiate the outgoing connection. This will also perform an SDP lookup of the given uuid to determine which channel to connect to.

The remote device will be authenticated and communication on this socket will be encrypted.

Use this socket only if an authenticated socket link is possible. Authentication refers to the authentication of the link key to prevent person-in-the-middle type of attacks. For example, for Bluetooth 2.1 devices, if any of the devices does not have an input and output capability or just has the ability to display a numeric key, a secure socket connection is not possible. In such a case, use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#createInsecureRfcommSocketToServiceRecord(java.util.UUID)`. For more details, refer to the Security Model section 5.2 (vol 3) of Bluetooth Core Specification version 2.1 + EDR.

Hint: If you are connecting to a Bluetooth serial board then try using the well-known SPP UUID 00001101-0000-1000-8000-00805F9B34FB. However if you are connecting to an Android peer then please generate your own unique UUID.

| Parameters ||
|---|---|
| `uuid` | [UUID](https://developer.android.com/reference/kotlin/java/util/UUID.html#)!: service record uuid to lookup RFCOMM channel |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket!` | a RFCOMM BluetoothServerSocket ready for an outgoing connection |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available, or insufficient permissions |

### createUsingSocketSettings

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun createUsingSocketSettings(settings: BluetoothSocketSettings): BluetoothSocket
```

Creates a client socket to connect to a remote Bluetooth server with the specified socket settings `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings` This API is used to connect to a remote server hosted using `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothAdapter#listenUsingSocketSettings(android.bluetooth.BluetoothSocketSettings)`.

- For \`BluetoothSocket.TYPE_RFCOMM\`: The RFCOMM UUID must be provided using android.bluetooth.BluetoothSocketSettings#setRfcommUuid().
- For \`BluetoothSocket.TYPE_LE\`: The L2cap protocol/service multiplexer (PSM) value must be provided using android.bluetooth.BluetoothSocketSettings#setL2capPsm().

<br />

Application using this API is responsible for obtaining protocol/service multiplexer (psm) value from remote device.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket#connect()` to initiate the outgoing connection.

| Parameters ||
|---|---|
| `settings` | [BluetoothSocketSettings](https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings): Bluetooth socket settings `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocketSettings`. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` | a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothSocket` ready for an outgoing connection. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.io.IOException` | on error, for example Bluetooth not available. |
| `java.lang.IllegalArgumentException` | if BluetoothSocket#TYPE_RFCOMM socket with no UUID is passed as input or if BluetoothSocket#TYPE_LE with invalid PSM is passed. |

### describeContents

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### disconnect

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disconnect(): Int
```

Disconnects all connected bluetooth profiles between the local and remote device. Disconnection is asynchronous, so you should listen to each profile's broadcast intent ACTION_CONNECTION_STATE_CHANGED to verify whether disconnection was successful. For example, to verify a2dp is disconnected, you would listen for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothA2dp#ACTION_CONNECTION_STATE_CHANGED:kotlin.String`. Once all profiles have disconnected, the ACL link should come down and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_DISCONNECTED:kotlin.String` should be broadcast.

In the rare event that one or more profiles fail to disconnect, call this method again to send another request to disconnect each connected profile.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission. Additionally, an app must either have both `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` or be associated with the Companion Device manager (see `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#associate(android.companion.AssociationRequest,%20android.companion.CompanionDeviceManager.Callback,%20android.os.Handler)`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` upon successful initiation of the operation, otherwise an error code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_DEVICE_NOT_BONDED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the device address is invalid |

### disconnectAcl

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun disconnectAcl(transport: Int): Int
```

Disconnects ACL links for this device.

If `transport` is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int`, it disconnects all ACL links for the device. Otherwise, it disconnects the ACL link for the specified transport.

Disconnection is asynchronous, so apps should listen to `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_ACL_DISCONNECTED:kotlin.String` to verify whether disconnection was successful.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission. Additionally, an app must either have `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` or have a Companion Device Manager association with this device (see `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#associate(android.companion.AssociationRequest,%20android.companion.CompanionDeviceManager.Callback,%20android.os.Handler)`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transport to disconnect (e.g. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int`). Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` upon successful setting, otherwise an error code. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_DEVICE_NOT_BONDED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the transport is invalid |

### equals

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | the reference object with which to compare. |
| `o` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### fetchUuids

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun fetchUuids(transport: Int): Boolean
```

Performs a service discovery on the remote device to get the UUIDs supported, allowing the caller to specify the transport.

This API is asynchronous. When discovery completes, the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_UUID:kotlin.String` intent is sent, containing the UUIDs supported by the remote device for the specified transport(s). Cached UUIDs may be sent if an error occurs or if discovery is lengthy. Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getUuids()` to retrieve cached UUIDs without initiating discovery.

The implementation already handles invalid transport arguments by throwing IllegalArgumentException and returns false when Bluetooth is disabled, covering the contract verification points. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The transport to use for discovery: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` for Classic Bluetooth (SDP), `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` for Bluetooth Low Energy (GATT), or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` to discover on all applicable transports (typically BR/EDR and LE for dual-mode devices). \* @return False if the check fails, True if the process of initiating an ACL connection to the remote device was started or cached UUIDs will be broadcast with the specific transport. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_AUTO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |

### fetchUuidsWithSdp

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun fetchUuidsWithSdp(): Boolean
```

Performs a service discovery on the remote device to get the UUIDs supported.

This API is asynchronous and `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_UUID:kotlin.String` intent is sent, with the UUIDs supported by the remote end. If there is an error in getting the SDP records or if the process takes a long time, or the device is bonding and we have its UUIDs cached, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_UUID:kotlin.String` intent is sent with the UUIDs that is currently present in the cache. Clients should use the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getUuids()` to get UUIDs if service discovery is not to be performed. If there is an ongoing bonding process, service discovery or device inquiry, the request will be queued.

To explicitly fetch UUIDs across all transports, use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#fetchUuids(kotlin.Int)` by calling `fetchUuids(BluetoothDevice.TRANSPORT_AUTO)`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | False if the check fails, True if the process of initiating an ACL connection to the remote device was started or cached UUIDs will be broadcast. |

### getAddress

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddress(): String!
```

Returns the hardware address of this BluetoothDevice.

For example, "00:11:22:AA:BB:CC".

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | Bluetooth hardware address as string |

### getAddressType

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAddressType(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Bluetooth address type. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_PUBLIC:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_RANDOM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_ANONYMOUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_UNKNOWN:kotlin.Int` |

### getAlias

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getAlias(): String?
```

Get the locally modifiable name (alias) of the remote Bluetooth device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | the Bluetooth alias, the friendly device name if no alias, or null if there was a problem |

### getBluetoothClass

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBluetoothClass(): BluetoothClass!
```

Get the Bluetooth class of the remote device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothClass!` | Bluetooth class object, or null on error |

### getBondState

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBondState(): Int
```

This API returns the bond state of the remote device.

Note: The bond state returned by this API may not correctly represent the actual bond state for all transports. To get the correct bond status for a specific transport, use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getBondStatus(kotlin.Int)`

Possible values for the bond state are: `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_NONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDING:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#BOND_BONDED:kotlin.Int`. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the bond state of the remote device |

### getBondStatus

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getBondStatus(transport: Int): BondStatus?
```

Returns the bond status of this device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transport to get the bond status for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BondStatus?` | The bond status of this device, or null if the device is not bonded. |

### getEncryptionStatus

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEncryptionStatus(transport: Int): EncryptionStatus?
```

Get the encryption status of the connected device. This API will return the encryption state (if connected). The encryption details are enclosed in a `https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus` object, which can be null if the device is not encrypted (or not connected). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the transport to get the link status for. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/EncryptionStatus?` | the encryption status of the device, null if the device is not encrypted or not connected. |

### getIdentityAddressWithType

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getIdentityAddressWithType(): BluetoothDevice.BluetoothAddress
```

Returns the identity address and identity address type of this BluetoothDevice. An identity address is a public or static random Bluetooth LE device address that serves as a unique identifier. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.BluetoothAddress` | a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.BluetoothAddress` containing identity address and identity address type. If Bluetooth is not enabled or identity address type is not available, it will return a `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice.BluetoothAddress` containing `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ADDRESS_TYPE_UNKNOWN:kotlin.Int` device for the identity address type. This value cannot be `null`. |

### getKeyMissingCount

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getKeyMissingCount(): Int
```

Get the number of times `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_KEY_MISSING:kotlin.String` intent was thrown for this device since the last successful encrypted connection. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | number of times `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_KEY_MISSING:kotlin.String` intent was thrown for this device since the last successful encrypted connection |

### getLeAppearance

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getLeAppearance(): Int
```

Get the Bluetooth LE Appearance of the remote device.

The LE Appearance values are defined by the Bluetooth SIG and provide a visual representation of the device type. For a complete list of valid LE Appearance values, refer to the [Bluetooth Assigned Numbers](https://www.bluetooth.com/wp-content/uploads/Files/Specification/HTML/Assigned_Numbers/out/en/Assigned_Numbers.pdf) document.

This value is returned from the local cache and can be retrieved even when the device is disconnected. The value represents a static physical characteristic and typically stays constant throughout the lifetime of a device.

The cache is populated either by extracting Appearance AD type from LE advertisements during device discovery prior to pairing, or by performing a GATT read on the GAP service's Appearance characteristic on first LE connection.

According to the Bluetooth SIG GAP specifications, the Appearance characteristic does not support GATT notifications/indications. The changes to a device's appearance are only broadcasted for bonded devices using the `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#ACTION_LE_APPEARANCE_CHANGED:kotlin.String` intent containing the new `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#EXTRA_LE_APPEARANCE:kotlin.String` value. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the LE Appearance value, or `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#LE_APPEARANCE_UNKNOWN:kotlin.Int` if the appearance is unknown or not yet available. |

### getName

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getName(): String!
```

Get the friendly Bluetooth name of the remote device.

The local adapter will automatically retrieve remote names when performing a device scan, and will cache them. This method just returns the name for this device from the cache. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the Bluetooth name, or null if there was a problem. |

### getType

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getType(): Int
```

Get the Bluetooth device type of the remote device. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the device type `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_CLASSIC:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_LE:kotlin.Int` `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_DUAL:kotlin.Int`. `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#DEVICE_TYPE_UNKNOWN:kotlin.Int` if it's not available |

### getUuids

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getUuids(): Array<ParcelUuid!>!
```

Returns the supported features (UUIDs) of the remote device.

This method does not start a service discovery procedure to retrieve the UUIDs from the remote device. Instead, the local cached copy of the service UUIDs are returned.

Use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#fetchUuidsWithSdp()` if fresh UUIDs are desired. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/android/os/ParcelUuid.html#!>!` | the supported features (UUIDs) of the remote device, or null on error |

### hashCode

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### isConnected

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun isConnected(transport: Int): Boolean
```

Returns whether there is an open connection to this device on the given transport. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String`

| Parameters ||
|---|---|
| `transport` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_BREDR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#TRANSPORT_LE:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if there is at least one open connection to this device. |

### setAlias

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setAlias(alias: String?): Int
```

Sets the locally modifiable name (alias) of the remote Bluetooth device. This method overwrites the previously stored alias. The new alias is saved in local storage so that the change is preserved over power cycles.

This method requires the calling app to have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission. Additionally, an app must either have the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` or be associated with the Companion Device manager (see `https://developer.android.com/reference/kotlin/android/companion/CompanionDeviceManager.html#associate(android.companion.AssociationRequest,%20android.companion.CompanionDeviceManager.Callback,%20android.os.Handler)`). 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Parameters ||
|---|---|
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: is the new locally modifiable name for the remote Bluetooth device which must be the empty string. If null, we clear the alias. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | whether the alias was successfully changed. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#SUCCESS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ENABLED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_BLUETOOTH_NOT_ALLOWED:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_MISSING_BLUETOOTH_CONNECT_PERMISSION:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothStatusCodes#ERROR_DEVICE_NOT_BONDED:kotlin.Int` |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the alias is the empty string |

### setPairingConfirmation

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPairingConfirmation(confirm: Boolean): Boolean
```

Confirm passkey for `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PASSKEY_CONFIRMATION:kotlin.Int` pairing. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`. 
Requires `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` and `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true confirmation has been sent out false for error |

### setPin

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setPin(pin: ByteArray!): Boolean
```

**Deprecated:** *Only privileged apps should be setting the pin code. General use of this API can interfere with pairing or cause security problems. Use #setPin(java.lang.String) instead.*

Set the pin during pairing when the pairing method is `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#PAIRING_VARIANT_PIN:kotlin.Int`

When the calling application targets API level 37 or higher, `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_PRIVILEGED:kotlin.String` is required. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#R:kotlin.Int` or lower, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_ADMIN:kotlin.String` permission which can be gained with a simple `<uses-permission>` manifest tag. 
For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int` or or higher, this requires the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BLUETOOTH_CONNECT:kotlin.String` permission which can be gained with `https://developer.android.com/reference/kotlin/android/app/Activity.html#requestPermissions(kotlin.Array,%20kotlin.Int)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true pin has been set false for error |

### toString

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of this BluetoothDevice.

For apps targeting `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#UPSIDE_DOWN_CAKE:kotlin.Int` (API level 34) or higher, this returns the MAC address of the device redacted by replacing the hexadecimal digits of leftmost 4 bytes (in big endian order) with "XX", e.g., "XX:XX:XX:XX:12:34". For apps targeting earlier versions, the MAC address is returned without redaction.

Warning: The return value of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#toString()` may change in the future. It is intended to be used in logging statements. Thus apps should never rely on the return value of `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#toString()` in their logic. Always use other appropriate APIs instead (e.g., use `https://developer.android.com/reference/kotlin/android/bluetooth/BluetoothDevice#getAddress()` to get the MAC address).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | string representation of this BluetoothDevice |

### writeToParcel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---|---|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<BluetoothDevice!>
```
