# BidirectionalStream.Callback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# Callback

Kotlin| [Java](../android/net/http/BidirectionalStream.Callback.md) 
| --- | --- |

```
interface Callback
```

| [android.net.http.BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md) |

Callback interface used to receive callbacks from a [BidirectionalStream](../android/net/http/BidirectionalStream.md).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCanceled](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)?`)` Invoked if the stream was canceled via [BidirectionalStream.cancel](../android/net/http/BidirectionalStream.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailed](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)?`, `error:` ` [HttpException](../android/net/http/HttpException.md)`)` Invoked if the stream failed for any reason after [BidirectionalStream.start](../android/net/http/BidirectionalStream.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReadCompleted](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)`, `buffer:` ` [ByteBuffer](../java/nio/ByteBuffer.md)`, `endOfStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Invoked when data is read into the buffer passed to [read()](../android/net/http/BidirectionalStream.md)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResponseHeadersReceived](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)`)` Invoked when initial response headers are received. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResponseTrailersReceived](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)`, `trailers:` ` [HeaderBlock](../android/net/http/HeaderBlock.md)`)` Invoked when trailers are received before closing the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStreamReady](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`)` Invoked when the stream is ready for reading and writing. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSucceeded](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)`)` Invoked when there is no data to be read or written and the stream is closed successfully remotely and locally. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWriteCompleted](../android/net/http/BidirectionalStream.Callback.md))`(`stream:` ` [BidirectionalStream](../android/net/http/BidirectionalStream.md)`, `info:` ` [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)`, `buffer:` ` [ByteBuffer](../java/nio/ByteBuffer.md)`, `endOfStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Invoked when the entire ByteBuffer passed to [write()](../android/net/http/BidirectionalStream.md))is sent. |

## Public methods

### onCanceled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onCanceled(
    stream: BidirectionalStream, 
    info: UrlResponseInfo?
): Unit
```

Invoked if the stream was canceled via [BidirectionalStream.cancel](../android/net/http/BidirectionalStream.md)). Once invoked, no further [BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md) methods will be invoked. Default implementation takes no action.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream that was canceled.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)?:the response information. May be`null`if no response was received. |

### onFailed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onFailed(
    stream: BidirectionalStream, 
    info: UrlResponseInfo?, 
    error: HttpException
): Unit
```

Invoked if the stream failed for any reason after [BidirectionalStream.start](../android/net/http/BidirectionalStream.md)). [HTTP/2 error codes](https://tools.ietf.org/html/rfc7540#section-7) are mapped to [NetworkException.getErrorCode](../android/net/http/NetworkException.md))codes. Once invoked, no further [BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md) methods will be invoked.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream which has failed.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md)?:the response information. May be`null`if no response was received. |
| `error` | [HttpException](../android/net/http/HttpException.md):information about the failure This value cannot be`null`. |
| --- | --- |

### onReadCompleted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onReadCompleted(
    stream: BidirectionalStream, 
    info: UrlResponseInfo, 
    buffer: ByteBuffer, 
    endOfStream: Boolean
): Unit
```

Invoked when data is read into the buffer passed to [read()](../android/net/http/BidirectionalStream.md)). Only part of the buffer may be populated. To continue reading, call [read()](../android/net/http/BidirectionalStream.md)). It may be invoked after`onResponseTrailersReceived()`, if there was pending read data before trailers were received.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream on which the read completed.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md):the response information This value cannot be`null`. |
| `buffer` | [ByteBuffer](../java/nio/ByteBuffer.md):the buffer that was passed to [read()](../android/net/http/BidirectionalStream.md)), now set to the end of the received data. If position is not updated, it means the remote side has signaled that it will send no more data. This value cannot be`null`. |
| --- | --- |
| `endOfStream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):if true, this is the last read data, remote will not send more data, and the read side is closed. |

### onResponseHeadersReceived

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onResponseHeadersReceived(
    stream: BidirectionalStream, 
    info: UrlResponseInfo
): Unit
```

Invoked when initial response headers are received. Headers are available from`info.` [getHeaders()](../android/net/http/UrlResponseInfo.md)). Consumer may call [read()](../android/net/http/BidirectionalStream.md))to start reading. Consumer may call [write()](../android/net/http/BidirectionalStream.md))to start writing or close the stream.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream on which response headers were received.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md):the response information. This value cannot be`null`. |

### onResponseTrailersReceived

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onResponseTrailersReceived(
    stream: BidirectionalStream, 
    info: UrlResponseInfo, 
    trailers: HeaderBlock
): Unit
```

Invoked when trailers are received before closing the stream. Only invoked when server sends trailers, which it may not. May be invoked while there is read data remaining in local buffer. Default implementation takes no action.

| Parameters ||
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream on which response trailers were received.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md):the response information This value cannot be`null`. |
| `trailers` | [HeaderBlock](../android/net/http/HeaderBlock.md):the trailers received This value cannot be`null`. |
| --- | --- |

### onStreamReady

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onStreamReady(stream: BidirectionalStream): Unit
```

Invoked when the stream is ready for reading and writing. Consumer may call [read()](../android/net/http/BidirectionalStream.md))to start reading data. Consumer may call [write()](../android/net/http/BidirectionalStream.md))to start writing data.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream that is ready.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |

### onSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onSucceeded(
    stream: BidirectionalStream, 
    info: UrlResponseInfo
): Unit
```

Invoked when there is no data to be read or written and the stream is closed successfully remotely and locally. Once invoked, no further [BidirectionalStream.Callback](../android/net/http/BidirectionalStream.Callback.md) methods will be invoked.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream which is closed successfully.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md):the response information This value cannot be`null`. |

### onWriteCompleted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onWriteCompleted(
    stream: BidirectionalStream, 
    info: UrlResponseInfo, 
    buffer: ByteBuffer, 
    endOfStream: Boolean
): Unit
```

Invoked when the entire ByteBuffer passed to [write()](../android/net/http/BidirectionalStream.md))is sent. The buffer's position is updated to be the same as the buffer's limit. The buffer's limit is not changed. To continue writing, call [write()](../android/net/http/BidirectionalStream.md)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](../android/net/http/BidirectionalStream.md):the stream on which the write completed.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](../android/net/http/BidirectionalStream.Builder.md)).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](../android/net/http/BidirectionalStream.md). This value cannot be`null`. |
| `info` | [UrlResponseInfo](../android/net/http/UrlResponseInfo.md):the response information This value cannot be`null`. |
| `buffer` | [ByteBuffer](../java/nio/ByteBuffer.md):the buffer that was passed to [write()](../android/net/http/BidirectionalStream.md)). The buffer's position is set to the buffer's limit. The buffer's limit is not changed. This value cannot be`null`. |
| --- | --- |
| `endOfStream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the endOfStream flag that was passed to the corresponding [write()](../android/net/http/BidirectionalStream.md)). If true, the write side is closed. |
