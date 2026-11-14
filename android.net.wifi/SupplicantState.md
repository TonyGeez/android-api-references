# SupplicantState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SupplicantState

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/SupplicantState "View this page in Java") 

```
class SupplicantState : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [kotlin.Enum](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-enum/index.html)\< [android.net.wifi.SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#)\> ||
| | ↳ | [android.net.wifi.SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#) |

| Known Direct Subclasses [SupplicantState.ASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:ASSOCIATED), [SupplicantState.ASSOCIATING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:ASSOCIATING), [SupplicantState.AUTHENTICATING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:AUTHENTICATING), [SupplicantState.COMPLETED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:COMPLETED), [SupplicantState.DISCONNECTED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:DISCONNECTED), [SupplicantState.DORMANT](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:DORMANT), [SupplicantState.FOUR_WAY_HANDSHAKE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:FOUR_WAY_HANDSHAKE), [SupplicantState.GROUP_HANDSHAKE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:GROUP_HANDSHAKE), [SupplicantState.INACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INACTIVE), [SupplicantState.INTERFACE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INTERFACE_DISABLED), [SupplicantState.INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INVALID), [SupplicantState.SCANNING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:SCANNING), and 1 others. |-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------| | [SupplicantState.ASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:ASSOCIATED) | Association completed. | | [SupplicantState.ASSOCIATING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:ASSOCIATING) | Trying to associate with a BSS/SSID. | | [SupplicantState.AUTHENTICATING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:AUTHENTICATING) | Trying to authenticate with a BSS/SSID | | [SupplicantState.COMPLETED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:COMPLETED) | All authentication completed. | | [SupplicantState.DISCONNECTED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:DISCONNECTED) | This state indicates that client is not associated, but is likely to start looking for an access point. | | [SupplicantState.DORMANT](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:DORMANT) | An Android-added state that is reported when a client issues an explicit DISCONNECT command. | | [SupplicantState.FOUR_WAY_HANDSHAKE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:FOUR_WAY_HANDSHAKE) | WPA 4-Way Key Handshake in progress. | | [SupplicantState.GROUP_HANDSHAKE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:GROUP_HANDSHAKE) | WPA Group Key Handshake in progress. | | [SupplicantState.INACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INACTIVE) | Inactive state (wpa_supplicant disabled). | | [SupplicantState.INTERFACE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INTERFACE_DISABLED) | Interface is disabled | | [SupplicantState.INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INVALID) | A pseudo-state that should normally never be seen. | | [SupplicantState.SCANNING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:SCANNING) | Scanning for a network. | | [SupplicantState.UNINITIALIZED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:UNINITIALIZED) | No connection to wpa_supplicant. | |

From

<br />

These enumeration values are used to indicate the current wpa_supplicant state. This is more fine-grained than most users will be interested in. In general, it is better to use [NetworkInfo.State](https://developer.android.com/reference/kotlin/android/net/NetworkInfo.State.html#).

<br />

Note, the order of these enum constants must match the numerical values of the state constants in`defs.h`in`wpa_supplicant`.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Enum values ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [ASSOCIATED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:ASSOCIATED) Association completed. |
| [ASSOCIATING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:ASSOCIATING) Trying to associate with a BSS/SSID. |
| [AUTHENTICATING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:AUTHENTICATING) Trying to authenticate with a BSS/SSID |
| [COMPLETED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:COMPLETED) All authentication completed. |
| [DISCONNECTED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:DISCONNECTED) This state indicates that client is not associated, but is likely to start looking for an access point. |
| [DORMANT](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:DORMANT) An Android-added state that is reported when a client issues an explicit DISCONNECT command. |
| [FOUR_WAY_HANDSHAKE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:FOUR_WAY_HANDSHAKE) WPA 4-Way Key Handshake in progress. |
| [GROUP_HANDSHAKE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:GROUP_HANDSHAKE) WPA Group Key Handshake in progress. |
| [INACTIVE](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INACTIVE) Inactive state (wpa_supplicant disabled). |
| [INTERFACE_DISABLED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INTERFACE_DISABLED) Interface is disabled |
| [INVALID](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:INVALID) A pseudo-state that should normally never be seen. |
| [SCANNING](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:SCANNING) Scanning for a network. |
| [UNINITIALIZED](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#ENUM_VALUE:UNINITIALIZED) No connection to wpa_supplicant. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValidState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#isValidState(android.net.wifi.SupplicantState))`(`state:` ` [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#)!`)` Returns`true`if the supplicant state is valid and`false`otherwise. |

## Enum values

### ASSOCIATED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ASSOCIATED : SupplicantState
```

