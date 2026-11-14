# WifiP2pUpnpServiceRequest

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pUpnpServiceRequest

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest "View this page in Java") 

```
open class WifiP2pUpnpServiceRequest : WifiP2pServiceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest) ||
| | ↳ | [android.net.wifi.p2p.nsd.WifiP2pUpnpServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#) |

A class for creating a Upnp service discovery request for use with [WifiP2pManager.addServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener))and [WifiP2pManager.removeServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#removeServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)){@see WifiP2pManager} {@see WifiP2pServiceRequest} {@see WifiP2pDnsSdServiceRequest}

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [WifiP2pUpnpServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#newInstance())`()` Create a service discovery request to search all UPnP services. |
| openstatic [WifiP2pUpnpServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#newInstance(kotlin.String))`(`st:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a service discovery request to search specified UPnP services. |

| Inherited functions ||
|---|---|
| From class [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest) |---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [WifiP2pUsdBasedServiceConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig)? | [getWifiP2pUsdBasedServiceConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#getWifiP2pUsdBasedServiceConfig())`()` <br /> /\*\* Get the service information configured to discover a service using un-synchronized service discovery (USD) protocol. See [WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#hashCode())`()` <br /> | | [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#newInstance(kotlin.Int))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Create a service discovery request. <br /> | | [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#newInstance(kotlin.Int,%20kotlin.String))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `queryData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a service discovery request. <br /> | ||

## Public methods

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): WifiP2pUpnpServiceRequest!
```

Create a service discovery request to search all UPnP services.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [WifiP2pUpnpServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#)! | service request for UPnP. |

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(st: String!): WifiP2pUpnpServiceRequest!
```

Create a service discovery request to search specified UPnP services.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `st` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:ssdp search target. Cannot be null. e.g ) - "ssdp:all" - "upnp:rootdevice" - "urn:schemas-upnp-org:device:MediaServer:2" - "urn:schemas-upnp-org:service:ContentDirectory:2" - "uuid:6859dede-8574-59ab-9332-123456789012" |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [WifiP2pUpnpServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUpnpServiceRequest#)! | service request for UPnP. |
