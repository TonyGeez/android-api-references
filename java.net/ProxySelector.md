# ProxySelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProxySelector

```
abstract class ProxySelector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.ProxySelector](ProxySelector.md) |

Selects the proxy server to use, if any, when connecting to the network resource referenced by a URL. A proxy selector is a concrete sub-class of this class and is registered by invoking the [setDefault](ProxySelector.md))method. The currently registered proxy selector can be retrieved by calling [getDefault](ProxySelector.md))method.

When a proxy selector is registered, for instance, a subclass of URLConnection class should call the [select](ProxySelector.md))method for each URL request so that the proxy selector can decide if a direct, or proxied connection should be used. The [select](ProxySelector.md))method returns an iterator over a collection with the preferred connection approach.

If a connection cannot be established to a proxy (PROXY or SOCKS) servers then the caller should call the proxy selector's [connectFailed](ProxySelector.md))method to notify the proxy selector that the proxy server is unavailable.

The default proxy selector does enforce a [set of System Properties](../java/net/doc-files/net-properties.md) related to proxy settings.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [ProxySelector](ProxySelector.md))`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connectFailed](ProxySelector.md))`(`uri:` ` [URI](URI.md)!`, `sa:` ` [SocketAddress](SocketAddress.md)!`, `ioe:` ` [IOException](../java.io/IOException.md)!`)` Called to indicate that a connection could not be established to a proxy/socks server. |
| openstatic [ProxySelector](ProxySelector.md)! | [getDefault](ProxySelector.md))`()` Gets the system-wide proxy selector. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Proxy](Proxy.md)!\>! | [select](ProxySelector.md))`(`uri:` ` [URI](URI.md)!`)` Selects all the applicable proxies based on the protocol to access the resource with and a destination address to access the resource at. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](ProxySelector.md))`(`ps:` ` [ProxySelector](ProxySelector.md)!`)` Sets (or unsets) the system-wide proxy selector. |

## Public constructors

### ProxySelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ProxySelector()
```

## Public methods

### connectFailed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun connectFailed(
    uri: URI!, 
    sa: SocketAddress!, 
    ioe: IOException!
): Unit
```

Called to indicate that a connection could not be established to a proxy/socks server. An implementation of this method can temporarily remove the proxies or reorder the sequence of proxies returned by [select(java.net.URI)](ProxySelector.md)), using the address and the IOException caught when trying to connect.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](URI.md)!:The URI that the proxy at sa failed to serve. |
| `sa` | [SocketAddress](SocketAddress.md)!:The socket address of the proxy/SOCKS server |
| `ioe` | [IOException](../java.io/IOException.md)!:The I/O exception thrown when the connect failed. |
| --- | --- |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.lang.IllegalArgumentException` | if either argument is null |

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): ProxySelector!
```

Gets the system-wide proxy selector.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------|
| [ProxySelector](ProxySelector.md)! | the system-wide`ProxySelector` |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](NetPermission.md)`("getProxySelector")` |

**See Also**

- [#setDefault(ProxySelector)](ProxySelector.md)) 

### select

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun select(uri: URI!): MutableList<Proxy!>!
```

Selects all the applicable proxies based on the protocol to access the resource with and a destination address to access the resource at. The format of the URI is defined as follow:

- http URI for http connections
- https URI for https connections
- `socket://host:port` 
 for tcp client sockets connections

<br />

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](URI.md)!:The URI that a connection is required to |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Proxy](Proxy.md)!>! | a List of Proxies. Each element in the the List is of type [Proxy](Proxy.md); when no proxy is available, the list will contain one element of type [Proxy](Proxy.md) that represents a direct connection. |

| Exceptions ||
|--------------------------------------|-------------------------|
| `java.lang.IllegalArgumentException` | if the argument is null |

### setDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(ps: ProxySelector!): Unit
```

Sets (or unsets) the system-wide proxy selector. Note: non-standard protocol handlers may ignore this setting.

| Parameters ||
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `ps` | [ProxySelector](ProxySelector.md)!:The HTTP proxy selector, or`null`to unset the proxy selector. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](NetPermission.md)`("setProxySelector")` |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/ProxySelector#getDefault()>
