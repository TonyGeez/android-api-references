# ProxySelector

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ProxySelector

```
abstract class ProxySelector
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector#) |

Selects the proxy server to use, if any, when connecting to the network resource referenced by a URL. A proxy selector is a concrete sub-class of this class and is registered by invoking the [setDefault](https://developer.android.com/reference/kotlin/java/net/ProxySelector#setDefault(java.net.ProxySelector))method. The currently registered proxy selector can be retrieved by calling [getDefault](https://developer.android.com/reference/kotlin/java/net/ProxySelector#getDefault())method.

When a proxy selector is registered, for instance, a subclass of URLConnection class should call the [select](https://developer.android.com/reference/kotlin/java/net/ProxySelector#select(java.net.URI))method for each URL request so that the proxy selector can decide if a direct, or proxied connection should be used. The [select](https://developer.android.com/reference/kotlin/java/net/ProxySelector#select(java.net.URI))method returns an iterator over a collection with the preferred connection approach.

If a connection cannot be established to a proxy (PROXY or SOCKS) servers then the caller should call the proxy selector's [connectFailed](https://developer.android.com/reference/kotlin/java/net/ProxySelector#connectFailed(java.net.URI,%20java.net.SocketAddress,%20java.io.IOException))method to notify the proxy selector that the proxy server is unavailable.

The default proxy selector does enforce a [set of System Properties](https://developer.android.com/reference/kotlin/java/net/doc-files/net-properties#Proxies) related to proxy settings.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector#ProxySelector())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [connectFailed](https://developer.android.com/reference/kotlin/java/net/ProxySelector#connectFailed(java.net.URI,%20java.net.SocketAddress,%20java.io.IOException))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `sa:` ` [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!`, `ioe:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!`)` Called to indicate that a connection could not be established to a proxy/socks server. |
| openstatic [ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector#)! | [getDefault](https://developer.android.com/reference/kotlin/java/net/ProxySelector#getDefault())`()` Gets the system-wide proxy selector. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy)!\>! | [select](https://developer.android.com/reference/kotlin/java/net/ProxySelector#select(java.net.URI))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`)` Selects all the applicable proxies based on the protocol to access the resource with and a destination address to access the resource at. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](https://developer.android.com/reference/kotlin/java/net/ProxySelector#setDefault(java.net.ProxySelector))`(`ps:` ` [ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector#)!`)` Sets (or unsets) the system-wide proxy selector. |

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

Called to indicate that a connection could not be established to a proxy/socks server. An implementation of this method can temporarily remove the proxies or reorder the sequence of proxies returned by [select(java.net.URI)](https://developer.android.com/reference/kotlin/java/net/ProxySelector#select(java.net.URI)), using the address and the IOException caught when trying to connect.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:The URI that the proxy at sa failed to serve. |
| `sa` | [SocketAddress](https://developer.android.com/reference/kotlin/java/net/SocketAddress)!:The socket address of the proxy/SOCKS server |
| `ioe` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!:The I/O exception thrown when the connect failed. |
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
| [ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector#)! | the system-wide`ProxySelector` |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission)`("getProxySelector")` |

**See Also**

- [#setDefault(ProxySelector)](https://developer.android.com/reference/kotlin/java/net/ProxySelector#setDefault(java.net.ProxySelector)) 

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
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:The URI that a connection is required to |

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy)!>! | a List of Proxies. Each element in the the List is of type [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy); when no proxy is available, the list will contain one element of type [Proxy](https://developer.android.com/reference/kotlin/java/net/Proxy) that represents a direct connection. |

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
| `ps` | [ProxySelector](https://developer.android.com/reference/kotlin/java/net/ProxySelector#)!:The HTTP proxy selector, or`null`to unset the proxy selector. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission)`("setProxySelector")` |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/ProxySelector#getDefault()>
