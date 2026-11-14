# WifiP2pDnsSdServiceRequest

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pDnsSdServiceRequest

Kotlin| [Java](https://developer.android.com/reference/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest "View this page in Java") 

```
open class WifiP2pDnsSdServiceRequest : WifiP2pServiceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest) ||
| | ↳ | [android.net.wifi.p2p.nsd.WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#) |

A class for creating a Bonjour service discovery request for use with [WifiP2pManager.addServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#addServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener))and [WifiP2pManager.removeServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/WifiP2pManager.html#removeServiceRequest(android.net.wifi.p2p.WifiP2pManager.Channel,%20android.net.wifi.p2p.nsd.WifiP2pServiceRequest,%20android.net.wifi.p2p.WifiP2pManager.ActionListener)){@see WifiP2pManager} {@see WifiP2pServiceRequest} {@see WifiP2pUpnpServiceRequest}

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#newInstance())`()` Create a service discovery request to search all Bonjour services. |
| openstatic [WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#newInstance(kotlin.String))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a service discovery to search for Bonjour services with the specified service type. |
| openstatic [WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#newInstance(kotlin.String,%20kotlin.String))`(`instanceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a service discovery request to get the TXT data from the specified Bonjour service. |

| Inherited functions ||
|---|---|
| From class [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest) |---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [WifiP2pUsdBasedServiceConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pUsdBasedServiceConfig)? | [getWifiP2pUsdBasedServiceConfig](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#getWifiP2pUsdBasedServiceConfig())`()` <br /> /\*\* Get the service information configured to discover a service using un-synchronized service discovery (USD) protocol. See [WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#hashCode())`()` <br /> | | [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#newInstance(kotlin.Int))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Create a service discovery request. <br /> | | [WifiP2pServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest)! | [newInstance](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#newInstance(kotlin.Int,%20kotlin.String))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `queryData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a service discovery request. <br /> | ||

## Public methods

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): WifiP2pDnsSdServiceRequest!
```

Create a service discovery request to search all Bonjour services.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#)! | service request for Bonjour. |

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(serviceType: String!): WifiP2pDnsSdServiceRequest!
```

Create a service discovery to search for Bonjour services with the specified service type.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `serviceType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:service type. Cannot be null "_afpovertcp._tcp."(Apple File Sharing over TCP) "_ipp._tcp" (IP Printing over TCP) "_http._tcp" (http service) |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| [WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#)! | service request for DnsSd. |

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(
    instanceName: String!, 
    serviceType: String!
): WifiP2pDnsSdServiceRequest!
```

Create a service discovery request to get the TXT data from the specified Bonjour service.

| Parameters ||
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `instanceName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:instance name. Cannot be null. "MyPrinter" |
| `serviceType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:service type. Cannot be null. e.g) "_afpovertcp._tcp"(Apple File Sharing over TCP) "_ipp._tcp" (IP Printing over TCP) |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [WifiP2pDnsSdServiceRequest](https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pDnsSdServiceRequest#)! | service request for Bonjour. |
