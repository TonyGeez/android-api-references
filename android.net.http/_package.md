# android.net.http

## Interfaces

| [Callback](../android/net/http/BidirectionalStream.Callback.md) | Callback interface used to receive callbacks from a `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream`. |
| --- | --- |
| [HttpConnectCallback](../android/net/http/Proxy.HttpConnectCallback.md) | Controls tunnels established via HTTP CONNECT. |
| [Callback](../android/net/http/UrlRequest.Callback.md) | Users of the HTTP stack extend this class to receive callbacks indicating the progress of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest` being processed. |
| [StatusListener](../android/net/http/UrlRequest.StatusListener.md) | Listener interface used with `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getStatus(android.net.http.UrlRequest.StatusListener)` to receive the status of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`. |
| --- | --- |

## Classes

| [BidirectionalStream](../android/net/http/BidirectionalStream.md) | Class for bidirectional sending and receiving of data over HTTP/2 or QUIC connections. |
| --- | --- |
| [ConnectionMigrationOptions](../android/net/http/ConnectionMigrationOptions.md) | A class configuring the HTTP connection migration functionality. |
| [DnsOptions](../android/net/http/DnsOptions.md) | A class configuring the host resolution functionality. |
| [FinishedRequestTimings](../android/net/http/FinishedRequestTimings.md) | Metrics collected for a single request. |
| --- | --- |
| [HeaderBlock](../android/net/http/HeaderBlock.md) | Unmodifiable container of headers or trailers. |
| [HttpEngine](../android/net/http/HttpEngine.md) | An engine to process `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`s, which uses the best HTTP stack available on the current platform. |
| [HttpResponseCache](../android/net/http/HttpResponseCache.md) | Caches HTTP and HTTPS responses to the filesystem so they may be reused, saving time and bandwidth. |
| --- | --- |
| [Proxy](../android/net/http/Proxy.md) | Represents a proxy that can be used by `https://developer.android.com/reference/kotlin/android/net/http/HttpEngine`. |
| [ProxyOptions](../android/net/http/ProxyOptions.md) | Defines a proxy configuration that can be used by `https://developer.android.com/reference/kotlin/android/net/http/HttpEngine`. |
| [QuicOptions](../android/net/http/QuicOptions.md) | Configuration options for QUIC. |
| --- | --- |
| [SslCertificate](../android/net/http/SslCertificate.md) | SSL certificate info (certificate details) class |
| [SslError](../android/net/http/SslError.md) | This class represents a set of one or more SSL errors and the associated SSL certificate. |
| [UploadDataProvider](../android/net/http/UploadDataProvider.md) | Abstract class allowing the embedder to provide an upload body to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`. |
| --- | --- |
| [UploadDataSink](../android/net/http/UploadDataSink.md) | Defines callbacks methods for `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider`. |
| [UrlRequest](../android/net/http/UrlRequest.md) | Controls an HTTP request (GET, PUT, POST etc). |
| [UrlResponseInfo](../android/net/http/UrlResponseInfo.md) | Basic information about a response. |
| --- | --- |
| [X509TrustManagerExtensions](../android/net/http/X509TrustManagerExtensions.md) | X509TrustManager wrapper exposing Android-added features. |

## Exceptions

| [CallbackException](../android/net/http/CallbackException.md) | Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback` or `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider` method throws an exception. |
| --- | --- |
| [HttpException](../android/net/http/HttpException.md) | Base exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)`. |
| [InlineExecutionProhibitedException](../android/net/http/InlineExecutionProhibitedException.md) | Thrown when an executor runs a submitted runnable inline in `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable)` and `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setDirectExecutorAllowed(kotlin.Boolean)` was not called. |
| [NetworkException](../android/net/http/NetworkException.md) | Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when the HTTP stack fails to process a network request. |
| --- | --- |
| [QuicException](../android/net/http/QuicException.md) | Subclass of `https://developer.android.com/reference/kotlin/android/net/http/NetworkException` which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). |
