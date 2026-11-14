Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# UrlRequest

```
abstract class UrlRequest
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.UrlRequest](UrlRequest.md) |

Controls an HTTP request (GET, PUT, POST etc). Created by `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder`, which can be obtained by calling `https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#newUrlRequestBuilder(kotlin.String,%20java.util.concurrent.Executor,%20android.net.http.UrlRequest.Callback)`. Note: All methods must be called on the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` passed to `https://developer.android.com/reference/kotlin/android/net/http/HttpEngine#newUrlRequestBuilder(kotlin.String,%20java.util.concurrent.Executor,%20android.net.http.UrlRequest.Callback)`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder` Builder for `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#`s. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback` Users of the HTTP stack extend this class to receive callbacks indicating the progress of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#` being processed. |
| open | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Status` Request status values returned by `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getStatus(android.net.http.UrlRequest.StatusListener)`. |
| --- | --- |
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.StatusListener` Listener interface used with `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getStatus(android.net.http.UrlRequest.StatusListener)` to receive the status of a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#REQUEST_PRIORITY_HIGHEST:kotlin.Int` Highest request priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#REQUEST_PRIORITY_IDLE:kotlin.Int` Lowest request priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#REQUEST_PRIORITY_LOW:kotlin.Int` Low request priority. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#REQUEST_PRIORITY_LOWEST:kotlin.Int` Very low request priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#REQUEST_PRIORITY_MEDIUM:kotlin.Int` Medium request priority. |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#cancel()()` Cancels the request. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#followRedirect()()` Follows a pending redirect. |
| open [FinishedRequestTimings](FinishedRequestTimings.md) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getFinishedRequestTimings()()` Returns the detailed timing metrics for the request. |
| --- | --- |
| abstract [HeaderBlock](HeaderBlock.md) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getHeaders()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#addHeader(kotlin.String,%20kotlin.String)` |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getHttpMethod()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setHttpMethod(kotlin.String)`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getPriority()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)` |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getStatus(android.net.http.UrlRequest.StatusListener)(listener: https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.StatusListener)` Queries the status of the request. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getTrafficStatsTag()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsTag(kotlin.Int)` |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#getTrafficStatsUid()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsUid(kotlin.Int)` |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#hasTrafficStatsTag()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsTag(kotlin.Int)` |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#hasTrafficStatsUid()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsUid(kotlin.Int)` |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#isCacheDisabled()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setCacheDisabled(kotlin.Boolean)` |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#isDirectExecutorAllowed()()` See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setDirectExecutorAllowed(kotlin.Boolean)` |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#isDone()()` Returns `true` if the request was successfully started and is now finished (completed, canceled, or failed). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#read(java.nio.ByteBuffer)(buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)` Attempts to read part of the response body into the provided buffer. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#start()()` Starts the request, all callbacks go to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback`. |

## Constants

### REQUEST_PRIORITY_HIGHEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val REQUEST_PRIORITY_HIGHEST: Int
```

Highest request priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)`.

 Value: 4

### REQUEST_PRIORITY_IDLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val REQUEST_PRIORITY_IDLE: Int
```

Lowest request priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)`.

 Value: 0

### REQUEST_PRIORITY_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val REQUEST_PRIORITY_LOW: Int
```

Low request priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)`.

 Value: 2

### REQUEST_PRIORITY_LOWEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val REQUEST_PRIORITY_LOWEST: Int
```

Very low request priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)`.

 Value: 1

### REQUEST_PRIORITY_MEDIUM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val REQUEST_PRIORITY_MEDIUM: Int
```

Medium request priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)`. This is the default priority given to the request.

 Value: 3

## Public methods

### cancel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun cancel(): Unit
```

Cancels the request. Can be called at any time. `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onCanceled(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo)` will be invoked when cancellation is complete and no further callback methods will be invoked. If the request has completed or has not started, calling `cancel()` has no effect and `onCanceled()` will not be invoked. If the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` passed in during `UrlRequest` construction runs tasks on a single thread, and `cancel()` is called on that thread, no callback methods (besides `onCanceled()`) will be invoked after `cancel()` is called. Otherwise, at most one callback method may be invoked after `cancel()` has completed.

### followRedirect

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun followRedirect(): Unit
```

Follows a pending redirect. Must only be called at most once for each invocation of `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onRedirectReceived(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20kotlin.String)`.

### getFinishedRequestTimings

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
open fun getFinishedRequestTimings(): FinishedRequestTimings
```

Returns the detailed timing metrics for the request.

This method can be only called when the request has reached a terminal callback. This is defined by the execution of one of the following callbacks: `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onSucceeded(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo)`, `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` or `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onCanceled(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo)`. It's also allowed to call this method in the terminal callback itself.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/http/FinishedRequestTimings` | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called before the terminal callback is called. |

### getHeaders

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getHeaders(): HeaderBlock
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#addHeader(kotlin.String,%20kotlin.String)`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/http/HeaderBlock` | This value cannot be `null`. |

### getHttpMethod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getHttpMethod(): String?
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setHttpMethod(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getPriority

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getPriority(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setPriority(kotlin.Int)`

### getStatus

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getStatus(listener: UrlRequest.StatusListener): Unit
```

Queries the status of the request.

This is most useful to query the status of the request before any of the `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback` methods are called by Cronet.

The `listener` will be invoked back on the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` passed in when the request was created. While you can assume the callback will be invoked in a timely fashion, the API doesn't make any guarantees about the latency, nor does it specify the order in which the listener and other callbacks will be invoked.

| Parameters ||
|---|---|
| `listener` | [UrlRequest.StatusListener](../android/net/http/UrlRequest.StatusListener.md): a `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.StatusListener` that will be invoked with the request's current status. This value cannot be `null`. |

### getTrafficStatsTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getTrafficStatsTag(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsTag(kotlin.Int)`

### getTrafficStatsUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getTrafficStatsUid(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsUid(kotlin.Int)`

### hasTrafficStatsTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun hasTrafficStatsTag(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsTag(kotlin.Int)`

### hasTrafficStatsUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun hasTrafficStatsUid(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setTrafficStatsUid(kotlin.Int)`

### isCacheDisabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun isCacheDisabled(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setCacheDisabled(kotlin.Boolean)`

### isDirectExecutorAllowed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun isDirectExecutorAllowed(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Builder#setDirectExecutorAllowed(kotlin.Boolean)`

### isDone

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun isDone(): Boolean
```

Returns `true` if the request was successfully started and is now finished (completed, canceled, or failed).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the request was successfully started and is now finished (completed, canceled, or failed). |

### read

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun read(buffer: ByteBuffer): Unit
```

Attempts to read part of the response body into the provided buffer. Must only be called at most once in response to each invocation of the `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onResponseStarted(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo)` and `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onReadCompleted(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer)` methods of the `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback`. Each call will result in an asynchronous call to either the `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback` `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onReadCompleted(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer)` method if data is read, its `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onSucceeded(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo)` method if there's no more data to read, or its `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback#onFailed(android.net.http.UrlRequest,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` method if there's an error.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md): `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` to write response body to. Must be a direct ByteBuffer. The embedder must not read or modify buffer's position, limit, or data between its position and limit until the request calls back into the `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback`. This value cannot be `null`. |

### start

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun start(): Unit
```

Starts the request, all callbacks go to `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest.Callback`. May only be called once. May not be called if `https://developer.android.com/reference/kotlin/android/net/http/UrlRequest#cancel()` has been called.
