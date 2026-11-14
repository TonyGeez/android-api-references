# WifiP2pManager.ExternalApproverRequestListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ExternalApproverRequestListener

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener "View this page in Java") 

```
interface ExternalApproverRequestListener
```

| [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#) |

Interface for callback invocation when an incoming request is received. This callback is registered by [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)).

## Summary

| Constants ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_CLOSE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_CLOSE:kotlin.Int) Detached since the [WifiP2pManager](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager) channel was closed, e. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_FAILURE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_FAILURE:kotlin.Int) Detached due to a framework failure. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_REMOVE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REMOVE:kotlin.Int) Detached by a call to [removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ActionListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [APPROVER_DETACH_REASON_REPLACE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REPLACE:kotlin.Int) Detached when a new approver replaces an old one. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_INVITATION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_INVITATION:kotlin.Int) This device received an invitation request from GO to join the group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_JOIN](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_JOIN:kotlin.Int) This GO device received a request from a peer to join the group. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [REQUEST_TYPE_NEGOTIATION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_NEGOTIATION:kotlin.Int) This device received a negotiation request from another peer. |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAttached](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onAttached(android.net.MacAddress))`(`deviceAddress:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)`)` Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener))is successful. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onConnectionRequested](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onConnectionRequested(kotlin.Int,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pDevice))`(`requestType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `config:` ` [WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig)`, `device:` ` [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice)`)` Called when there is an incoming connection request which matches a peer (identified by its [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)) registered by the external approver through [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDetached](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onDetached(android.net.MacAddress,%20kotlin.Int))`(`deviceAddress:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)`, `reason:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener))has failed. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPasswordGenerated](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onPasswordGenerated(android.net.MacAddress,%20kotlin.String))`(`deviceAddress:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)`, `password:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called when a Wi-Fi Direct R2 pairing bootstrapping password is generated by the WiFi service. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPinGenerated](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onPinGenerated(android.net.MacAddress,%20kotlin.String))`(`deviceAddress:` ` [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)`, `pin:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Called when a WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN is generated by the WiFi service. |

## Constants

### APPROVER_DETACH_REASON_CLOSE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_CLOSE: Int
```

Detached since the [WifiP2pManager](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager) channel was closed, e.g. by using [Channel.close()](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.Channel#close())method. Used in [onDetached(android.net.MacAddress,int)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onDetached(android.net.MacAddress,%20kotlin.Int)). 

 Value: 3

### APPROVER_DETACH_REASON_FAILURE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_FAILURE: Int
```

Detached due to a framework failure. Used in [onDetached(android.net.MacAddress,int)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onDetached(android.net.MacAddress,%20kotlin.Int)). 

 Value: 1

### APPROVER_DETACH_REASON_REMOVE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_REMOVE: Int
```

Detached by a call to [removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ActionListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#removeExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)). Used in [onDetached(android.net.MacAddress,int)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onDetached(android.net.MacAddress,%20kotlin.Int)). 

 Value: 0

### APPROVER_DETACH_REASON_REPLACE

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val APPROVER_DETACH_REASON_REPLACE: Int
```

Detached when a new approver replaces an old one. Used in [onDetached(android.net.MacAddress,int)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onDetached(android.net.MacAddress,%20kotlin.Int)). 

 Value: 2

### REQUEST_TYPE_INVITATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_INVITATION: Int
```

This device received an invitation request from GO to join the group. Used in [onConnectionRequested(int,android.net.wifi.p2p.WifiP2pConfig,android.net.wifi.p2p.WifiP2pDevice)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onConnectionRequested(kotlin.Int,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pDevice)). 

 Value: 1

### REQUEST_TYPE_JOIN

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_JOIN: Int
```

This GO device received a request from a peer to join the group. Used in [onConnectionRequested(int,android.net.wifi.p2p.WifiP2pConfig,android.net.wifi.p2p.WifiP2pDevice)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onConnectionRequested(kotlin.Int,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pDevice)). 

 Value: 2

### REQUEST_TYPE_NEGOTIATION

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val REQUEST_TYPE_NEGOTIATION: Int
```

This device received a negotiation request from another peer. Used in [onConnectionRequested(int,android.net.wifi.p2p.WifiP2pConfig,android.net.wifi.p2p.WifiP2pDevice)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#onConnectionRequested(kotlin.Int,%20android.net.wifi.p2p.WifiP2pConfig,%20android.net.wifi.p2p.WifiP2pDevice)). 

 Value: 0

## Public methods

### onAttached

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onAttached(deviceAddress: MacAddress): Unit
```

Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener))is successful.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#):is the peer MAC address used in the registration. This value cannot be`null`. |

### onConnectionRequested

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onConnectionRequested(
    requestType: Int, 
    config: WifiP2pConfig, 
    device: WifiP2pDevice
): Unit
```

Called when there is an incoming connection request which matches a peer (identified by its [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#)) registered by the external approver through [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)). The external approver is expected to follow up with a connection decision using the [setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,int,android.net.wifi.p2p.WifiP2pManager.ActionListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener))with [CONNECTION_REQUEST_ACCEPT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_ACCEPT:kotlin.Int), [CONNECTION_REQUEST_REJECT](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_REJECT:kotlin.Int), or [CONNECTION_REQUEST_DEFER_TO_SERVICE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_TO_SERVICE:kotlin.Int).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `requestType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is one of [REQUEST_TYPE_NEGOTIATION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_NEGOTIATION:kotlin.Int), [REQUEST_TYPE_INVITATION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_INVITATION:kotlin.Int), and [REQUEST_TYPE_JOIN](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_JOIN:kotlin.Int). Value is [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_NEGOTIATION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_NEGOTIATION:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_INVITATION](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_INVITATION:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_JOIN](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#REQUEST_TYPE_JOIN:kotlin.Int) |
| `config` | [WifiP2pConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pConfig):is the peer configuration. This value cannot be`null`. |
| `device` | [WifiP2pDevice](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pDevice):is the peer information. This value cannot be`null`. |

### onDetached

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDetached(
    deviceAddress: MacAddress, 
    reason: Int
): Unit
```

Called when an approver registration via [addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#addExternalApprover(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener))has failed.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#):is the peer MAC address used in the registration. This value cannot be`null`. |
| `reason` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):is the failure reason. Value is [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REMOVE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REMOVE:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_FAILURE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_FAILURE:kotlin.Int), [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REPLACE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_REPLACE:kotlin.Int), or [android.net.wifi.p2p.WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_CLOSE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.ExternalApproverRequestListener#APPROVER_DETACH_REASON_CLOSE:kotlin.Int) |

### onPasswordGenerated

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onPasswordGenerated(
    deviceAddress: MacAddress, 
    password: String
): Unit
```

Called when a Wi-Fi Direct R2 pairing bootstrapping password is generated by the WiFi service. The external approver can display the password, exchange the password via Out-Of-Band way or ask the wifi service to show the password as usual using the [setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,int,android.net.wifi.p2p.WifiP2pManager.ActionListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener))with [CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PASSWORD_TO_SERVICE:kotlin.Int).

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#):is the peer MAC address used in the registration. This value cannot be`null`. |
| `password` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):is a Wi-Fi Direct R2 pairing bootstrapping password. This value cannot be`null`. |

### onPinGenerated

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPinGenerated(
    deviceAddress: MacAddress, 
    pin: String
): Unit
```

Called when a WPS PIN or Wi-Fi Direct R2 pairing bootstrapping PIN is generated by the WiFi service. The external approver can display the PIN, exchange the PIN via Out-Of-Band way or ask the wifi service to show the PIN as usual using the [setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,android.net.MacAddress,int,android.net.wifi.p2p.WifiP2pManager.ActionListener)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#setConnectionRequestResult(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.MacAddress,%20kotlin.Int,%20android.net.wifi.p2p.WifiP2pManager.ActionListener))with [CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager#CONNECTION_REQUEST_DEFER_SHOW_PIN_TO_SERVICE:kotlin.Int).

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `deviceAddress` | [MacAddress](https://developer.android.com/reference/kotlin/android/net/MacAddress.html#):is the peer MAC address used in the registration. This value cannot be`null`. |
| `pin` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):is a WPS PIN or a Wi-Fi Direct R2 pairing bootstrapping PIN. This value cannot be`null`. |
