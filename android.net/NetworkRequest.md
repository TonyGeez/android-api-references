# NetworkRequest

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NetworkRequest

Kotlin| [Java](../android/net/NetworkRequest.md) 
| --- | --- |

```
open class NetworkRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.NetworkRequest](../android/net/NetworkRequest.md) |

An object describing a network that the application is interested in.

@see [NetworkRequest.Builder](https://developer.android.com/training/basics/network-ops/reading-network-state> this general guide</a> on how to use NetworkCapabilities and related classes. NetworkRequest defines a request for a network, made through <code><a docref=) and used to request a network via android.net.ConnectivityManager#requestNetwork or to listen for changes via the android.net.ConnectivityManager#registerNetworkCallback family of functions.

android.net.ConnectivityManager#requestNetwork will try to find a connected network matching the NetworkRequest, and return it if there is one. As long as the request is outstanding, the system will try to find the best possible network that matches the request. The request will keep up the currently best connected network, and if a better one is found (e.g. cheaper or faster) the system will bring up that better network to better serve the request. A request filed with android.net.ConnectivityManager#requestNetwork will only match one network at a time (the one the system thinks is best), even if other networks can match the request that are being kept up by other requests. For example, an application needing a network with [NetworkCapabilities.NET_CAPABILITY_INTERNET](../android/net/NetworkCapabilities.md) should use android.net.ConnectivityManager#requestNetwork to request the system keeps one up. A general cellular network can satisfy this request, but if the system finds a free Wi-Fi network which is expected to be faster, it will try and connect to that Wi-Fi network and switch the request over to it once it is connected. The cell network may stay connected if there are outstanding requests (from the same app or from other apps on the system) that match the cell network but not the Wi-Fi network, such as a request with [NetworkCapabilities.NET_CAPABILITY_MMS](../android/net/NetworkCapabilities.md). When a network is no longer needed to serve any request, the system can tear it down at any time and usually does so immediately, so make sure to keep up requests for the networks your app needs.

By contrast, requests filed with android.net.ConnectivityManager#registerNetworkCallback will receive callbacks for all matching networks, and will not cause the system to keep up the networks they match. Use this to listen to networks that the device is connected to, but that you don't want the system to keep up for your use case.

Applications build a NetworkRequest and pass it to one of the [ConnectivityManager](../android/net/ConnectivityManager.md) methods above together with a [ConnectivityManager.NetworkCallback](../android/net/ConnectivityManager.NetworkCallback.md) object. The callback will then start receiving method calls about networks that match the request.

Networks are brought up and/or matched according to the capabilities set in the builder. For example, a request with [NetworkCapabilities.NET_CAPABILITY_MMS](../android/net/NetworkCapabilities.md) lets the system match and/or bring up a network that is capable to send MMS. A request with [NetworkCapabilities.NET_CAPABILITY_NOT_METERED](../android/net/NetworkCapabilities.md) matches a network that doesn't charge the user for usage. See [NetworkCapabilities](../android/net/NetworkCapabilities.md) for a list of capabilities and their description.

While all capabilities can be matched with the android.net.ConnectivityManager#registerNetworkCallback family of methods, not all capabilities can be used to request that the system brings up a network with android.net.ConnectivityManager#requestNetwork. For example, an application cannot use android.net.ConnectivityManager#requestNetwork to ask the system to bring up a network with [NetworkCapabilities.NET_CAPABILITY_CAPTIVE_PORTAL](../android/net/NetworkCapabilities.md), because the system won't know if a network has a captive portal before it connects to that network. Similarly, some capabilities may require a specific permission or privilege to be requested. Look up the specific capability and the android.net.ConnectivityManager#requestNetwork method for limitations applicable to each capability.

Also, starting with [Build.VERSION_CODES.UPSIDE_DOWN_CAKE](../android/os/Build.VERSION_CODES.md), some capabilities require the application to self-certify by explicitly adding the [android.content.pm.PackageManager#PROPERTY_SELF_CERTIFIED_NETWORK_CAPABILITIES](../android/content/pm/PackageManager.md) property in the AndroidManifest.xml, which points to an XML resource file. In the XML resource file, the application declares what kind of network capabilities the application wants to have. Here is an example self-certification XML resource file : 

```kotlin
<code>&lt;network-capabilities-declaration xmlns:android="http://schemas.android.com/apk/res/android"&gt;
      &lt;uses-network-capability android:name="NET_CAPABILITY_PRIORITIZE_LATENCY"/&gt;
      &lt;uses-network-capability android:name="NET_CAPABILITY_PRIORITIZE_BANDWIDTH"/&gt;
  &lt;/network-capabilities-declaration&gt;
   </code>
