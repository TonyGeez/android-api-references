# HttpConnectionParams

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 22](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# HttpConnectionParams

```
class HttpConnectionParams : CoreConnectionPNames
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [org.apache.http.params.HttpConnectionParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#) |

| **This class was deprecated in API level 22.**
|
| Please use java.net.URL#openConnection instead. Please visit [this webpage](http://android-developers.blogspot.com/2011/09/androids-http-clients.html) for further details.

An adaptor for accessing connection parameters in [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams). 
Note that the*implements* relation to [CoreConnectionPNames](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames) is for compatibility with existing application code only. References to the parameter names should use the interface, not this class.

## Summary

| Inherited constants ||
|---|---|
| From class [CoreConnectionPNames](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames) |----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [CONNECTION_TIMEOUT](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#CONNECTION_TIMEOUT:kotlin.String) <br /> Determines the timeout until a connection is etablished. A value of zero means the timeout is not used. The default value is zero. This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_HEADER_COUNT](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#MAX_HEADER_COUNT:kotlin.String) <br /> Determines the maximum HTTP header count allowed. If set to a positive value, the number of HTTP headers received from the data stream exceeding this limit will cause an IOException. A negative or zero value will effectively disable the check. This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [MAX_LINE_LENGTH](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#MAX_LINE_LENGTH:kotlin.String) <br /> Determines the maximum line length limit. If set to a positive value, any HTTP line exceeding this limit will cause an IOException. A negative or zero value will effectively disable the check. This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SOCKET_BUFFER_SIZE](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#SOCKET_BUFFER_SIZE:kotlin.String) <br /> Determines the size of the internal socket buffer used to buffer data while receiving / transmitting HTTP messages. This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SO_LINGER](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#SO_LINGER:kotlin.String) <br /> Sets SO_LINGER with the specified linger time in seconds. The maximum timeout value is platform specific. Value 0 implies that the option is disabled. Value -1 implies that the JRE default is used. The setting only affects socket close. This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SO_TIMEOUT](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#SO_TIMEOUT:kotlin.String) <br /> Defines the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. A timeout value of zero is interpreted as an infinite timeout. This value is used when no socket timeout is set in the method parameters. This parameter expects a value of type [Integer](https://developer.android.com/reference/kotlin/java/lang/Integer.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [STALE_CONNECTION_CHECK](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#STALE_CONNECTION_CHECK:kotlin.String) <br /> Determines whether stale connection check is to be used. Disabling stale connection check may result in slight performance improvement at the risk of getting an I/O error when executing a request over a connection that has been closed at the server side. This parameter expects a value of type [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#). <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [TCP_NODELAY](https://developer.android.com/reference/kotlin/org/apache/http/params/CoreConnectionPNames#TCP_NODELAY:kotlin.String) <br /> Determines whether Nagle's algorithm is to be used. The Nagle's algorithm tries to conserve bandwidth by minimizing the number of segments that are sent. When applications wish to decrease network latency and increase performance, they can disable Nagle's algorithm (that is enable TCP_NODELAY). Data will be sent earlier, at the cost of an increase in bandwidth consumption. This parameter expects a value of type [Boolean](https://developer.android.com/reference/kotlin/java/lang/Boolean.html#). <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConnectionTimeout](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#getConnectionTimeout(org.apache.http.params.HttpParams))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`)` Returns the timeout until a connection is etablished. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLinger](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#getLinger(org.apache.http.params.HttpParams))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`)` Returns linger-on-close timeout. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSoTimeout](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#getSoTimeout(org.apache.http.params.HttpParams))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`)` Returns the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSocketBufferSize](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#getSocketBufferSize(org.apache.http.params.HttpParams))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`)` <br /> |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getTcpNoDelay](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#getTcpNoDelay(org.apache.http.params.HttpParams))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`)` Tests if Nagle's algorithm is to be used. |
| static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isStaleCheckingEnabled](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#isStaleCheckingEnabled(org.apache.http.params.HttpParams))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`)` Tests whether stale connection check is to be used. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setConnectionTimeout](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#setConnectionTimeout(org.apache.http.params.HttpParams,%20kotlin.Int))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the timeout until a connection is etablished. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setLinger](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#setLinger(org.apache.http.params.HttpParams,%20kotlin.Int))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`, `value:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns linger-on-close timeout. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSoTimeout](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#setSoTimeout(org.apache.http.params.HttpParams,%20kotlin.Int))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`, `timeout:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setSocketBufferSize](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#setSocketBufferSize(org.apache.http.params.HttpParams,%20kotlin.Int))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStaleCheckingEnabled](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#setStaleCheckingEnabled(org.apache.http.params.HttpParams,%20kotlin.Boolean))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Defines whether stale connection check is to be used. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTcpNoDelay](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpConnectionParams#setTcpNoDelay(org.apache.http.params.HttpParams,%20kotlin.Boolean))`(`params:` ` [HttpParams](https://developer.android.com/reference/kotlin/org/apache/http/params/HttpParams)!`, `value:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Determines whether Nagle's algorithm is to be used. |

## Public methods

### getConnectionTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getConnectionTimeout(params: HttpParams!): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the timeout until a connection is etablished. A value of zero means the timeout is not used. The default value is zero.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | timeout in milliseconds. |

### getLinger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getLinger(params: HttpParams!): Int
```

**Deprecated:** *Deprecated in Java.*

Returns linger-on-close timeout. Value 0 implies that the option is disabled. Value -1 implies that the JRE default is used.

| Return ||
|----------------------------------------------------------------------------|-----------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the linger-on-close timeout |

### getSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSoTimeout(params: HttpParams!): Int
```

**Deprecated:** *Deprecated in Java.*

Returns the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. A timeout value of zero is interpreted as an infinite timeout. This value is used when no socket timeout is set in the method parameters.

| Return ||
|----------------------------------------------------------------------------|-------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | timeout in milliseconds |

### getSocketBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getSocketBufferSize(params: HttpParams!): Int
```

**Deprecated:** *Deprecated in Java.* 

### getTcpNoDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getTcpNoDelay(params: HttpParams!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Tests if Nagle's algorithm is to be used.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if the Nagle's algorithm is to NOT be used (that is enable TCP_NODELAY), false otherwise. |

### isStaleCheckingEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun isStaleCheckingEnabled(params: HttpParams!): Boolean
```

**Deprecated:** *Deprecated in Java.*

Tests whether stale connection check is to be used. Disabling stale connection check may result in slight performance improvement at the risk of getting an I/O error when executing a request over a connection that has been closed at the server side.

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if stale connection check is to be used, false otherwise. |

### setConnectionTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setConnectionTimeout(
    params: HttpParams!, 
    timeout: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the timeout until a connection is etablished. A value of zero means the timeout is not used. The default value is zero.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Timeout in milliseconds. |

### setLinger

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setLinger(
    params: HttpParams!, 
    value: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Returns linger-on-close timeout. This option disables/enables immediate return from a close() of a TCP Socket. Enabling this option with a non-zero Integer timeout means that a close() will block pending the transmission and acknowledgement of all data written to the peer, at which point the socket is closed gracefully. Value 0 implies that the option is disabled. Value -1 implies that the JRE default is used.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------|
| `value` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the linger-on-close timeout |

### setSoTimeout

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setSoTimeout(
    params: HttpParams!, 
    timeout: Int
): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the default socket timeout (SO_TIMEOUT) in milliseconds which is the timeout for waiting for data. A timeout value of zero is interpreted as an infinite timeout. This value is used when no socket timeout is set in the method parameters.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------|
| `timeout` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Timeout in milliseconds |

### setSocketBufferSize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setSocketBufferSize(
    params: HttpParams!, 
    size: Int
): Unit
```

**Deprecated:** *Deprecated in Java.* 

### setStaleCheckingEnabled

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setStaleCheckingEnabled(
    params: HttpParams!, 
    value: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Defines whether stale connection check is to be used. Disabling stale connection check may result in slight performance improvement at the risk of getting an I/O error when executing a request over a connection that has been closed at the server side.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if stale connection check is to be used, false otherwise. |

### setTcpNoDelay

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setTcpNoDelay(
    params: HttpParams!, 
    value: Boolean
): Unit
```

**Deprecated:** *Deprecated in Java.*

Determines whether Nagle's algorithm is to be used. The Nagle's algorithm tries to conserve bandwidth by minimizing the number of segments that are sent. When applications wish to decrease network latency and increase performance, they can disable Nagle's algorithm (that is enable TCP_NODELAY). Data will be sent earlier, at the cost of an increase in bandwidth consumption.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `value` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the Nagle's algorithm is to NOT be used (that is enable TCP_NODELAY), false otherwise. |
