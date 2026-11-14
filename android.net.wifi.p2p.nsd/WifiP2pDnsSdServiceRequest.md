# WifiP2pDnsSdServiceRequest

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pDnsSdServiceRequest

Kotlin| [Java](WifiP2pDnsSdServiceRequest.md) 
| --- | --- |

```
open class WifiP2pDnsSdServiceRequest : WifiP2pServiceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pServiceRequest](WifiP2pServiceRequest.md) ||
| | ↳ | [android.net.wifi.p2p.nsd.WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md) |

A class for creating a Bonjour service discovery request for use with [WifiP2pManager.addServiceRequest](../android.net.wifi.p2p/WifiP2pManager.md))and [WifiP2pManager.removeServiceRequest](../android.net.wifi.p2p/WifiP2pManager.md)){@see WifiP2pManager} {@see WifiP2pServiceRequest} {@see WifiP2pUpnpServiceRequest}

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md)! | [newInstance](WifiP2pDnsSdServiceRequest.md))`()` Create a service discovery request to search all Bonjour services. |
| openstatic [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md)! | [newInstance](WifiP2pDnsSdServiceRequest.md))`(`serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a service discovery to search for Bonjour services with the specified service type. |
| openstatic [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md)! | [newInstance](WifiP2pDnsSdServiceRequest.md))`(`instanceName:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `serviceType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a service discovery request to get the TXT data from the specified Bonjour service. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [WifiP2pServiceRequest](WifiP2pServiceRequest.md) |---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WifiP2pServiceRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md)? | [getWifiP2pUsdBasedServiceConfig](WifiP2pServiceRequest.md))`()` <br /> /\*\* Get the service information configured to discover a service using un-synchronized service discovery (USD) protocol. See [WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)](WifiP2pServiceRequest.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WifiP2pServiceRequest.md))`()` <br /> | | [WifiP2pServiceRequest](WifiP2pServiceRequest.md)! | [newInstance](WifiP2pServiceRequest.md))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Create a service discovery request. <br /> | | [WifiP2pServiceRequest](WifiP2pServiceRequest.md)! | [newInstance](WifiP2pServiceRequest.md))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `queryData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a service discovery request. <br /> | ||

## Public methods

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): WifiP2pDnsSdServiceRequest!
```

Create a service discovery request to search all Bonjour services.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md)! | service request for Bonjour. |

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
| [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md)! | service request for DnsSd. |

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
| [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md)! | service request for Bonjour. |
