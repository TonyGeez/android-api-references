# WifiP2pUpnpServiceRequest

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pUpnpServiceRequest

Kotlin| [Java](WifiP2pUpnpServiceRequest.md) 
| --- | --- |

```
open class WifiP2pUpnpServiceRequest : WifiP2pServiceRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pServiceRequest](WifiP2pServiceRequest.md) ||
| | ↳ | [android.net.wifi.p2p.nsd.WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md) |

A class for creating a Upnp service discovery request for use with [WifiP2pManager.addServiceRequest](../android.net.wifi.p2p/WifiP2pManager.md))and [WifiP2pManager.removeServiceRequest](../android.net.wifi.p2p/WifiP2pManager.md)){@see WifiP2pManager} {@see WifiP2pServiceRequest} {@see WifiP2pDnsSdServiceRequest}

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md)! | [newInstance](WifiP2pUpnpServiceRequest.md))`()` Create a service discovery request to search all UPnP services. |
| openstatic [WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md)! | [newInstance](WifiP2pUpnpServiceRequest.md))`(`st:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Create a service discovery request to search specified UPnP services. |

| Inherited functions ||
|---|---|
| From class [WifiP2pServiceRequest](WifiP2pServiceRequest.md) |---------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WifiP2pServiceRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> | | [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md)? | [getWifiP2pUsdBasedServiceConfig](WifiP2pServiceRequest.md))`()` <br /> /\*\* Get the service information configured to discover a service using un-synchronized service discovery (USD) protocol. See [WifiP2pServiceRequest(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)](WifiP2pServiceRequest.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WifiP2pServiceRequest.md))`()` <br /> | | [WifiP2pServiceRequest](WifiP2pServiceRequest.md)! | [newInstance](WifiP2pServiceRequest.md))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Create a service discovery request. <br /> | | [WifiP2pServiceRequest](WifiP2pServiceRequest.md)! | [newInstance](WifiP2pServiceRequest.md))`(`protocolType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `queryData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Create a service discovery request. <br /> | ||

## Public methods

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun newInstance(): WifiP2pUpnpServiceRequest!
```

Create a service discovery request to search all UPnP services.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| [WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md)! | service request for UPnP. |

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
| [WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md)! | service request for UPnP. |
