# HttpEngine

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# HttpEngine

Kotlin| [Java](https://developer.android.com/reference/android/net/http/HttpEngine "View this page in Java") 
| --- | --- |

```
abstract class HttpEngine
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#) |

An engine to process [UrlRequest](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest) s, which uses the best HTTP stack available on the current platform. An instance of this class can be created using [Builder](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine.Builder).

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine.Builder) A builder for [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#) s, which allows runtime configuration of [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindToNetwork](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#bindToNetwork(android.net.Network))`(`network:` ` [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)?`)` Binds the engine to the specified network. |
| abstract [URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory.html#) | [createUrlStreamHandlerFactory](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#createUrlStreamHandlerFactory())`()` Creates a [URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory.html#) to handle HTTP and HTTPS traffic. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersionString](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#getVersionString())`()` <br /> |
| --- | --- |
| abstract [BidirectionalStream.Builder](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder) | [newBidirectionalStreamBuilder](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#newBidirectionalStreamBuilder(kotlin.String,%20java.util.concurrent.Executor,%20android.net.http.BidirectionalStream.Callback))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback)`)` Creates a builder for [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream) objects. |
| abstract [UrlRequest.Builder](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder) | [newUrlRequestBuilder](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#newUrlRequestBuilder(kotlin.String,%20java.util.concurrent.Executor,%20android.net.http.UrlRequest.Callback))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback)`)` Creates a builder for [UrlRequest](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest). |
| abstract [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#) | [openConnection](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#openConnection(java.net.URL))`(`url:` ` [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)`)` Establishes a new connection to the resource specified by the [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)`url`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#shutdown())`()` Shuts down the [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#) if there are no active requests, otherwise throws an exception. |

## Public methods

### bindToNetwork

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open fun bindToNetwork(network: Network?): Unit
```

Binds the engine to the specified network. All requests created through this engine will use the network associated to this handle. If this network disconnects all requests will fail, the exact error will depend on the stage of request processing when the network disconnects.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `network` | [Network](https://developer.android.com/reference/kotlin/android/net/Network.html#)?:the network to bind the engine to. Specify`null`to unbind. |

### createUrlStreamHandlerFactory

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun createUrlStreamHandlerFactory(): URLStreamHandlerFactory
```

Creates a [URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory.html#) to handle HTTP and HTTPS traffic. An instance of this class can be installed via [URL.setURLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URL.html#setURLStreamHandlerFactory(java.net.URLStreamHandlerFactory))thus using this [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#) by default for all requests created via java.net.URL#openConnection.

This [java.net.HttpURLConnection](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#) implementation does not implement all features offered by the API:

- the HTTP cache installed via [HttpResponseCache.install()](https://developer.android.com/reference/kotlin/android/net/http/HttpResponseCache#install(java.io.File,%20kotlin.Long))
- the HTTP authentication method installed via [java.net.Authenticator#setDefault](https://developer.android.com/reference/kotlin/java/net/Authenticator.html#setDefault(java.net.Authenticator))
- the HTTP cookie storage installed via [java.net.CookieHandler#setDefault](https://developer.android.com/reference/kotlin/java/net/CookieHandler.html#setDefault(java.net.CookieHandler))

While we support and encourages requests using the HTTPS protocol, we don't provide support for the [HttpsURLConnection](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#) API. This lack of support also includes not using certain HTTPS features provided via [HttpsURLConnection](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#):

- the HTTPS hostname verifier installed via [HttpsURLConnection.setDefaultHostnameVerifier()](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#setDefaultHostnameVerifier(javax.net.ssl.HostnameVerifier))
- the HTTPS socket factory installed via [HttpsURLConnection.setDefaultSSLSocketFactory()](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#setDefaultSSLSocketFactory(javax.net.ssl.SSLSocketFactory))

| Return ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory.html#) | an [URLStreamHandlerFactory](https://developer.android.com/reference/kotlin/java/net/URLStreamHandlerFactory.html#) instance implemented by this [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#). This value cannot be`null`. |

### getVersionString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
open static fun getVersionString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a human-readable version string of the engine. This value cannot be`null`. |

### newBidirectionalStreamBuilder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun newBidirectionalStreamBuilder(
    url: String, 
    executor: Executor, 
    callback: BidirectionalStream.Callback
): BidirectionalStream.Builder
```

Creates a builder for [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream) objects. All callbacks for generated`BidirectionalStream`objects will be invoked on`executor`.`executor`must not run tasks on the current thread, otherwise the networking operations may block and exceptions may be thrown at shutdown time.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):URL for the generated streams. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#):the [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which`callback`methods will be invoked. This value cannot be`null`. |
| `callback` | [BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback):the [BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback) object that gets invoked upon different events occurring. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [BidirectionalStream.Builder](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder) | the created builder. This value cannot be`null`. |

### newUrlRequestBuilder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun newUrlRequestBuilder(
    url: String, 
    executor: Executor, 
    callback: UrlRequest.Callback
): UrlRequest.Builder
```

Creates a builder for [UrlRequest](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest). All callbacks for generated [UrlRequest](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest) objects will be invoked on`executor`'s threads.`executor`must not run tasks on the thread calling [Executor.execute](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable))to prevent blocking networking operations and causing exceptions during shutdown.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):URL for the generated requests. This value cannot be`null`. |
| `executor` | [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#): [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#) on which all callbacks will be invoked. This value cannot be`null`. |
| `callback` | [UrlRequest.Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback):callback object that gets invoked on different events. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------|
| [UrlRequest.Builder](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder) | This value cannot be`null`. |

### openConnection

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun openConnection(url: URL): URLConnection
```

Establishes a new connection to the resource specified by the [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#)`url`.

**Note:** This [java.net.HttpURLConnection](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#) implementation is subject to certain limitations, see [createUrlStreamHandlerFactory](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#createUrlStreamHandlerFactory())for details.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [URL](https://developer.android.com/reference/kotlin/java/net/URL.html#):URL of resource to connect to. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection.html#) | an [java.net.HttpURLConnection](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#) instance implemented by this [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#). This value cannot be`null`. |

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | if an error occurs while opening the connection. |

### shutdown

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun shutdown(): Unit
```

Shuts down the [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#) if there are no active requests, otherwise throws an exception. Cannot be called on network thread - the thread the HTTP stack calls into Executor on (which is different from the thread the Executor invokes callbacks on). May block until all the [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#) resources have been cleaned up.
