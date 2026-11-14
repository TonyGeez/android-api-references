Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WifiP2pServiceRequest

Kotlin | [Java](WifiP2pServiceRequest.md)
| --- | --- |

```
open class WifiP2pServiceRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.wifi.p2p.nsd.WifiP2pServiceRequest](WifiP2pServiceRequest.md) |

| Known Direct Subclasses [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md), [WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md) |---|---| | [WifiP2pDnsSdServiceRequest](WifiP2pDnsSdServiceRequest.md) | A class for creating a Bonjour service discovery request for use with addServiceRequest and removeServiceRequest | | [WifiP2pUpnpServiceRequest](WifiP2pUpnpServiceRequest.md) | A class for creating a Upnp service discovery request for use with addServiceRequest and removeServiceRequest | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

A class for creating a service discovery request for use with addServiceRequest and removeServiceRequest

This class is used to create service discovery request for custom vendor specific service discovery protocol `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_VENDOR_SPECIFIC:kotlin.Int` or to search all service protocols `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_ALL:kotlin.Int`.

For the purpose of creating a UPnP or Bonjour service request, use WifiP2pUpnpServiceRequest or WifiP2pDnsSdServiceRequest respectively.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| WifiP2pServiceRequest Constructor for creating a service discovery request for discovering the service using un-synchronized service discovery (USD) protocol. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Implement the Parcelable interface |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | equals Indicates whether some other object is "equal to" this one. |
| open [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md)? | getWifiP2pUsdBasedServiceConfig /\*\* Get the service information configured to discover a service using un-synchronized service discovery (USD) protocol. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | hashCode Returns a hash code value for the object. |
| open static [WifiP2pServiceRequest](WifiP2pServiceRequest.md)! | newInstance Create a service discovery request. |
| open static [WifiP2pServiceRequest](WifiP2pServiceRequest.md)! | newInstance Create a service discovery request. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Implement the Parcelable interface |

## Public constructors

### WifiP2pServiceRequest

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
WifiP2pServiceRequest(usdConfig: WifiP2pUsdBasedServiceConfig)
```

Constructor for creating a service discovery request for discovering the service using un-synchronized service discovery (USD) protocol. Refer Wi-Fi Alliance Wi-Fi Direct R2 specification section 3.7 - "Unsynchronized Service Discovery (USD)" for the details.

| Parameters ||
|---|---|
| `usdConfig` | [WifiP2pUsdBasedServiceConfig](WifiP2pUsdBasedServiceConfig.md): See WifiP2pUsdBasedServiceConfig This value cannot be `null`. |

| Return ||
|---|---|
| | service discovery request containing USD based service configuration. |

## Public methods

### describeContents

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun equals(other: Any?): Boolean
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

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getWifiP2pUsdBasedServiceConfig

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWifiP2pUsdBasedServiceConfig(): WifiP2pUsdBasedServiceConfig?
```

/\*\* Get the service information configured to discover a service using un-synchronized service discovery (USD) protocol. See WifiP2pServiceRequest.

| Return ||
|---|---|
| WifiP2pUsdBasedServiceConfig | A valid or not null WifiP2pUsdBasedServiceConfig if the service information is configured to discover a service using un-synchronized service discovery (USD) protocol. Otherwise, it is null. |

### hashCode

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the equals method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the equals method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(protocolType: Int): WifiP2pServiceRequest!
```

Create a service discovery request.

| Parameters ||
|---|---|
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): can be `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_ALL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_VENDOR_SPECIFIC:kotlin.Int`. In order to create a UPnP or Bonjour service request, use WifiP2pUpnpServiceRequest or WifiP2pDnsSdServiceRequest respectively |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#!` | service discovery request. |

### newInstance

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun newInstance(
    protocolType: Int, 
    queryData: String!
): WifiP2pServiceRequest!
```

Create a service discovery request.

| Parameters ||
|---|---|
| `protocolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): can be `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_ALL:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceInfo#SERVICE_TYPE_VENDOR_SPECIFIC:kotlin.Int`. In order to create a UPnP or Bonjour service request, use WifiP2pUpnpServiceRequest or WifiP2pDnsSdServiceRequest respectively |
| `queryData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: hex string that is vendor specific. Can be null. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/wifi/p2p/nsd/WifiP2pServiceRequest#!` | service discovery request. |

### writeToParcel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |
