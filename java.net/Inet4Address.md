# Inet4Address

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Inet4Address

```
class Inet4Address : InetAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.InetAddress](InetAddress.md) ||
| | ↳ | [java.net.Inet4Address](Inet4Address.md) |

This class represents an Internet Protocol version 4 (IPv4) address. Defined by [*RFC 790: Assigned Numbers*](http://www.ietf.org/rfc/rfc790.txt), [*RFC 1918: Address Allocation for Private Internets*](http://www.ietf.org/rfc/rfc1918.txt), and [*RFC 2365: Administratively Scoped IP Multicast*](http://www.ietf.org/rfc/rfc2365.txt)

### Textual representation of IP addresses

Textual representation of IPv4 address used as input to methods takes one of the following forms:

- `d.d.d.d`
- `d.d.d`
- `d.d`
- `d`

<br />

When four parts are specified, each is interpreted as a byte of data and assigned, from left to right, to the four bytes of an IPv4 address.

When a three part address is specified, the last part is interpreted as a 16-bit quantity and placed in the right most two bytes of the network address. This makes the three part address format convenient for specifying Class B net- work addresses as 128.net.host.

When a two part address is supplied, the last part is interpreted as a 24-bit quantity and placed in the right most three bytes of the network address. This makes the two part address format convenient for specifying Class A network addresses as net.host.

When only one part is given, the value is stored directly in the network address without any byte rearrangement.

For methods that return a textual representation as output value, the first form, i.e. a dotted-quad string, is used.

#### The Scope of a Multicast Address

Historically the IPv4 TTL field in the IP header has doubled as a multicast scope field: a TTL of 0 means node-local, 1 means link-local, up through 32 means site-local, up through 64 means region-local, up through 128 means continent-local, and up through 255 are global. However, the administrative scoping is preferred. Please refer to [*RFC 2365: Administratively Scoped IP Multicast*](http://www.ietf.org/rfc/rfc2365.txt)

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](Inet4Address.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)! | [getAddress](Inet4Address.md))`()` Returns the raw IP address of this`InetAddress`object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getHostAddress](Inet4Address.md))`()` Returns the IP address string in textual presentation form. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](Inet4Address.md))`()` Returns a hashcode for this IP address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAnyLocalAddress](Inet4Address.md))`()` Utility routine to check if the InetAddress is a wildcard address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLinkLocalAddress](Inet4Address.md))`()` Utility routine to check if the InetAddress is an link local address. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isLoopbackAddress](Inet4Address.md))`()` Utility routine to check if the InetAddress is a loopback address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCGlobal](Inet4Address.md))`()` Utility routine to check if the multicast address has global scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCLinkLocal](Inet4Address.md))`()` Utility routine to check if the multicast address has link scope. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCNodeLocal](Inet4Address.md))`()` Utility routine to check if the multicast address has node scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCOrgLocal](Inet4Address.md))`()` Utility routine to check if the multicast address has organization scope. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMCSiteLocal](Inet4Address.md))`()` Utility routine to check if the multicast address has site scope. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMulticastAddress](Inet4Address.md))`()` Utility routine to check if the InetAddress is an IP multicast address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSiteLocalAddress](Inet4Address.md))`()` Utility routine to check if the InetAddress is a site local address. |

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

### getHostAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHostAddress(): String?
```

Returns the IP address string in textual presentation form.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the raw IP address in a string format. |

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

Utility routine to check if the InetAddress is a wildcard address.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | a`boolean`indicating if the Inetaddress is a wildcard address. |

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

Utility routine to check if the InetAddress is an IP multicast address. IP multicast address is a Class D address i.e first four bits of the address are 1110.

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
