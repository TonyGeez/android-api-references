# android.net.http

## Interfaces

| [Callback](../android/net/http/BidirectionalStream.Callback.md) | Callback interface used to receive callbacks from a BidirectionalStream. |
| --- | --- |
| [HttpConnectCallback](../android/net/http/Proxy.HttpConnectCallback.md) | Controls tunnels established via HTTP CONNECT. |
| [Callback](../android/net/http/UrlRequest.Callback.md) | Users of the HTTP stack extend this class to receive callbacks indicating the progress of a UrlRequest being processed. |
| [StatusListener](../android/net/http/UrlRequest.StatusListener.md) | Listener interface used with getStatus to receive the status of a UrlRequest. |
| --- | --- |

## Classes

| [BidirectionalStream](BidirectionalStream.md) | Class for bidirectional sending and receiving of data over HTTP/2 or QUIC connections. |
| --- | --- |
| [ConnectionMigrationOptions](ConnectionMigrationOptions.md) | A class configuring the HTTP connection migration functionality. |
| [DnsOptions](DnsOptions.md) | A class configuring the host resolution functionality. |
| [FinishedRequestTimings](FinishedRequestTimings.md) | Metrics collected for a single request. |
| --- | --- |
| [HeaderBlock](HeaderBlock.md) | Unmodifiable container of headers or trailers. |
| [HttpEngine](HttpEngine.md) | An engine to process UrlRequests, which uses the best HTTP stack available on the current platform. |
| [HttpResponseCache](HttpResponseCache.md) | Caches HTTP and HTTPS responses to the filesystem so they may be reused, saving time and bandwidth. |
| --- | --- |
| [Proxy](../android/net/http/Proxy.md) | Represents a proxy that can be used by HttpEngine. |
| [ProxyOptions](../android/net/http/ProxyOptions.md) | Defines a proxy configuration that can be used by HttpEngine. |
| [QuicOptions](QuicOptions.md) | Configuration options for QUIC. |
| --- | --- |
| [SslCertificate](SslCertificate.md) | SSL certificate info (certificate details) class |
| [SslError](SslError.md) | This class represents a set of one or more SSL errors and the associated SSL certificate. |
| [UploadDataProvider](UploadDataProvider.md) | Abstract class allowing the embedder to provide an upload body to UrlRequest. |
| --- | --- |
| [UploadDataSink](UploadDataSink.md) | Defines callbacks methods for UploadDataProvider. |
| [UrlRequest](UrlRequest.md) | Controls an HTTP request (GET, PUT, POST etc). |
| [UrlResponseInfo](UrlResponseInfo.md) | Basic information about a response. |
| --- | --- |
| [X509TrustManagerExtensions](X509TrustManagerExtensions.md) | X509TrustManager wrapper exposing Android-added features. |

## Exceptions

| [CallbackException](CallbackException.md) | Exception passed to onFailed when `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback` or UploadDataProvider method throws an exception. |
| --- | --- |
| [HttpException](HttpException.md) | Base exception passed to onFailed. |
| [InlineExecutionProhibitedException](InlineExecutionProhibitedException.md) | Thrown when an executor runs a submitted runnable inline in execute and setDirectExecutorAllowed was not called. |
| [NetworkException](NetworkException.md) | Exception passed to onFailed when the HTTP stack fails to process a network request. |
| --- | --- |
| [QuicException](QuicException.md) | Subclass of NetworkException which contains a detailed [QUIC](https://www.chromium.org/quic) error code from [QuicErrorCode](https://cs.chromium.org/search/?q=symbol:%5CbQuicErrorCode%5Cb). |
