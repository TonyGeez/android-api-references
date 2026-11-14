# UrlResponseInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# UrlResponseInfo

Kotlin| [Java](../android/net/http/UrlResponseInfo.md) 
| --- | --- |

```
abstract class UrlResponseInfo
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.UrlResponseInfo](../android/net/http/UrlResponseInfo.md) |

Basic information about a response. Included in [UrlRequest.Callback](../android/net/http/UrlRequest.Callback.md) callbacks. Each [onRedirectReceived()](../android/net/http/UrlRequest.Callback.md))callback gets a different copy of`UrlResponseInfo`describing a particular redirect response.

## Summary

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------|---|
| [UrlResponseInfo](../android/net/http/UrlResponseInfo.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [HeaderBlock](../android/net/http/HeaderBlock.md) | [getHeaders](../android/net/http/UrlResponseInfo.md))`()` Returns the response headers. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getHttpStatusCode](../android/net/http/UrlResponseInfo.md))`()` Returns the HTTP status code. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getHttpStatusText](../android/net/http/UrlResponseInfo.md))`()` Returns the HTTP status text of the status line. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getNegotiatedProtocol](../android/net/http/UrlResponseInfo.md))`()` Returns the protocol (for example 'quic/1+spdy/3') negotiated with the server. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getReceivedByteCount](../android/net/http/UrlResponseInfo.md))`()` Returns a minimum count of bytes received from the network to process this request. |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getUrl](../android/net/http/UrlResponseInfo.md))`()` Returns the URL the response is for. |
| --- | --- |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\> | [getUrlChain](../android/net/http/UrlResponseInfo.md))`()` Returns the URL chain. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [wasCached](../android/net/http/UrlResponseInfo.md))`()` Returns`true`if the response came from the cache, including requests that were revalidated over the network before being retrieved from the cache. |

## Public constructors

### UrlResponseInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
UrlResponseInfo()
```

## Public methods

### getHeaders

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getHeaders(): HeaderBlock
```

Returns the response headers.

| Return ||
|--------------------------------------------------------------------------------------------|-----------------------------|
| [HeaderBlock](../android/net/http/HeaderBlock.md) | This value cannot be`null`. |

### getHttpStatusCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getHttpStatusCode(): Int
```

Returns the HTTP status code. When a resource is retrieved from the cache, whether it was revalidated or not, the original status code is returned.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the HTTP status code. |

### getHttpStatusText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getHttpStatusText(): String
```

Returns the HTTP status text of the status line. For example, if the request received a "HTTP/1.1 200 OK" response, this method returns "OK".

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the HTTP status text of the status line. This value cannot be`null`. |

### getNegotiatedProtocol

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getNegotiatedProtocol(): String
```

Returns the protocol (for example 'quic/1+spdy/3') negotiated with the server. Returns an empty string if no protocol was negotiated, the protocol is not known, or when using plain HTTP or HTTPS.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the protocol negotiated with the server. This value cannot be`null`. |

### getReceivedByteCount

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getReceivedByteCount(): Long
```

Returns a minimum count of bytes received from the network to process this request. This count may ignore certain overheads (for example IP and TCP/UDP framing, SSL handshake and framing, proxy handling). This count is taken prior to decompression (for example GZIP) and includes headers and data from all redirects. This value may change (even for one [UrlResponseInfo](../android/net/http/UrlResponseInfo.md) instance) as the request progresses until completion, when [onSucceeded()](../android/net/http/UrlRequest.Callback.md)), [onFailed()](../android/net/http/UrlRequest.Callback.md)), or [onCanceled()](../android/net/http/UrlRequest.Callback.md))is called.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | a minimum count of bytes received from the network to process this request. |

### getUrl

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getUrl(): String
```

Returns the URL the response is for. This is the URL after following redirects, so it may not be the originally requested URL.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the URL the response is for. This value cannot be`null`. |

### getUrlChain

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getUrlChain(): MutableList<String!>
```

Returns the URL chain. The first entry is the originally requested URL; the following entries are redirects followed.

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!> | the URL chain. This value cannot be`null`. |

### wasCached

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun wasCached(): Boolean
```

Returns`true`if the response came from the cache, including requests that were revalidated over the network before being retrieved from the cache.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the response came from the cache,`false`otherwise. |
