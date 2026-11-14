# UploadDataProvider

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# UploadDataProvider

Kotlin| [Java](UploadDataProvider.md) 
| --- | --- |

```
abstract class UploadDataProvider : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.UploadDataProvider](UploadDataProvider.md) |

Abstract class allowing the embedder to provide an upload body to [UrlRequest](UrlRequest.md). It supports both non-chunked (size known in advanced) and chunked (size not known in advance) uploads. Be aware that not all servers support chunked uploads.

An upload is either always chunked, across multiple uploads if the data ends up being sent more than once, or never chunked.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [UploadDataProvider](UploadDataProvider.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](UploadDataProvider.md))`()` Called when this UploadDataProvider is no longer needed by a request, so that resources (like a file) can be explicitly released. |
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getLength](UploadDataProvider.md))`()` If this is a non-chunked upload, returns the length of the upload. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [read](UploadDataProvider.md))`(`uploadDataSink:` ` [UploadDataSink](UploadDataSink.md)`, `byteBuffer:` ` [ByteBuffer](../java.nio/ByteBuffer.md)`)` Reads upload data into`byteBuffer`. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [rewind](UploadDataProvider.md))`(`uploadDataSink:` ` [UploadDataSink](UploadDataSink.md)`)` Rewinds upload data. |

## Public constructors

### UploadDataProvider

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
UploadDataProvider()
```

## Public methods

### close

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun close(): Unit
```

Called when this UploadDataProvider is no longer needed by a request, so that resources (like a file) can be explicitly released.

| Exceptions ||
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if any IOException occurred during the process. This will cause the request to fail if it is not yet complete; otherwise it will be logged. |

### getLength

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun getLength(): Long
```

If this is a non-chunked upload, returns the length of the upload. Must always return -1 if this is a chunked upload.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the length of the upload for non-chunked uploads, -1 otherwise. |

| Exceptions ||
|-----------------------|-------------------------------------------------|
| `java.io.IOException` | if any IOException occurred during the process. |

### read

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun read(
    uploadDataSink: UploadDataSink, 
    byteBuffer: ByteBuffer
): Unit
```

Reads upload data into`byteBuffer`. Upon completion, the buffer's position is updated to the end of the bytes that were read. The buffer's limit is not changed. Each call of this method must be followed be a single call, either synchronous or asynchronous, to`uploadDataSink`: [UploadDataSink.onReadSucceeded](UploadDataSink.md))on success or [android.net.http.UploadDataSink#onReadError](UploadDataSink.md))on failure. Neither read nor rewind will be called until one of those methods or the other is called. Even if the associated [UrlRequest](UrlRequest.md) is canceled, one or the other must still be called before resources can be safely freed. Throwing an exception will also result in resources being freed and the request being errored out.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uploadDataSink` | [UploadDataSink](UploadDataSink.md):The object to notify when the read has completed, successfully or otherwise. This value cannot be`null`. |
| `byteBuffer` | [ByteBuffer](../java.nio/ByteBuffer.md):The buffer to copy the read bytes into. Do not change byteBuffer's limit. This value cannot be`null`. |

| Exceptions ||
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if any IOException occurred during the process. [android.net.http.UrlRequest.Callback#onFailed](../android/net/http/UrlRequest.Callback.md))will be called with the thrown exception set as the cause of the [CallbackException](CallbackException.md). |

### rewind

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun rewind(uploadDataSink: UploadDataSink): Unit
```

Rewinds upload data. Each call must be followed be a single call, either synchronous or asynchronous, to`uploadDataSink`: [UploadDataSink.onRewindSucceeded](UploadDataSink.md))on success or [UploadDataSink.onRewindError](UploadDataSink.md))on failure. Neither read nor rewind will be called until one of those methods or the other is called. Even if the associated [UrlRequest](UrlRequest.md) is canceled, one or the other must still be called before resources can be safely freed. Throwing an exception will also result in resources being freed and the request being errored out.

If rewinding is not supported, this should call [UploadDataSink.onRewindError](UploadDataSink.md)). Note that rewinding is required to follow redirects that preserve the upload body, and for retrying when the server times out stale sockets.

| Parameters ||
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `uploadDataSink` | [UploadDataSink](UploadDataSink.md):The object to notify when the rewind operation has completed, successfully or otherwise. This value cannot be`null`. |

| Exceptions ||
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.io.IOException` | if any IOException occurred during the process. [android.net.http.UrlRequest.Callback#onFailed](../android/net/http/UrlRequest.Callback.md))will be called with the thrown exception set as the cause of the [CallbackException](CallbackException.md). |
