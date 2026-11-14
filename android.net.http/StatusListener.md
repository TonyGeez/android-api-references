Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# StatusListener

Kotlin | [Java](https://developer.android.com/reference/android/net/http/UrlRequest.StatusListener "View this page in Java")

```
interface StatusListener
```

| [android.net.http.UrlRequest.StatusListener](https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.StatusListener#) |

Listener interface used with `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getStatus(android.net.http.UrlRequest.StatusListener)` to receive the status of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`.

## Summary

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.StatusListener#onStatus(kotlin.Int)(status: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Invoked on `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`'s `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`'s thread when request status is obtained. |

## Public methods

### onStatus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun onStatus(status: Int): Unit
```

Invoked on `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest`'s `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`'s thread when request status is obtained.

| Parameters ||
|---|---|
| `status` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): integer representing the status of the request. It is one of the values defined in `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#INVALID:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#WAITING_FOR_STALLED_SOCKET_POOL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#WAITING_FOR_AVAILABLE_SOCKET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#WAITING_FOR_DELEGATE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#WAITING_FOR_CACHE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#DOWNLOADING_PAC_FILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#RESOLVING_PROXY_FOR_URL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#RESOLVING_PROXY_FOR_URL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#RESOLVING_HOST_IN_PAC_FILE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#ESTABLISHING_PROXY_TUNNEL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#RESOLVING_HOST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#CONNECTING:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#SSL_HANDSHAKE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#SENDING_REQUEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#WAITING_FOR_RESPONSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status#READING_RESPONSE:kotlin.Int` |
