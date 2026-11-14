# InetSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InetSocketAddress

```
open class InetSocketAddress : SocketAddress
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [java.net.SocketAddress](../java/net/SocketAddress.md) ||
| | ↳ | [java.net.InetSocketAddress](../java/net/InetSocketAddress.md) |

This class implements an IP Socket Address (IP address + port number) It can also be a pair (hostname + port number), in which case an attempt will be made to resolve the hostname. If resolution fails then the address is said to be*unresolved*but can still be used on some circumstances like connecting through a proxy.

It provides an immutable object used by sockets for binding, connecting, or as returned values.

The*wildcard* is a special local IP address. It usually means "any" and can only be used for`bind`operations.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [InetSocketAddress](../java/net/InetSocketAddress.md))`(`port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket address where the IP address is the wildcard address and the port number a specified value. |
| [InetSocketAddress](../java/net/InetSocketAddress.md))`(`hostname:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket address from a hostname and a port number. |
| [InetSocketAddress](../java/net/InetSocketAddress.md))`(`addr:` ` [InetAddress](../java/net/InetAddress.md)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates a socket address from an IP address and a port number. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [InetSocketAddress](../java/net/InetSocketAddress.md)! | [createUnresolved](../java/net/InetSocketAddress.md))`(`host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Creates an unresolved socket address from a hostname and a port number. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../java/net/InetSocketAddress.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| [InetAddress](../java/net/InetAddress.md)! | [getAddress](../java/net/InetSocketAddress.md))`()` Gets the`InetAddress`. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHostName](../java/net/InetSocketAddress.md))`()` Gets the`hostname`. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getHostString](../java/net/InetSocketAddress.md))`()` Returns the hostname, or the String form of the address if it doesn't have a hostname (it was created using a literal). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPort](../java/net/InetSocketAddress.md))`()` Gets the port number. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../java/net/InetSocketAddress.md))`()` Returns a hashcode for this socket address. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isUnresolved](../java/net/InetSocketAddress.md))`()` Checks whether the address has been resolved or not. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../java/net/InetSocketAddress.md))`()` Constructs a string representation of this InetSocketAddress. |
| --- | --- |

## Public constructors

### InetSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InetSocketAddress(port: Int)
```

Creates a socket address where the IP address is the wildcard address and the port number a specified value.

A valid port value is between 0 and 65535. A port number of`zero`will let the system pick up an ephemeral port in a`bind`operation.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------|
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The port number |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values. |

### InetSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InetSocketAddress(
    hostname: String!, 
    port: Int)
```

Creates a socket address from a hostname and a port number.

An attempt will be made to resolve the hostname into an InetAddress. If that attempt fails, the address will be flagged as*unresolved*.

If there is a security manager, its`checkConnect`method is called with the host name as its argument to check the permission to resolve it. This could result in a SecurityException.

A valid port value is between 0 and 65535. A port number of`zero`will let the system pick up an ephemeral port in a`bind`operation.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------|
| `hostname` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Host name |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The port number |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the port parameter is outside the range of valid port values, or if the hostname parameter is`null`. |
| `java.lang.SecurityException` | if a security manager is present and permission to resolve the host name is denied. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/InetSocketAddress#isUnresolved()> 

### InetSocketAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
InetSocketAddress(
    addr: InetAddress!, 
    port: Int)
```

Creates a socket address from an IP address and a port number.

A valid port value is between 0 and 65535. A port number of`zero`will let the system pick up an ephemeral port in a`bind`operation.

A`null`address will assign the*wildcard*address.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------|
| `addr` | [InetAddress](../java/net/InetAddress.md)!:The IP address |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The port number |

| Exceptions ||
|--------------------------------------|----------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the port parameter is outside the specified range of valid port values. |

## Public methods

### createUnresolved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun createUnresolved(
    host: String!, 
    port: Int
): InetSocketAddress!
```

Creates an unresolved socket address from a hostname and a port number.

No attempt will be made to resolve the hostname into an InetAddress. The address will be flagged as*unresolved*.

A valid port value is between 0 and 65535. A port number of`zero`will let the system pick up an ephemeral port in a`bind`operation.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the Host name |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The port number |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [InetSocketAddress](../java/net/InetSocketAddress.md)! | an`InetSocketAddress`representing the unresolved socket address |

| Exceptions ||
|--------------------------------------|---------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalArgumentException` | if the port parameter is outside the range of valid port values, or if the hostname parameter is`null`. |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/InetSocketAddress#isUnresolved()> 

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and it represents the same address as this object.

Two instances of`InetSocketAddress`represent the same address if both the InetAddresses (or hostnames if it is unresolved) and port numbers are equal. If both addresses are unresolved, then the hostname and the port number are compared. Note: Hostnames are case insensitive. e.g. "FooBar" and "foobar" are considered equal.

| Parameters ||
|-------|--------------------------------|
| `obj` | the object to compare against. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

**See Also**

- [java.net.InetAddress#equals(java.lang.Object)](../java/net/InetAddress.md)) 

### getAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAddress(): InetAddress!
```

Gets the`InetAddress`.

| Return ||
|-------------------------------------------------------------------------------------|----------------------------------------------|
| [InetAddress](../java/net/InetAddress.md)! | the InetAddress or`null`if it is unresolved. |

### getHostName

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHostName(): String!
```

Gets the`hostname`. Note: This method may trigger a name service reverse lookup if the address was created with a literal IP address.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the hostname part of the address. |

### getHostString

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getHostString(): String!
```

Returns the hostname, or the String form of the address if it doesn't have a hostname (it was created using a literal). This has the benefit of**not**attempting a reverse lookup.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | the hostname, or String representation of the address. |

### getPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getPort(): Int
```

Gets the port number.

| Return ||
|----------------------------------------------------------------------------|------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the port number. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this socket address.

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this socket address. |

### isUnresolved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isUnresolved(): Boolean
```

Checks whether the address has been resolved or not.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the hostname couldn't be resolved into an`InetAddress`. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Constructs a string representation of this InetSocketAddress. This string is constructed by calling [InetAddress.toString()](../java/net/InetAddress.md))on the InetAddress and concatenating the port number (with a colon).

If the address is an IPv6 address, the IPv6 literal is enclosed in square brackets, for example:`"localhost/[0:0:0:0:0:0:0:1]:80"`. If the address is [unresolved](../java/net/InetSocketAddress.md)),`<unresolved>`is displayed in place of the address literal, for example`"foo/<unresolved>:80"`.

To retrieve a string representation of the hostname or the address, use [getHostString()](../java/net/InetSocketAddress.md)), rather than parsing the string returned by this [toString()](../java/net/InetSocketAddress.md))method.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this object. |
