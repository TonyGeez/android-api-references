# android.net.http

## Interfaces

| [Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback) | Callback interface used to receive callbacks from a `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream`. |
| [HttpConnectCallback](https://developer.android.com/reference/kotlin/android/net/http/Proxy.HttpConnectCallback) | Controls tunnels established via HTTP CONNECT. |
| [Callback](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback) | Users of the HTTP stack extend this class to receive callbacks indicating the progress of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest` being processed. |
| [StatusListener](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.StatusListener) | Listener interface used with `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getStatus(android.net.http.UrlRequest.StatusListener)` to receive the status of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`. |

## Classes

| [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream) | Class for bidirectional sending and receiving of data over HTTP/2 or QUIC connections. |
| [ConnectionMigrationOptions](https://developer.android.com/reference/kotlin/android/net/http/ConnectionMigrationOptions) | A class configuring the HTTP connection migration functionality. |
| [DnsOptions](https://developer.android.com/reference/kotlin/android/net/http/DnsOptions) | A class configuring the host resolution functionality. |
| [FinishedRequestTimings](https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings) | Metrics collected for a single request. |
| [HeaderBlock](https://developer.android.com/reference/kotlin/android/net/http/HeaderBlock) | Unmodifiable container of headers or trailers. |
| [HttpEngine](https://developer.android.com/reference/kotlin/android/net/http/HttpEngine) | An engine to process `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`s, which uses the best HTTP stack available on the current platform. |
| [HttpResponseCache](https://developer.android.com/reference/kotlin/android/net/http/HttpResponseCache) | Caches HTTP and HTTPS responses to the filesystem so they may be reused, saving time and bandwidth. |
| [Proxy](https://developer.android.com/reference/kotlin/android/net/http/Proxy) | Represents a proxy that can be used by `https://developer.android.com/reference/kotlin/android/net/http/HttpEngine`. |
| [ProxyOptions](https://developer.android.com/reference/kotlin/android/net/http/ProxyOptions) | Defines a proxy configuration that can be used by `https://developer.android.com/reference/kotlin/android/net/http/HttpEngine`. |
| [QuicOptions](https://developer.android.com/reference/kotlin/android/net/http/QuicOptions) | Configuration options for QUIC. |
| [SslCertificate](https://developer.android.com/reference/kotlin/android/net/http/SslCertificate) | SSL certificate info (certificate details) class |
| [SslError](https://developer.android.com/reference/kotlin/android/net/http/SslError) | This class represents a set of one or more SSL errors and the associated SSL certificate. |
| [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) | Abstract class allowing the embedder to provide an upload body to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`. |
| [UploadDataSink](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink) | Defines callbacks methods for `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider`. |
| [UrlRequest](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest) | Controls an HTTP request (GET, PUT, POST etc). |
| [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo) | Basic information about a response. |
| [X509TrustManagerExtensions](https://developer.android.com/reference/kotlin/android/net/http/X509TrustManagerExtensions) | X509TrustManager wrapper exposing Android-added features. |

## Exceptions

| [CallbackException](https://developer.android.com/reference/kotlin/android/net/http/CallbackException) | Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback` or `https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider` method throws an exception. |
| [HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException) | Base exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)`. |
| [InlineExecutionProhibitedException](https://developer.android.com/reference/kotlin/android/net/http/InlineExecutionProhibitedException) | Thrown when an executor runs a submitted runnable inline in `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#execute(java.lang.Runnable)` and `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setDirectExecutorAllowed(kotlin.Boolean)` was not called. |
| [NetworkException](https://developer.android.com/reference/kotlin/android/net/http/NetworkException) | Exception passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` when the HTTP stack fails to process a network request. |
| [QuicException](https://developer.android.com/reference/kotlin/android/net/http/QuicException) | Subclass of `https://developer.android.com/reference/kotlin/android/net/http/NetworkException` which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). |
