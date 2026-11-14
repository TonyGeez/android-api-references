Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpURLConnection

```
abstract class HttpURLConnection : URLConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [java.net.URLConnection](https://developer.android.com/reference/kotlin/java/net/URLConnection) ||
| | ↳ | [java.net.HttpURLConnection](https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#) |

| Known Direct Subclasses [HttpsURLConnection](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#) |---|---| | [HttpsURLConnection](https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#) | `HttpsURLConnection` extends `HttpURLConnection` with support for https-specific features. | |

A URLConnection with support for HTTP-specific features. See [the spec](http://www.w3.org/pub/WWW/Protocols/) for details.

Uses of this class follow a pattern:

1. Obtain a new `HttpURLConnection` by calling `https://developer.android.com/reference/kotlin/java/net/URL#openConnection()` and casting the result to `HttpURLConnection`.
2. Prepare the request. The primary property of a request is its URI. Request headers may also include metadata such as credentials, preferred content types, and session cookies.
3. Optionally upload a request body. Instances must be configured with `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoOutput(kotlin.Boolean)` if they include a request body. Transmit data by writing to the stream returned by `https://developer.android.com/reference/kotlin/java/net/URLConnection#getOutputStream()`.
4. Read the response. Response headers typically include metadata such as the response body's content type and length, modified dates and session cookies. The response body may be read from the stream returned by `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()`. If the response has no body, that method returns an empty stream.
5. Disconnect. Once the response body has been read, the `HttpURLConnection` should be closed by calling `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#disconnect()`. Disconnecting releases the resources held by a connection so they may be closed or reused.

For example, to retrieve the webpage at `http://www.android.com/`:

```kotlin
<code>URL url = new URL("http://www.android.com/");
    HttpURLConnection urlConnection = (HttpURLConnection) url.openConnection();
    try {
      InputStream in = new BufferedInputStream(urlConnection.getInputStream());
      readStream(in);
    } finally {
      urlConnection.disconnect();
    }
  </code>
```

### Secure Communication with HTTPS

Calling `https://developer.android.com/reference/kotlin/java/net/URL#openConnection()` on a URL with the "https" scheme will return an `HttpsURLConnection`, which allows for overriding the default `https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier.html#` and `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory.html#`. An application-supplied `SSLSocketFactory` created from an `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLContext.html#` can provide a custom `https://developer.android.com/reference/kotlin/javax/net/ssl/X509TrustManager.html#` for verifying certificate chains and a custom `https://developer.android.com/reference/kotlin/javax/net/ssl/X509KeyManager.html#` for supplying client certificates. See `https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection.html#` for more details.

### Response Handling

`HttpURLConnection` will follow up to five HTTP redirects. It will follow redirects from one origin server to another. This implementation doesn't follow redirects from HTTPS to HTTP or vice versa.

If the HTTP response indicates that an error occurred, `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()` will throw an `https://developer.android.com/reference/kotlin/java/io/IOException.html#`. Use `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getErrorStream()` to read the error response. The headers can be read in the normal way using `https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFields()`,

### Posting Content

To upload data to a web server, configure the connection for output using `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoOutput(kotlin.Boolean)`.

For best performance, you should call either `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFixedLengthStreamingMode(kotlin.Int)` when the body length is known in advance, or `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setChunkedStreamingMode(kotlin.Int)` when it is not. Otherwise `HttpURLConnection` will be forced to buffer the complete request body in memory before it is transmitted, wasting (and possibly exhausting) heap and increasing latency.

For example, to perform an upload:

```kotlin
<code>HttpURLConnection urlConnection = (HttpURLConnection) url.openConnection();
    try {
      urlConnection.setDoOutput(true);
      urlConnection.setChunkedStreamingMode(0);
 
      OutputStream out = new BufferedOutputStream(urlConnection.getOutputStream());
      writeStream(out);
 
      InputStream in = new BufferedInputStream(urlConnection.getInputStream());
      readStream(in);
    } finally {
      urlConnection.disconnect();
    }
  </code>
```

### Performance

The input and output streams returned by this class are **not buffered** . Most callers should wrap the returned streams with `https://developer.android.com/reference/kotlin/java/io/BufferedInputStream.html#` or `https://developer.android.com/reference/kotlin/java/io/BufferedOutputStream.html#`. Callers that do only bulk reads or writes may omit buffering.

When transferring large amounts of data to or from a server, use streams to limit how much data is in memory at once. Unless you need the entire body to be in memory at once, process it as a stream (rather than storing the complete body as a single byte array or string).

To reduce latency, this class may reuse the same underlying `Socket` for multiple request/response pairs. As a result, HTTP connections may be held open longer than necessary. Calls to `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#disconnect()` may return the socket to a pool of connected sockets.

By default, this implementation of `HttpURLConnection` requests that servers use gzip compression and it automatically decompresses the data for callers of `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()`. The Content-Encoding and Content-Length response headers are cleared in this case. Gzip compression can be disabled by setting the acceptable encodings in the request header:

```kotlin
<code>urlConnection.setRequestProperty("Accept-Encoding", "identity");
  </code>
```

Setting the Accept-Encoding request header explicitly disables automatic decompression and leaves the response headers intact; callers must handle decompression as needed, according to the Content-Encoding header of the response.

`https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLength()` returns the number of bytes transmitted and cannot be used to predict how many bytes can be read from `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()` for compressed streams. Instead, read that stream until it is exhausted, i.e. when java.io.InputStream#read returns -1.

