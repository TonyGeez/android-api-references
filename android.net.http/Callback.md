# BidirectionalStream.Callback

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# Callback

Kotlin| [Java](https://developer.android.com/reference/android/net/http/BidirectionalStream.Callback "View this page in Java") 
| --- | --- |

```
interface Callback
```

| [android.net.http.BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#) |

Callback interface used to receive callbacks from a [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCanceled](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onCanceled(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)?`)` Invoked if the stream was canceled via [BidirectionalStream.cancel](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#cancel()). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFailed](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onFailed(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HttpException))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)?`, `error:` ` [HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException)`)` Invoked if the stream failed for any reason after [BidirectionalStream.start](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#start()). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReadCompleted](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onReadCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)`, `buffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)`, `endOfStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Invoked when data is read into the buffer passed to [read()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer)). |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResponseHeadersReceived](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onResponseHeadersReceived(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)`)` Invoked when initial response headers are received. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onResponseTrailersReceived](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onResponseTrailersReceived(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20android.net.http.HeaderBlock))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)`, `trailers:` ` [HeaderBlock](https://developer.android.com/reference/kotlin/android/net/http/HeaderBlock)`)` Invoked when trailers are received before closing the stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStreamReady](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onStreamReady(android.net.http.BidirectionalStream))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`)` Invoked when the stream is ready for reading and writing. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSucceeded](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onSucceeded(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)`)` Invoked when there is no data to be read or written and the stream is closed successfully remotely and locally. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onWriteCompleted](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#onWriteCompleted(android.net.http.BidirectionalStream,%20android.net.http.UrlResponseInfo,%20java.nio.ByteBuffer,%20kotlin.Boolean))`(`stream:` ` [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream)`, `info:` ` [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)`, `buffer:` ` [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#)`, `endOfStream:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Invoked when the entire ByteBuffer passed to [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean))is sent. |

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

Invoked if the stream was canceled via [BidirectionalStream.cancel](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#cancel()). Once invoked, no further [BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#) methods will be invoked. Default implementation takes no action.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream that was canceled.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)?:the response information. May be`null`if no response was received. |

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

Invoked if the stream failed for any reason after [BidirectionalStream.start](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#start()). [HTTP/2 error codes](https://tools.ietf.org/html/rfc7540#section-7) are mapped to [NetworkException.getErrorCode](https://developer.android.com/reference/kotlin/android/net/http/NetworkException#getErrorCode())codes. Once invoked, no further [BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#) methods will be invoked.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream which has failed.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo)?:the response information. May be`null`if no response was received. |
| `error` | [HttpException](https://developer.android.com/reference/kotlin/android/net/http/HttpException):information about the failure This value cannot be`null`. |
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

Invoked when data is read into the buffer passed to [read()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer)). Only part of the buffer may be populated. To continue reading, call [read()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer)). It may be invoked after`onResponseTrailersReceived()`, if there was pending read data before trailers were received.

| Parameters ||
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream on which the read completed.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo):the response information This value cannot be`null`. |
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#):the buffer that was passed to [read()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer)), now set to the end of the received data. If position is not updated, it means the remote side has signaled that it will send no more data. This value cannot be`null`. |
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

Invoked when initial response headers are received. Headers are available from`info.` [getHeaders()](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo#getHeaders()). Consumer may call [read()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer))to start reading. Consumer may call [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean))to start writing or close the stream.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream on which response headers were received.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo):the response information. This value cannot be`null`. |

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
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream on which response trailers were received.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo):the response information This value cannot be`null`. |
| `trailers` | [HeaderBlock](https://developer.android.com/reference/kotlin/android/net/http/HeaderBlock):the trailers received This value cannot be`null`. |
| --- | --- |

### onStreamReady

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onStreamReady(stream: BidirectionalStream): Unit
```

Invoked when the stream is ready for reading and writing. Consumer may call [read()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#read(java.nio.ByteBuffer))to start reading data. Consumer may call [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean))to start writing data.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream that is ready.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |

### onSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onSucceeded(
    stream: BidirectionalStream, 
    info: UrlResponseInfo
): Unit
```

Invoked when there is no data to be read or written and the stream is closed successfully remotely and locally. Once invoked, no further [BidirectionalStream.Callback](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Callback#) methods will be invoked.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream which is closed successfully.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo):the response information This value cannot be`null`. |

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

Invoked when the entire ByteBuffer passed to [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean))is sent. The buffer's position is updated to be the same as the buffer's limit. The buffer's limit is not changed. To continue writing, call [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean)).

| Parameters ||
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `stream` | [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream):the stream on which the write completed.**This is not guaranteed to be the same object as the one received by other callbacks, nor is it guaranteed to be the one returned by [BidirectionalStream.Builder.build](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream.Builder#build()).** However, method calls on this object will have the same effects as calls on the original [BidirectionalStream](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream). This value cannot be`null`. |
| `info` | [UrlResponseInfo](https://developer.android.com/reference/kotlin/android/net/http/UrlResponseInfo):the response information This value cannot be`null`. |
| `buffer` | [ByteBuffer](https://developer.android.com/reference/kotlin/java/nio/ByteBuffer.html#):the buffer that was passed to [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean)). The buffer's position is set to the buffer's limit. The buffer's limit is not changed. This value cannot be`null`. |
| --- | --- |
| `endOfStream` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):the endOfStream flag that was passed to the corresponding [write()](https://developer.android.com/reference/kotlin/android/net/http/BidirectionalStream#write(java.nio.ByteBuffer,%20kotlin.Boolean)). If true, the write side is closed. |
