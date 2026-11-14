Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# BidirectionalStream

```
abstract class BidirectionalStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.BidirectionalStream](../android/net/http/BidirectionalStream.md) |

Class for bidirectional sending and receiving of data over HTTP/2 or QUIC connections. Created by `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder`. Note: There are ordering restrictions on methods of `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#`; please see individual methods for description of restrictions.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder` Builder for `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#`s. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback` Callback interface used to receive callbacks from a `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_HIGHEST:kotlin.Int` Highest stream priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_IDLE:kotlin.Int` Lowest stream priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_LOW:kotlin.Int` Low stream priority. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_LOWEST:kotlin.Int` Very low stream priority. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_MEDIUM:kotlin.Int` Medium stream priority. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#BidirectionalStream()()` <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#cancel()()` Cancels the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#flush()()` Flushes pending writes. |
| open [FinishedRequestTimings](../android/net/http/FinishedRequestTimings.md) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#getFinishedRequestTimings()()` Returns the detailed timing metrics for the request. |
| --- | --- |
| abstract [HeaderBlock](../android/net/http/HeaderBlock.md) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#getHeaders()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#addHeader(kotlin.String,%20kotlin.String)` |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#getHttpMethod()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setHttpMethod(kotlin.String)`. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#getPriority()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)` |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#getTrafficStatsTag()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsTag(kotlin.Int)` |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#getTrafficStatsUid()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsUid(kotlin.Int)` |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#hasTrafficStatsTag()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsTag(kotlin.Int)` |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#hasTrafficStatsUid()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsUid(kotlin.Int)` |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#isDelayRequestHeadersUntilFirstFlushEnabled()()` See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setDelayRequestHeadersUntilFirstFlushEnabled(kotlin.Boolean)` |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#isDone()()` Returns `true` if the stream was successfully started and is now done (succeeded, canceled, or failed). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer)(buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)` Reads data from the stream into the provided buffer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#start()()` Starts the stream, all callbacks go to the `callback` argument passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder`'s constructor. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean)(buffer: https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#, endOfStream: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Attempts to write data from the provided buffer into the stream. |
| --- | --- |

## Constants

### STREAM_PRIORITY_HIGHEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_HIGHEST: Int
```

Highest stream priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)`.

 Value: 4

### STREAM_PRIORITY_IDLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_IDLE: Int
```

Lowest stream priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)`.

 Value: 0

### STREAM_PRIORITY_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_LOW: Int
```

Low stream priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)`.

 Value: 2

### STREAM_PRIORITY_LOWEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_LOWEST: Int
```

Very low stream priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)`.

 Value: 1

### STREAM_PRIORITY_MEDIUM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_MEDIUM: Int
```

Medium stream priority. Passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)`. This is the default priority given to the stream.

 Value: 3

## Public constructors

### BidirectionalStream

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
BidirectionalStream()
```

## Public methods

### cancel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun cancel(): Unit
```

Cancels the stream. Can be called at any time after `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#start()`. `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onCanceled(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo)` will be invoked when cancelation is complete and no further callback methods will be invoked. If the stream has completed or has not started, calling `cancel()` has no effect and `onCanceled()` will not be invoked. If the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` passed in during `BidirectionalStream` construction runs tasks on a single thread, and `cancel()` is called on that thread, no listener methods (besides `onCanceled()`) will be invoked after `cancel()` is called. Otherwise, at most one callback method may be invoked after `cancel()` has completed.

### flush

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun flush(): Unit
```

Flushes pending writes. This method should not be invoked before `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onStreamReady(android.net.http.BidirectionalStream)`. For previously delayed `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean)`s, a corresponding `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onWriteCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)` will be invoked when the buffer is sent.

### getFinishedRequestTimings

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
open fun getFinishedRequestTimings(): FinishedRequestTimings
```

Returns the detailed timing metrics for the request.

This method can be only called when the request has reached a terminal callback. This is defined by the execution of one of the following callbacks: `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onSucceeded(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo)`, `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onFailed(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` or `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onCanceled(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo)`. It's also allowed to call this method in the terminal callback itself.

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

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#addHeader(kotlin.String,%20kotlin.String)`

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/http/HeaderBlock` | This value cannot be `null`. |

### getHttpMethod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getHttpMethod(): String
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setHttpMethod(kotlin.String)`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getPriority

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getPriority(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setPriority(kotlin.Int)`

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_LOWEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_MEDIUM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_HIGHEST:kotlin.Int` |

### getTrafficStatsTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getTrafficStatsTag(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsTag(kotlin.Int)`

### getTrafficStatsUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getTrafficStatsUid(): Int
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsUid(kotlin.Int)`

### hasTrafficStatsTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun hasTrafficStatsTag(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsTag(kotlin.Int)`

### hasTrafficStatsUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun hasTrafficStatsUid(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setTrafficStatsUid(kotlin.Int)`

### isDelayRequestHeadersUntilFirstFlushEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun isDelayRequestHeadersUntilFirstFlushEnabled(): Boolean
```

See `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#setDelayRequestHeadersUntilFirstFlushEnabled(kotlin.Boolean)`

### isDone

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun isDone(): Boolean
```

Returns `true` if the stream was successfully started and is now done (succeeded, canceled, or failed).

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the stream was successfully started and is now done (completed, canceled, or failed), otherwise returns `false` to indicate stream is not yet started or is in progress. |

### read

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun read(buffer: ByteBuffer): Unit
```

Reads data from the stream into the provided buffer. Can only be called at most once in response to each invocation of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onStreamReady(android.net.http.BidirectionalStream)`/ `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onResponseHeadersReceived(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo)` and `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onReadCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)` methods of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback`. Each call will result in an invocation of one of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback`'s `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onReadCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)` method if data is read, or its `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onFailed(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` method if there's an error. An attempt to read data into `buffer` starting at `buffer.position()` is begun. At most `buffer.remaining()` bytes are read. `buffer.position()` is updated upon invocation of `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onReadCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)` to indicate how much data was read.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java/nio/ByteBuffer.md): the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` to read data into. Must be a direct ByteBuffer. The embedder must not read or modify buffer's position, limit, or data between its position and limit until `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onReadCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onCanceled(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo)`, or `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onFailed(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` are invoked. This value cannot be `null`. |

### start

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun start(): Unit
```

Starts the stream, all callbacks go to the `callback` argument passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder`'s constructor. Should only be called once.

### write

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun write(
    buffer: ByteBuffer, 
    endOfStream: Boolean
): Unit
```

Attempts to write data from the provided buffer into the stream. If auto flush is disabled, data will be sent only after `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#flush()` is called. Each call will result in an invocation of one of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback`'s `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onWriteCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)` method if data is sent, or its `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onFailed(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` method if there's an error. An attempt to write data from `buffer` starting at `buffer.position()` is begun. `buffer.remaining()` bytes will be written. `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onWriteCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)` will be invoked only when the full ByteBuffer is written.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java/nio/ByteBuffer.md): the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` to write data from. Must be a direct ByteBuffer. The embedder must not read or modify buffer's position, limit, or data between its position and limit until `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onWriteCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean)`, `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onCanceled(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo)`, or `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onFailed(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException)` are invoked. Can be empty when `endOfStream` is `true`. This value cannot be `null`. |
| `endOfStream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true`, then `buffer` is the last buffer to be written, and once written, stream is closed from the client side, resulting in half-closed stream or a fully closed stream if the remote side has already closed. |
