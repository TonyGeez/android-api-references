# InetAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InetAddress

```
open class InetAddress : Serializable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) |

| Known Direct Subclasses [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address), [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address) |--------------------------------------------------------------------------------------|----------------------------------------------------------------------| | [Inet4Address](https://developer.android.com/reference/kotlin/java/net/Inet4Address) | This class represents an Internet Protocol version 4 (IPv4) address. | | [Inet6Address](https://developer.android.com/reference/kotlin/java/net/Inet6Address) | This class represents an Internet Protocol version 6 (IPv6) address. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This class represents an Internet Protocol (IP) address.

An IP address is either a 32-bit or 128-bit unsigned number used by IP, a lower-level protocol on which protocols like UDP and TCP are built. The IP address architecture is defined by [*RFC 790: Assigned Numbers*](http://www.ietf.org/rfc/rfc790.txt), [*RFC 1918: Address Allocation for Private Internets*](http://www.ietf.org/rfc/rfc1918.txt), [*RFC 2365: Administratively Scoped IP Multicast*](http://www.ietf.org/rfc/rfc2365.txt), and [*RFC 2373: IP Version 6 Addressing Architecture*](http://www.ietf.org/rfc/rfc2373.txt). An instance of an InetAddress consists of an IP address and possibly its corresponding host name (depending on whether it is constructed with a host name or whether it has already done reverse host name resolution).

### Address types

| *unicast* | An identifier for a single interface. A packet sent to a unicast address is delivered to the interface identified by that address. The Unspecified Address -- Also called anylocal or wildcard address. It must never be assigned to any node. It indicates the absence of an address. One example of its use is as the target of bind, which allows a server to accept a client connection on any interface, in case the server host has multiple interfaces. The*unspecified*address must not be used as the destination address of an IP packet. The*Loopback*Addresses -- This is the address assigned to the loopback interface. Anything sent to this IP address loops around and becomes IP input on the local host. This address is often used when testing a client. |
| --- | --- |
| *multicast* | An identifier for a set of interfaces (typically belonging to different nodes). A packet sent to a multicast address is delivered to all interfaces identified by that address. |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

#### IP address scope

*Link-local*addresses are designed to be used for addressing on a single link for purposes such as auto-address configuration, neighbor discovery, or when no routers are present.

*Site-local*addresses are designed to be used for addressing inside of a site without the need for a global prefix.

*Global*addresses are unique across the internet.

#### Textual representation of IP addresses

The textual representation of an IP address is address family specific.

For IPv4 address format, please refer to [Inet4Address#format](https://developer.android.com/reference/kotlin/java/net/Inet4Address#format); For IPv6 address format, please refer to [Inet6Address#format](https://developer.android.com/reference/kotlin/java/net/Inet6Address#format).

There is a [couple of System Properties](https://developer.android.com/reference/kotlin/java/net/doc-files/net-properties#Ipv4IPv6) affecting how IPv4 and IPv6 addresses are used.

#### Host Name Resolution

Host name-to-IP address*resolution* is accomplished through the use of a combination of local machine configuration information and network naming services such as the Domain Name System (DNS) and Network Information Service(NIS). The particular naming services(s) being used is by default the local machine configured one. For any host name, its corresponding IP address is returned.

*Reverse name resolution*means that for any IP address, the host associated with the IP address is returned.

The InetAddress class provides methods to resolve host names to their IP addresses and vice versa.

#### InetAddress Caching

The InetAddress class has a cache to store successful as well as unsuccessful host name resolutions.

By default, when a security manager is installed, in order to protect against DNS spoofing attacks, the result of positive host name resolutions are cached forever. When a security manager is not installed, the default behavior is to cache entries for a finite (implementation dependent) period of time. The result of unsuccessful host name resolution is cached for a very short period of time (10 seconds) to improve performance.

If the default behavior is not desired, then a Java security property can be set to a different Time-to-live (TTL) value for positive caching. Likewise, a system admin can configure a different negative caching TTL value when needed.

Two Java security properties control the TTL values used for positive and negative host name resolution caching:

**networkaddress.cache.ttl**

: Indicates the caching policy for successful name lookups from the name service. The value is specified as as integer to indicate the number of seconds to cache the successful lookup. The default setting is to cache for an implementation specific period of time.A value of -1 indicates "cache forever".

**networkaddress.cache.negative.ttl**(default: 10)

: Indicates the caching policy for un-successful name lookups from the name service. The value is specified as as integer to indicate the number of seconds to cache the failure for un-successful lookups.A value of 0 indicates "never cache". A value of -1 indicates "cache forever".

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/net/InetAddress#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| open [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#getAddress())`()` Returns the raw IP address of this`InetAddress`object. |
| openstatic [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#)!\>! | [getAllByName](https://developer.android.com/reference/kotlin/java/net/InetAddress#getAllByName(kotlin.String))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Given the name of a host, returns an array of its IP addresses, based on the configured name service on the system. |
| --- | --- |
| openstatic [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | [getByAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByAddress(kotlin.ByteArray))`(`addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Returns an`InetAddress`object given the raw IP address . |
| openstatic [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | [getByAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByAddress(kotlin.String,%20kotlin.ByteArray))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` Creates an InetAddress based on the provided host name and IP address. |
| openstatic [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | [getByName](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByName(kotlin.String))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Determines the IP address of a host, given the host's name. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getCanonicalHostName](https://developer.android.com/reference/kotlin/java/net/InetAddress#getCanonicalHostName())`()` Gets the fully qualified domain name for this IP address. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHostAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#getHostAddress())`()` Returns the IP address string in textual presentation. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getHostName](https://developer.android.com/reference/kotlin/java/net/InetAddress#getHostName())`()` Gets the host name for this IP address. |
| --- | --- |
| openstatic [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | [getLocalHost](https://developer.android.com/reference/kotlin/java/net/InetAddress#getLocalHost())`()` Returns the address of the local host. |
| openstatic [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | [getLoopbackAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#getLoopbackAddress())`()` Returns the loopback address. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/net/InetAddress#hashCode())`()` Returns a hashcode for this IP address. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnyLocalAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#isAnyLocalAddress())`()` Utility routine to check if the InetAddress in a wildcard address. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLinkLocalAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#isLinkLocalAddress())`()` Utility routine to check if the InetAddress is an link local address. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoopbackAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#isLoopbackAddress())`()` Utility routine to check if the InetAddress is a loopback address. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCGlobal](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMCGlobal())`()` Utility routine to check if the multicast address has global scope. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCLinkLocal](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMCLinkLocal())`()` Utility routine to check if the multicast address has link scope. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCNodeLocal](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMCNodeLocal())`()` Utility routine to check if the multicast address has node scope. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCOrgLocal](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMCOrgLocal())`()` Utility routine to check if the multicast address has organization scope. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCSiteLocal](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMCSiteLocal())`()` Utility routine to check if the multicast address has site scope. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMulticastAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#isMulticastAddress())`()` Utility routine to check if the InetAddress is an IP multicast address. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReachable](https://developer.android.com/reference/kotlin/java/net/InetAddress#isReachable(kotlin.Int))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Test whether that address is reachable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReachable](https://developer.android.com/reference/kotlin/java/net/InetAddress#isReachable(java.net.NetworkInterface,%20kotlin.Int,%20kotlin.Int))`(`netif:` ` [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)?`, `ttl:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Test whether that address is reachable. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSiteLocalAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#isSiteLocalAddress())`()` Utility routine to check if the InetAddress is a site local address. |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/net/InetAddress#toString())`()` Converts this IP address to a`String`. |

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and it represents the same IP address as this object.

Two instances of`InetAddress`represent the same IP address if the length of the byte arrays returned by`getAddress`is the same for both, and each of the array components is the same for the byte arrays.

| Parameters ||
|-------|--------------------------------|
| `obj` | the object to compare against. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

**See Also**

- [java.net.InetAddress#getAddress()](https://developer.android.com/reference/kotlin/java/net/InetAddress#getAddress()) 

### getAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAddress(): ByteArray!
```

Returns the raw IP address of this`InetAddress`object. The result is in network byte order: the highest order byte of the address is in`getAddress()[0]`.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the raw IP address of this object. |

### getAllByName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getAllByName(host: String?): Array<InetAddress!>!
```

Given the name of a host, returns an array of its IP addresses, based on the configured name service on the system.

The host name can either be a machine name, such as "`java.sun.com`", or a textual representation of its IP address. If a literal IP address is supplied, only the validity of the address format is checked.

For`host`specified in*literal IPv6 address* , either the form defined in RFC 2732 or the literal IPv6 address format defined in RFC 2373 is accepted. A literal IPv6 address may also be qualified by appending a scoped zone identifier or scope_id. The syntax and usage of scope_ids is described [here](https://developer.android.com/reference/kotlin/java/net/Inet6Address#scoped).

If the host is`null`then an`InetAddress`representing an address of the loopback interface is returned. See [RFC 3330](http://www.ietf.org/rfc/rfc3330.txt) section 2 and [RFC 2373](http://www.ietf.org/rfc/rfc2373.txt) section 2.5.3.

If there is a security manager and`host`is not null and`host.length() `is not equal to zero, the security manager's`checkConnect`method is called with the hostname and`-1`as its arguments to see if the operation is allowed.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the name of the host, or`null`. |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#)!>! | an array of all the IP addresses for a given host name. |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.net.UnknownHostException` | if no IP address for the`host`could be found, or if a scope_id was specified for a global IPv6 address. |
| `java.lang.SecurityException` | if a security manager exists and its`checkConnect`method doesn't allow the operation. |

**See Also**

### getByAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getByAddress(addr: ByteArray!): InetAddress
```

Returns an`InetAddress`object given the raw IP address . The argument is in network byte order: the highest order byte of the address is in`getAddress()[0]`.

This method doesn't block, i.e. no reverse name service lookup is performed.

IPv4 address byte array must be 4 bytes long and IPv6 byte array must be 16 bytes long

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `addr` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the raw IP address in network byte order |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | an InetAddress object created from the raw IP address. |

| Exceptions ||
|---------------------------------|------------------------------------|
| `java.net.UnknownHostException` | if IP address is of illegal length |

### getByAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getByAddress(
    host: String?, 
    addr: ByteArray!
): InetAddress
```

Creates an InetAddress based on the provided host name and IP address. No name service is checked for the validity of the address.

The host name can either be a machine name, such as "`java.sun.com`", or a textual representation of its IP address.

No validity checking is done on the host name either.

If addr specifies an IPv4 address an instance of Inet4Address will be returned; otherwise, an instance of Inet6Address will be returned.

IPv4 address byte array must be 4 bytes long and IPv6 byte array must be 16 bytes long

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the specified host |
| `addr` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the raw IP address in network byte order |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | an InetAddress object created from the raw IP address. |

| Exceptions ||
|---------------------------------|------------------------------------|
| `java.net.UnknownHostException` | if IP address is of illegal length |

### getByName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getByName(host: String?): InetAddress
```

Determines the IP address of a host, given the host's name.

The host name can either be a machine name, such as "`java.sun.com`", or a textual representation of its IP address. If a literal IP address is supplied, only the validity of the address format is checked.

For`host`specified in literal IPv6 address, either the form defined in RFC 2732 or the literal IPv6 address format defined in RFC 2373 is accepted. IPv6 scoped addresses are also supported. See [here](https://developer.android.com/reference/kotlin/java/net/Inet6Address#scoped) for a description of IPv6 scoped addresses.

If the host is`null`then an`InetAddress`representing an address of the loopback interface is returned. See [RFC 3330](http://www.ietf.org/rfc/rfc3330.txt) section 2 and [RFC 2373](http://www.ietf.org/rfc/rfc2373.txt) section 2.5.3.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:the specified host, or`null`. |

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | an IP address for the given host name. |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.net.UnknownHostException` | if no IP address for the`host`could be found, or if a scope_id was specified for a global IPv6 address. |
| `java.lang.SecurityException` | if a security manager exists and its checkConnect method doesn't allow the operation |

### getCanonicalHostName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCanonicalHostName(): String
```

Gets the fully qualified domain name for this IP address. Best effort method, meaning we may not be able to return the FQDN depending on the underlying system configuration.

If there is a security manager, this method first calls its`checkConnect`method with the hostname and`-1`as its arguments to see if the calling code is allowed to know the hostname for this IP address, i.e., to connect to the host. If the operation is not allowed, it will return the textual representation of the IP address.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the fully qualified domain name for this IP address, or if the operation is not allowed by the security check, the textual representation of the IP address. |

**See Also**

### getHostAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHostAddress(): String?
```

Returns the IP address string in textual presentation.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the raw IP address in a string format. |

### getHostName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getHostName(): String
```

Gets the host name for this IP address.

If this InetAddress was created with a host name, this host name will be remembered and returned; otherwise, a reverse name lookup will be performed and the result will be returned based on the system configured name lookup service. If a lookup of the name service is required, call [getCanonicalHostName](https://developer.android.com/reference/kotlin/java/net/InetAddress#getCanonicalHostName()).

If there is a security manager, its`checkConnect`method is first called with the hostname and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, it will return the textual representation of the IP address.

| Return ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the host name for this IP address, or if the operation is not allowed by the security check, the textual representation of the IP address. |

**See Also**

- [java.net.InetAddress#getCanonicalHostName](https://developer.android.com/reference/kotlin/java/net/InetAddress#getCanonicalHostName()) 

### getLocalHost

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLocalHost(): InetAddress
```

Returns the address of the local host. This is achieved by retrieving the name of the host from the system, then resolving that name into an`InetAddress`.

Note: The resolved address may be cached for a short period of time.

If there is a security manager, its`checkConnect`method is called with the local host name and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, an InetAddress representing the loopback address is returned.

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | the address of the local host. |

| Exceptions ||
|---------------------------------|---------------------------------------------------------------|
| `java.net.UnknownHostException` | if the local host name could not be resolved into an address. |

**See Also**

- [java.net.InetAddress#getByName(java.lang.String)](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByName(kotlin.String)) 

### getLoopbackAddress

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getLoopbackAddress(): InetAddress
```

Returns the loopback address.

The InetAddress returned will represent the IPv4 loopback address, 127.0.0.1, or the IPv6 loopback address, ::1. The IPv4 loopback address returned is only one of many in the form 127.\*.\*.\*

| Return ||
|-------------------------------------------------------------------------------------|------------------------------------|
| [InetAddress](https://developer.android.com/reference/kotlin/java/net/InetAddress#) | the InetAddress loopback instance. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

Returns a hashcode for this IP address.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this IP address. |

### isAnyLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isAnyLocalAddress(): Boolean
```

Utility routine to check if the InetAddress in a wildcard address.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the Inetaddress is a wildcard address. |

### isLinkLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLinkLocalAddress(): Boolean
```

Utility routine to check if the InetAddress is an link local address.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is a link local address; or false if address is not a link local unicast address. |

### isLoopbackAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isLoopbackAddress(): Boolean
```

Utility routine to check if the InetAddress is a loopback address.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is a loopback address; or false otherwise. |

### isMCGlobal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMCGlobal(): Boolean
```

Utility routine to check if the multicast address has global scope.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of global scope, false if it is not of global scope or it is not a multicast address |

### isMCLinkLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMCLinkLocal(): Boolean
```

Utility routine to check if the multicast address has link scope.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of link-local scope, false if it is not of link-local scope or it is not a multicast address |

### isMCNodeLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMCNodeLocal(): Boolean
```

Utility routine to check if the multicast address has node scope.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of node-local scope, false if it is not of node-local scope or it is not a multicast address |

### isMCOrgLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMCOrgLocal(): Boolean
```

Utility routine to check if the multicast address has organization scope.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of organization-local scope, false if it is not of organization-local scope or it is not a multicast address |

### isMCSiteLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMCSiteLocal(): Boolean
```

Utility routine to check if the multicast address has site scope.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of site-local scope, false if it is not of site-local scope or it is not a multicast address |

### isMulticastAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isMulticastAddress(): Boolean
```

Utility routine to check if the InetAddress is an IP multicast address.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is an IP multicast address |

### isReachable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReachable(timeout: Int): Boolean
```

Test whether that address is reachable. Best effort is made by the implementation to try to reach the host, but firewalls and server configuration may block requests resulting in a unreachable status while some specific ports may be accessible.

Android implementation attempts ICMP ECHO REQUESTs first, on failure it will fall back to TCP ECHO REQUESTs. Success on either protocol will return true.

The timeout value, in milliseconds, indicates the maximum amount of time the try should take. If the operation times out before getting an answer, the host is deemed unreachable. A negative value will result in an IllegalArgumentException being thrown.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the time, in milliseconds, before the call aborts |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address is reachable. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.io.IOException` | if a network error occurs |
| `java.lang.IllegalArgumentException` | if`timeout`is negative. |

### isReachable

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isReachable(
    netif: NetworkInterface?, 
    ttl: Int, 
    timeout: Int
): Boolean
```

Test whether that address is reachable. Best effort is made by the implementation to try to reach the host, but firewalls and server configuration may block requests resulting in a unreachable status while some specific ports may be accessible.

Android implementation attempts ICMP ECHO REQUESTs first, on failure it will fall back to TCP ECHO REQUESTs. Success on either protocol will return true.

The`network interface`and`ttl`parameters let the caller specify which network interface the test will go through and the maximum number of hops the packets should go through. A negative value for the`ttl`will result in an IllegalArgumentException being thrown.

The timeout value, in milliseconds, indicates the maximum amount of time the try should take. If the operation times out before getting an answer, the host is deemed unreachable. A negative value will result in an IllegalArgumentException being thrown.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `netif` | [NetworkInterface](https://developer.android.com/reference/kotlin/java/net/NetworkInterface)?:the NetworkInterface through which the test will be done, or null for any interface |
| `ttl` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the maximum numbers of hops to try or 0 for the default |
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the time, in milliseconds, before the call aborts |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address is reachable. |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if either`timeout`or`ttl`are negative. |
| `java.io.IOException` | if a network error occurs |

### isSiteLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isSiteLocalAddress(): Boolean
```

Utility routine to check if the InetAddress is a site local address.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is a site local address; or false if address is not a site local unicast address. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Converts this IP address to a`String`. The string returned is of the form: hostname / literal IP address. If the host name is unresolved, no reverse name service lookup is performed. The hostname part will be represented by an empty string.

| Return ||
|----------------------------------------------------------------------------------|---------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this IP address. |
