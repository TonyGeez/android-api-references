# URLStreamHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# URLStreamHandler

```
abstract class URLStreamHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.net.URLStreamHandler](URLStreamHandler.md) |

The abstract class`URLStreamHandler`is the common superclass for all stream protocol handlers. A stream protocol handler knows how to make a connection for a particular protocol type, such as`http`or`https`.

In most cases, an instance of a`URLStreamHandler`subclass is not created directly by an application. Rather, the first time a protocol name is encountered when constructing a`URL`, the appropriate stream protocol handler is automatically loaded.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------|---|
| [URLStreamHandler](URLStreamHandler.md))`()` <br /> |

| Protected methods ||
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](URLStreamHandler.md))`(`u1:` ` [URL](URL.md)!`, `u2:` ` [URL](URL.md)!`)` Provides the default equals calculation. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDefaultPort](URLStreamHandler.md))`()` Returns the default port for a URL parsed by this handler. |
| open [InetAddress](InetAddress.md)! | [getHostAddress](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`)` Get the IP address of our host. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`)` Provides the default hash calculation. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hostsEqual](URLStreamHandler.md))`(`u1:` ` [URL](URL.md)!`, `u2:` ` [URL](URL.md)!`)` Compares the host components of two URLs. |
| abstract [URLConnection](URLConnection.md)! | [openConnection](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`)` Opens a connection to the object referenced by the`URL`argument. |
| --- | --- |
| open [URLConnection](URLConnection.md)! | [openConnection](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`, `p:` ` [Proxy](Proxy.md)!`)` Same as openConnection(URL), except that the connection will be made through the specified proxy; Protocol handlers that do not support proxying will ignore the proxy parameter and make a normal connection. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [parseURL](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`, `spec:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `limit:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Parses the string representation of a`URL`into a`URL`object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [sameFile](URLStreamHandler.md))`(`u1:` ` [URL](URL.md)!`, `u2:` ` [URL](URL.md)!`)` Compare two urls to see whether they refer to the same file, i. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURL](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `file:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ref:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the fields of the`URL`argument to the indicated values. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setURL](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`, `protocol:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `host:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `port:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `authority:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `userInfo:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `query:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `ref:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Sets the fields of the`URL`argument to the indicated values. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [toExternalForm](URLStreamHandler.md))`(`u:` ` [URL](URL.md)!`)` Converts a`URL`of a specific protocol to a`String`. |
| --- | --- |

## Public constructors

### URLStreamHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
URLStreamHandler()
```

## Protected methods

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun equals(
    u1: URL!, 
    u2: URL!
): Boolean
```

Provides the default equals calculation. May be overidden by handlers for other protocols that have different requirements for equals(). This method requires that none of its arguments is null. This is guaranteed by the fact that it is only called by java.net.URL class.

| Parameters ||
|------|----------------------------------------------------------------------------------|
| `u1` | [URL](URL.md)!:a URL object |
| `u2` | [URL](URL.md)!:a URL object |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the two urls are considered equal, ie. they refer to the same fragment in the same file. |

### getDefaultPort

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getDefaultPort(): Int
```

Returns the default port for a URL parsed by this handler. This method is meant to be overidden by handlers with default port numbers.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the default port for a`URL`parsed by this handler. |

### getHostAddress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getHostAddress(u: URL!): InetAddress!
```

Get the IP address of our host. An empty host field or a DNS failure will result in a null return.

| Parameters ||
|-----|----------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:a URL object |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------------------------------|
| [InetAddress](InetAddress.md)! | an`InetAddress`representing the host IP address. |

### hashCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun hashCode(u: URL!): Int
```

Provides the default hash calculation. May be overidden by handlers for other protocols that have different requirements for hashCode calculation.

| Parameters ||
|-----|----------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:a URL object |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an`int`suitable for hash table indexing |

### hostsEqual

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun hostsEqual(
    u1: URL!, 
    u2: URL!
): Boolean
```

Compares the host components of two URLs.

| Parameters ||
|------|-----------------------------------------------------------------------------------------------------------|
| `u1` | [URL](URL.md)!:the URL of the first host to compare |
| `u2` | [URL](URL.md)!:the URL of the second host to compare |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if and only if they are equal,`false`otherwise. |

### openConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected abstract fun openConnection(u: URL!): URLConnection!
```

Opens a connection to the object referenced by the`URL`argument. This method should be overridden by a subclass.

If for the handler's protocol (such as HTTP or JAR), there exists a public, specialized URLConnection subclass belonging to one of the following packages or one of their subpackages: java.lang, java.io, java.util, java.net, the connection returned will be of that subclass. For example, for HTTP an HttpURLConnection will be returned, and for JAR a JarURLConnection will be returned.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:the URL that this connects to. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [URLConnection](URLConnection.md)! | a`URLConnection`object for the`URL`. |

| Exceptions ||
|-----------------------|------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while opening the connection. |

### openConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun openConnection(
    u: URL!, 
    p: Proxy!
): URLConnection!
```

Same as openConnection(URL), except that the connection will be made through the specified proxy; Protocol handlers that do not support proxying will ignore the proxy parameter and make a normal connection. Calling this method preempts the system's default ProxySelector settings.

| Parameters ||
|-----|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:the URL that this connects to. |
| `p` | [Proxy](Proxy.md)!:the proxy through which the connection will be made. If direct connection is desired, Proxy.NO_PROXY should be specified. |

| Return ||
|-----------------------------------------------------------------------------------------|--------------------------------------|
| [URLConnection](URLConnection.md)! | a`URLConnection`object for the`URL`. |

| Exceptions ||
|-------------------------------------------|---------------------------------------------------------------------------|
| `java.io.IOException` | if an I/O error occurs while opening the connection. |
| `java.lang.IllegalArgumentException` | if either u or p is null, or p has the wrong type. |
| `java.lang.UnsupportedOperationException` | if the subclass that implements the protocol doesn't support this method. |
| --- | --- |

### parseURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun parseURL(
    u: URL!, 
    spec: String!, 
    start: Int, 
    limit: Int
): Unit
```

