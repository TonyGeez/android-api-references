# UploadDataSink

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# UploadDataSink

Kotlin| [Java](../android/net/http/UploadDataSink.md) 
| --- | --- |

```
abstract class UploadDataSink
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.http.UploadDataSink](../android/net/http/UploadDataSink.md) |

Defines callbacks methods for [UploadDataProvider](../android/net/http/UploadDataProvider.md). All methods may be called synchronously or asynchronously, on any thread.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------|---|
| [UploadDataSink](../android/net/http/UploadDataSink.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReadError](../android/net/http/UploadDataSink.md))`(`exception:` ` [Exception](../java/lang/Exception.md)`)` Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a read fails. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReadSucceeded](../android/net/http/UploadDataSink.md))`(`finalChunk:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a read succeeds. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRewindError](../android/net/http/UploadDataSink.md))`(`exception:` ` [Exception](../java/lang/Exception.md)`)` Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a rewind fails, or if rewinding uploads is not supported. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRewindSucceeded](../android/net/http/UploadDataSink.md))`()` Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a rewind succeeds. |

## Public constructors

### UploadDataSink

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
UploadDataSink()
```

## Public methods

### onReadError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onReadError(exception: Exception): Unit
```

Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a read fails.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [Exception](../java/lang/Exception.md):Exception passed on to the embedder. This value cannot be`null`. |

### onReadSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onReadSucceeded(finalChunk: Boolean): Unit
```

Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a read succeeds.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `finalChunk` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):For chunked uploads,`true`if this is the final read. It must be`false`for non-chunked uploads. |

### onRewindError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onRewindError(exception: Exception): Unit
```

Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a rewind fails, or if rewinding uploads is not supported.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [Exception](../java/lang/Exception.md):Exception passed on to the embedder. This value cannot be`null`. |

### onRewindSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onRewindSucceeded(): Unit
```

Called by [UploadDataProvider](../android/net/http/UploadDataProvider.md) when a rewind succeeds.
