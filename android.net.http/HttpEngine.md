# HttpEngine

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# HttpEngine

Kotlin| [Java](../android/net/http/HttpEngine.md) 
| --- | --- |

```
abstract class HttpEngine
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.HttpEngine](../android/net/http/HttpEngine.md) |

An engine to process [UrlRequest](../android/net/http/UrlRequest.md) s, which uses the best HTTP stack available on the current platform. An instance of this class can be created using [Builder](../android/net/http/HttpEngine.Builder.md).

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [Builder](../android/net/http/HttpEngine.Builder.md) A builder for [HttpEngine](../android/net/http/HttpEngine.md) s, which allows runtime configuration of [HttpEngine](../android/net/http/HttpEngine.md). |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [bindToNetwork](../android/net/http/HttpEngine.md))`(`network:` ` [Network](../android/net/Network.md)?`)` Binds the engine to the specified network. |
| abstract [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md) | [createUrlStreamHandlerFactory](../android/net/http/HttpEngine.md))`()` Creates a [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md) to handle HTTP and HTTPS traffic. |
| openstatic [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getVersionString](../android/net/http/HttpEngine.md))`()` <br /> |
| --- | --- |
| abstract [BidirectionalStream.Builder](../android/net/http/BidirectionalStream.Builder.md) | [newBidirectionalStreamBuilder](../android/net/http/HttpEngine.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md)`)` Creates a builder for [BidirectionalStream](../android/net/http/BidirectionalStream.md) objects. |
| abstract [UrlRequest.Builder](../android/net/http/UrlRequest.Builder.md) | [newUrlRequestBuilder](../android/net/http/HttpEngine.md))`(`url:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `executor:` ` [Executor](../java/util/concurrent/Executor.md)`, `callback:` ` [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md)`)` Creates a builder for [UrlRequest](../android/net/http/UrlRequest.md). |
| abstract [URLConnection](../java/net/URLConnection.md) | [openConnection](../android/net/http/HttpEngine.md))`(`url:` ` [URL](../java/net/URL.md)`)` Establishes a new connection to the resource specified by the [URL](../java/net/URL.md)`url`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [shutdown](../android/net/http/HttpEngine.md))`()` Shuts down the [HttpEngine](../android/net/http/HttpEngine.md) if there are no active requests, otherwise throws an exception. |

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
| `network` | [Network](../android/net/Network.md)?:the network to bind the engine to. Specify`null`to unbind. |

### createUrlStreamHandlerFactory

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun createUrlStreamHandlerFactory(): URLStreamHandlerFactory
```

Creates a [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md) to handle HTTP and HTTPS traffic. An instance of this class can be installed via [URL.setURLStreamHandlerFactory](../java/net/URL.md))thus using this [HttpEngine](../android/net/http/HttpEngine.md) by default for all requests created via java.net.URL#openConnection.

This [java.net.HttpURLConnection](../java/net/HttpURLConnection.md) implementation does not implement all features offered by the API:

- the HTTP cache installed via [HttpResponseCache.install()](../android/net/http/HttpResponseCache.md))
- the HTTP authentication method installed via [java.net.Authenticator#setDefault](../java/net/Authenticator.md))
- the HTTP cookie storage installed via [java.net.CookieHandler#setDefault](../java/net/CookieHandler.md))

While we support and encourages requests using the HTTPS protocol, we don't provide support for the [HttpsURLConnection](../javax/net/ssl/HttpsURLConnection.md) API. This lack of support also includes not using certain HTTPS features provided via [HttpsURLConnection](../javax/net/ssl/HttpsURLConnection.md):

- the HTTPS hostname verifier installed via [HttpsURLConnection.setDefaultHostnameVerifier()](../javax/net/ssl/HttpsURLConnection.md))
- the HTTPS socket factory installed via [HttpsURLConnection.setDefaultSSLSocketFactory()](../javax/net/ssl/HttpsURLConnection.md))

| Return ||
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md) | an [URLStreamHandlerFactory](../java/net/URLStreamHandlerFactory.md) instance implemented by this [HttpEngine](../android/net/http/HttpEngine.md). This value cannot be`null`. |

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

Creates a builder for [BidirectionalStream](../android/net/http/BidirectionalStream.md) objects. All callbacks for generated`BidirectionalStream`objects will be invoked on`executor`.`executor`must not run tasks on the current thread, otherwise the networking operations may block and exceptions may be thrown at shutdown time.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):URL for the generated streams. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md):the [Executor](../java/util/concurrent/Executor.md) on which`callback`methods will be invoked. This value cannot be`null`. |
| `callback` | [BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md):the [BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md) object that gets invoked upon different events occurring. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [BidirectionalStream.Builder](../android/net/http/BidirectionalStream.Builder.md) | the created builder. This value cannot be`null`. |

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

Creates a builder for [UrlRequest](../android/net/http/UrlRequest.md). All callbacks for generated [UrlRequest](../android/net/http/UrlRequest.md) objects will be invoked on`executor`'s threads.`executor`must not run tasks on the thread calling [Executor.execute](../java/util/concurrent/Executor.md))to prevent blocking networking operations and causing exceptions during shutdown.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):URL for the generated requests. This value cannot be`null`. |
| `executor` | [Executor](../java/util/concurrent/Executor.md): [Executor](../java/util/concurrent/Executor.md) on which all callbacks will be invoked. This value cannot be`null`. |
| `callback` | [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md):callback object that gets invoked on different events. This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------|
| [UrlRequest.Builder](../android/net/http/UrlRequest.Builder.md) | This value cannot be`null`. |

### openConnection

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun openConnection(url: URL): URLConnection
```

Establishes a new connection to the resource specified by the [URL](../java/net/URL.md)`url`.

**Note:** This [java.net.HttpURLConnection](../java/net/HttpURLConnection.md) implementation is subject to certain limitations, see [createUrlStreamHandlerFactory](../android/net/http/HttpEngine.md))for details.

| Parameters ||
|-------|-------------------------------------------------------------------------------------------------------------------------------------|
| `url` | [URL](../java/net/URL.md):URL of resource to connect to. This value cannot be`null`. |

| Return ||
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [URLConnection](../java/net/URLConnection.md) | an [java.net.HttpURLConnection](../java/net/HttpURLConnection.md) instance implemented by this [HttpEngine](../android/net/http/HttpEngine.md). This value cannot be`null`. |

| Exceptions ||
|-----------------------|--------------------------------------------------|
| `java.io.IOException` | if an error occurs while opening the connection. |

### shutdown

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun shutdown(): Unit
```

Shuts down the [HttpEngine](../android/net/http/HttpEngine.md) if there are no active requests, otherwise throws an exception. Cannot be called on network thread - the thread the HTTP stack calls into Executor on (which is different from the thread the Executor invokes callbacks on). May block until all the [HttpEngine](../android/net/http/HttpEngine.md) resources have been cleaned up.
