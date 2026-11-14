# NsdServiceInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NsdServiceInfo

Kotlin| [Java](../android/net/nsd/NsdServiceInfo.md) 
| --- | --- |

```
class NsdServiceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.nsd.NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md) |

A class representing service information for network service discovery

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/nsd/NsdServiceInfo.md))`()` Implement the Parcelable interface |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | [getAttributes](../android/net/nsd/NsdServiceInfo.md))`()` Retrieve attributes as a map of String keys to byte\[\] values. |
| [InetAddress](../java/net/InetAddress.md)! | [getHost](../android/net/nsd/NsdServiceInfo.md))`()` Get the host address. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](../java/net/InetAddress.md)!\> | [getHostAddresses](../android/net/nsd/NsdServiceInfo.md))`()` Get the host addresses. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHostname](../android/net/nsd/NsdServiceInfo.md))`()` Get the hostname. |
| [Network](../android/net/Network.md)? | [getNetwork](../android/net/nsd/NsdServiceInfo.md))`()` Get the network where the service can be found. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](../android/net/nsd/NsdServiceInfo.md))`()` Get port number. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceName](../android/net/nsd/NsdServiceInfo.md))`()` Get the service name |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceType](../android/net/nsd/NsdServiceInfo.md))`()` Get the service type |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSubtypes](../android/net/nsd/NsdServiceInfo.md))`()` Returns subtypes of this service instance. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAttribute](../android/net/nsd/NsdServiceInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove an attribute by key |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](../android/net/nsd/NsdServiceInfo.md))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add a service attribute as a key/value pair. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHost](../android/net/nsd/NsdServiceInfo.md))`(`s:` ` [InetAddress](../java/net/InetAddress.md)!`)` Set the host address |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHostAddresses](../android/net/nsd/NsdServiceInfo.md))`(`addresses:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](../java/net/InetAddress.md)!>`)` Set the host addresses. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNetwork](../android/net/nsd/NsdServiceInfo.md))`(`network:` ` [Network](../android/net/Network.md)?`)` Set the network where the service can be found. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPort](../android/net/nsd/NsdServiceInfo.md))`(`p:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set port number |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceName](../android/net/nsd/NsdServiceInfo.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the service name |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceType](../android/net/nsd/NsdServiceInfo.md))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the service type |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSubtypes](../android/net/nsd/NsdServiceInfo.md))`(`subtypes:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Sets the subtypes to be advertised for this service instance. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/nsd/NsdServiceInfo.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/nsd/NsdServiceInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md)!\> | [CREATOR](../android/net/nsd/NsdServiceInfo.md) Implement the Parcelable interface |

## Public constructors

### NsdServiceInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
NsdServiceInfo()
```

## Public methods

### describeContents

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAttributes(): MutableMap<String!, ByteArray!>!
```

Retrieve attributes as a map of String keys to byte\[\] values. The attributes map is only valid for a resolved service.

The returned map is unmodifiable; changes must be made through [setAttribute](../android/net/nsd/NsdServiceInfo.md))and [removeAttribute](../android/net/nsd/NsdServiceInfo.md)). 

### getHost

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHost(): InetAddress!
```

**Deprecated:** *Use [getHostAddresses()](../android/net/nsd/NsdServiceInfo.md))to get the entire list of addresses for the host.*

Get the host address. The host address is valid for a resolved service. 

### getHostAddresses

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
fun getHostAddresses(): MutableList<InetAddress!>
```

Get the host addresses. All host addresses are valid for the resolved service. All addresses share the same port

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](../java/net/InetAddress.md)!> | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getPort()> 

### getHostname

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
fun getHostname(): String?
```

Get the hostname.

When a service is resolved through android.net.nsd.NsdManager#resolveService or [NsdManager.registerServiceInfoCallback](../android/net/nsd/NsdManager.md)), this returns the hostname of the resolved service. In all other cases, this will be null. The top level domain ".local." is omitted. For example, this returns "MyHost" when the service's hostname is "MyHost.local.". 

### getNetwork

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getNetwork(): Network?
```

Get the network where the service can be found. This is set if this [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md) was obtained from android.net.nsd.NsdManager#discoverServices or android.net.nsd.NsdManager#resolveService, unless the service was found on a network interface that does not have a [Network](../android/net/Network.md)(such as a tethering downstream, where services are advertised from devices connected to this device via tethering).

| Return ||
|--------------------------------------------------------------------------------------|--------------------------|
| [Network](../android/net/Network.md)? | This value may be`null`. |

### getPort

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPort(): Int
```

Get port number. The port number is valid for a resolved service. The port is valid for all addresses. 
**See Also**

- <https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getHostAddresses()> 

### getServiceName

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceName(): String!
```

Get the service name 

### getServiceType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getServiceType(): String!
```

Get the service type 

### getSubtypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun getSubtypes(): MutableSet<String!>
```

Returns subtypes of this service instance. When this object is returned by the service discovery/browse APIs (etc. [NsdManager.DiscoveryListener](../android/net/nsd/NsdManager.DiscoveryListener.md)), the return value may or may not include the subtypes of this service.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | This value cannot be`null`. |

### removeAttribute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun removeAttribute(key: String!): Unit
```

Remove an attribute by key 

### setAttribute

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setAttribute(
    key: String!, 
    value: String!
): Unit
```

Add a service attribute as a key/value pair.

Service attributes are included as DNS-SD TXT record pairs.

The key must be US-ASCII printable characters, excluding the '=' character. Values may be UTF-8 strings or null. The total length of key + value must be less than 255 bytes.

Keys should be short, ideally no more than 9 characters, and unique per instance of [NsdServiceInfo](../android/net/nsd/NsdServiceInfo.md). Calling [setAttribute](../android/net/nsd/NsdServiceInfo.md))twice with the same key will overwrite first value. 

### setHost

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setHost(s: InetAddress!): Unit
```

**Deprecated:** *Use [setHostAddresses(java.util.List)](../android/net/nsd/NsdServiceInfo.md))to set multiple addresses for the host.*

Set the host address 

### setHostAddresses

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 7](https://developer.android.com/sdkExtensions) 

```
fun setHostAddresses(addresses: MutableList<InetAddress!>): Unit
```

Set the host addresses.

When registering hosts/services, there can only be one registration including address records for a given hostname.

For example, if a client registers a service with the hostname "MyHost" and the address records of 192.168.1.1 and 192.168.1.2, then other registrations for the hostname "MyHost" must not have any address record, otherwise there will be a conflict.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addresses` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](../java/net/InetAddress.md)!\>:This value cannot be`null`. |

### setNetwork

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun setNetwork(network: Network?): Unit
```

Set the network where the service can be found.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](../android/net/Network.md)?:The network, or null to search for, or to announce, the service on all connected networks. |

### setPort

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setPort(p: Int): Unit
```

Set port number 

### setServiceName

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setServiceName(s: String!): Unit
```

Set the service name 

### setServiceType

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setServiceType(s: String!): Unit
```

Set the service type 

### setSubtypes

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 12](https://developer.android.com/sdkExtensions) 

```
fun setSubtypes(subtypes: MutableSet<String!>): Unit
```

Sets the subtypes to be advertised for this service instance. The elements in`subtypes`should be the subtype identifiers which have the trailing "._sub" removed. For example, the subtype should be "_printer" for "_printer._sub._http._tcp.local". Only one subtype will be registered if multiple elements of`subtypes`have the same case-insensitive value.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `subtypes` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>:This value cannot be`null`. |

### toString

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NsdServiceInfo!>
```

Implement the Parcelable interface
