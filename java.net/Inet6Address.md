# Inet6Address

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Inet6Address

```
class Inet6Address : InetAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.InetAddress](InetAddress.md) ||
| | ↳ | [java.net.Inet6Address](Inet6Address.md) |

This class represents an Internet Protocol version 6 (IPv6) address. Defined by [*RFC 2373: IP Version 6 Addressing Architecture*](http://www.ietf.org/rfc/rfc2373.txt).

### Textual representation of IP addresses

Textual representation of IPv6 address used as input to methods takes one of the following forms:

1. The preferred formis x:x:x:x:x:x:x:x, where the 'x's are the hexadecimal values of the eight 16-bit pieces of the address. This is the full form. For example,

 | `1080:0:0:0:8:800:200C:417A` | |
| --- | --- |

 Note that it is not necessary to write the leading zeros in an individual field. However, there must be at least one numeral in every field, except as described below.
2. Due to some methods of allocating certain styles of IPv6 addresses, it will be common for addresses to contain long strings of zero bits. In order to make writing addresses containing zero bits easier, a special syntax is available to compress the zeros. The use of "::" indicates multiple groups of 16-bits of zeros. The "::" can only appear once in an address. The "::" can also be used to compress the leading and/or trailing zeros in an address. For example,

 | `1080::8:800:200C:417A` | |
| --- | --- |

3. An alternative form that is sometimes more convenient when dealing with a mixed environment of IPv4 and IPv6 nodes is x:x:x:x:x:x:d.d.d.d, where the 'x's are the hexadecimal values of the six high-order 16-bit pieces of the address, and the 'd's are the decimal values of the four low-order 8-bit pieces of the standard IPv4 representation address, for example,

 | `::FFFF:129.144.52.38` | |
| --- | --- |
 | `::129.144.52.38` | |

 where "::FFFF:d.d.d.d" and "::d.d.d.d" are, respectively, the general forms of an IPv4-mapped IPv6 address and an IPv4-compatible IPv6 address. Note that the IPv4 portion must be in the "d.d.d.d" form. The following forms are invalid:

 | `::FFFF:d.d.d` | |
| --- | --- |
 | `::FFFF:d.d` | |
 | `::d.d.d` | |
 | `::d.d` | |
| --- | --- |

 The following form:

 | `::FFFF:d` | |
| --- | --- |

 is valid, however it is an unconventional representation of the IPv4-compatible IPv6 address,

 | `::255.255.0.d` | |
| --- | --- |

 while "::d" corresponds to the general IPv6 address "0:0:0:0:0:0:0:d".

<br />

For methods that return a textual representation as output value, the full form is used. Inet6Address will return the full form because it is unambiguous when used in combination with other textual data.

#### Special IPv6 address

| *IPv4-mapped address* | Of the form::ffff:w.x.y.z, this IPv6 address is used to represent an IPv4 address. It allows the native program to use the same address data structure and also the same socket when communicating with both IPv4 and IPv6 nodes. In InetAddress and Inet6Address, it is used for internal representation; it has no functional role. Java will never return an IPv4-mapped address. These classes can take an IPv4-mapped address as input, both in byte array and text representation. However, it will be converted into an IPv4 address. |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|

#### Textual representation of IPv6 scoped addresses

The textual representation of IPv6 addresses as described above can be extended to specify IPv6 scoped addresses. This extension to the basic addressing architecture is described in \[draft-ietf-ipngwg-scoping-arch-04.txt\].

Because link-local and site-local addresses are non-global, it is possible that different hosts may have the same destination address and may be reachable through different interfaces on the same originating system. In this case, the originating system is said to be connected to multiple zones of the same scope. In order to disambiguate which is the intended destination zone, it is possible to append a zone identifier (or*scope_id*) to an IPv6 address.

The general format for specifying the*scope_id*is the following:
*IPv6-address* %*scope_id*

The IPv6-address is a literal IPv6 address as described above. The*scope_id*refers to an interface on the local system, and it can be specified in two ways.

1. *As a numeric identifier.*This must be a positive integer that identifies the particular interface and scope as understood by the system. Usually, the numeric values can be determined through administration tools on the system. Each interface may have multiple values, one for each scope. If the scope is unspecified, then the default value used is zero.
2. *As a string.* This must be the exact string that is returned by [java.net.NetworkInterface#getName()](NetworkInterface.md))for the particular interface in question. When an Inet6Address is created in this way, the numeric scope-id is determined at the time the object is created by querying the relevant NetworkInterface.

Note also, that the numeric*scope_id*can be retrieved from Inet6Address instances returned from the NetworkInterface class. This can be used to find out the current scope ids configured on the system.

## Summary

| Public methods ||
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Inet6Address.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getAddress](Inet6Address.md))`()` Returns the raw IP address of this`InetAddress`object. |
| static [Inet6Address](Inet6Address.md)! | [getByAddress](Inet6Address.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `scope_id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create an Inet6Address in the exact manner of[java.net.InetAddress#getByAddress(java.lang.String,byte[])](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByAddress(kotlin.String,%20kotlin.ByteArray))except that the IPv6 scope_id is set to the given numeric value. |
| --- | --- |
| static [Inet6Address](Inet6Address.md)! | [getByAddress](Inet6Address.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `nif:` ` [NetworkInterface](NetworkInterface.md)!`)` Create an Inet6Address in the exact manner of[java.net.InetAddress#getByAddress(java.lang.String,byte[])](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByAddress(kotlin.String,%20kotlin.ByteArray))except that the IPv6 scope_id is set to the value corresponding to the given interface for the address type specified in`addr`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHostAddress](Inet6Address.md))`()` Returns the IP address string in textual presentation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getScopeId](Inet6Address.md))`()` Returns the numeric scopeId, if this instance is associated with an interface. |
| --- | --- |
| [NetworkInterface](NetworkInterface.md)! | [getScopedInterface](Inet6Address.md))`()` Returns the scoped interface, if this instance was created with with a scoped interface. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Inet6Address.md))`()` Returns a hashcode for this IP address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnyLocalAddress](Inet6Address.md))`()` Utility routine to check if the InetAddress in a wildcard address. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isIPv4CompatibleAddress](Inet6Address.md))`()` Utility routine to check if the InetAddress is an IPv4 compatible IPv6 address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLinkLocalAddress](Inet6Address.md))`()` Utility routine to check if the InetAddress is an link local address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoopbackAddress](Inet6Address.md))`()` Utility routine to check if the InetAddress is a loopback address. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCGlobal](Inet6Address.md))`()` Utility routine to check if the multicast address has global scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCLinkLocal](Inet6Address.md))`()` Utility routine to check if the multicast address has link scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCNodeLocal](Inet6Address.md))`()` Utility routine to check if the multicast address has node scope. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCOrgLocal](Inet6Address.md))`()` Utility routine to check if the multicast address has organization scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCSiteLocal](Inet6Address.md))`()` Utility routine to check if the multicast address has site scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMulticastAddress](Inet6Address.md))`()` Utility routine to check if the InetAddress is an IP multicast address. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSiteLocalAddress](Inet6Address.md))`()` Utility routine to check if the InetAddress is a site local address. |

| Inherited functions ||
|---|---|
| From class [InetAddress](InetAddress.md) |----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [InetAddress](InetAddress.md)!>! | [getAllByName](InetAddress.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Given the name of a host, returns an array of its IP addresses, based on the configured name service on the system. The host name can either be a machine name, such as "`java.sun.com`", or a textual representation of its IP address. If a literal IP address is supplied, only the validity of the address format is checked. For`host`specified in*literal IPv6 address* , either the form defined in RFC 2732 or the literal IPv6 address format defined in RFC 2373 is accepted. A literal IPv6 address may also be qualified by appending a scoped zone identifier or scope_id. The syntax and usage of scope_ids is described [here](Inet6Address.md). If the host is`null`then an`InetAddress`representing an address of the loopback interface is returned. See [RFC 3330](http://www.ietf.org/rfc/rfc3330.txt) section 2 and [RFC 2373](http://www.ietf.org/rfc/rfc2373.txt) section 2.5.3. If there is a security manager and`host`is not null and`host.length() `is not equal to zero, the security manager's`checkConnect`method is called with the hostname and`-1`as its arguments to see if the operation is allowed. <br /> | | [InetAddress](InetAddress.md) | [getByAddress](InetAddress.md))`(`addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Returns an`InetAddress`object given the raw IP address . The argument is in network byte order: the highest order byte of the address is in`getAddress()[0]`. This method doesn't block, i.e. no reverse name service lookup is performed. IPv4 address byte array must be 4 bytes long and IPv6 byte array must be 16 bytes long <br /> | | [InetAddress](InetAddress.md) | [getByAddress](InetAddress.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`, `addr:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`)` <br /> Creates an InetAddress based on the provided host name and IP address. No name service is checked for the validity of the address. The host name can either be a machine name, such as "`java.sun.com`", or a textual representation of its IP address. No validity checking is done on the host name either. If addr specifies an IPv4 address an instance of Inet4Address will be returned; otherwise, an instance of Inet6Address will be returned. IPv4 address byte array must be 4 bytes long and IPv6 byte array must be 16 bytes long <br /> | | [InetAddress](InetAddress.md) | [getByName](InetAddress.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` <br /> Determines the IP address of a host, given the host's name. The host name can either be a machine name, such as "`java.sun.com`", or a textual representation of its IP address. If a literal IP address is supplied, only the validity of the address format is checked. For`host`specified in literal IPv6 address, either the form defined in RFC 2732 or the literal IPv6 address format defined in RFC 2373 is accepted. IPv6 scoped addresses are also supported. See [here](Inet6Address.md) for a description of IPv6 scoped addresses. If the host is`null`then an`InetAddress`representing an address of the loopback interface is returned. See [RFC 3330](http://www.ietf.org/rfc/rfc3330.txt) section 2 and [RFC 2373](http://www.ietf.org/rfc/rfc2373.txt) section 2.5.3. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getCanonicalHostName](InetAddress.md))`()` <br /> Gets the fully qualified domain name for this IP address. Best effort method, meaning we may not be able to return the FQDN depending on the underlying system configuration. If there is a security manager, this method first calls its`checkConnect`method with the hostname and`-1`as its arguments to see if the calling code is allowed to know the hostname for this IP address, i.e., to connect to the host. If the operation is not allowed, it will return the textual representation of the IP address. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getHostName](InetAddress.md))`()` <br /> Gets the host name for this IP address. If this InetAddress was created with a host name, this host name will be remembered and returned; otherwise, a reverse name lookup will be performed and the result will be returned based on the system configured name lookup service. If a lookup of the name service is required, call [getCanonicalHostName](InetAddress.md)). If there is a security manager, its`checkConnect`method is first called with the hostname and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, it will return the textual representation of the IP address. <br /> | | [InetAddress](InetAddress.md) | [getLocalHost](InetAddress.md))`()` <br /> Returns the address of the local host. This is achieved by retrieving the name of the host from the system, then resolving that name into an`InetAddress`. Note: The resolved address may be cached for a short period of time. If there is a security manager, its`checkConnect`method is called with the local host name and`-1`as its arguments to see if the operation is allowed. If the operation is not allowed, an InetAddress representing the loopback address is returned. <br /> | | [InetAddress](InetAddress.md) | [getLoopbackAddress](InetAddress.md))`()` <br /> Returns the loopback address. The InetAddress returned will represent the IPv4 loopback address, 127.0.0.1, or the IPv6 loopback address, ::1. The IPv4 loopback address returned is only one of many in the form 127.\*.\*.\* <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReachable](InetAddress.md))`(`timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Test whether that address is reachable. Best effort is made by the implementation to try to reach the host, but firewalls and server configuration may block requests resulting in a unreachable status while some specific ports may be accessible. Android implementation attempts ICMP ECHO REQUESTs first, on failure it will fall back to TCP ECHO REQUESTs. Success on either protocol will return true. The timeout value, in milliseconds, indicates the maximum amount of time the try should take. If the operation times out before getting an answer, the host is deemed unreachable. A negative value will result in an IllegalArgumentException being thrown. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isReachable](InetAddress.md))`(`netif:` ` [NetworkInterface](NetworkInterface.md)?`, `ttl:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Test whether that address is reachable. Best effort is made by the implementation to try to reach the host, but firewalls and server configuration may block requests resulting in a unreachable status while some specific ports may be accessible. Android implementation attempts ICMP ECHO REQUESTs first, on failure it will fall back to TCP ECHO REQUESTs. Success on either protocol will return true. The`network interface`and`ttl`parameters let the caller specify which network interface the test will go through and the maximum number of hops the packets should go through. A negative value for the`ttl`will result in an IllegalArgumentException being thrown. The timeout value, in milliseconds, indicates the maximum amount of time the try should take. If the operation times out before getting an answer, the host is deemed unreachable. A negative value will result in an IllegalArgumentException being thrown. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](InetAddress.md))`()` <br /> Converts this IP address to a`String`. The string returned is of the form: hostname / literal IP address. If the host name is unresolved, no reverse name service lookup is performed. The hostname part will be represented by an empty string. <br /> | ||

## Public methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
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

- [java.net.InetAddress#getAddress()](InetAddress.md)) 

### getAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddress(): ByteArray!
```

Returns the raw IP address of this`InetAddress`object. The result is in network byte order: the highest order byte of the address is in`getAddress()[0]`.

| Return ||
|------------------------------------------------------------------------------------------|------------------------------------|
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | the raw IP address of this object. |

### getByAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getByAddress(
    host: String!, 
    addr: ByteArray!, 
    scope_id: Int
): Inet6Address!
```

Create an Inet6Address in the exact manner of[java.net.InetAddress#getByAddress(java.lang.String,byte[])](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByAddress(kotlin.String,%20kotlin.ByteArray))except that the IPv6 scope_id is set to the given numeric value. The scope_id is not checked to determine if it corresponds to any interface on the system. See [here](Inet6Address.md) for a description of IPv6 scoped addresses.

| Parameters ||
|------------|-----------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the specified host |
| `addr` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the raw IP address in network byte order |
| `scope_id` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the numeric scope_id for the address. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Inet6Address](Inet6Address.md)! | an Inet6Address object created from the raw IP address. |

| Exceptions ||
|---------------------------------|-------------------------------------|
| `java.net.UnknownHostException` | if IP address is of illegal length. |

### getByAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getByAddress(
    host: String!, 
    addr: ByteArray!, 
    nif: NetworkInterface!
): Inet6Address!
```

Create an Inet6Address in the exact manner of[java.net.InetAddress#getByAddress(java.lang.String,byte[])](https://developer.android.com/reference/kotlin/java/net/InetAddress#getByAddress(kotlin.String,%20kotlin.ByteArray))except that the IPv6 scope_id is set to the value corresponding to the given interface for the address type specified in`addr`. The call will fail with an UnknownHostException if the given interface does not have a numeric scope_id assigned for the given address type (eg. link-local or site-local). See [here](Inet6Address.md) for a description of IPv6 scoped addresses.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the specified host |
| `addr` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the raw IP address in network byte order |
| `nif` | [NetworkInterface](NetworkInterface.md)!:an interface this address must be associated with. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------|
| [Inet6Address](Inet6Address.md)! | an Inet6Address object created from the raw IP address. |

| Exceptions ||
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| `java.net.UnknownHostException` | if IP address is of illegal length, or if the interface does not have a numeric scope_id assigned for the given address type. |

### getHostAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHostAddress(): String?
```

Returns the IP address string in textual presentation. If the instance was created specifying a scope identifier then the scope id is appended to the IP address preceded by a "%" (per-cent) character. This can be either a numeric value or a string, depending on which was used to create the instance.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the raw IP address in a string format. |

### getScopeId

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScopeId(): Int
```

Returns the numeric scopeId, if this instance is associated with an interface. If no scoped_id is set, the returned value is zero.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the scopeId, or zero if not set. |

### getScopedInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getScopedInterface(): NetworkInterface!
```

Returns the scoped interface, if this instance was created with with a scoped interface.

| Return ||
|-----------------------------------------------------------------------------------------------|-------------------------------------------|
| [NetworkInterface](NetworkInterface.md)! | the scoped interface, or null if not set. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this IP address.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this IP address. |

### isAnyLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isAnyLocalAddress(): Boolean
```

Utility routine to check if the InetAddress in a wildcard address.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the Inetaddress is a wildcard address. |

### isIPv4CompatibleAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isIPv4CompatibleAddress(): Boolean
```

Utility routine to check if the InetAddress is an IPv4 compatible IPv6 address.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is an IPv4 compatible IPv6 address; or false if address is IPv4 address. |

### isLinkLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLinkLocalAddress(): Boolean
```

Utility routine to check if the InetAddress is an link local address.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is a link local address; or false if address is not a link local unicast address. |

### isLoopbackAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isLoopbackAddress(): Boolean
```

Utility routine to check if the InetAddress is a loopback address.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is a loopback address; or false otherwise. |

### isMCGlobal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMCGlobal(): Boolean
```

Utility routine to check if the multicast address has global scope.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of global scope, false if it is not of global scope or it is not a multicast address |

### isMCLinkLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMCLinkLocal(): Boolean
```

Utility routine to check if the multicast address has link scope.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of link-local scope, false if it is not of link-local scope or it is not a multicast address |

### isMCNodeLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMCNodeLocal(): Boolean
```

Utility routine to check if the multicast address has node scope.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of node-local scope, false if it is not of node-local scope or it is not a multicast address |

### isMCOrgLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMCOrgLocal(): Boolean
```

Utility routine to check if the multicast address has organization scope.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of organization-local scope, false if it is not of organization-local scope or it is not a multicast address |

### isMCSiteLocal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMCSiteLocal(): Boolean
```

Utility routine to check if the multicast address has site scope.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the address has is a multicast address of site-local scope, false if it is not of site-local scope or it is not a multicast address |

### isMulticastAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isMulticastAddress(): Boolean
```

Utility routine to check if the InetAddress is an IP multicast address. 11111111 at the start of the address identifies the address as being a multicast address.

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is an IP multicast address |

### isSiteLocalAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isSiteLocalAddress(): Boolean
```

Utility routine to check if the InetAddress is a site local address.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the InetAddress is a site local address; or false if address is not a site local unicast address. |
