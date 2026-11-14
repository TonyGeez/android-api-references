# CoreConnectionPNames

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CoreConnectionPNames

```
interface CoreConnectionPNames
```

| [org.apache.http.params.CoreConnectionPNames](CoreConnectionPNames.md) |

| Known Direct Subclasses [HttpConnectionParams](HttpConnectionParams.md) |--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------| | [HttpConnectionParams](HttpConnectionParams.md) | An adaptor for accessing connection parameters in [HttpParams](HttpParams.md). | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

Defines parameter names for connections in HttpCore.

## Summary

| Constants ||
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONNECTION_TIMEOUT](CoreConnectionPNames.md) Determines the timeout until a connection is etablished. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_HEADER_COUNT](CoreConnectionPNames.md) Determines the maximum HTTP header count allowed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_LINE_LENGTH](CoreConnectionPNames.md) Determines the maximum line length limit. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SOCKET_BUFFER_SIZE](CoreConnectionPNames.md) Determines the size of the internal socket buffer used to buffer data while receiving / transmitting HTTP messages. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SO_LINGER](CoreConnectionPNames.md) Sets SO_LINGER with the specified linger time in seconds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SO_TIMEOUT](CoreConnectionPNames.md) Defines the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STALE_CONNECTION_CHECK](CoreConnectionPNames.md) Determines whether stale connection check is to be used. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TCP_NODELAY](CoreConnectionPNames.md) Determines whether Nagle's algorithm is to be used. |

## Constants

### CONNECTION_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONNECTION_TIMEOUT: String
```

**Deprecated:** *Deprecated in Java.*

Determines the timeout until a connection is etablished. A value of zero means the timeout is not used. The default value is zero.

This parameter expects a value of type [Integer](../java.lang/Integer.md). 

 Value: "http.connection.timeout"

### MAX_HEADER_COUNT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_HEADER_COUNT: String
```

**Deprecated:** *Deprecated in Java.*

Determines the maximum HTTP header count allowed. If set to a positive value, the number of HTTP headers received from the data stream exceeding this limit will cause an IOException. A negative or zero value will effectively disable the check.

This parameter expects a value of type [Integer](../java.lang/Integer.md). 

 Value: "http.connection.max-header-count"

### MAX_LINE_LENGTH

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MAX_LINE_LENGTH: String
```

**Deprecated:** *Deprecated in Java.*

Determines the maximum line length limit. If set to a positive value, any HTTP line exceeding this limit will cause an IOException. A negative or zero value will effectively disable the check.

This parameter expects a value of type [Integer](../java.lang/Integer.md). 

 Value: "http.connection.max-line-length"

### SOCKET_BUFFER_SIZE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SOCKET_BUFFER_SIZE: String
```

**Deprecated:** *Deprecated in Java.*

Determines the size of the internal socket buffer used to buffer data while receiving / transmitting HTTP messages.

This parameter expects a value of type [Integer](../java.lang/Integer.md). 

 Value: "http.socket.buffer-size"

### SO_LINGER

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SO_LINGER: String
```

**Deprecated:** *Deprecated in Java.*

Sets SO_LINGER with the specified linger time in seconds. The maximum timeout value is platform specific. Value 0 implies that the option is disabled. Value -1 implies that the JRE default is used. The setting only affects socket close.

This parameter expects a value of type [Integer](../java.lang/Integer.md). 

 Value: "http.socket.linger"

**See Also**

- [java.net.SocketOptions#SO_LINGER](../java.net/SocketOptions.md) 

### SO_TIMEOUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SO_TIMEOUT: String
```

**Deprecated:** *Deprecated in Java.*

Defines the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. A timeout value of zero is interpreted as an infinite timeout. This value is used when no socket timeout is set in the method parameters.

This parameter expects a value of type [Integer](../java.lang/Integer.md). 

 Value: "http.socket.timeout"

**See Also**

- [java.net.SocketOptions#SO_TIMEOUT](../java.net/SocketOptions.md) 

### STALE_CONNECTION_CHECK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val STALE_CONNECTION_CHECK: String
```

**Deprecated:** *Deprecated in Java.*

Determines whether stale connection check is to be used. Disabling stale connection check may result in slight performance improvement at the risk of getting an I/O error when executing a request over a connection that has been closed at the server side.

This parameter expects a value of type [Boolean](../java.lang/Boolean.md). 

 Value: "http.connection.stalecheck"

### TCP_NODELAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TCP_NODELAY: String
```

**Deprecated:** *Deprecated in Java.*

Determines whether Nagle's algorithm is to be used. The Nagle's algorithm tries to conserve bandwidth by minimizing the number of segments that are sent. When applications wish to decrease network latency and increase performance, they can disable Nagle's algorithm (that is enable TCP_NODELAY). Data will be sent earlier, at the cost of an increase in bandwidth consumption.

This parameter expects a value of type [Boolean](../java.lang/Boolean.md). 

 Value: "http.tcp.nodelay"

**See Also**

- [java.net.SocketOptions#TCP_NODELAY](../java.net/SocketOptions.md)
