# ResponseCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ResponseCache

```
abstract class ResponseCache
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [java.net.ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache#) |

| Known Direct Subclasses [HttpResponseCache](https://developer.android.com/reference/kotlin/android/net/http/HttpResponseCache.html#) |--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------| | [HttpResponseCache](https://developer.android.com/reference/kotlin/android/net/http/HttpResponseCache.html#) | Caches HTTP and HTTPS responses to the filesystem so they may be reused, saving time and bandwidth. | |

Represents implementations of URLConnection caches. An instance of such a class can be registered with the system by doing ResponseCache.setDefault(ResponseCache), and the system will call this object in order to:

- store resource data which has been retrieved from an external source into the cache
- try to fetch a requested resource that may have been stored in the cache

The ResponseCache implementation decides which resources should be cached, and for how long they should be cached. If a request resource cannot be retrieved from the cache, then the protocol handlers will fetch the resource from its original location. The settings for URLConnection#useCaches controls whether the protocol is allowed to use a cached response. For more information on HTTP caching, see [*RFC 2616: Hypertext Transfer Protocol -- HTTP/1.1*](http://www.ietf.org/rfc/rfc2616.txt)

<br />

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------|---|
| [ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache#ResponseCache())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CacheResponse](https://developer.android.com/reference/kotlin/java/net/CacheResponse)! | [get](https://developer.android.com/reference/kotlin/java/net/ResponseCache#get(java.net.URI,%20kotlin.String,%20kotlin.collections.MutableMap))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `rqstMethod:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `rqstHeaders:` ` [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!,` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!>!`)` Retrieve the cached response based on the requesting uri, request method and request headers. |
| openstatic [ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache#)! | [getDefault](https://developer.android.com/reference/kotlin/java/net/ResponseCache#getDefault())`()` Gets the system-wide response cache. |
| abstract [CacheRequest](https://developer.android.com/reference/kotlin/java/net/CacheRequest)! | [put](https://developer.android.com/reference/kotlin/java/net/ResponseCache#put(java.net.URI,%20java.net.URLConnection))`(`uri:` ` [URI](https://developer.android.com/reference/kotlin/java/net/URI)!`, `conn:` ` [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection)!`)` The protocol handler calls this method after a resource has been retrieved, and the ResponseCache must decide whether or not to store the resource in its cache. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDefault](https://developer.android.com/reference/kotlin/java/net/ResponseCache#setDefault(java.net.ResponseCache))`(`responseCache:` ` [ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache#)!`)` Sets (or unsets) the system-wide cache. |

## Public constructors

### ResponseCache

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
ResponseCache()
```

## Public methods

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun get(
    uri: URI!, 
    rqstMethod: String!, 
    rqstHeaders: MutableMap<String!, MutableList<String!>!>!
): CacheResponse!
```

Retrieve the cached response based on the requesting uri, request method and request headers. Typically this method is called by the protocol handler before it sends out the request to get the network resource. If a cached response is returned, that resource is used instead.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:a`URI`used to reference the requested network resource |
| `rqstMethod` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:a`String`representing the request method |
| `rqstHeaders` | [MutableMap](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!, [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!\>!:- a Map from request header field names to lists of field values representing the current request headers |

| Return ||
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [CacheResponse](https://developer.android.com/reference/kotlin/java/net/CacheResponse)! | a`CacheResponse`instance if available from cache, or null otherwise |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if any one of the arguments is null |

**See Also**

- [java.net.URLConnection#setUseCaches(boolean)](https://developer.android.com/reference/kotlin/java/net/URLConnection#setUseCaches(kotlin.Boolean))
- [java.net.URLConnection#getUseCaches()](https://developer.android.com/reference/kotlin/java/net/URLConnection#getUseCaches())
- [java.net.URLConnection#setDefaultUseCaches(boolean)](https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultUseCaches(kotlin.Boolean))
- [java.net.URLConnection#getDefaultUseCaches()](https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultUseCaches()) 

### getDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDefault(): ResponseCache!
```

Gets the system-wide response cache.

| Return ||
|------------------------------------------------------------------------------------------|--------------------------------|
| [ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache#)! | the system-wide`ResponseCache` |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission)`("getResponseCache")` |

**See Also**

- [#setDefault(ResponseCache)](https://developer.android.com/reference/kotlin/java/net/ResponseCache#setDefault(java.net.ResponseCache)) 

### put

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun put(
    uri: URI!, 
    conn: URLConnection!
): CacheRequest!
```

The protocol handler calls this method after a resource has been retrieved, and the ResponseCache must decide whether or not to store the resource in its cache. If the resource is to be cached, then put() must return a CacheRequest object which contains an OutputStream that the protocol handler will use to write the resource into the cache. If the resource is not to be cached, then put must return null.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uri` | [URI](https://developer.android.com/reference/kotlin/java/net/URI)!:a`URI`used to reference the requested network resource |
| `conn` | [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection)!:- a URLConnection instance that is used to fetch the response to be cached |

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [CacheRequest](https://developer.android.com/reference/kotlin/java/net/CacheRequest)! | a`CacheRequest`for recording the response to be cached. Null return indicates that the caller does not intend to cache the response. |

| Exceptions ||
|--------------------------------------|-------------------------------------|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if any one of the arguments is null |

### setDefault

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun setDefault(responseCache: ResponseCache!): Unit
```

Sets (or unsets) the system-wide cache. Note: non-standard procotol handlers may ignore this setting.

| Parameters ||
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| `responseCache` | [ResponseCache](https://developer.android.com/reference/kotlin/java/net/ResponseCache#)!:The response cache, or`null`to unset the cache. |

| Exceptions ||
|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.SecurityException` | If a security manager has been installed and it denies [NetPermission](https://developer.android.com/reference/kotlin/java/net/NetPermission)`("setResponseCache")` |

**See Also**

- <https://developer.android.com/reference/kotlin/java/net/ResponseCache#getDefault()>