```
Look up the specific capability to learn whether its usage requires this self-certification.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/net/NetworkRequest.Builder.md) Builder used to create [NetworkRequest](../android/net/NetworkRequest.md) objects. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [canBeSatisfiedBy](../android/net/NetworkRequest.md))`(`nc:` ` [NetworkCapabilities](../android/net/NetworkCapabilities.md)?`)` Returns true if and only if the capabilities requested in this NetworkRequest are satisfied by the provided [NetworkCapabilities](../android/net/NetworkCapabilities.md). |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/NetworkRequest.md))`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/NetworkRequest.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getCapabilities](../android/net/NetworkRequest.md))`()` Gets all the capabilities set on this`NetworkRequest`instance. |
| open [NetworkSpecifier](../android/net/NetworkSpecifier.md)? | [getNetworkSpecifier](../android/net/NetworkRequest.md))`()` <br /> |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!\> | [getSubscriptionIds](../android/net/NetworkRequest.md))`()` Gets all the subscription ids set on this`NetworkRequest`instance. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getTransportTypes](../android/net/NetworkRequest.md))`()` Gets all the transports set on this`NetworkRequest`instance. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasCapability](../android/net/NetworkRequest.md))`(`capability:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasTransport](../android/net/NetworkRequest.md))`(`transportType:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/NetworkRequest.md))`()` <br /> |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/NetworkRequest.md))`()` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/NetworkRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NetworkRequest](../android/net/NetworkRequest.md)!\> | [CREATOR](../android/net/NetworkRequest.md) <br /> |

## Public methods

### canBeSatisfiedBy

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun canBeSatisfiedBy(nc: NetworkCapabilities?): Boolean
```

Returns true if and only if the capabilities requested in this NetworkRequest are satisfied by the provided [NetworkCapabilities](../android/net/NetworkCapabilities.md).

| Parameters ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `nc` | [NetworkCapabilities](../android/net/NetworkCapabilities.md)?:Capabilities that should satisfy this NetworkRequest. null capabilities do not satisfy any request. |

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|--------------------------|
| `obj` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getCapabilities

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCapabilities(): IntArray
```

Gets all the capabilities set on this`NetworkRequest`instance.