Parses the string representation of a`URL`into a`URL`object.

If there is any inherited context, then it has already been copied into the`URL`argument.

The`parseURL`method of`URLStreamHandler`parses the string representation as if it were an`http`specification. Most URL protocol families have a similar parsing. A stream protocol handler for a protocol that has a different syntax must override this routine.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:the`URL`to receive the result of parsing the spec. |
| `spec` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the`String`representing the URL that must be parsed. |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character index at which to begin parsing. This is just past the '`:`' (if there is one) that specifies the determination of the protocol name. |
| --- | --- |
| `limit` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the character position to stop parsing at. This is the end of the string or the position of the "" character, if present. All information after the sharp sign indicates an anchor. |

### sameFile

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun sameFile(
    u1: URL!, 
    u2: URL!
): Boolean
```

Compare two urls to see whether they refer to the same file, i.e., having the same protocol, host, port, and path. This method requires that none of its arguments is null. This is guaranteed by the fact that it is only called indirectly by java.net.URL class.

| Parameters ||
|------|----------------------------------------------------------------------------------|
| `u1` | [URL](URL.md)!:a URL object |
| `u2` | [URL](URL.md)!:a URL object |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if u1 and u2 refer to the same file |

### setURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setURL(
    u: URL!, 
    protocol: String!, 
    host: String!, 
    port: Int, 
    file: String!, 
    ref: String!
): Unit
```

**Deprecated:** *Use setURL(URL, String, String, int, String, String, String, String);*

Sets the fields of the`URL`argument to the indicated values. Only classes derived from URLStreamHandler are able to use this method to set the values of the URL fields.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:the URL to modify. |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the protocol name. This value is ignored since 1.2. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the remote host value for the URL. |
| --- | --- |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the remote machine. |
| `file` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the file. |
| `ref` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the reference. |
| --- | --- |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------|
| `java.lang.SecurityException` | if the protocol handler of the URL is different from this one |

### setURL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun setURL(
    u: URL!, 
    protocol: String!, 
    host: String!, 
    port: Int, 
    authority: String!, 
    userInfo: String!, 
    path: String!, 
    query: String!, 
    ref: String!
): Unit
```

Sets the fields of the`URL`argument to the indicated values. Only classes derived from URLStreamHandler are able to use this method to set the values of the URL fields.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:the URL to modify. |
| `protocol` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the protocol name. |
| `host` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the remote host value for the URL. |
| --- | --- |
| `port` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the port on the remote machine. |
| `authority` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the authority part for the URL. |
| `userInfo` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the userInfo part of the URL. |
| --- | --- |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the path component of the URL. |
| `query` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the query part for the URL. |
| `ref` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the reference. |
| --- | --- |

| Exceptions ||
|-------------------------------|---------------------------------------------------------------|
| `java.lang.SecurityException` | if the protocol handler of the URL is different from this one |

### toExternalForm

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun toExternalForm(u: URL!): String!
```

Converts a`URL`of a specific protocol to a`String`.

| Parameters ||
|-----|------------------------------------------------------------------------------|
| `u` | [URL](URL.md)!:the URL. |

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | a string representation of the`URL`argument. |
