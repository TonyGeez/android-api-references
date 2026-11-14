Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpsURLConnection

```
abstract class HttpsURLConnection : HttpURLConnection
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [java.net.URLConnection](../java.net/URLConnection.md) |||
| | ↳ | [java.net.HttpURLConnection](../java.net/HttpURLConnection.md) ||
| | | ↳ | [javax.net.ssl.HttpsURLConnection](HttpsURLConnection.md) |
| --- | --- | --- | --- |

`HttpsURLConnection` extends `HttpURLConnection` with support for https-specific features.

See <http://www.w3.org/pub/WWW/Protocols/> and [RFC 2818](http://www.ietf.org/) for more details on the https specification.

This class uses `HostnameVerifier` and `SSLSocketFactory`. There are default implementations defined for both classes. However, the implementations can be replaced on a per-class (static) or per-instance basis. All new `HttpsURLConnection`s instances will be assigned the "default" static values at instance creation, but they can be overriden by calling the appropriate per-instance set method(s) before `connect`ing.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_ACCEPTED:kotlin.Int` HTTP Status-Code 202: Accepted. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_BAD_GATEWAY:kotlin.Int` HTTP Status-Code 502: Bad Gateway. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_BAD_METHOD:kotlin.Int` HTTP Status-Code 405: Method Not Allowed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_BAD_REQUEST:kotlin.Int` HTTP Status-Code 400: Bad Request. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_CLIENT_TIMEOUT:kotlin.Int` HTTP Status-Code 408: Request Time-Out. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_CONFLICT:kotlin.Int` HTTP Status-Code 409: Conflict. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_CREATED:kotlin.Int` HTTP Status-Code 201: Created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_ENTITY_TOO_LARGE:kotlin.Int` HTTP Status-Code 413: Request Entity Too Large. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_FORBIDDEN:kotlin.Int` HTTP Status-Code 403: Forbidden. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_GATEWAY_TIMEOUT:kotlin.Int` HTTP Status-Code 504: Gateway Timeout. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_GONE:kotlin.Int` HTTP Status-Code 410: Gone. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_INTERNAL_ERROR:kotlin.Int` HTTP Status-Code 500: Internal Server Error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_LENGTH_REQUIRED:kotlin.Int` HTTP Status-Code 411: Length Required. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_MOVED_PERM:kotlin.Int` HTTP Status-Code 301: Moved Permanently. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_MOVED_TEMP:kotlin.Int` HTTP Status-Code 302: Temporary Redirect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_MULT_CHOICE:kotlin.Int` HTTP Status-Code 300: Multiple Choices. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_NOT_ACCEPTABLE:kotlin.Int` HTTP Status-Code 406: Not Acceptable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_NOT_AUTHORITATIVE:kotlin.Int` HTTP Status-Code 203: Non-Authoritative Information. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_NOT_FOUND:kotlin.Int` HTTP Status-Code 404: Not Found. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_NOT_IMPLEMENTED:kotlin.Int` HTTP Status-Code 501: Not Implemented. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_NOT_MODIFIED:kotlin.Int` HTTP Status-Code 304: Not Modified. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_NO_CONTENT:kotlin.Int` HTTP Status-Code 204: No Content. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_OK:kotlin.Int` HTTP Status-Code 200: OK. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_PARTIAL:kotlin.Int` HTTP Status-Code 206: Partial Content. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_PAYMENT_REQUIRED:kotlin.Int` HTTP Status-Code 402: Payment Required. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_PRECON_FAILED:kotlin.Int` HTTP Status-Code 412: Precondition Failed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_PROXY_AUTH:kotlin.Int` HTTP Status-Code 407: Proxy Authentication Required. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_REQ_TOO_LONG:kotlin.Int` HTTP Status-Code 414: Request-URI Too Large. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_RESET:kotlin.Int` HTTP Status-Code 205: Reset Content. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_SEE_OTHER:kotlin.Int` HTTP Status-Code 303: See Other. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_SERVER_ERROR:kotlin.Int` HTTP Status-Code 500: Internal Server Error. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_UNAUTHORIZED:kotlin.Int` HTTP Status-Code 401: Unauthorized. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_UNAVAILABLE:kotlin.Int` HTTP Status-Code 503: Service Unavailable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_UNSUPPORTED_TYPE:kotlin.Int` HTTP Status-Code 415: Unsupported Media Type. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_USE_PROXY:kotlin.Int` HTTP Status-Code 305: Use Proxy. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#HTTP_VERSION:kotlin.Int` HTTP Status-Code 505: HTTP Version Not Supported. <br /> | ||

