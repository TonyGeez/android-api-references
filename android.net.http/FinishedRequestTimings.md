Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

# FinishedRequestTimings

```
class FinishedRequestTimings
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.http.FinishedRequestTimings](https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#) |

Metrics collected for a single request. Most of these metrics are timestamps for events during the lifetime of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream` or `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`, which can be used to build a detailed timeline for investigating performance.

Timestamps are derived from a monotonic clock.

Start times are reported as the time when a request started waiting for an event, not when the event actually started. If a metric is not available, including cases when a request finished before reaching that stage, start and end times will be `null`. If no time was spent blocking on an event, start and end will be the same time.

A metric can be null if it's unavailable (e.g. SSL metrics are null if the host name was not resolved).

## Summary

| Public methods ||
|---|---|
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getConnectingEnd()()` Returns the timestamp for when the connection establishment ended. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getConnectingStart()()` Returns the timestamp for when the connection attempt began. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getDnsEnd()()` Returns the timestamp when the DNS lookup finished. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getDnsStart()()` Returns the timestamp when DNS lookup started. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getReceivedByteCount()()` Returns total bytes received. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getRequestEnd()()` Returns the timestamp when the request finished. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getRequestStart()()` Returns the timestamp when the request started. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getSendingEnd()()` Returns the timestamp when sending the request finished. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getSendingStart()()` Returns the timestamp when sending the request started. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getSentByteCount()()` Returns total bytes sent. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getTlsHandshakeEnd()()` Returns the timestamp when TLS handshake finished. |
| [Instant](https://developer.android.com/reference/kotlin/java/time/Instant.html#)? | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getTlsHandshakeStart()()` Returns the timestamp when TLS handshake started. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#wasSocketReused()()` Returns whether the socket was reused from a previous request. |

## Public methods

### getConnectingEnd

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getConnectingEnd(): Instant?
```

Returns the timestamp for when the connection establishment ended. If the connection used by the request is already active, this returns null.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing when the connection establishment finished. If using HTTPS, TLS handshake is completed. In some cases, such as 0-RTT, the stack may start sending data before connection establishment is considered complete; in such cases, this timestamp may occur after `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getSendingStart()`. |

### getConnectingStart

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getConnectingStart(): Instant?
```

Returns the timestamp for when the connection attempt began. If a connection is already active, this returns null.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing when the connection establishment started, or null. |

### getDnsEnd

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getDnsEnd(): Instant?
```

Returns the timestamp when the DNS lookup finished.

This value is `null` if no DNS lookup was required, such as when the request reuses an existing connection. If a lookup was attempted, this value will be non-null, regardless of whether the lookup succeeded (via network or cache) or failed.

See RequestFinishedTimings for more detailed timing information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | the `https://developer.android.com/reference/kotlin/java/time/Instant.html#` when the DNS lookup completed, or `null` if no lookup was performed. |

### getDnsStart

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getDnsStart(): Instant?
```

Returns the timestamp when DNS lookup started. If a connection is already active, this returns null.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing when the DNS lookup started, or null. |

### getReceivedByteCount

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getReceivedByteCount(): Long
```

Returns total bytes received.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is 0 or greater |

### getRequestEnd

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getRequestEnd(): Instant?
```

Returns the timestamp when the request finished.

This value is `null` if the request failed to start, as documented in `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings#getRequestStart()`. If the request started successfully, this reflects the time it reached a terminal state, including success, failure, or cancellation.

See RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | the `https://developer.android.com/reference/kotlin/java/time/Instant.html#` when the request finished, or `null` if the request never started. |

### getRequestStart

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getRequestStart(): Instant?
```

Returns the timestamp when the request started.

This value is `null` if the request fails initial validation checks during `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#start()` or org.chromium.net.BidirectionalStream#start() (for example, if an invalid header is provided).

See RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | the `https://developer.android.com/reference/kotlin/java/time/Instant.html#` when the request began, or `null` if the request failed before starting. |

### getSendingEnd

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getSendingEnd(): Instant?
```

Returns the timestamp when sending the request finished.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing the end of sending HTTP request (including the body). This value may be `null`. |

### getSendingStart

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getSendingStart(): Instant?
```

Returns the timestamp when sending the request started.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing the beginning of sending HTTP request headers. This value may be `null`. |

### getSentByteCount

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getSentByteCount(): Long
```

Returns total bytes sent.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | Value is 0 or greater |

### getTlsHandshakeEnd

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getTlsHandshakeEnd(): Instant?
```

Returns the timestamp when TLS handshake finished. This will always be equal to #getConnectEnd.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing when the TLS establishment finished. This value may be `null`. |

### getTlsHandshakeStart

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun getTlsHandshakeStart(): Instant?
```

Returns the timestamp when TLS handshake started.

See the documentation on RequestFinishedTimings for more information.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/time/Instant.html#?` | `https://developer.android.com/reference/kotlin/java/time/Instant.html#` representing when the TLS handshake has started. This will be later than getConnectStart. In cases where the TLS handshake is started immediately (e.g. QUIC), this may be equal to getConnectStart. This value may be `null`. |

### wasSocketReused

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
fun wasSocketReused(): Boolean
```

Returns whether the socket was reused from a previous request. Cases where this can happen include: reusing an idle socket that was used to complete a previous HTTP/1 request; multiplexing streams on a single HTTP/2 or QUIC connection.

Note that when a socket is reused, then DNS, connect and SSL timings are meaningless and undefined, as the request did not go through any of these stages.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if a socket has been reused. |
