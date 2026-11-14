Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# BidirectionalStream

```
abstract class BidirectionalStream
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.BidirectionalStream](BidirectionalStream.md) |

Class for bidirectional sending and receiving of data over HTTP/2 or QUIC connections. Created by `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder`. Note: There are ordering restrictions on methods of BidirectionalStream; please see individual methods for description of restrictions.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder` Builder for BidirectionalStreams. |
| abstract | `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback` Callback interface used to receive callbacks from a BidirectionalStream. |

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
| BidirectionalStream <br /> |

| Public methods ||
|---|---|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | cancel Cancels the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | flush Flushes pending writes. |
| open [FinishedRequestTimings](FinishedRequestTimings.md) | getFinishedRequestTimings Returns the detailed timing metrics for the request. |
| --- | --- |
| abstract [HeaderBlock](HeaderBlock.md) | getHeaders See addHeader |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | getHttpMethod See setHttpMethod. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPriority See setPriority |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTrafficStatsTag See setTrafficStatsTag |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getTrafficStatsUid See setTrafficStatsUid |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasTrafficStatsTag See setTrafficStatsTag |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | hasTrafficStatsUid See setTrafficStatsUid |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDelayRequestHeadersUntilFirstFlushEnabled See setDelayRequestHeadersUntilFirstFlushEnabled |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isDone Returns `true` if the stream was successfully started and is now done (succeeded, canceled, or failed). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | read Reads data from the stream into the provided buffer. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | start Starts the stream, all callbacks go to the `callback` argument passed to `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder`'s constructor. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | write Attempts to write data from the provided buffer into the stream. |
| --- | --- |

## Constants

### STREAM_PRIORITY_HIGHEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_HIGHEST: Int
```

Highest stream priority. Passed to setPriority.

 Value: 4

### STREAM_PRIORITY_IDLE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_IDLE: Int
```

Lowest stream priority. Passed to setPriority.

 Value: 0

### STREAM_PRIORITY_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_LOW: Int
```

Low stream priority. Passed to setPriority.

 Value: 2

### STREAM_PRIORITY_LOWEST

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_LOWEST: Int
```

Very low stream priority. Passed to setPriority.

 Value: 1

### STREAM_PRIORITY_MEDIUM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
static val STREAM_PRIORITY_MEDIUM: Int
```

Medium stream priority. Passed to setPriority. This is the default priority given to the stream.

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

Cancels the stream. Can be called at any time after start. onCanceled will be invoked when cancelation is complete and no further callback methods will be invoked. If the stream has completed or has not started, calling `cancel()` has no effect and `onCanceled()` will not be invoked. If the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` passed in during `BidirectionalStream` construction runs tasks on a single thread, and `cancel()` is called on that thread, no listener methods (besides `onCanceled()`) will be invoked after `cancel()` is called. Otherwise, at most one callback method may be invoked after `cancel()` has completed.

### flush

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun flush(): Unit
```

Flushes pending writes. This method should not be invoked before onStreamReady. For previously delayed writes, a corresponding onWriteCompleted will be invoked when the buffer is sent.

### getFinishedRequestTimings

Added in [API level 37.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 23](https://developer.android.com/sdkExtensions)

```
open fun getFinishedRequestTimings(): FinishedRequestTimings
```

Returns the detailed timing metrics for the request.

This method can be only called when the request has reached a terminal callback. This is defined by the execution of one of the following callbacks: onSucceeded, onFailed or onCanceled. It's also allowed to call this method in the terminal callback itself.

| Return ||
|---|---|
| FinishedRequestTimings | This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | If called before the terminal callback is called. |

### getHeaders

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getHeaders(): HeaderBlock
```

See addHeader

| Return ||
|---|---|
| HeaderBlock | This value cannot be `null`. |

### getHttpMethod

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getHttpMethod(): String
```

See setHttpMethod.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | This value cannot be `null`. |

### getPriority

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getPriority(): Int
```

See setPriority

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Value is one of the following: - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_IDLE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_LOWEST:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_LOW:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_MEDIUM:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#STREAM_PRIORITY_HIGHEST:kotlin.Int` |

### getTrafficStatsTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getTrafficStatsTag(): Int
```

See setTrafficStatsTag

### getTrafficStatsUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun getTrafficStatsUid(): Int
```

See setTrafficStatsUid

### hasTrafficStatsTag

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun hasTrafficStatsTag(): Boolean
```

See setTrafficStatsTag

### hasTrafficStatsUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun hasTrafficStatsUid(): Boolean
```

See setTrafficStatsUid

### isDelayRequestHeadersUntilFirstFlushEnabled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

```
abstract fun isDelayRequestHeadersUntilFirstFlushEnabled(): Boolean
```

See setDelayRequestHeadersUntilFirstFlushEnabled

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

Reads data from the stream into the provided buffer. Can only be called at most once in response to each invocation of the onStreamReady/ onResponseHeadersReceived and onReadCompleted methods of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback`. Each call will result in an invocation of one of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback`'s onReadCompleted method if data is read, or its onFailed method if there's an error. An attempt to read data into `buffer` starting at `buffer.position()` is begun. At most `buffer.remaining()` bytes are read. `buffer.position()` is updated upon invocation of onReadCompleted to indicate how much data was read.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md): the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` to read data into. Must be a direct ByteBuffer. The embedder must not read or modify buffer's position, limit, or data between its position and limit until onReadCompleted, onCanceled, or onFailed are invoked. This value cannot be `null`. |

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

Attempts to write data from the provided buffer into the stream. If auto flush is disabled, data will be sent only after flush is called. Each call will result in an invocation of one of the `https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback`'s onWriteCompleted method if data is sent, or its onFailed method if there's an error. An attempt to write data from `buffer` starting at `buffer.position()` is begun. `buffer.remaining()` bytes will be written. onWriteCompleted will be invoked only when the full ByteBuffer is written.

| Parameters ||
|---|---|
| `buffer` | [ByteBuffer](../java.nio/ByteBuffer.md): the `https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#` to write data from. Must be a direct ByteBuffer. The embedder must not read or modify buffer's position, limit, or data between its position and limit until onWriteCompleted, onCanceled, or onFailed are invoked. Can be empty when `endOfStream` is `true`. This value cannot be `null`. |
| `endOfStream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): if `true`, then `buffer` is the last buffer to be written, and once written, stream is closed from the client side, resulting in half-closed stream or a fully closed stream if the remote side has already closed. |