| Protected constructors ||
|---|---|
| HttpsURLConnection Creates an `HttpsURLConnection` using the URL specified. |

| Public methods ||
|---|---|
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | getCipherSuite Returns the cipher suite in use on this connection. |
| open static [HostnameVerifier](HostnameVerifier.md)! | getDefaultHostnameVerifier Gets the default `HostnameVerifier` that is inherited by new instances of this class. |
| open static [SSLSocketFactory](SSLSocketFactory.md)! | getDefaultSSLSocketFactory Gets the default static `SSLSocketFactory` that is inherited by new instances of this class. |
| --- | --- |
| open [HostnameVerifier](HostnameVerifier.md)! | getHostnameVerifier Gets the `HostnameVerifier` in place on this instance. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>! | getLocalCertificates Returns the certificate(s) that were sent to the server during handshaking. |
| open [Principal](../java.security/Principal.md)! | getLocalPrincipal Returns the principal that was sent to the server during handshaking. |
| --- | --- |
| open [Principal](../java.security/Principal.md)! | getPeerPrincipal Returns the server's principal which was established as part of defining the session. |
| open [SSLSocketFactory](SSLSocketFactory.md)! | getSSLSocketFactory Gets the SSL socket factory to be used when creating sockets for secure https URL connections. |
| abstract [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [Certificate](../java.security.cert/Certificate.md)!\>! | getServerCertificates Returns the server's certificate chain which was established as part of defining the session. |
| --- | --- |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDefaultHostnameVerifier Sets the default `HostnameVerifier` inherited by a new instance of this class. |
| open static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setDefaultSSLSocketFactory Sets the default `SSLSocketFactory` inherited by new instances of this class. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setHostnameVerifier Sets the `HostnameVerifier` for this instance. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setSSLSocketFactory Sets the `SSLSocketFactory` to be used when this instance creates sockets for secure https URL connections. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | addRequestProperty Adds a general request property specified by a key-value pair. This method will not overwrite existing values associated with the same key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | connect Opens a communications link to the resource referenced by this URL, if such a connection has not already been established. If the `connect` method is called when the connection has already been opened (indicated by the `connected` field having the value `true`), the call is ignored. URLConnection objects go through two phases: first they are created, then they are connected. After being created, and before being connected, various options can be specified (e.g., doInput and UseCaches). After connecting, it is an error to try to set them. Operations that depend on being connected, like getContentLength, will implicitly perform the connection, if necessary. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getAllowUserInteraction Returns the value of the `allowUserInteraction` field for this object. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getConnectTimeout Returns setting for connect timeout. 0 return implies that the option is disabled (i.e., timeout of infinity). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | getContent Retrieves the contents of this URL connection. This method first determines the content type of the object by calling the `getContentType` method. If this is the first time that the application has seen that specific content type, a content handler for that content type is created: 1. If the application has set up a content handler factory instance using the `setContentHandlerFactory` method, the `createContentHandler` method of that instance is called with the content type as an argument; the result is a content handler for that content type. 2. If no content handler factory has yet been set up, or if the factory's `createContentHandler` method returns `null`, then the application loads the class named: ```kotlin sun.net.www.content.<<i>contentType</i>> ``` where \<*contentType* \> is formed by taking the content-type string, replacing all slash characters with a `period` ('.'), and all other non-alphanumeric characters with the underscore character '`_`'. The alphanumeric characters are specifically the 26 uppercase ASCII letters '`A`' through '`Z`', the 26 lowercase ASCII letters '`a`' through '`z`', and the 10 ASCII digits '`0`' through '`9`'. If the specified class does not exist, or is not a subclass of `ContentHandler`, then an `UnknownServiceException` is thrown. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | getContent Retrieves the contents of this URL connection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getContentEncoding Returns the value of the `content-encoding` header field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getContentLength Returns the value of the `content-length` header field. **Note** : getContentLengthLong should be preferred over this method, since it returns a `long` instead and is therefore more portable. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getContentLengthLong Returns the value of the `content-length` header field as a long. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getContentType Returns the value of the `content-type` header field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getDate Returns the value of the `date` header field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getDefaultAllowUserInteraction Returns the default value of the `allowUserInteraction` field. Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getDefaultRequestProperty Returns the value of the default request property. Default request properties are set for every connection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getDefaultUseCaches Returns the default value of a `URLConnection`'s `useCaches` flag. Ths default is "sticky", being a part of the static state of all URLConnections. This flag applies to the next, and all following URLConnections that are created. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getDoInput Returns the value of this `URLConnection`'s `doInput` flag. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getDoOutput Returns the value of this `URLConnection`'s `doOutput` flag. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getExpiration Returns the value of the `expires` header field. <br /> | | `https://developer.android.com/reference/kotlin/java/net/FileNameMap.html#!` | getFileNameMap Returns a `https://developer.android.com/reference/kotlin/java/net/FileNameMap.html#` implementation suitable for guessing a content type based on a URL's "file" component. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getHeaderField Returns the value of the named header field. If called on a connection that sets the same header multiple times with possibly different values, only the last value is returned. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getHeaderFieldInt Returns the value of the named field parsed as a number. This form of `getHeaderField` exists because some connection types (e.g., `http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getHeaderFieldLong Returns the value of the named field parsed as a number. This form of `getHeaderField` exists because some connection types (e.g., `http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!` | getHeaderFields Returns an unmodifiable Map of the header fields. The Map keys are Strings that represent the response-header field names. Each Map value is an unmodifiable List of Strings that represents the corresponding field values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getIfModifiedSince Returns the value of this object's `ifModifiedSince` field. <br /> | | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | getInputStream Returns an input stream that reads from this open connection. A SocketTimeoutException can be thrown when reading from the returned input stream if the read timeout expires before data is available for read. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getLastModified Returns the value of the `last-modified` header field. The result is the number of milliseconds since January 1, 1970 GMT. <br /> | | `https://developer.android.com/reference/kotlin/java/io/OutputStream.html#!` | getOutputStream Returns an output stream that writes to this connection. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getReadTimeout Returns setting for read timeout. 0 return implies that the option is disabled (i.e., timeout of infinity). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-map/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!>!` | getRequestProperties Returns an unmodifiable Map of general request properties for this connection. The Map keys are Strings that represent the request-header field names. Each Map value is a unmodifiable List of Strings that represents the corresponding field values. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getRequestProperty Returns the value of the named general request property for this connection. <br /> | | `https://developer.android.com/reference/kotlin/java/net/URL.html#!` | getURL Returns the value of this `URLConnection`'s `URL` field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getUseCaches Returns the value of this `URLConnection`'s `useCaches` field. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | guessContentTypeFromName Tries to determine the content type of an object, based on the specified "file" component of a URL. This is a convenience method that can be used by subclasses that override the `getContentType` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | guessContentTypeFromStream Tries to determine the type of an input stream based on the characters at the beginning of the input stream. This method can be used by subclasses that override the `getContentType` method. Ideally, this routine would not be needed. But many `http` servers return the incorrect content type; in addition, there are many nonstandard extensions. Direct inspection of the bytes to determine the content type is often more accurate than believing the content type claimed by the `http` server. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setAllowUserInteraction Set the value of the `allowUserInteraction` field of this `URLConnection`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setConnectTimeout Sets a specified timeout value, in milliseconds, to be used when opening a communications link to the resource referenced by this URLConnection. If the timeout expires before the connection can be established, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout. Some non-standard implementation of this method may ignore the specified timeout. To see the connect timeout set, please call getConnectTimeout(). **Warning** : If the hostname resolves to multiple IP addresses, Android's default implementation of `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#` will try each in [RFC 3484](http://www.ietf.org/rfc/rfc3484.txt) order. If connecting to each of these addresses fails, multiple timeouts will elapse before the connect attempt throws an exception. Host names that support both IPv6 and IPv4 always have at least 2 IP addresses. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setContentHandlerFactory Sets the `ContentHandlerFactory` of an application. It can be called at most once by an application. The `ContentHandlerFactory` instance is used to construct a content handler from a content type If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDefaultAllowUserInteraction Sets the default value of the `allowUserInteraction` field for all future `URLConnection` objects to the specified value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDefaultRequestProperty Sets the default value of a general request property. When a `URLConnection` is created, it is initialized with these properties. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDefaultUseCaches Sets the default value of the `useCaches` field to the specified value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDoInput Sets the value of the `doInput` field for this `URLConnection` to the specified value. A URL connection can be used for input and/or output. Set the DoInput flag to true if you intend to use the URL connection for input, false if not. The default is true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setDoOutput Sets the value of the `doOutput` field for this `URLConnection` to the specified value. A URL connection can be used for input and/or output. Set the DoOutput flag to true if you intend to use the URL connection for output, false if not. The default is false. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFileNameMap Sets the FileNameMap. If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setIfModifiedSince Sets the value of the `ifModifiedSince` field of this `URLConnection` to the specified value. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setReadTimeout Sets the read timeout to a specified timeout, in milliseconds. A non-zero value specifies the timeout when reading from Input stream when a connection is established to a resource. If the timeout expires before there is data available for read, a java.net.SocketTimeoutException is raised. A timeout of zero is interpreted as an infinite timeout. Some non-standard implementation of this method ignores the specified timeout. To see the read timeout set, please call getReadTimeout(). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setRequestProperty Sets the general request property. If a property with the key already exists, overwrite its value with the new value. NOTE: HTTP requires all request properties which can legally have multiple instances with the same key to use a comma-separated list syntax which enables multiple properties to be appended into a single property. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setUseCaches Sets the value of the `useCaches` field of this `URLConnection` to the specified value. Some protocols do caching of documents. Occasionally, it is important to be able to "tunnel through" and ignore the caches (e.g., the "reload" button in a browser). If the UseCaches flag on a connection is true, the connection is allowed to use whatever caches it can. If false, caches are to be ignored. The default value comes from DefaultUseCaches, which defaults to true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | toString Returns a `String` representation of this URL connection. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | disconnect Indicates that other requests to the server are unlikely in the near future. Calling disconnect() should not imply that this HttpURLConnection instance can be reused for other requests. <br /> | | `https://developer.android.com/reference/kotlin/java/io/InputStream.html#!` | getErrorStream Returns the error stream if the connection failed but the server sent useful data nonetheless. The typical example is when an HTTP server responds with a 404, which will cause a FileNotFoundException to be thrown in connect, but the server sent an HTML help page with suggestions as to what to do. This method will not cause a connection to be initiated. If the connection was not connected, or if the server did not have an error while connecting or if the server had an error but no error data was sent, this method will return null. This is the default. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getFollowRedirects Returns a `boolean` indicating whether or not HTTP redirects (3xx) should be automatically followed. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getHeaderField Returns the value for the `n`th header field. Some implementations may treat the `0`th header field as special, i.e. as the status line returned by the HTTP server. This method can be used in conjunction with the getHeaderFieldKey method to iterate through all the headers in the message. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | getHeaderFieldDate Returns the value of the named field parsed as date. The result is the number of milliseconds since January 1, 1970 GMT represented by the named field. This form of `getHeaderField` exists because some connection types (e.g., `http-ng`) have pre-parsed headers. Classes for that connection type can override this method and short-circuit the parsing. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getHeaderFieldKey Returns the key for the `n`th header field. Some implementations may treat the `0`th header field as special, i.e. as the status line returned by the HTTP server. In this case, getHeaderField returns the status line, but `getHeaderFieldKey(0)` returns null. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | getInstanceFollowRedirects Returns the value of this `HttpURLConnection`'s `instanceFollowRedirects` field. <br /> | | `https://developer.android.com/reference/kotlin/java/security/Permission.html#!` | getPermission Returns a `https://developer.android.com/reference/kotlin/java/net/SocketPermission.html#` object representing the permission necessary to connect to the destination host and port. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getRequestMethod Get the request method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getResponseCode Gets the status code from an HTTP response message. For example, in the case of the following status lines: ```kotlin HTTP/1.0 200 OK HTTP/1.0 401 Unauthorized ``` It will return 200 and 401 respectively. Returns -1 if no code can be discerned from the response (i.e., the response is not valid HTTP). <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | getResponseMessage Gets the HTTP response message, if any, returned along with the response code from a server. From responses like: ```kotlin HTTP/1.0 200 OK HTTP/1.0 404 Not Found ``` Extracts the Strings "OK" and "Not Found" respectively. Returns null if none could be discerned from the responses (the result was not valid HTTP). <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setChunkedStreamingMode This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is **not** known in advance. In this mode, chunked transfer encoding is used to send the request body. Note, not all HTTP servers support this mode. When output streaming is enabled, authentication and redirection cannot be handled automatically. A HttpRetryException will be thrown when reading the response if authentication or redirection are required. This exception can be queried for the details of the error. This method must be called before the URLConnection is connected. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFixedLengthStreamingMode This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance. An exception will be thrown if the application attempts to write more data than the indicated content-length, or if the application closes the OutputStream before writing the indicated amount. When output streaming is enabled, authentication and redirection cannot be handled automatically. A HttpRetryException will be thrown when reading the response if authentication or redirection are required. This exception can be queried for the details of the error. This method must be called before the URLConnection is connected. **NOTE:** setFixedLengthStreamingMode is recommended instead of this method as it allows larger content lengths to be set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFixedLengthStreamingMode This method is used to enable streaming of a HTTP request body without internal buffering, when the content length is known in advance. An exception will be thrown if the application attempts to write more data than the indicated content-length, or if the application closes the OutputStream before writing the indicated amount. When output streaming is enabled, authentication and redirection cannot be handled automatically. A [HttpRetryException](../java.net/HttpRetryException.md) will be thrown when reading the response if authentication or redirection are required. This exception can be queried for the details of the error. This method must be called before the URLConnection is connected. The content length set by invoking this method takes precedence over any value set by setFixedLengthStreamingMode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setFollowRedirects Sets whether HTTP redirects (requests with response code 3xx) should be automatically followed by this class. True by default. Applets cannot change this variable. If there is a security manager, this method first calls the security manager's `checkSetFactory` method to ensure the operation is allowed. This could result in a SecurityException. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setInstanceFollowRedirects Sets whether HTTP redirects (requests with response code 3xx) should be automatically followed by this `HttpURLConnection` instance. The default value comes from followRedirects, which defaults to true. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setRequestMethod Set the method for the URL request, one of: - GET - POST - HEAD - OPTIONS - PUT - DELETE - TRACE are legal, subject to protocol restrictions. The default method is GET. <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | usingProxy Indicates if the connection is going through a proxy. <br /> | ||

| Properties ||
|---|---|
| [HostnameVerifier](HostnameVerifier.md)! | `https://developer.android.com/reference/kotlin/javax/net/ssl/HttpsURLConnection#hostnameVerifier:javax.net.ssl.HostnameVerifier` The `hostnameVerifier` for this object. |

| Inherited properties ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#allowUserInteraction:kotlin.Boolean` If `true`, this `URL` is being examined in a context in which it makes sense to allow user interactions such as popping up an authentication dialog. If `false`, then no user interaction is allowed. The value of this field can be set by the `setAllowUserInteraction` method. Its value is returned by the `getAllowUserInteraction` method. Its default value is the value of the argument in the last invocation of the `setDefaultAllowUserInteraction` method. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#connected:kotlin.Boolean` If `false`, this connection object has not created a communications link to the specified URL. If `true`, the communications link has been established. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#doInput:kotlin.Boolean` This variable is set by the `setDoInput` method. Its value is returned by the `getDoInput` method. A URL connection can be used for input and/or output. Setting the `doInput` flag to `true` indicates that the application intends to read data from the URL connection. The default value of this field is `true`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#doOutput:kotlin.Boolean` This variable is set by the `setDoOutput` method. Its value is returned by the `getDoOutput` method. A URL connection can be used for input and/or output. Setting the `doOutput` flag to `true` indicates that the application intends to write data to the URL connection. The default value of this field is `false`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#ifModifiedSince:kotlin.Long` Some protocols support skipping the fetching of the object unless the object has been modified more recently than a certain time. A nonzero value gives a time as the number of milliseconds since January 1, 1970, GMT. The object is fetched only if it has been modified more recently than that time. This variable is set by the `setIfModifiedSince` method. Its value is returned by the `getIfModifiedSince` method. The default value of this field is `0`, indicating that the fetching must always occur. <br /> | | `https://developer.android.com/reference/kotlin/java/net/URL.html#!` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#url:java.net.URL` The URL represents the remote object on the World Wide Web to which this connection is opened. The value of this field can be accessed by the `getURL` method. The default value of this variable is the value of the URL argument in the `URLConnection` constructor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/URLConnection.html#useCaches:kotlin.Boolean` If `true`, the protocol is allowed to use caching whenever it can. If `false`, the protocol must always try to get a fresh copy of the object. This field is set by the `setUseCaches` method. Its value is returned by the `getUseCaches` method. Its default value is the value given in the last invocation of the `setDefaultUseCaches` method. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#chunkLength:kotlin.Int` The chunk-length when using chunked encoding streaming mode for output. A value of `-1` means chunked encoding is disabled for output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#fixedContentLength:kotlin.Int` The fixed content-length when using fixed-length streaming mode. A value of `-1` means fixed-length streaming mode is disabled for output. **NOTE:** `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#fixedContentLengthLong:kotlin.Long` is recommended instead of this field, as it allows larger content lengths to be set. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#fixedContentLengthLong:kotlin.Long` The fixed content-length when using fixed-length streaming mode. A value of `-1` means fixed-length streaming mode is disabled for output. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#instanceFollowRedirects:kotlin.Boolean` If `true`, the protocol will automatically follow redirects. If `false`, the protocol will not automatically follow redirects. This field is set by the `setInstanceFollowRedirects` method. Its value is returned by the `getInstanceFollowRedirects` method. Its default value is based on the value of the static followRedirects at HttpURLConnection construction time. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#method:kotlin.String` The HTTP method (GET,POST,PUT,etc.). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#responseCode:kotlin.Int` An `int` representing the three digit HTTP Status-Code. - 1xx: Informational - 2xx: Success - 3xx: Redirection - 4xx: Client Error - 5xx: Server Error <br /> <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | `https://developer.android.com/reference/kotlin/java/net/HttpURLConnection.html#responseMessage:kotlin.String` The HTTP response message. <br /> | ||

## Protected constructors

### HttpsURLConnection

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected HttpsURLConnection(url: URL!)
```

Creates an `HttpsURLConnection` using the URL specified.

| Parameters ||
|---|---|
| `url` | [URL](../java.net/URL.md)!: the URL |

## Public methods

### getCipherSuite

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getCipherSuite(): String!
```

Returns the cipher suite in use on this connection.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the cipher suite |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method is called before the connection has been established. |

### getDefaultHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultHostnameVerifier(): HostnameVerifier!
```

Gets the default `HostnameVerifier` that is inherited by new instances of this class.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier!` | the default host name verifier |

**See Also**

- setDefaultHostnameVerifier

### getDefaultSSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getDefaultSSLSocketFactory(): SSLSocketFactory!
```

Gets the default static `SSLSocketFactory` that is inherited by new instances of this class.

The socket factories are used when creating sockets for secure https URL connections.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory!` | the default `SSLSocketFactory` |

**See Also**

- setDefaultSSLSocketFactory

### getHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getHostnameVerifier(): HostnameVerifier!
```

Gets the `HostnameVerifier` in place on this instance.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/HostnameVerifier!` | the host name verifier |

**See Also**

- setHostnameVerifier
- setDefaultHostnameVerifier

### getLocalCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getLocalCertificates(): Array<Certificate!>!
```

Returns the certificate(s) that were sent to the server during handshaking.

Note: This method is useful only when using certificate-based cipher suites.

When multiple certificates are available for use in a handshake, the implementation chooses what it considers the "best" certificate chain available, and transmits that to the other side. This method allows the caller to know which certificate chain was actually sent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#!>!` | an ordered array of certificates, with the client's own certificate first followed by any certificate authorities. If no certificates were sent, then null is returned. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method is called before the connection has been established. |

**See Also**

- getLocalPrincipal

### getLocalPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getLocalPrincipal(): Principal!
```

Returns the principal that was sent to the server during handshaking.

Note: Subclasses should override this method. If not overridden, it will default to returning the X500Principal of the end-entity certificate that was sent to the server for certificate-based ciphersuites or, return null for non-certificate based ciphersuites, such as Kerberos.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Principal.html#!` | the principal sent to the server. Returns an X500Principal of the end-entity certificate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. If no principal was sent, then null is returned. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method is called before the connection has been established. |

**See Also**

- getLocalCertificates
- getPeerPrincipal

### getPeerPrincipal

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getPeerPrincipal(): Principal!
```

Returns the server's principal which was established as part of defining the session.

Note: Subclasses should override this method. If not overridden, it will default to returning the X500Principal of the server's end-entity certificate for certificate-based ciphersuites, or throw an SSLPeerUnverifiedException for non-certificate based ciphersuites, such as Kerberos.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/security/Principal.html#!` | the server's principal. Returns an X500Principal of the end-entity certiticate for X509-based cipher suites, and KerberosPrincipal for Kerberos cipher suites. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method is called before the connection has been established. |
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer was not verified |

**See Also**

- getServerCertificates
- getLocalPrincipal

### getSSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSSLSocketFactory(): SSLSocketFactory!
```

Gets the SSL socket factory to be used when creating sockets for secure https URL connections.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/javax/net/ssl/SSLSocketFactory!` | the `SSLSocketFactory` |

**See Also**

- setSSLSocketFactory

### getServerCertificates

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getServerCertificates(): Array<Certificate!>!
```

Returns the server's certificate chain which was established as part of defining the session.

Note: This method can be used only when using certificate-based cipher suites; using it with non-certificate-based cipher suites, such as Kerberos, will throw an SSLPeerUnverifiedException.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/security/cert/Certificate.html#!>!` | an ordered array of server certificates, with the peer's own certificate first followed by any certificate authorities. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | if this method is called before the connection has been established. |
| `javax.net.ssl.SSLPeerUnverifiedException` | if the peer is not verified. |

**See Also**

- getPeerPrincipal

### setDefaultHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setDefaultHostnameVerifier(v: HostnameVerifier!): Unit
```

Sets the default `HostnameVerifier` inherited by a new instance of this class.

Developers are *strongly* discouraged from changing the default `HostnameVerifier` as getDefaultHostnameVerifier is used by several classes for hostname verification on Android.

| User | Effect |
|---|---|
| Android's default TrustManager, as used with Android's default SSLContext, SSLSocketFactory and SSLSocket implementations. | The `HostnameVerifier` is used to verify the peer's certificate hostname after connecting if `SSLParameters.setEndpointIdentificationAlgorithm("HTTPS")` has been called. Instances use the *current* default `HostnameVerifier` at verification time. |
| `https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory.html#` | The current default `HostnameVerifier` is used from various `createSocket` methods. See `https://developer.android.com/reference/kotlin/android/net/SSLCertificateSocketFactory.html#` for details; for example createSocket. |
| Android's default HttpsURLConnection implementation. | The `HostnameVerifier` is used after a successful TLS handshake to verify the URI host against the TLS session server. Instances use the default `HostnameVerifier` set *when they were created* unless overridden with setHostnameVerifier. Android's `HttpsURLConnection` relies on the `HostnameVerifier` for the *entire* hostname verification step. |
| --- | --- |

If this method is not called, the default `HostnameVerifier` will check the hostname according to RFC 2818.

| Parameters ||
|---|---|
| `v` | [HostnameVerifier](HostnameVerifier.md)!: the default host name verifier |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `HostnameVerifier` parameter is null. |
| `java.lang.SecurityException` | if a security manager exists and its `checkPermission` method does not allow `SSLPermission("setHostnameVerifier")` |

**See Also**

- getDefaultHostnameVerifier

### setDefaultSSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun setDefaultSSLSocketFactory(sf: SSLSocketFactory!): Unit
```

Sets the default `SSLSocketFactory` inherited by new instances of this class.

The socket factories are used when creating sockets for secure https URL connections.

| Parameters ||
|---|---|
| `sf` | [SSLSocketFactory](SSLSocketFactory.md)!: the default SSL socket factory |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the SSLSocketFactory parameter is null. |
| `java.lang.SecurityException` | if a security manager exists and its `checkSetFactory` method does not allow a socket factory to be specified. |

**See Also**

- getDefaultSSLSocketFactory

### setHostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setHostnameVerifier(v: HostnameVerifier!): Unit
```

Sets the `HostnameVerifier` for this instance.

New instances of this class inherit the default static hostname verifier set by setDefaultHostnameVerifier. Calls to this method replace this object's `HostnameVerifier`.

Android's `HttpsURLConnection` relies on the `HostnameVerifier` for the *entire* hostname verification step.

| Parameters ||
|---|---|
| `v` | [HostnameVerifier](HostnameVerifier.md)!: the host name verifier |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `HostnameVerifier` parameter is null. |

**See Also**

- getHostnameVerifier
- setDefaultHostnameVerifier

### setSSLSocketFactory

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSSLSocketFactory(sf: SSLSocketFactory!): Unit
```

Sets the `SSLSocketFactory` to be used when this instance creates sockets for secure https URL connections.

New instances of this class inherit the default static `SSLSocketFactory` set by setDefaultSSLSocketFactory. Calls to this method replace this object's `SSLSocketFactory`.

| Parameters ||
|---|---|
| `sf` | [SSLSocketFactory](SSLSocketFactory.md)!: the SSL socket factory |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the `SSLSocketFactory` parameter is null. |
| `java.lang.SecurityException` | if a security manager exists and its `checkSetFactory` method does not allow a socket factory to be specified. |

**See Also**

- getSSLSocketFactory

## Properties

### hostnameVerifier

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected var hostnameVerifier: HostnameVerifier!
```

The `hostnameVerifier` for this object.
