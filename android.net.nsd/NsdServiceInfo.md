# NsdServiceInfo

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NsdServiceInfo

Kotlin| [Java](https://developer.android.com/reference/android/net/nsd/NsdServiceInfo "View this page in Java") 
| --- | --- |

```
class NsdServiceInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.nsd.NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#) |

A class representing service information for network service discovery

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------|---|
| [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#NsdServiceInfo())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#describeContents())`()` Implement the Parcelable interface |
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!\>! | [getAttributes](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getAttributes())`()` Retrieve attributes as a map of String keys to byte\[\] values. |
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)! | [getHost](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getHost())`()` Get the host address. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!\> | [getHostAddresses](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getHostAddresses())`()` Get the host addresses. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHostname](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getHostname())`()` Get the hostname. |
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)? | [getNetwork](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getNetwork())`()` Get the network where the service can be found. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getPort())`()` Get port number. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceName](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getServiceName())`()` Get the service name |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getServiceType](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getServiceType())`()` Get the service type |
| --- | --- |
| [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getSubtypes](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getSubtypes())`()` Returns subtypes of this service instance. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [removeAttribute](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#removeAttribute(kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Remove an attribute by key |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setAttribute](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setAttribute(kotlin.String,%20kotlin.String))`(`key:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `value:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Add a service attribute as a key/value pair. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHost](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setHost(java.net.InetAddress))`(`s:` ` [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!`)` Set the host address |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHostAddresses](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setHostAddresses(kotlin.collections.MutableList))`(`addresses:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!>`)` Set the host addresses. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNetwork](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setNetwork(android.net.Network))`(`network:` ` [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)?`)` Set the network where the service can be found. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setPort](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setPort(kotlin.Int))`(`p:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Set port number |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceName](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setServiceName(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the service name |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setServiceType](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setServiceType(kotlin.String))`(`s:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Set the service type |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSubtypes](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setSubtypes(kotlin.collections.MutableSet))`(`subtypes:` ` [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>`)` Sets the subtypes to be advertised for this service instance. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getAttributes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAttributes(): MutableMap<String!, ByteArray!>!
```

Retrieve attributes as a map of String keys to byte\[\] values. The attributes map is only valid for a resolved service.

The returned map is unmodifiable; changes must be made through [setAttribute](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setAttribute(kotlin.String,%20kotlin.String))and [removeAttribute](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#removeAttribute(kotlin.String)). 

### getHost

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHost(): InetAddress!
```

**Deprecated:** *Use [getHostAddresses()](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getHostAddresses())to get the entire list of addresses for the host.*

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
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!> | This value cannot be`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#getPort()> 

### getHostname

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 17](https://developer.android.com/sdkExtensions) 

```
fun getHostname(): String?
```

Get the hostname.

When a service is resolved through android.net.nsd.NsdManager#resolveService or [NsdManager.registerServiceInfoCallback](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager#registerServiceInfoCallback(android.net.nsd.NsdServiceInfo,%20java.util.concurrent.Executor,%20android.net.nsd.NsdManager.ServiceInfoCallback)), this returns the hostname of the resolved service. In all other cases, this will be null. The top level domain ".local." is omitted. For example, this returns "MyHost" when the service's hostname is "MyHost.local.". 

### getNetwork

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun getNetwork(): Network?
```

Get the network where the service can be found. This is set if this [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#) was obtained from android.net.nsd.NsdManager#discoverServices or android.net.nsd.NsdManager#resolveService, unless the service was found on a network interface that does not have a [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)(such as a tethering downstream, where services are advertised from devices connected to this device via tethering).

| Return ||
|--------------------------------------------------------------------------------------|--------------------------|
| [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)? | This value may be`null`. |

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

Returns subtypes of this service instance. When this object is returned by the service discovery/browse APIs (etc. [NsdManager.DiscoveryListener](https://developer.android.com/reference/kotlin/android/net/nsd/NsdManager.DiscoveryListener)), the return value may or may not include the subtypes of this service.

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

Keys should be short, ideally no more than 9 characters, and unique per instance of [NsdServiceInfo](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#). Calling [setAttribute](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setAttribute(kotlin.String,%20kotlin.String))twice with the same key will overwrite first value. 

### setHost

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setHost(s: InetAddress!): Unit
```

**Deprecated:** *Use [setHostAddresses(java.util.List)](https://developer.android.com/reference/kotlin/android/net/nsd/NsdServiceInfo#setHostAddresses(kotlin.collections.MutableList))to set multiple addresses for the host.*

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
| `addresses` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!\>:This value cannot be`null`. |

### setNetwork

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [T Extensions 3](https://developer.android.com/sdkExtensions) 

```
fun setNetwork(network: Network?): Unit
```

Set the network where the service can be found.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)?:The network, or null to search for, or to announce, the service on all connected networks. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<NsdServiceInfo!>
```

Implement the Parcelable interface