Association completed.

<br />

This state is entered when the driver reports that association has been successfully completed with an AP. If IEEE 802.1X is used (with or without WPA/WPA2), wpa_supplicant remains in this state until the IEEE 802.1X/EAPOL authentication has been completed. 

### ASSOCIATING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val ASSOCIATING : SupplicantState
```

Trying to associate with a BSS/SSID.

<br />

This state is entered when wpa_supplicant has found a suitable BSS to associate with and the driver is configured to try to associate with this BSS in ap_scan=1 mode. When using ap_scan=2 mode, this state is entered when the driver is configured to try to associate with a network using the configured SSID and security policy. 

### AUTHENTICATING

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val AUTHENTICATING : SupplicantState
```

Trying to authenticate with a BSS/SSID

<br />

This state is entered when wpa_supplicant has found a suitable BSS to authenticate with and the driver is configured to try to authenticate with this BSS. 

### COMPLETED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val COMPLETED : SupplicantState
```

All authentication completed.

<br />

This state is entered when the full authentication process is completed. In case of WPA2, this happens when the 4-Way Handshake is successfully completed. With WPA, this state is entered after the Group Key Handshake; with IEEE 802.1X (non-WPA) connection is completed after dynamic keys are received (or if not used, after the EAP authentication has been completed). With static WEP keys and plaintext connections, this state is entered when an association has been completed.

<br />

This state indicates that the supplicant has completed its processing for the association phase and that data connection is fully configured. Note, however, that there may not be any IP address associated with the connection yet. Typically, a DHCP request needs to be sent at this point to obtain an address. 

### DISCONNECTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DISCONNECTED : SupplicantState
```

This state indicates that client is not associated, but is likely to start looking for an access point. This state is entered when a connection is lost. 

### DORMANT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val DORMANT : SupplicantState
```

An Android-added state that is reported when a client issues an explicit DISCONNECT command. In such a case, the supplicant is not only dissociated from the current access point (as for the DISCONNECTED state above), but it also does not attempt to connect to any access point until a RECONNECT or REASSOCIATE command is issued by the client. 

### FOUR_WAY_HANDSHAKE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val FOUR_WAY_HANDSHAKE : SupplicantState
```

WPA 4-Way Key Handshake in progress.

<br />

This state is entered when WPA/WPA2 4-Way Handshake is started. In case of WPA-PSK, this happens when receiving the first EAPOL-Key frame after association. In case of WPA-EAP, this state is entered when the IEEE 802.1X/EAPOL authentication has been completed. 

### GROUP_HANDSHAKE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val GROUP_HANDSHAKE : SupplicantState
```

WPA Group Key Handshake in progress.

<br />

This state is entered when 4-Way Key Handshake has been completed (i.e., when the supplicant sends out message 4/4) and when Group Key rekeying is started by the AP (i.e., when supplicant receives message 1/2). 

### INACTIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INACTIVE : SupplicantState
```

Inactive state (wpa_supplicant disabled).

<br />

This state is entered if there are no enabled networks in the configuration. wpa_supplicant is not trying to associate with a new network and external interaction (e.g., ctrl_iface call to add or enable a network) is needed to start association. 

### INTERFACE_DISABLED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INTERFACE_DISABLED : SupplicantState
```

Interface is disabled

<br />

This state is entered if the network interface is disabled. wpa_supplicant refuses any new operations that would use the radio until the interface has been enabled. 

### INVALID

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val INVALID : SupplicantState
```

A pseudo-state that should normally never be seen. 

### SCANNING

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val SCANNING : SupplicantState
```

Scanning for a network.

<br />

This state is entered when wpa_supplicant starts scanning for a network. 

### UNINITIALIZED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
enum val UNINITIALIZED : SupplicantState
```

No connection to wpa_supplicant.

<br />

This is an additional pseudo-state to handle the case where wpa_supplicant is not running and/or we have not been able to establish a connection to it.

## Public methods

### isValidState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isValidState(state: SupplicantState!): Boolean
```

Returns`true`if the supplicant state is valid and`false`otherwise.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `state` | [SupplicantState](https://developer.android.com/reference/kotlin/android/net/wifi/SupplicantState#)!:The supplicant state |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the supplicant state is valid and`false`otherwise. |
