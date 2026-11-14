# CookieHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CookieHandler

```
abstract class CookieHandler
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.net.CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#) |

| Known Direct Subclasses [CookieManager](https://developer.android.com/reference/kotlin/java/net/CookieManager) |----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CookieManager](https://developer.android.com/reference/kotlin/java/net/CookieManager) | CookieManager provides a concrete implementation of [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#), which separates the storage of cookies from the policy surrounding accepting and rejecting cookies. | |

A CookieHandler object provides a callback mechanism to hook up a HTTP state management policy implementation into the HTTP protocol handler. The HTTP state management mechanism specifies a way to create a stateful session with HTTP requests and responses.

A system-wide CookieHandler to be used by the [HTTP URL stream protocol handler](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection) can be registered by doing a CookieHandler.setDefault(CookieHandler). The currently registered CookieHandler can be retrieved by calling CookieHandler.getDefault(). For more information on HTTP state management, see [*RFC 2965: HTTP State Management Mechanism*](http://www.ietf.org/rfc/rfc2965.txt)

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#CookieHandler())`()` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>! | [get](https://developer.android.com/reference/kotlin/java/net/CookieHandler#get(java.net.URI,%20kotlin.collections.MutableMap))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `requestHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` Gets all the applicable cookies from a cookie cache for the specified uri in the request header. |
| openstatic [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#)! | [getDefault](https://developer.android.com/reference/kotlin/java/net/CookieHandler#getDefault())`()` Gets the system-wide cookie handler. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [put](https://developer.android.com/reference/kotlin/java/net/CookieHandler#put(java.net.URI,%20kotlin.collections.MutableMap))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `responseHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` Sets all the applicable cookies, examples are response header fields that are named Set-Cookie2, present in the response headers into a cookie cache. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](https://developer.android.com/reference/kotlin/java/net/CookieHandler#setDefault(java.net.CookieHandler))`(`cHandler:` ` [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#)!`)` Sets (or unsets) the system-wide cookie handler. |

## Public constructors

### CookieHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CookieHandler()
```

## Public methods

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(
    uri: URI!, 
    requestHeaders: MutableMap<String!, MutableList<String!>!>!
): MutableMap<String!, MutableList<String!>!>!
```

Gets all the applicable cookies from a cookie cache for the specified uri in the request header.

The`URI`passed as an argument specifies the intended use for the cookies. In particular the scheme should reflect whether the cookies will be sent over http, https or used in another context like javascript. The host part should reflect either the destination of the cookies or their origin in the case of javascript.

It is up to the implementation to take into account the`URI`and the cookies attributes and security settings to determine which ones should be returned.

HTTP protocol implementers should make sure that this method is called after all request headers related to choosing cookies are added, and before the request is sent.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:a`URI`representing the intended use for the cookies |
| `requestHeaders` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:- a Map from request header field names to lists of field values representing the current request headers |

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>! | an immutable map from state management headers, with field names "Cookie" or "Cookie2" to a list of cookies containing state information |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if either argument is null |

**See Also**

- [#put(URI, Map)](https://developer.android.com/reference/kotlin/java/net/CookieHandler#put(java.net.URI,%20kotlin.collections.MutableMap)) 

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): CookieHandler!
```

Gets the system-wide cookie handler.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#)! | the system-wide cookie handler; A null return means there is no system-wide cookie handler currently set. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission)`("getCookieHandler")` |

**See Also**

- [#setDefault(CookieHandler)](https://developer.android.com/reference/kotlin/java/net/CookieHandler#setDefault(java.net.CookieHandler)) 

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(
    uri: URI!, 
    responseHeaders: MutableMap<String!, MutableList<String!>!>!
): Unit
```

Sets all the applicable cookies, examples are response header fields that are named Set-Cookie2, present in the response headers into a cookie cache.

| Parameters ||
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:a`URI`where the cookies come from |
| `responseHeaders` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:an immutable map from field names to lists of field values representing the response header fields returned |

| Exceptions ||
|--------------------------------------|----------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if either argument is null |

**See Also**

- [#get(URI, Map)](https://developer.android.com/reference/kotlin/java/net/CookieHandler#get(java.net.URI,%20kotlin.collections.MutableMap)) 

### setDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(cHandler: CookieHandler!): Unit
```

Sets (or unsets) the system-wide cookie handler. Note: non-standard http protocol handlers may ignore this setting.

| Parameters ||
|------------|-------------------------------------------------------------------------------------------------------------------------------------|
| `cHandler` | [CookieHandler](https://developer.android.com/reference/kotlin/java/net/CookieHandler#)!:The HTTP cookie handler, or`null`to unset. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission)`("setCookieHandler")` |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/CookieHandler#getDefault()>