### Handling Network Sign-On

Some Wi-Fi networks block Internet access until the user clicks through a sign-on page. Such sign-on pages are typically presented by using HTTP redirects. You can use `https://developer.android.com/reference/kotlin/java/net/URLConnection#getURL()` to test if your connection has been unexpectedly redirected. This check is not valid until **after** the response headers have been received, which you can trigger by calling `https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFields()` or `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()`. For example, to check that a response was not redirected to an unexpected host:

```kotlin
<code>HttpURLConnection urlConnection = (HttpURLConnection) url.openConnection();
    try {
      InputStream in = new BufferedInputStream(urlConnection.getInputStream());
      if (!url.getHost().equals(urlConnection.getURL().getHost())) {
        // we were redirected! Kick the user out to the browser to sign on?
      }
      ...
    } finally {
      urlConnection.disconnect();
    }
  </code>
```

### HTTP Authentication

`HttpURLConnection` supports [HTTP basic authentication](http://www.ietf.org/rfc/rfc2617). Use `https://developer.android.com/reference/kotlin/java/net/Authenticator` to set the VM-wide authentication handler:

```kotlin
<code>Authenticator.setDefault(new Authenticator() {
      protected PasswordAuthentication getPasswordAuthentication() {
        return new PasswordAuthentication(username, password.toCharArray());
      }
    });
  </code>
```
Unless paired with HTTPS, this is **not** a secure mechanism for user authentication. In particular, the username, password, request and response are all transmitted over the network without encryption.

### Sessions with Cookies

To establish and maintain a potentially long-lived session between client and server, `HttpURLConnection` includes an extensible cookie manager. Enable VM-wide cookie management using `https://developer.android.com/reference/kotlin/java/net/CookieHandler` and `https://developer.android.com/reference/kotlin/java/net/CookieManager`:

```kotlin
<code>CookieManager cookieManager = new CookieManager();
    CookieHandler.setDefault(cookieManager);
  </code>
```
By default, `CookieManager` accepts cookies from the [origin server](http://www.w3.org/Protocols/rfc2616/rfc2616-sec1.html) only. Two other policies are included: `https://developer.android.com/reference/kotlin/java/net/CookiePolicy#ACCEPT_ALL:java.net.CookiePolicy` and `https://developer.android.com/reference/kotlin/java/net/CookiePolicy#ACCEPT_NONE:java.net.CookiePolicy`. Implement `https://developer.android.com/reference/kotlin/java/net/CookiePolicy` to define a custom policy.

The default `CookieManager` keeps all accepted cookies in memory. It will forget these cookies when the VM exits. Implement `https://developer.android.com/reference/kotlin/java/net/CookieStore` to define a custom cookie store.

In addition to the cookies set by HTTP responses, you may set cookies programmatically. To be included in HTTP request headers, cookies must have the domain and path properties set.

By default, new instances of `HttpCookie` work only with servers that support [RFC 2965](http://www.ietf.org/rfc/rfc2965.txt) cookies. Many web servers support only the older specification, [RFC 2109](http://www.ietf.org/rfc/rfc2109.txt). For compatibility with the most web servers, set the cookie version to 0.

For example, to receive `www.twitter.com` in French:

```kotlin
<code>HttpCookie cookie = new HttpCookie("lang", "fr");
    cookie.setDomain("twitter.com");
    cookie.setPath("/");
    cookie.setVersion(0);
    cookieManager.getCookieStore().add(new URI("http://twitter.com/"), cookie);
  </code>
```

### HTTP Methods

`HttpURLConnection` uses the `GET` method by default. It will use `POST` if `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoOutput(kotlin.Boolean)` has been called. Other HTTP methods (`OPTIONS`, `HEAD`, `PUT`, `DELETE` and `TRACE`) can be used with `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setRequestMethod(kotlin.String)`.

### Proxies

By default, this class will connect directly to the [origin server](http://www.w3.org/Protocols/rfc2616/rfc2616-sec1.html). It can also connect via an `https://developer.android.com/reference/kotlin/java/net/Proxy.Type` or `https://developer.android.com/reference/kotlin/java/net/Proxy.Type` proxy. To use a proxy, use `https://developer.android.com/reference/kotlin/java/net/URL#openConnection(java.net.Proxy)` when creating the connection.

### IPv6 Support

This class includes transparent support for IPv6. For hosts with both IPv4 and IPv6 addresses, it will attempt to connect to each of a host's addresses until a connection is established.

### Response Caching

Android 4.0 (Ice Cream Sandwich, API level 15) includes a response cache. See `android.net.http.HttpResponseCache` for instructions on enabling HTTP caching in your application.

### Avoiding Bugs In Earlier Releases

Prior to Android 2.2 (Froyo), this class had some frustrating bugs. In particular, calling `close()` on a readable `InputStream` could [poison the connection pool](http://code.google.com/p/android/issues/detail?id=2939). Work around this by disabling connection pooling:

```kotlin
<code>private void disableConnectionReuseIfNecessary() {
    // Work around pre-Froyo bugs in HTTP connection reuse.
    if (Integer.parseInt(Build.VERSION.SDK) &lt; Build.VERSION_CODES.FROYO) {
      System.setProperty("http.keepAlive", "false");
    }
  }</code>
```

Each instance of `HttpURLConnection` may be used for one request/response pair. Instances of this class are not thread safe.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_ACCEPTED:kotlin.Int` HTTP Status-Code 202: Accepted. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_BAD_GATEWAY:kotlin.Int` HTTP Status-Code 502: Bad Gateway. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_BAD_METHOD:kotlin.Int` HTTP Status-Code 405: Method Not Allowed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_BAD_REQUEST:kotlin.Int` HTTP Status-Code 400: Bad Request. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_CLIENT_TIMEOUT:kotlin.Int` HTTP Status-Code 408: Request Time-Out. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_CONFLICT:kotlin.Int` HTTP Status-Code 409: Conflict. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_CREATED:kotlin.Int` HTTP Status-Code 201: Created. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_ENTITY_TOO_LARGE:kotlin.Int` HTTP Status-Code 413: Request Entity Too Large. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_FORBIDDEN:kotlin.Int` HTTP Status-Code 403: Forbidden. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_GATEWAY_TIMEOUT:kotlin.Int` HTTP Status-Code 504: Gateway Timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_GONE:kotlin.Int` HTTP Status-Code 410: Gone. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_INTERNAL_ERROR:kotlin.Int` HTTP Status-Code 500: Internal Server Error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_LENGTH_REQUIRED:kotlin.Int` HTTP Status-Code 411: Length Required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_MOVED_PERM:kotlin.Int` HTTP Status-Code 301: Moved Permanently. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_MOVED_TEMP:kotlin.Int` HTTP Status-Code 302: Temporary Redirect. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_MULT_CHOICE:kotlin.Int` HTTP Status-Code 300: Multiple Choices. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_NOT_ACCEPTABLE:kotlin.Int` HTTP Status-Code 406: Not Acceptable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_NOT_AUTHORITATIVE:kotlin.Int` HTTP Status-Code 203: Non-Authoritative Information. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_NOT_FOUND:kotlin.Int` HTTP Status-Code 404: Not Found. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_NOT_IMPLEMENTED:kotlin.Int` HTTP Status-Code 501: Not Implemented. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_NOT_MODIFIED:kotlin.Int` HTTP Status-Code 304: Not Modified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_NO_CONTENT:kotlin.Int` HTTP Status-Code 204: No Content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_OK:kotlin.Int` HTTP Status-Code 200: OK. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_PARTIAL:kotlin.Int` HTTP Status-Code 206: Partial Content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_PAYMENT_REQUIRED:kotlin.Int` HTTP Status-Code 402: Payment Required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_PRECON_FAILED:kotlin.Int` HTTP Status-Code 412: Precondition Failed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_PROXY_AUTH:kotlin.Int` HTTP Status-Code 407: Proxy Authentication Required. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_REQ_TOO_LONG:kotlin.Int` HTTP Status-Code 414: Request-URI Too Large. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_RESET:kotlin.Int` HTTP Status-Code 205: Reset Content. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_SEE_OTHER:kotlin.Int` HTTP Status-Code 303: See Other. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_SERVER_ERROR:kotlin.Int` HTTP Status-Code 500: Internal Server Error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_UNAUTHORIZED:kotlin.Int` HTTP Status-Code 401: Unauthorized. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_UNAVAILABLE:kotlin.Int` HTTP Status-Code 503: Service Unavailable. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_UNSUPPORTED_TYPE:kotlin.Int` HTTP Status-Code 415: Unsupported Media Type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_USE_PROXY:kotlin.Int` HTTP Status-Code 305: Use Proxy. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HTTP_VERSION:kotlin.Int` HTTP Status-Code 505: HTTP Version Not Supported. |

| Protected constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#HttpURLConnection(java.net.URL)(u: https://developer.android.com/reference/kotlin/java/net/URL!)` Constructor for the HttpURLConnection. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#disconnect()()` Indicates that other requests to the server are unlikely in the near future. |
| open [InputStream](https://developer.android.com/reference/kotlin/java/io/InputStream.html#)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getErrorStream()()` Returns the error stream if the connection failed but the server sent useful data nonetheless. |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getFollowRedirects()()` Returns a `boolean` indicating whether or not HTTP redirects (3xx) should be automatically followed. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getHeaderField(kotlin.Int)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value for the `n`th header field. |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getHeaderFieldDate(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, Default: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the value of the named field parsed as date. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getHeaderFieldKey(kotlin.Int)(n: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the key for the `n`th header field. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getInstanceFollowRedirects()()` Returns the value of this `HttpURLConnection`'s `instanceFollowRedirects` field. |
| open [Permission](https://developer.android.com/reference/kotlin/java/security/Permission.html#)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getPermission()()` Returns a `https://developer.android.com/reference/kotlin/java/net/SocketPermission` object representing the permission necessary to connect to the destination host and port. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getRequestMethod()()` Get the request method. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getResponseCode()()` Gets the status code from an HTTP response message. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getResponseMessage()()` Gets the HTTP response message, if any, returned along with the response code from a server. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setChunkedStreamingMode(kotlin.Int)(chunklen: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is **not** known in advance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFixedLengthStreamingMode(kotlin.Int)(contentLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFixedLengthStreamingMode(kotlin.Long)(contentLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFollowRedirects(kotlin.Boolean)(set: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether HTTP redirects (requests with response code 3xx) should be automatically followed by this class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setInstanceFollowRedirects(kotlin.Boolean)(followRedirects: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether HTTP redirects (requests with response code 3xx) should be automatically followed by this `HttpURLConnection` instance. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setRequestMethod(kotlin.String)(method: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Set the method for the URL request, one of: - GET - POST - HEAD - OPTIONS - PUT - DELETE - TRACE are legal, subject to protocol restrictions. <br /> |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#usingProxy()()` Indicates if the connection is going through a proxy. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/URLConnection` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#addRequestProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Adds a general request property specified by a key-value pair. This method will not overwrite existing values associated with the same key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#connect()()` Opens a communications link to the resource referenced by this URL, if such a connection has not already been established. If the `connect` method is called when the connection has already been opened (indicated by the `connected` field having the value `true`), the call is ignored. URLConnection objects go through two phases: first they are created, then they are connected. After being created, and before being connected, various options can be specified (e.g., doInput and UseCaches). After connecting, it is an error to try to set them. Operations that depend on being connected, like getContentLength, will implicitly perform the connection, if necessary. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getAllowUserInteraction()()` Returns the value of the `allowUserInteraction` field for this object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getConnectTimeout()()` Returns setting for connect timeout. 0 return implies that the option is disabled (i.e., timeout of infinity). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent()()` Retrieves the contents of this URL connection. This method first determines the content type of the object by calling the `getContentType` method. If this is the first time that the application has seen that specific content type, a content handler for that content type is created: 1. If the application has set up a content handler factory instance using the `setContentHandlerFactory` method, the `createContentHandler` method of that instance is called with the content type as an argument; the result is a content handler for that content type. 2. If no content handler factory has yet been set up, or if the factory's `createContentHandler` method returns `null`, then the application loads the class named: ```kotlin sun.net.www.content.<<i>contentType</i>> ``` where \<*contentType* \> is formed by taking the content-type string, replacing all slash characters with a `period` ('.'), and all other non-alphanumeric characters with the underscore character '`_`'. The alphanumeric characters are specifically the 26 uppercase ASCII letters '`A`' through '`Z`', the 26 lowercase ASCII letters '`a`' through '`z`', and the 10 ASCII digits '`0`' through '`9`'. If the specified class does not exist, or is not a subclass of `ContentHandler`, then an `UnknownServiceException` is thrown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContent(kotlin.Array)(classes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!>!>!)` Retrieves the contents of this URL connection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentEncoding()()` Returns the value of the `content-encoding` header field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLength()()` Returns the value of the `content-length` header field. **Note** : `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLengthLong()` should be preferred over this method, since it returns a `long` instead and is therefore more portable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentLengthLong()()` Returns the value of the `content-length` header field as a long. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getContentType()()` Returns the value of the `content-type` header field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getDate()()` Returns the value of the `date` header field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultAllowUserInteraction()()` Returns the default value of the `allowUserInteraction` field. Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultRequestProperty(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value of the default request property. Default request properties are set for every connection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getDefaultUseCaches()()` Returns the default value of a `URLConnection`'s `useCaches` flag. Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getDoInput()()` Returns the value of this `URLConnection`'s `doInput` flag. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getDoOutput()()` Returns the value of this `URLConnection`'s `doOutput` flag. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getExpiration()()` Returns the value of the `expires` header field. <br /> | | `https://developer.android.com/reference/kotlin/java/net/FileNameMap!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getFileNameMap()()` Returns a `https://developer.android.com/reference/kotlin/java/net/FileNameMap` implementation suitable for guessing a content type based on a URL's "file" component. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderField(kotlin.String)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value of the named header field. If called on a connection that sets the same header multiple times with possibly different values, only the last value is returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldInt(kotlin.String,%20kotlin.Int)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, Default: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the value of the named field parsed as a number. This form of `getHeaderField` exists because some connection types (e.g., `http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFieldLong(kotlin.String,%20kotlin.Long)(name: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, Default: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Returns the value of the named field parsed as a number. This form of `getHeaderField` exists because some connection types (e.g., `http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getHeaderFields()()` Returns an unmodifiable Map of the header fields. The Map keys are Strings that represent the response-header field names. Each Map value is an unmodifiable List of Strings that represents the corresponding field values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getIfModifiedSince()()` Returns the value of this object's `ifModifiedSince` field. <br /> | | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getInputStream()()` Returns an input stream that reads from this open connection. A SocketTimeoutException can be thrown when reading from the returned input stream if the read timeout expires before data is available for read. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getLastModified()()` Returns the value of the `last-modified` header field. The result is the number of milliseconds since January 1, 1970 GMT. <br /> | | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getOutputStream()()` Returns an output stream that writes to this connection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getReadTimeout()()` Returns setting for read timeout. 0 return implies that the option is disabled (i.e., timeout of infinity). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getRequestProperties()()` Returns an unmodifiable Map of general request properties for this connection. The Map keys are Strings that represent the request-header field names. Each Map value is a unmodifiable List of Strings that represents the corresponding field values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getRequestProperty(kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Returns the value of the named general request property for this connection. <br /> | | `https://developer.android.com/reference/kotlin/java/net/URL!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getURL()()` Returns the value of this `URLConnection`'s `URL` field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#getUseCaches()()` Returns the value of this `URLConnection`'s `useCaches` field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#guessContentTypeFromName(kotlin.String)(fname: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Tries to determine the content type of an object, based on the specified "file" component of a URL. This is a convenience method that can be used by subclasses that override the `getContentType` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#guessContentTypeFromStream(java.io.InputStream)(is: https://developer.android.com/reference/kotlin/java/io/InputStream.html#!)` Tries to determine the type of an input stream based on the characters at the beginning of the input stream. This method can be used by subclasses that override the `getContentType` method. Ideally, this routine would not be needed. But many `http` servers return the incorrect content type; in addition, there are many nonstandard extensions. Direct inspection of the bytes to determine the content type is often more accurate than believing the content type claimed by the `http` server. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setAllowUserInteraction(kotlin.Boolean)(allowuserinteraction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set the value of the `allowUserInteraction` field of this `URLConnection`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setConnectTimeout(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets a specified timeout value, in milliseconds, to be used when opening a communications link to the resource referenced by this URLConnection. If the timeout expires before the connection can be established, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout. Some non-standard implementation of this method may ignore the specified timeout. To see the connect timeout set, please call getConnectTimeout(). **Warning** : If the hostname resolves to multiple IP addresses, Android's default implementation of `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#` will try each in [RFC 3484](http://www.ietf.org/rfc/rfc3484.txt) order. If connecting to each of these addresses fails, multiple timeouts will elapse before the connect attempt throws an exception. Host names that support both IPv6 and IPv4 always have at least 2 IP addresses. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setContentHandlerFactory(java.net.ContentHandlerFactory)(fac: https://developer.android.com/reference/kotlin/java/net/ContentHandlerFactory!)` Sets the `ContentHandlerFactory` of an application. It can be called at most once by an application. The `ContentHandlerFactory` instance is used to construct a content handler from a content type If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultAllowUserInteraction(kotlin.Boolean)(defaultallowuserinteraction: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the default value of the `allowUserInteraction` field for all future `URLConnection` objects to the specified value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultRequestProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the default value of a general request property. When a `URLConnection` is created, it is initialized with these properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDefaultUseCaches(kotlin.Boolean)(defaultusecaches: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the default value of the `useCaches` field to the specified value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoInput(kotlin.Boolean)(doinput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the value of the `doInput` field for this `URLConnection` to the specified value. A URL connection can be used for input and/or output. Set the DoInput flag to true if you intend to use the URL connection for input, false if not. The default is true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setDoOutput(kotlin.Boolean)(dooutput: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the value of the `doOutput` field for this `URLConnection` to the specified value. A URL connection can be used for input and/or output. Set the DoOutput flag to true if you intend to use the URL connection for output, false if not. The default is false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setFileNameMap(java.net.FileNameMap)(map: https://developer.android.com/reference/kotlin/java/net/FileNameMap!)` Sets the FileNameMap. If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setIfModifiedSince(kotlin.Long)(ifmodifiedsince: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the value of the `ifModifiedSince` field of this `URLConnection` to the specified value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setReadTimeout(kotlin.Int)(timeout: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the read timeout to a specified timeout, in milliseconds. A non-zero value specifies the timeout when reading from Input stream when a connection is established to a resource. If the timeout expires before there is data available for read, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout. Some non-standard implementation of this method ignores the specified timeout. To see the read timeout set, please call getReadTimeout(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setRequestProperty(kotlin.String,%20kotlin.String)(key: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, value: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Sets the general request property. If a property with the key already exists, overwrite its value with the new value. NOTE: HTTP requires all request properties which can legally have multiple instances with the same key to use a comma-separated list syntax which enables multiple properties to be appended into a single property. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#setUseCaches(kotlin.Boolean)(usecaches: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets the value of the `useCaches` field of this `URLConnection` to the specified value. Some protocols do caching of documents. Occasionally, it is important to be able to "tunnel through" and ignore the caches (e.g., the "reload" button in a browser). If the UseCaches flag on a connection is true, the connection is allowed to use whatever caches it can. If false, caches are to be ignored. The default value comes from DefaultUseCaches, which defaults to true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#toString()()` Returns a `String` representation of this URL connection. <br /> | ||

| Properties ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#chunkLength:kotlin.Int` The chunk-length when using chunked encoding streaming mode for output. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#fixedContentLength:kotlin.Int` The fixed content-length when using fixed-length streaming mode. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#fixedContentLengthLong:kotlin.Long` The fixed content-length when using fixed-length streaming mode. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#instanceFollowRedirects:kotlin.Boolean` If `true`, the protocol will automatically follow redirects. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#method:kotlin.String` The HTTP method (GET,POST,PUT,etc.). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#responseCode:kotlin.Int` An `int` representing the three digit HTTP Status-Code. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#responseMessage:kotlin.String` The HTTP response message. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/URLConnection` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#allowUserInteraction:kotlin.Boolean` If `true`, this `URL` is being examined in a context in which it makes sense to allow user interactions such as popping up an authentication dialog. If `false`, then no user interaction is allowed. The value of this field can be set by the `setAllowUserInteraction` method. Its value is returned by the `getAllowUserInteraction` method. Its default value is the value of the argument in the last invocation of the `setDefaultAllowUserInteraction` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#connected:kotlin.Boolean` If `false`, this connection object has not created a communications link to the specified URL. If `true`, the communications link has been established. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#doInput:kotlin.Boolean` This variable is set by the `setDoInput` method. Its value is returned by the `getDoInput` method. A URL connection can be used for input and/or output. Setting the `doInput` flag to `true` indicates that the application intends to read data from the URL connection. The default value of this field is `true`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#doOutput:kotlin.Boolean` This variable is set by the `setDoOutput` method. Its value is returned by the `getDoOutput` method. A URL connection can be used for input and/or output. Setting the `doOutput` flag to `true` indicates that the application intends to write data to the URL connection. The default value of this field is `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#ifModifiedSince:kotlin.Long` Some protocols support skipping the fetching of the object unless the object has been modified more recently than a certain time. A nonzero value gives a time as the number of milliseconds since January 1, 1970, GMT. The object is fetched only if it has been modified more recently than that time. This variable is set by the `setIfModifiedSince` method. Its value is returned by the `getIfModifiedSince` method. The default value of this field is `0`, indicating that the fetching must always occur. <br /> | | `https://developer.android.com/reference/kotlin/java/net/URL!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#url:java.net.URL` The URL represents the remote object on the World Wide Web to which this connection is opened. The value of this field can be accessed by the `getURL` method. The default value of this variable is the value of the URL argument in the `URLConnection` constructor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection#useCaches:kotlin.Boolean` If `true`, the protocol is allowed to use caching whenever it can. If `false`, the protocol must always try to get a fresh copy of the object. This field is set by the `setUseCaches` method. Its value is returned by the `getUseCaches` method. Its default value is the value given in the last invocation of the `setDefaultUseCaches` method. <br /> | ||

## Constants

### HTTP_ACCEPTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_ACCEPTED: Int
```

HTTP Status-Code 202: Accepted.

 Value: 202

### HTTP_BAD_GATEWAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_BAD_GATEWAY: Int
```

HTTP Status-Code 502: Bad Gateway.

 Value: 502

### HTTP_BAD_METHOD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_BAD_METHOD: Int
```

HTTP Status-Code 405: Method Not Allowed.

 Value: 405

### HTTP_BAD_REQUEST

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_BAD_REQUEST: Int
```

HTTP Status-Code 400: Bad Request.

 Value: 400

### HTTP_CLIENT_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_CLIENT_TIMEOUT: Int
```

HTTP Status-Code 408: Request Time-Out.

 Value: 408

### HTTP_CONFLICT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_CONFLICT: Int
```

HTTP Status-Code 409: Conflict.

 Value: 409

### HTTP_CREATED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_CREATED: Int
```

HTTP Status-Code 201: Created.

 Value: 201

### HTTP_ENTITY_TOO_LARGE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_ENTITY_TOO_LARGE: Int
```

HTTP Status-Code 413: Request Entity Too Large.

 Value: 413

### HTTP_FORBIDDEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_FORBIDDEN: Int
```

HTTP Status-Code 403: Forbidden.

 Value: 403

### HTTP_GATEWAY_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_GATEWAY_TIMEOUT: Int
```

HTTP Status-Code 504: Gateway Timeout.

 Value: 504

### HTTP_GONE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_GONE: Int
```

HTTP Status-Code 410: Gone.

 Value: 410

### HTTP_INTERNAL_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_INTERNAL_ERROR: Int
```

HTTP Status-Code 500: Internal Server Error.

 Value: 500

### HTTP_LENGTH_REQUIRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_LENGTH_REQUIRED: Int
```

HTTP Status-Code 411: Length Required.

 Value: 411

### HTTP_MOVED_PERM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_MOVED_PERM: Int
```

HTTP Status-Code 301: Moved Permanently.

 Value: 301

### HTTP_MOVED_TEMP

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_MOVED_TEMP: Int
```

HTTP Status-Code 302: Temporary Redirect.

 Value: 302

### HTTP_MULT_CHOICE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_MULT_CHOICE: Int
```

HTTP Status-Code 300: Multiple Choices.

 Value: 300

### HTTP_NOT_ACCEPTABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_NOT_ACCEPTABLE: Int
```

HTTP Status-Code 406: Not Acceptable.

 Value: 406

### HTTP_NOT_AUTHORITATIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_NOT_AUTHORITATIVE: Int
```

HTTP Status-Code 203: Non-Authoritative Information.

 Value: 203

### HTTP_NOT_FOUND

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_NOT_FOUND: Int
```

HTTP Status-Code 404: Not Found.

 Value: 404

### HTTP_NOT_IMPLEMENTED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_NOT_IMPLEMENTED: Int
```

HTTP Status-Code 501: Not Implemented.

 Value: 501

### HTTP_NOT_MODIFIED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_NOT_MODIFIED: Int
```

HTTP Status-Code 304: Not Modified.

 Value: 304

### HTTP_NO_CONTENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_NO_CONTENT: Int
```

HTTP Status-Code 204: No Content.

 Value: 204

### HTTP_OK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_OK: Int
```

HTTP Status-Code 200: OK.

 Value: 200

### HTTP_PARTIAL

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_PARTIAL: Int
```

HTTP Status-Code 206: Partial Content.

 Value: 206

### HTTP_PAYMENT_REQUIRED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_PAYMENT_REQUIRED: Int
```

HTTP Status-Code 402: Payment Required.

 Value: 402

### HTTP_PRECON_FAILED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_PRECON_FAILED: Int
```

HTTP Status-Code 412: Precondition Failed.

 Value: 412

### HTTP_PROXY_AUTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_PROXY_AUTH: Int
```

HTTP Status-Code 407: Proxy Authentication Required.

 Value: 407

### HTTP_REQ_TOO_LONG

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_REQ_TOO_LONG: Int
```

HTTP Status-Code 414: Request-URI Too Large.

 Value: 414

### HTTP_RESET

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_RESET: Int
```

HTTP Status-Code 205: Reset Content.

 Value: 205

### HTTP_SEE_OTHER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_SEE_OTHER: Int
```

HTTP Status-Code 303: See Other.

 Value: 303

### HTTP_SERVER_ERROR

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_SERVER_ERROR: Int
```

**Deprecated:** *it is misplaced and shouldn't have existed.*

HTTP Status-Code 500: Internal Server Error.

 Value: 500

### HTTP_UNAUTHORIZED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_UNAUTHORIZED: Int
```

HTTP Status-Code 401: Unauthorized.

 Value: 401

### HTTP_UNAVAILABLE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_UNAVAILABLE: Int
```

HTTP Status-Code 503: Service Unavailable.

 Value: 503

### HTTP_UNSUPPORTED_TYPE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_UNSUPPORTED_TYPE: Int
```

HTTP Status-Code 415: Unsupported Media Type.

 Value: 415

### HTTP_USE_PROXY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_USE_PROXY: Int
```

HTTP Status-Code 305: Use Proxy.

 Value: 305

### HTTP_VERSION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val HTTP_VERSION: Int
```

HTTP Status-Code 505: HTTP Version Not Supported.

 Value: 505

## Protected constructors

### HttpURLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected HttpURLConnection(u: URL!)
```

Constructor for the HttpURLConnection.

| Parameters ||
|---|---|
| `u` | [URL](https://developer.android.com/reference/kotlin/java/net/URL)!: the URL |

## Public methods

### disconnect

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun disconnect(): Unit
```

Indicates that other requests to the server are unlikely in the near future. Calling disconnect() should not imply that this HttpURLConnection instance can be reused for other requests.

### getErrorStream

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getErrorStream(): InputStream!
```

Returns the error stream if the connection failed but the server sent useful data nonetheless. The typical example is when an HTTP server responds with a 404, which will cause a FileNotFoundException to be thrown in connect, but the server sent an HTML help page with suggestions as to what to do.

This method will not cause a connection to be initiated. If the connection was not connected, or if the server did not have an error while connecting or if the server had an error but no error data was sent, this method will return null. This is the default.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | an error stream if any, null if there have been no errors, the connection is not connected or the server sent no useful data. |

### getFollowRedirects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getFollowRedirects(): Boolean
```

Returns a `boolean` indicating whether or not HTTP redirects (3xx) should be automatically followed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if HTTP redirects should be automatically followed, `false` if not. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFollowRedirects(kotlin.Boolean)`

### getHeaderField

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeaderField(n: Int): String!
```

Returns the value for the `n`th header field. Some implementations may treat the `0`th header field as special, i.e. as the status line returned by the HTTP server.

This method can be used in conjunction with the `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getHeaderFieldKey(kotlin.Int)` method to iterate through all the headers in the message.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an index, where `n>=0`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the value of the `n`th header field, or `null` if the value does not exist. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getHeaderFieldKey(kotlin.Int)`

### getHeaderFieldDate

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeaderFieldDate(
    name: String!, 
    Default: Long
): Long
```

Returns the value of the named field parsed as date. The result is the number of milliseconds since January 1, 1970 GMT represented by the named field.

This form of `getHeaderField` exists because some connection types (e.g., `http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing.

| Parameters ||
|---|---|
| `name` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the name of the header field. |
| `Default` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): a default value. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | the value of the field, parsed as a date. The value of the `Default` argument is returned if the field is missing or malformed. |

### getHeaderFieldKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHeaderFieldKey(n: Int): String!
```

Returns the key for the `n`th header field. Some implementations may treat the `0`th header field as special, i.e. as the status line returned by the HTTP server. In this case, `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getHeaderField(kotlin.Int)` returns the status line, but `getHeaderFieldKey(0)` returns null.

| Parameters ||
|---|---|
| `n` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): an index, where `n >=0`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the key for the `n`th header field, or `null` if the key does not exist. |

### getInstanceFollowRedirects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstanceFollowRedirects(): Boolean
```

Returns the value of this `HttpURLConnection`'s `instanceFollowRedirects` field.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | the value of this `HttpURLConnection`'s `instanceFollowRedirects` field. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#instanceFollowRedirects:kotlin.Boolean`
- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setInstanceFollowRedirects(kotlin.Boolean)`

### getPermission

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPermission(): Permission!
```

Returns a `https://developer.android.com/reference/kotlin/java/net/SocketPermission` object representing the permission necessary to connect to the destination host and port.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Permission.html#!` | a `SocketPermission` object representing the permission necessary to connect to the destination host and port. |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurs while computing the permission. |

### getRequestMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRequestMethod(): String!
```

Get the request method.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the HTTP request method |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setRequestMethod(kotlin.String)`

### getResponseCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResponseCode(): Int
```

Gets the status code from an HTTP response message. For example, in the case of the following status lines:

```kotlin
HTTP/1.0 200 OK
  HTTP/1.0 401 Unauthorized
  
```
It will return 200 and 401 respectively. Returns -1 if no code can be discerned from the response (i.e., the response is not valid HTTP).

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the HTTP Status-Code, or -1 |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred connecting to the server. |

### getResponseMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getResponseMessage(): String!
```

Gets the HTTP response message, if any, returned along with the response code from a server. From responses like:

```kotlin
HTTP/1.0 200 OK
  HTTP/1.0 404 Not Found
  
```
Extracts the Strings "OK" and "Not Found" respectively. Returns null if none could be discerned from the responses (the result was not valid HTTP).

<br />

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the HTTP response message, or `null` |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an error occurred connecting to the server. |

### setChunkedStreamingMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setChunkedStreamingMode(chunklen: Int): Unit
```

This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is **not** known in advance. In this mode, chunked transfer encoding is used to send the request body. Note, not all HTTP servers support this mode.

When output streaming is enabled, authentication and redirection cannot be handled automatically. A HttpRetryException will be thrown when reading the response if authentication or redirection are required. This exception can be queried for the details of the error.

This method must be called before the URLConnection is connected.

| Parameters ||
|---|---|
| `chunklen` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes to write in each chunk. If chunklen is less than or equal to zero, a default value will be used. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if URLConnection is already connected or if a different streaming mode is already enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFixedLengthStreamingMode(kotlin.Int)`

### setFixedLengthStreamingMode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFixedLengthStreamingMode(contentLength: Int): Unit
```

This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance.

An exception will be thrown if the application attempts to write more data than the indicated content-length, or if the application closes the OutputStream before writing the indicated amount.

When output streaming is enabled, authentication and redirection cannot be handled automatically. A HttpRetryException will be thrown when reading the response if authentication or redirection are required. This exception can be queried for the details of the error.

This method must be called before the URLConnection is connected.

**NOTE:** `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFixedLengthStreamingMode(kotlin.Long)` is recommended instead of this method as it allows larger content lengths to be set.

| Parameters ||
|---|---|
| `contentLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The number of bytes which will be written to the OutputStream. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a content length less than zero is specified. |
| `java.lang.IllegalStateException` | if URLConnection is already connected or if a different streaming mode is already enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setChunkedStreamingMode(kotlin.Int)`

### setFixedLengthStreamingMode

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFixedLengthStreamingMode(contentLength: Long): Unit
```

This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance.

An exception will be thrown if the application attempts to write more data than the indicated content-length, or if the application closes the OutputStream before writing the indicated amount.

When output streaming is enabled, authentication and redirection cannot be handled automatically. A [HttpRetryException](https://developer.android.com/reference/kotlin/java/net/HttpRetryException) will be thrown when reading the response if authentication or redirection are required. This exception can be queried for the details of the error.

This method must be called before the URLConnection is connected.

The content length set by invoking this method takes precedence over any value set by `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFixedLengthStreamingMode(kotlin.Int)`.

| Parameters ||
|---|---|
| `contentLength` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The number of bytes which will be written to the OutputStream. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if a content length less than zero is specified. |
| `java.lang.IllegalStateException` | if URLConnection is already connected or if a different streaming mode is already enabled. |

### setFollowRedirects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setFollowRedirects(set: Boolean): Unit
```

Sets whether HTTP redirects (requests with response code 3xx) should be automatically followed by this class. True by default. Applets cannot change this variable.

If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException.

| Parameters ||
|---|---|
| `set` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): a `boolean` indicating whether or not to follow HTTP redirects. |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager exists and its `checkSetFactory` method doesn't allow the operation. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/lang/SecurityManager.html#checkSetFactory()`
- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getFollowRedirects()`

### setInstanceFollowRedirects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInstanceFollowRedirects(followRedirects: Boolean): Unit
```

Sets whether HTTP redirects (requests with response code 3xx) should be automatically followed by this `HttpURLConnection` instance.

The default value comes from followRedirects, which defaults to true.

| Parameters ||
|---|---|
| `followRedirects` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): a `boolean` indicating whether or not to follow HTTP redirects. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#instanceFollowRedirects:kotlin.Boolean`
- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getInstanceFollowRedirects()`

### setRequestMethod

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRequestMethod(method: String!): Unit
```

Set the method for the URL request, one of:

- GET
- POST
- HEAD
- OPTIONS
- PUT
- DELETE
- TRACE

are legal, subject to protocol restrictions. The default method is GET.

<br />

| Parameters ||
|---|---|
| `method` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: the HTTP method |

| Exceptions ||
|---|---|
| `java.lang.SecurityException` | if a security manager is set and the method is "TRACE", but the "allowHttpTrace" NetPermission is not granted. |
| `java.net.ProtocolException` | if the method cannot be reset or if the requested method isn't valid for HTTP. |

**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getRequestMethod()`

### usingProxy

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun usingProxy(): Boolean
```

Indicates if the connection is going through a proxy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | a boolean indicating if the connection is using a proxy. |

## Properties

### chunkLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var chunkLength: Int
```

The chunk-length when using chunked encoding streaming mode for output. A value of `-1` means chunked encoding is disabled for output.

### fixedContentLength

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var fixedContentLength: Int
```

The fixed content-length when using fixed-length streaming mode. A value of `-1` means fixed-length streaming mode is disabled for output.

**NOTE:** `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#fixedContentLengthLong:kotlin.Long` is recommended instead of this field, as it allows larger content lengths to be set.

### fixedContentLengthLong

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var fixedContentLengthLong: Long
```

The fixed content-length when using fixed-length streaming mode. A value of `-1` means fixed-length streaming mode is disabled for output.

### instanceFollowRedirects

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var instanceFollowRedirects: Boolean
```

If `true`, the protocol will automatically follow redirects. If `false`, the protocol will not automatically follow redirects.

This field is set by the `setInstanceFollowRedirects` method. Its value is returned by the `getInstanceFollowRedirects` method.

Its default value is based on the value of the static followRedirects at HttpURLConnection construction time.
**See Also**

- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setInstanceFollowRedirects(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#getInstanceFollowRedirects()`
- `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection#setFollowRedirects(kotlin.Boolean)`

### method

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var method: String!
```

The HTTP method (GET,POST,PUT,etc.).

### responseCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var responseCode: Int
```

An `int` representing the three digit HTTP Status-Code.

- 1xx: Informational
- 2xx: Success
- 3xx: Redirection
- 4xx: Client Error
- 5xx: Server Error

<br />

### responseMessage

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var responseMessage: String!
```

The HTTP response message.
