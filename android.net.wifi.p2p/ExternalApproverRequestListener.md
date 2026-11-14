# WifiP2pManager.ExternalApproverRequestListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExternalApproverRequestListener

Kotlin| [Java](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) 
| --- | --- |

```
interface ExternalApproverRequestListener
```

| [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) |

Interface for callback invocation when an incoming request is received. This callback is registered by [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_CLOSE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) Detached since the [WifiP2pManager](../android/net/wifi/p2p/WifiP2pManager.md) channel was closed, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_FAILURE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) Detached due to a framework failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_REMOVE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) Detached by a call to [removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ActionListener)](../android/net/wifi/p2p/WifiP2pManager.md)). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_REPLACE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) Detached when a new approver replaces an old one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_INVITATION](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) This device received an invitation request from GO to join the group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_JOIN](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) This GO device received a request from a peer to join the group. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_NEGOTIATION](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) This device received a negotiation request from another peer. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttached](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md))`(`deviceAddress:` ` [MacAddress](../android/net/MacAddress.md)`)` Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md))is successful. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionRequested](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md))`(`requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `config:` ` [WifiP2pConfig](../android/net/wifi/p2p/WifiP2pConfig.md)`, `device:` ` [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md)`)` Called when there is an incoming connection request which matches a peer (identified by its [MacAddress](../android/net/MacAddress.md)) registered by the external approver through [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetached](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md))`(`deviceAddress:` ` [MacAddress](../android/net/MacAddress.md)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md))has failed. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPasswordGenerated](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md))`(`deviceAddress:` ` [MacAddress](../android/net/MacAddress.md)`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called when a Wi-Fi Direct R2 pairing bootstrapping password is generated by the WiFi service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPinGenerated](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md))`(`deviceAddress:` ` [MacAddress](../android/net/MacAddress.md)`, `pin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called when a WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN is generated by the WiFi service. |

## Constants

### APPROVER_DETACH_REASON_CLOSE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_CLOSE: Int
```

Detached since the [WifiP2pManager](../android/net/wifi/p2p/WifiP2pManager.md) channel was closed, e.g. by using [Channel.close()](../android/net/wifi/p2p/WifiP2pManager.Channel.md))method. Used in [onDetached(android.net.MacAddress,int)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 3

### APPROVER_DETACH_REASON_FAILURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_FAILURE: Int
```

Detached due to a framework failure. Used in [onDetached(android.net.MacAddress,int)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 1

### APPROVER_DETACH_REASON_REMOVE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_REMOVE: Int
```

Detached by a call to [removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ActionListener)](../android/net/wifi/p2p/WifiP2pManager.md)). Used in [onDetached(android.net.MacAddress,int)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 0

### APPROVER_DETACH_REASON_REPLACE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_REPLACE: Int
```

Detached when a new approver replaces an old one. Used in [onDetached(android.net.MacAddress,int)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 2

### REQUEST_TYPE_INVITATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_INVITATION: Int
```

This device received an invitation request from GO to join the group. Used in [onConnectionRequested(int,android.net.wifi.p2p.WifiP2pConfig,android.net.wifi.p2p.WifiP2pDevice)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 1

### REQUEST_TYPE_JOIN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_JOIN: Int
```

This GO device received a request from a peer to join the group. Used in [onConnectionRequested(int,android.net.wifi.p2p.WifiP2pConfig,android.net.wifi.p2p.WifiP2pDevice)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 2

### REQUEST_TYPE_NEGOTIATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_NEGOTIATION: Int
```

This device received a negotiation request from another peer. Used in [onConnectionRequested(int,android.net.wifi.p2p.WifiP2pConfig,android.net.wifi.p2p.WifiP2pDevice)](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md)). 

 Value: 0

## Public methods

### onAttached

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAttached(deviceAddress: MacAddress): Unit
```

Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md))is successful.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](../android/net/MacAddress.md):is the peer MAC address used in the registration. This value cannot be`null`. |

### onConnectionRequested

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnectionRequested(
    requestType: Int, 
    config: WifiP2pConfig, 
    device: WifiP2pDevice
): Unit
```

Called when there is an incoming connection request which matches a peer (identified by its [MacAddress](../android/net/MacAddress.md)) registered by the external approver through [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md)). The external approver is expected to follow up with a connection decision using the [setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,int,android.net.wifi.p2p.WifiP2pManager.ActionListener)](../android/net/wifi/p2p/WifiP2pManager.md))with [CONNECTION_REQUEST_ACCEPT](../android/net/wifi/p2p/WifiP2pManager.md), [CONNECTION_REQUEST_REJECT](../android/net/wifi/p2p/WifiP2pManager.md), or [CONNECTION_REQUEST_DEFER_TO_SERVICE](../android/net/wifi/p2p/WifiP2pManager.md).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is one of [REQUEST_TYPE_NEGOTIATION](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), [REQUEST_TYPE_INVITATION](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), and [REQUEST_TYPE_JOIN](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md). Value is [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_NEGOTIATION](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_INVITATION](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), or [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_JOIN](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) |
| `config` | [WifiP2pConfig](../android/net/wifi/p2p/WifiP2pConfig.md):is the peer configuration. This value cannot be`null`. |
| `device` | [WifiP2pDevice](../android/net/wifi/p2p/WifiP2pDevice.md):is the peer information. This value cannot be`null`. |
| --- | --- |

### onDetached

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDetached(
    deviceAddress: MacAddress, 
    reason: Int
): Unit
```

Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](../android/net/wifi/p2p/WifiP2pManager.md))has failed.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](../android/net/MacAddress.md):is the peer MAC address used in the registration. This value cannot be`null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the failure reason. Value is [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REMOVE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_FAILURE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REPLACE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md), or [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_CLOSE](../android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener.md) |

### onPasswordGenerated

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPasswordGenerated(
    deviceAddress: MacAddress, 
    password: String
): Unit
```

Called when a Wi-Fi Direct R2 pairing bootstrapping password is generated by the WiFi service. The external approver can display the password, exchange the password via Out-Of-Band way or ask the wifi service to show the password as usual using the [setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,int,android.net.wifi.p2p.WifiP2pManager.ActionListener)](../android/net/wifi/p2p/WifiP2pManager.md))with [CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE](../android/net/wifi/p2p/WifiP2pManager.md).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](../android/net/MacAddress.md):is the peer MAC address used in the registration. This value cannot be`null`. |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):is a Wi-Fi Direct R2 pairing bootstrapping password. This value cannot be`null`. |

### onPinGenerated

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPinGenerated(
    deviceAddress: MacAddress, 
    pin: String
): Unit
```

Called when a WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN is generated by the WiFi service. The external approver can display the PIN, exchange the PIN via Out-Of-Band way or ask the wifi service to show the PIN as usual using the [setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,int,android.net.wifi.p2p.WifiP2pManager.ActionListener)](../android/net/wifi/p2p/WifiP2pManager.md))with [CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE](../android/net/wifi/p2p/WifiP2pManager.md).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](../android/net/MacAddress.md):is the peer MAC address used in the registration. This value cannot be`null`. |
| `pin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):is a WPS PIN or a Wi-Fi Direct R2 pairing bootstrapping PIN. This value cannot be`null`. |
