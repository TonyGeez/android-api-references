# LinkProperties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkProperties

Kotlin| [Java](https://developer.android.com/reference/android/net/LinkProperties "View this page in Java") 

```
class LinkProperties : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties#) |

Describes the properties of a network link. A link represents a connection to a network. It may have multiple addresses and multiple gateways, multiple dns servers but only one http proxy and one network interface. Note that this is just a holder of data. Modifying it does not affect live networks.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties#LinkProperties())`()` Constructs a new`LinkProperties`with default values. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addRoute](https://developer.android.com/reference/kotlin/android/net/LinkProperties#addRoute(android.net.RouteInfo))`(`route:` ` [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo)`)` Adds a [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) to this`LinkProperties`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/net/LinkProperties#clear())`()` Clears this object to its initial state. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/net/LinkProperties#describeContents())`()` Implement the Parcelable interface |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/net/LinkProperties#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`LinkProperties`instance against the target LinkProperties in`obj`. |
| [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address.html#)? | [getDhcpServerAddress](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getDhcpServerAddress())`()` Get DHCP server address |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!\> | [getDnsServers](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getDnsServers())`()` Returns all the [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) for DNS servers on this link. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDomains](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getDomains())`()` Get the DNS domains search path set for this link. |
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)? | [getHttpProxy](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getHttpProxy())`()` Gets the recommended [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)(or`null`) set on this link. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInterfaceName](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getInterfaceName())`()` Gets the interface name for this link. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress)!\> | [getLinkAddresses](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getLinkAddresses())`()` Returns all the [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) on this link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMtu](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getMtu())`()` Gets any non-default MTU size set for this link. |
| [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix)? | [getNat64Prefix](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getNat64Prefix())`()` Returns the NAT64 prefix in use on this link, if any. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPrivateDnsServerName](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getPrivateDnsServerName())`()` Returns the private DNS server name that is in use. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo)!\> | [getRoutes](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getRoutes())`()` Returns all the [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) set on this link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/net/LinkProperties#hashCode())`()` Generate hashcode based on significant fields Equal objects must produce the same hash code, while unequal objects may have the same hash codes. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivateDnsActive](https://developer.android.com/reference/kotlin/android/net/LinkProperties#isPrivateDnsActive())`()` Returns whether private DNS is currently in use on this network. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWakeOnLanSupported](https://developer.android.com/reference/kotlin/android/net/LinkProperties#isWakeOnLanSupported())`()` Returns whether the network interface supports WakeOnLAN |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDhcpServerAddress](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setDhcpServerAddress(java.net.Inet4Address))`(`serverAddress:` ` [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address.html#)?`)` Set DHCP server address. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDnsServers](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setDnsServers(kotlin.collections.MutableCollection))`(`dnsServers:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!>`)` Replaces the DNS servers in this`LinkProperties`with the given [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) of [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) objects. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDomains](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setDomains(kotlin.String))`(`domains:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the DNS domain search path used on this link. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHttpProxy](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setHttpProxy(android.net.ProxyInfo))`(`proxy:` ` [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)?`)` Sets the recommended [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo) to use on this link, or`null`for none. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterfaceName](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setInterfaceName(kotlin.String))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the interface name for this link. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLinkAddresses](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setLinkAddresses(kotlin.collections.MutableCollection))`(`addresses:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress)!>`)` Replaces the [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) in this`LinkProperties`with the given [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) of [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMtu](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setMtu(kotlin.Int))`(`mtu:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the Maximum Transmission Unit size to use on this link. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNat64Prefix](https://developer.android.com/reference/kotlin/android/net/LinkProperties#setNat64Prefix(android.net.IpPrefix))`(`prefix:` ` [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix)?`)` Sets the NAT64 prefix in use on this link. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/net/LinkProperties#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/net/LinkProperties#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface. |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [LinkProperties](https://developer.android.com/reference/kotlin/android/net/LinkProperties#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/net/LinkProperties#CREATOR:android.os.Parcelable.Creator) Implement the Parcelable interface. |

## Public constructors

### LinkProperties

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
LinkProperties()
```

Constructs a new`LinkProperties`with default values.

## Public methods

### addRoute

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun addRoute(route: RouteInfo): Boolean
```

Adds a [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) to this`LinkProperties`. If there is a [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) with the same destination, gateway and interface with different properties (e.g., different MTU), it will be updated. If the [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) had an interface name set and that differs from the interface set for this`LinkProperties`an [IllegalArgumentException](https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#) will be thrown. The proper course is to add either un-named or properly named [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `route` | [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo):A [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) to add to this object. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`was added or updated, false otherwise. |

### clear

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clear(): Unit
```

Clears this object to its initial state. 

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Implement the Parcelable interface

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this`LinkProperties`instance against the target LinkProperties in`obj`. Two LinkPropertieses are equal if all their fields are equal in values. For collection fields, such as mDnses, containsAll() is used to check if two collections contains the same elements, independent of order. There are two thoughts regarding containsAll() 1. Duplicated elements. eg, (A, B, B) and (A, A, B) are equal. 2. Worst case performance is O(n\^2).

| Parameters ||
|-------|----------------------------------------------------------------|
| `obj` | the object to be tested for equality. This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if both objects are equal,`false`otherwise. |

### getDhcpServerAddress

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDhcpServerAddress(): Inet4Address?
```

Get DHCP server address

| Return ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address.html#)? | The current DHCP server address. This value may be`null`. |

### getDnsServers

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDnsServers(): MutableList<InetAddress!>
```

Returns all the [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) for DNS servers on this link.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!> | An unmodifiable [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) for DNS servers on this link. This value cannot be`null`. |

### getDomains

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomains(): String?
```

Get the DNS domains search path set for this link. May be`null`if not set.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | A [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) containing the comma separated domains to search when resolving host names on this link or`null`. |

### getHttpProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHttpProxy(): ProxyInfo?
```

Gets the recommended [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)(or`null`) set on this link.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)? | The [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo) set on this link or`null`. |

### getInterfaceName

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInterfaceName(): String?
```

Gets the interface name for this link. May be`null`if not set.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The interface name set for this link or`null`. |

### getLinkAddresses

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLinkAddresses(): MutableList<LinkAddress!>
```

Returns all the [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) on this link. Typically a link will have one IPv4 address and one or more IPv6 addresses.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress)!> | An unmodifiable [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) for this link. This value cannot be`null`. |

### getMtu

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMtu(): Int
```

Gets any non-default MTU size set for this link. Note that if the default is being used this will return 0.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The mtu value set for this link. |

### getNat64Prefix

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getNat64Prefix(): IpPrefix?
```

Returns the NAT64 prefix in use on this link, if any.

| Return ||
|----------------------------------------------------------------------------------|----------------------------|
| [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix)? | the NAT64 prefix or`null`. |

### getPrivateDnsServerName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivateDnsServerName(): String?
```

Returns the private DNS server name that is in use. If not`null`, private DNS is in strict mode. In this mode, applications should ensure that all DNS queries are encrypted and sent to this hostname and that queries are only sent if the hostname's certificate is valid. If`null`and [isPrivateDnsActive](https://developer.android.com/reference/kotlin/android/net/LinkProperties#isPrivateDnsActive())is`true`, private DNS is in opportunistic mode, and applications should ensure that DNS queries are encrypted and sent to a DNS server returned by [getDnsServers](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getDnsServers()). System DNS will handle each of these cases correctly, but applications implementing their own DNS lookups must make sure to follow these requirements.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The private DNS server name. |

### getRoutes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoutes(): MutableList<RouteInfo!>
```

Returns all the [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) set on this link. Only unicast routes are returned for apps targeting Android S or below.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo)!> | An unmodifiable [List](https://developer.android.com/reference/kotlin/java/util/List.html#) of [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) for this link. This value cannot be`null`. |

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Generate hashcode based on significant fields Equal objects must produce the same hash code, while unequal objects may have the same hash codes.

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### isPrivateDnsActive

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isPrivateDnsActive(): Boolean
```

Returns whether private DNS is currently in use on this network. When private DNS is in use, applications must not send unencrypted DNS queries as doing so could reveal private user information. Furthermore, if private DNS is in use and [getPrivateDnsServerName](https://developer.android.com/reference/kotlin/android/net/LinkProperties#getPrivateDnsServerName())is not`null`, DNS queries must be sent to the specified DNS server.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if private DNS is in use,`false`otherwise. |

### isWakeOnLanSupported

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isWakeOnLanSupported(): Boolean
```

Returns whether the network interface supports WakeOnLAN

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if interface supports WakeOnLAN,`false`otherwise. |

### setDhcpServerAddress

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDhcpServerAddress(serverAddress: Inet4Address?): Unit
```

Set DHCP server address.

| Parameters ||
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `serverAddress` | [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address.html#)?:the server address to set. This value may be`null`. |

### setDnsServers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDnsServers(dnsServers: MutableCollection<InetAddress!>): Unit
```

Replaces the DNS servers in this`LinkProperties`with the given [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) of [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#) objects.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dnsServers` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress.html#)!\>:The [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) of DNS servers to set in this object. This value cannot be`null`. |

### setDomains

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDomains(domains: String?): Unit
```

Sets the DNS domain search path used on this link.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `domains` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) listing in priority order the comma separated domains to search when resolving host names on this link. This value may be`null`. |

### setHttpProxy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setHttpProxy(proxy: ProxyInfo?): Unit
```

Sets the recommended [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo) to use on this link, or`null`for none. Note that Http Proxies are only a hint - the system recommends their use, but it does not enforce it and applications may ignore them.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `proxy` | [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo)?:A [ProxyInfo](https://developer.android.com/reference/kotlin/android/net/ProxyInfo) defining the HTTP Proxy to use on this link. This value may be`null`. |

### setInterfaceName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInterfaceName(iface: String?): Unit
```

Sets the interface name for this link. All [RouteInfo](https://developer.android.com/reference/kotlin/android/net/RouteInfo) already set for this will have their interface changed to match this new value.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iface` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The name of the network interface used for this link. This value may be`null`. |

### setLinkAddresses

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLinkAddresses(addresses: MutableCollection<LinkAddress!>): Unit
```

Replaces the [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) in this`LinkProperties`with the given [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) of [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addresses` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress)!\>:The [Collection](https://developer.android.com/reference/kotlin/java/util/Collection.html#) of [LinkAddress](https://developer.android.com/reference/kotlin/android/net/LinkAddress) to set in this object. This value cannot be`null`. |

### setMtu

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setMtu(mtu: Int): Unit
```

Sets the Maximum Transmission Unit size to use on this link. This should not be used unless the system default (1500) is incorrect. Values less than 68 or greater than 10000 will be ignored.

| Parameters ||
|-------|----------------------------------------------------------------------------------------------------------|
| `mtu` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The MTU to use for this link. |

### setNat64Prefix

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setNat64Prefix(prefix: IpPrefix?): Unit
```

Sets the NAT64 prefix in use on this link. Currently, only 96-bit prefixes (i.e., where the 32-bit IPv4 address is at the end of the 128-bit IPv6 address) are supported or`null`for no prefix.

| Parameters ||
|----------|-----------------------------------------------------------------------------------------------------------------------------|
| `prefix` | [IpPrefix](https://developer.android.com/reference/kotlin/android/net/IpPrefix)?:the NAT64 prefix. This value may be`null`. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Implement the Parcelable interface.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LinkProperties!>
```

Implement the Parcelable interface.
