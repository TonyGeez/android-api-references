# Proxy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Proxy

```
open class Proxy
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.net.Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy#) |

This class represents a proxy setting, typically a type (http, socks) and a socket address. A`Proxy`is an immutable object.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------|
| | [Type](https://developer.android.com/reference/kotlin/java/net/Proxy.Type) Represents the proxy type. |

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy#Proxy(java.net.Proxy.Type,%20java.net.SocketAddress))`(`type:` ` [Proxy.Type](https://developer.android.com/reference/kotlin/java/net/Proxy.Type)!`, `sa:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`)` Creates an entry representing a PROXY connection. |

| Public methods ||
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)! | [address](https://developer.android.com/reference/kotlin/java/net/Proxy#address())`()` Returns the socket address of the proxy, or`null`if its a direct connection. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/java/net/Proxy#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Compares this object against the specified object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/java/net/Proxy#hashCode())`()` Returns a hashcode for this Proxy. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/java/net/Proxy#toString())`()` Constructs a string representation of this Proxy. |
| open [Proxy.Type](https://developer.android.com/reference/kotlin/java/net/Proxy.Type)! | [type](https://developer.android.com/reference/kotlin/java/net/Proxy#type())`()` Returns the proxy type. |

| Properties ||
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy#)! | [NO_PROXY](https://developer.android.com/reference/kotlin/java/net/Proxy#NO_PROXY:java.net.Proxy) A proxy setting that represents a`DIRECT`connection, basically telling the protocol handler not to use any proxying. |

## Public constructors

### Proxy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Proxy(
    type: Proxy.Type!, 
    sa: SocketAddress!)
```

Creates an entry representing a PROXY connection. Certain combinations are illegal. For instance, for types Http, and Socks, a SocketAddress**must**be provided.

Use the`Proxy.NO_PROXY`constant for representing a direct connection.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------|
| `type` | [Proxy.Type](https://developer.android.com/reference/kotlin/java/net/Proxy.Type)!:the`Type`of the proxy |
| `sa` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!:the`SocketAddress`for that proxy |

| Exceptions ||
|--------------------------------------|------------------------------------------------|
| `java.lang.IllegalArgumentException` | when the type and the address are incompatible |

## Public methods

### address

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun address(): SocketAddress!
```

Returns the socket address of the proxy, or`null`if its a direct connection.

| Return ||
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)! | a`SocketAddress`representing the socket end point of the proxy |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

Compares this object against the specified object. The result is`true`if and only if the argument is not`null`and it represents the same proxy as this object.

Two instances of`Proxy`represent the same address if both the SocketAddresses and type are equal.

| Parameters ||
|-------|--------------------------------|
| `obj` | the object to compare against. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the objects are the same;`false`otherwise. |

**See Also**

- [java.net.InetSocketAddress#equals(java.lang.Object)](https://developer.android.com/reference/kotlin/java/net/InetSocketAddress#equals(kotlin.Any)) 

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

Returns a hashcode for this Proxy.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this Proxy. |

### toString

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun toString(): String
```

Constructs a string representation of this Proxy. This String is constructed by calling toString() on its type and concatenating " @ " and the toString() result from its address if its type is not`DIRECT`.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of this object. |

### type

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun type(): Proxy.Type!
```

Returns the proxy type.

| Return ||
|-----------------------------------------------------------------------------------|------------------------------------|
| [Proxy.Type](https://developer.android.com/reference/kotlin/java/net/Proxy.Type)! | a Type representing the proxy type |

## Properties

### NO_PROXY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NO_PROXY: Proxy!
```

A proxy setting that represents a`DIRECT`connection, basically telling the protocol handler not to use any proxying. Used, for instance, to create sockets bypassing any other global proxy settings (like SOCKS):

`Socket s = new Socket(Proxy.NO_PROXY);`
