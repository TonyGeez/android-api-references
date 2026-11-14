# WifiP2pServiceInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pServiceInfo

Kotlin| [Java](WifiP2pServiceInfo.md) 
| --- | --- |

```
open class WifiP2pServiceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pServiceInfo](WifiP2pServiceInfo.md) |

| Known Direct Subclasses [WifiP2pDnsSdServiceInfo](WifiP2pDnsSdServiceInfo.md), [WifiP2pUpnpServiceInfo](WifiP2pUpnpServiceInfo.md) |----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------| | [WifiP2pDnsSdServiceInfo](WifiP2pDnsSdServiceInfo.md) | A class for storing Bonjour service information that is advertised over a Wi-Fi peer-to-peer setup. | | [WifiP2pUpnpServiceInfo](WifiP2pUpnpServiceInfo.md) | A class for storing Upnp service information that is advertised over a Wi-Fi peer-to-peer setup. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A class for storing service information that is advertised over a Wi-Fi peer-to-peer setup

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_ALL](WifiP2pServiceInfo.md) All service protocol types. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_BONJOUR](WifiP2pServiceInfo.md) DNS based service discovery protocol. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_UPNP](WifiP2pServiceInfo.md) UPnP protocol. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SERVICE_TYPE_VENDOR_SPECIFIC](WifiP2pServiceInfo.md) Vendor Specific protocol |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WifiP2pServiceInfo](WifiP2pServiceInfo.md))`(`usdConfig:` ` [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md)`)` Constructor for creating a service information for advertising the service using un-synchronized service discovery (USD) protocol. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](WifiP2pServiceInfo.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md)? | [getWifiP2pUsdBasedServiceConfig](WifiP2pServiceInfo.md))`()` Get the service information configured to advertise using un-synchronized service discovery (USD) protocol. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](WifiP2pServiceInfo.md))`()` <br /> |
| --- | --- |

## Constants

### SERVICE_TYPE_ALL

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_TYPE_ALL: Int
```

All service protocol types. 

 Value: 0

### SERVICE_TYPE_BONJOUR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_TYPE_BONJOUR: Int
```

DNS based service discovery protocol. 

 Value: 1

### SERVICE_TYPE_UPNP

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_TYPE_UPNP: Int
```

UPnP protocol. 

 Value: 2

### SERVICE_TYPE_VENDOR_SPECIFIC

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SERVICE_TYPE_VENDOR_SPECIFIC: Int
```

Vendor Specific protocol 

 Value: 255

## Public constructors

### WifiP2pServiceInfo

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WifiP2pServiceInfo(usdConfig: WifiP2pUsdBasedServiceConfig)
```

Constructor for creating a service information for advertising the service using un-synchronized service discovery (USD) protocol. Refer Wi-Fi Alliance Wi-Fi Direct R2 specification section 3.7 - "Unsynchronized Service Discovery (USD)" for the details.

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `usdConfig` | [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md):See [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md) This value cannot be`null`. |

| Return ||
|---|----------------------------------------------------------|
| | service info containing USD based service configuration. |

## Public methods

### equals

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getWifiP2pUsdBasedServiceConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWifiP2pUsdBasedServiceConfig(): WifiP2pUsdBasedServiceConfig?
```

Get the service information configured to advertise using un-synchronized service discovery (USD) protocol. See [WifiP2pServiceInfo(android.net.wifi.p2p.nsd.WifiP2pUsdBasedServiceConfig)](WifiP2pServiceInfo.md))

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md)? | A valid or not null [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md) if the service information is configured to advertise using un-synchronized service discovery (USD) protocol. Otherwise, it is null. |

### hashCode

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |
