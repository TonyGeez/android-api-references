# CoreConnectionPNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CoreConnectionPNames

```
interface CoreConnectionPNames
```

| [org.apache.http.params.CoreConnectionPNames](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#) |

| Known Direct Subclasses [HttpConnectionParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [HttpConnectionParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams) | An adaptor for accessing connection parameters in [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams). | |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

Defines parameter names for connections in HttpCore.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONNECTION_TIMEOUT](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#CONNECTION_TIMEOUT:kotlin.String) Determines the timeout until a connection is etablished. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_HEADER_COUNT](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#MAX_HEADER_COUNT:kotlin.String) Determines the maximum HTTP header count allowed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_LINE_LENGTH](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#MAX_LINE_LENGTH:kotlin.String) Determines the maximum line length limit. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SOCKET_BUFFER_SIZE](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#SOCKET_BUFFER_SIZE:kotlin.String) Determines the size of the internal socket buffer used to buffer data while receiving / transmitting HTTP messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SO_LINGER](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#SO_LINGER:kotlin.String) Sets SO_LINGER with the specified linger time in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SO_TIMEOUT](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#SO_TIMEOUT:kotlin.String) Defines the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STALE_CONNECTION_CHECK](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#STALE_CONNECTION_CHECK:kotlin.String) Determines whether stale connection check is to be used. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TCP_NODELAY](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#TCP_NODELAY:kotlin.String) Determines whether Nagle's algorithm is to be used. |

## Constants

### CONNECTION_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_TIMEOUT: String
```

**Deprecated:** *Deprecated in Java.*

Determines the timeout until a connection is etablished. A value of zero means the timeout is not used. The default value is zero.

This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). 

 Value: "http.connection.timeout"

### MAX_HEADER_COUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_HEADER_COUNT: String
```

**Deprecated:** *Deprecated in Java.*

Determines the maximum HTTP header count allowed. If set to a positive value, the number of HTTP headers received from the data stream exceeding this limit will cause an IOException. A negative or zero value will effectively disable the check.

This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). 

 Value: "http.connection.max-header-count"

### MAX_LINE_LENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_LINE_LENGTH: String
```

**Deprecated:** *Deprecated in Java.*

Determines the maximum line length limit. If set to a positive value, any HTTP line exceeding this limit will cause an IOException. A negative or zero value will effectively disable the check.

This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). 

 Value: "http.connection.max-line-length"

### SOCKET_BUFFER_SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_BUFFER_SIZE: String
```

**Deprecated:** *Deprecated in Java.*

Determines the size of the internal socket buffer used to buffer data while receiving / transmitting HTTP messages.

This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). 

 Value: "http.socket.buffer-size"

### SO_LINGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SO_LINGER: String
```

**Deprecated:** *Deprecated in Java.*

Sets SO_LINGER with the specified linger time in seconds. The maximum timeout value is platform specific. Value 0 implies that the option is disabled. Value -1 implies that the JRE default is used. The setting only affects socket close.

This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). 

 Value: "http.socket.linger"

**See Also**

- [java.net.SocketOptions#SO_LINGER](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_LINGER:kotlin.Int) 

### SO_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SO_TIMEOUT: String
```

**Deprecated:** *Deprecated in Java.*

Defines the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. A timeout value of zero is interpreted as an infinite timeout. This value is used when no socket timeout is set in the method parameters.

This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). 

 Value: "http.socket.timeout"

**See Also**

- [java.net.SocketOptions#SO_TIMEOUT](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#SO_TIMEOUT:kotlin.Int) 

### STALE_CONNECTION_CHECK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STALE_CONNECTION_CHECK: String
```

**Deprecated:** *Deprecated in Java.*

Determines whether stale connection check is to be used. Disabling stale connection check may result in slight performance improvement at the risk of getting an I/O error when executing a request over a connection that has been closed at the server side.

This parameter expects a value of type [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#). 

 Value: "http.connection.stalecheck"

### TCP_NODELAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TCP_NODELAY: String
```

**Deprecated:** *Deprecated in Java.*

Determines whether Nagle's algorithm is to be used. The Nagle's algorithm tries to conserve bandwidth by minimizing the number of segments that are sent. When applications wish to decrease network latency and increase performance, they can disable Nagle's algorithm (that is enable TCP_NODELAY). Data will be sent earlier, at the cost of an increase in bandwidth consumption.

This parameter expects a value of type [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#). 

 Value: "http.tcp.nodelay"

**See Also**

- [java.net.SocketOptions#TCP_NODELAY](https://developer.android.com/reference/kotlin/java/net/SocketOptions.html#TCP_NODELAY:kotlin.Int)