| Return ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | an array of capability values for this instance. This value cannot be`null`. Value is [android.net.NetworkCapabilities#NET_CAPABILITY_MMS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_SUPL](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_DUN](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_FOTA](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_IMS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_CBS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_WIFI_P2P](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_IA](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_RCS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_XCAP](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_EIMS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_METERED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_INTERNET](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_RESTRICTED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_TRUSTED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_VPN](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_VALIDATED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_ROAMING](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_FOREGROUND](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_CONGESTED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_SUSPENDED](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_OEM_PAID, [android.net.NetworkCapabilities#NET_CAPABILITY_MCX](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_PARTIAL_CONNECTIVITY, [android.net.NetworkCapabilities#NET_CAPABILITY_TEMPORARILY_NOT_METERED](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_OEM_PRIVATE, android.net.NetworkCapabilities.NET_CAPABILITY_VEHICLE_INTERNAL, android.net.NetworkCapabilities.NET_CAPABILITY_NOT_VCN_MANAGED, [android.net.NetworkCapabilities#NET_CAPABILITY_ENTERPRISE](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_VSIM, android.net.NetworkCapabilities.NET_CAPABILITY_BIP, [android.net.NetworkCapabilities#NET_CAPABILITY_HEAD_UNIT](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_MMTEL](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_LATENCY](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_BANDWIDTH](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_LOCAL_NETWORK](../android/net/NetworkCapabilities.md), or [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED](../android/net/NetworkCapabilities.md) |

### getNetworkSpecifier

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNetworkSpecifier(): NetworkSpecifier?
```

| Return ||
|--------------------------------------------------------------------------------------------------|--------------------------|
| [NetworkSpecifier](../android/net/NetworkSpecifier.md)? | This value may be`null`. |

**See Also**

- [android.net.NetworkRequest.Builder#setNetworkSpecifier(NetworkSpecifier)](../android/net/NetworkRequest.Builder.md)) 

### getSubscriptionIds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [U Extensions 12](https://developer.android.com/sdkExtensions) 

```
open fun getSubscriptionIds(): MutableSet<Int!>
```

Gets all the subscription ids set on this`NetworkRequest`instance.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)!> | Set of Integer values for this instance. This value cannot be`null`. |

### getTransportTypes

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getTransportTypes(): IntArray
```

Gets all the transports set on this`NetworkRequest`instance.

| Return ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | an array of transport type values for this instance. This value cannot be`null`. Value is [android.net.NetworkCapabilities#TRANSPORT_CELLULAR](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_WIFI](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_BLUETOOTH](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_ETHERNET](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_VPN](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_WIFI_AWARE](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_LOWPAN](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.TRANSPORT_TEST, [android.net.NetworkCapabilities#TRANSPORT_USB](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_THREAD](../android/net/NetworkCapabilities.md), or [android.net.NetworkCapabilities#TRANSPORT_SATELLITE](../android/net/NetworkCapabilities.md) |

### hasCapability

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasCapability(capability: Int): Boolean
```

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `capability` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.NetworkCapabilities#NET_CAPABILITY_MMS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_SUPL](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_DUN](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_FOTA](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_IMS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_CBS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_WIFI_P2P](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_IA](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_RCS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_XCAP](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_EIMS](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_METERED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_INTERNET](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_RESTRICTED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_TRUSTED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_VPN](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_VALIDATED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_CAPTIVE_PORTAL](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_ROAMING](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_FOREGROUND](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_CONGESTED](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_SUSPENDED](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_OEM_PAID, [android.net.NetworkCapabilities#NET_CAPABILITY_MCX](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_PARTIAL_CONNECTIVITY, [android.net.NetworkCapabilities#NET_CAPABILITY_TEMPORARILY_NOT_METERED](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_OEM_PRIVATE, android.net.NetworkCapabilities.NET_CAPABILITY_VEHICLE_INTERNAL, android.net.NetworkCapabilities.NET_CAPABILITY_NOT_VCN_MANAGED, [android.net.NetworkCapabilities#NET_CAPABILITY_ENTERPRISE](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.NET_CAPABILITY_VSIM, android.net.NetworkCapabilities.NET_CAPABILITY_BIP, [android.net.NetworkCapabilities#NET_CAPABILITY_HEAD_UNIT](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_MMTEL](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_LATENCY](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_PRIORITIZE_BANDWIDTH](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#NET_CAPABILITY_LOCAL_NETWORK](../android/net/NetworkCapabilities.md), or [android.net.NetworkCapabilities#NET_CAPABILITY_NOT_BANDWIDTH_CONSTRAINED](../android/net/NetworkCapabilities.md) |

**See Also**

- [android.net.NetworkRequest.Builder#addCapability(int)](../android/net/NetworkRequest.Builder.md)) 

### hasTransport

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hasTransport(transportType: Int): Boolean
```

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `transportType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is [android.net.NetworkCapabilities#TRANSPORT_CELLULAR](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_WIFI](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_BLUETOOTH](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_ETHERNET](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_VPN](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_WIFI_AWARE](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_LOWPAN](../android/net/NetworkCapabilities.md), android.net.NetworkCapabilities.TRANSPORT_TEST, [android.net.NetworkCapabilities#TRANSPORT_USB](../android/net/NetworkCapabilities.md), [android.net.NetworkCapabilities#TRANSPORT_THREAD](../android/net/NetworkCapabilities.md), or [android.net.NetworkCapabilities#TRANSPORT_SATELLITE](../android/net/NetworkCapabilities.md) |

**See Also**

- [android.net.NetworkRequest.Builder#addTransportType(int)](../android/net/NetworkRequest.Builder.md)) 

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NetworkRequest!>
```
