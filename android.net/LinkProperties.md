# LinkProperties

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LinkProperties

Kotlin| [Java](../android/net/LinkProperties.md) 
| --- | --- |

```
class LinkProperties : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.LinkProperties](../android/net/LinkProperties.md) |

Describes the properties of a network link. A link represents a connection to a network. It may have multiple addresses and multiple gateways, multiple dns servers but only one http proxy and one network interface. Note that this is just a holder of data. Modifying it does not affect live networks.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [LinkProperties](../android/net/LinkProperties.md))`()` Constructs a new`LinkProperties`with default values. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [addRoute](../android/net/LinkProperties.md))`(`route:` ` [RouteInfo](../android/net/RouteInfo.md)`)` Adds a [RouteInfo](../android/net/RouteInfo.md) to this`LinkProperties`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/net/LinkProperties.md))`()` Clears this object to its initial state. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/net/LinkProperties.md))`()` Implement the Parcelable interface |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/net/LinkProperties.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this`LinkProperties`instance against the target LinkProperties in`obj`. |
| [Inet4Address](../java/net/Inet4Address.md)? | [getDhcpServerAddress](../android/net/LinkProperties.md))`()` Get DHCP server address |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [InetAddress](../java/net/InetAddress.md)!\> | [getDnsServers](../android/net/LinkProperties.md))`()` Returns all the [InetAddress](../java/net/InetAddress.md) for DNS servers on this link. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getDomains](../android/net/LinkProperties.md))`()` Get the DNS domains search path set for this link. |
| [ProxyInfo](../android/net/ProxyInfo.md)? | [getHttpProxy](../android/net/LinkProperties.md))`()` Gets the recommended [ProxyInfo](../android/net/ProxyInfo.md)(or`null`) set on this link. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInterfaceName](../android/net/LinkProperties.md))`()` Gets the interface name for this link. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [LinkAddress](../android/net/LinkAddress.md)!\> | [getLinkAddresses](../android/net/LinkProperties.md))`()` Returns all the [LinkAddress](../android/net/LinkAddress.md) on this link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMtu](../android/net/LinkProperties.md))`()` Gets any non-default MTU size set for this link. |
| [IpPrefix](../android/net/IpPrefix.md)? | [getNat64Prefix](../android/net/LinkProperties.md))`()` Returns the NAT64 prefix in use on this link, if any. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getPrivateDnsServerName](../android/net/LinkProperties.md))`()` Returns the private DNS server name that is in use. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RouteInfo](../android/net/RouteInfo.md)!\> | [getRoutes](../android/net/LinkProperties.md))`()` Returns all the [RouteInfo](../android/net/RouteInfo.md) set on this link. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/net/LinkProperties.md))`()` Generate hashcode based on significant fields Equal objects must produce the same hash code, while unequal objects may have the same hash codes. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrivateDnsActive](../android/net/LinkProperties.md))`()` Returns whether private DNS is currently in use on this network. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isWakeOnLanSupported](../android/net/LinkProperties.md))`()` Returns whether the network interface supports WakeOnLAN |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDhcpServerAddress](../android/net/LinkProperties.md))`(`serverAddress:` ` [Inet4Address](../java/net/Inet4Address.md)?`)` Set DHCP server address. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDnsServers](../android/net/LinkProperties.md))`(`dnsServers:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [InetAddress](../java/net/InetAddress.md)!>`)` Replaces the DNS servers in this`LinkProperties`with the given [Collection](../java/util/Collection.md) of [InetAddress](../java/net/InetAddress.md) objects. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDomains](../android/net/LinkProperties.md))`(`domains:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the DNS domain search path used on this link. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setHttpProxy](../android/net/LinkProperties.md))`(`proxy:` ` [ProxyInfo](../android/net/ProxyInfo.md)?`)` Sets the recommended [ProxyInfo](../android/net/ProxyInfo.md) to use on this link, or`null`for none. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setInterfaceName](../android/net/LinkProperties.md))`(`iface:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Sets the interface name for this link. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLinkAddresses](../android/net/LinkProperties.md))`(`addresses:` ` [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)< [LinkAddress](../android/net/LinkAddress.md)!>`)` Replaces the [LinkAddress](../android/net/LinkAddress.md) in this`LinkProperties`with the given [Collection](../java/util/Collection.md) of [LinkAddress](../android/net/LinkAddress.md). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMtu](../android/net/LinkProperties.md))`(`mtu:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the Maximum Transmission Unit size to use on this link. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setNat64Prefix](../android/net/LinkProperties.md))`(`prefix:` ` [IpPrefix](../android/net/IpPrefix.md)?`)` Sets the NAT64 prefix in use on this link. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/net/LinkProperties.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/net/LinkProperties.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Implement the Parcelable interface. |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [LinkProperties](../android/net/LinkProperties.md)!\> | [CREATOR](../android/net/LinkProperties.md) Implement the Parcelable interface. |

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

Adds a [RouteInfo](../android/net/RouteInfo.md) to this`LinkProperties`. If there is a [RouteInfo](../android/net/RouteInfo.md) with the same destination, gateway and interface with different properties (e.g., different MTU), it will be updated. If the [RouteInfo](../android/net/RouteInfo.md) had an interface name set and that differs from the interface set for this`LinkProperties`an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) will be thrown. The proper course is to add either un-named or properly named [RouteInfo](../android/net/RouteInfo.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `route` | [RouteInfo](../android/net/RouteInfo.md):A [RouteInfo](../android/net/RouteInfo.md) to add to this object. This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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
| [Inet4Address](../java/net/Inet4Address.md)? | The current DHCP server address. This value may be`null`. |

### getDnsServers

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDnsServers(): MutableList<InetAddress!>
```

Returns all the [InetAddress](../java/net/InetAddress.md) for DNS servers on this link.

| Return ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [InetAddress](../java/net/InetAddress.md)!> | An unmodifiable [List](../java/util/List.md) of [InetAddress](../java/net/InetAddress.md) for DNS servers on this link. This value cannot be`null`. |

### getDomains

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDomains(): String?
```

Get the DNS domains search path set for this link. May be`null`if not set.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | A [String](../java/lang/String.md) containing the comma separated domains to search when resolving host names on this link or`null`. |

### getHttpProxy

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHttpProxy(): ProxyInfo?
```

Gets the recommended [ProxyInfo](../android/net/ProxyInfo.md)(or`null`) set on this link.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [ProxyInfo](../android/net/ProxyInfo.md)? | The [ProxyInfo](../android/net/ProxyInfo.md) set on this link or`null`. |

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

Returns all the [LinkAddress](../android/net/LinkAddress.md) on this link. Typically a link will have one IPv4 address and one or more IPv6 addresses.

| Return ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [LinkAddress](../android/net/LinkAddress.md)!> | An unmodifiable [List](../java/util/List.md) of [LinkAddress](../android/net/LinkAddress.md) for this link. This value cannot be`null`. |

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
| [IpPrefix](../android/net/IpPrefix.md)? | the NAT64 prefix or`null`. |

### getPrivateDnsServerName

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPrivateDnsServerName(): String?
```

Returns the private DNS server name that is in use. If not`null`, private DNS is in strict mode. In this mode, applications should ensure that all DNS queries are encrypted and sent to this hostname and that queries are only sent if the hostname's certificate is valid. If`null`and [isPrivateDnsActive](../android/net/LinkProperties.md))is`true`, private DNS is in opportunistic mode, and applications should ensure that DNS queries are encrypted and sent to a DNS server returned by [getDnsServers](../android/net/LinkProperties.md)). System DNS will handle each of these cases correctly, but applications implementing their own DNS lookups must make sure to follow these requirements.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | The private DNS server name. |

### getRoutes

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRoutes(): MutableList<RouteInfo!>
```

Returns all the [RouteInfo](../android/net/RouteInfo.md) set on this link. Only unicast routes are returned for apps targeting Android S or below.

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RouteInfo](../android/net/RouteInfo.md)!> | An unmodifiable [List](../java/util/List.md) of [RouteInfo](../android/net/RouteInfo.md) for this link. This value cannot be`null`. |

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

Returns whether private DNS is currently in use on this network. When private DNS is in use, applications must not send unencrypted DNS queries as doing so could reveal private user information. Furthermore, if private DNS is in use and [getPrivateDnsServerName](../android/net/LinkProperties.md))is not`null`, DNS queries must be sent to the specified DNS server.

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
| `serverAddress` | [Inet4Address](../java/net/Inet4Address.md)?:the server address to set. This value may be`null`. |

### setDnsServers

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDnsServers(dnsServers: MutableCollection<InetAddress!>): Unit
```

Replaces the DNS servers in this`LinkProperties`with the given [Collection](../java/util/Collection.md) of [InetAddress](../java/net/InetAddress.md) objects.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dnsServers` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [InetAddress](../java/net/InetAddress.md)!\>:The [Collection](../java/util/Collection.md) of DNS servers to set in this object. This value cannot be`null`. |

### setDomains

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDomains(domains: String?): Unit
```

Sets the DNS domain search path used on this link.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `domains` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:A [String](../java/lang/String.md) listing in priority order the comma separated domains to search when resolving host names on this link. This value may be`null`. |

### setHttpProxy

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setHttpProxy(proxy: ProxyInfo?): Unit
```

Sets the recommended [ProxyInfo](../android/net/ProxyInfo.md) to use on this link, or`null`for none. Note that Http Proxies are only a hint - the system recommends their use, but it does not enforce it and applications may ignore them.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `proxy` | [ProxyInfo](../android/net/ProxyInfo.md)?:A [ProxyInfo](../android/net/ProxyInfo.md) defining the HTTP Proxy to use on this link. This value may be`null`. |

### setInterfaceName

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setInterfaceName(iface: String?): Unit
```

Sets the interface name for this link. All [RouteInfo](../android/net/RouteInfo.md) already set for this will have their interface changed to match this new value.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `iface` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The name of the network interface used for this link. This value may be`null`. |

### setLinkAddresses

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setLinkAddresses(addresses: MutableCollection<LinkAddress!>): Unit
```

Replaces the [LinkAddress](../android/net/LinkAddress.md) in this`LinkProperties`with the given [Collection](../java/util/Collection.md) of [LinkAddress](../android/net/LinkAddress.md).

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `addresses` | [MutableCollection](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-collection/index.html)\< [LinkAddress](../android/net/LinkAddress.md)!\>:The [Collection](../java/util/Collection.md) of [LinkAddress](../android/net/LinkAddress.md) to set in this object. This value cannot be`null`. |

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
| `prefix` | [IpPrefix](../android/net/IpPrefix.md)?:the NAT64 prefix. This value may be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<LinkProperties!>
```

Implement the Parcelable interface.
