# UploadDataSink

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions)

# UploadDataSink

Kotlin| [Java](https://developer.android.com/reference/android/net/http/UploadDataSink "View this page in Java") 

```
abstract class UploadDataSink
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.net.http.UploadDataSink](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink#) |

Defines callbacks methods for [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider). All methods may be called synchronously or asynchronously, on any thread.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------|---|
| [UploadDataSink](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink#UploadDataSink())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReadError](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink#onReadError(java.lang.Exception))`(`exception:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)`)` Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a read fails. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReadSucceeded](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink#onReadSucceeded(kotlin.Boolean))`(`finalChunk:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a read succeeds. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRewindError](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink#onRewindError(java.lang.Exception))`(`exception:` ` [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#)`)` Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a rewind fails, or if rewinding uploads is not supported. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRewindSucceeded](https://developer.android.com/reference/kotlin/android/net/http/UploadDataSink#onRewindSucceeded())`()` Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a rewind succeeds. |

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

Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a read fails.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#):Exception passed on to the embedder. This value cannot be`null`. |

### onReadSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onReadSucceeded(finalChunk: Boolean): Unit
```

Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a read succeeds.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `finalChunk` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):For chunked uploads,`true`if this is the final read. It must be`false`for non-chunked uploads. |

### onRewindError

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onRewindError(exception: Exception): Unit
```

Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a rewind fails, or if rewinding uploads is not supported.

| Parameters ||
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| `exception` | [Exception](https://developer.android.com/reference/kotlin/java/lang/Exception.html#):Exception passed on to the embedder. This value cannot be`null`. |

### onRewindSucceeded

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 7](https://developer.android.com/sdkExtensions) 

```
abstract fun onRewindSucceeded(): Unit
```

Called by [UploadDataProvider](https://developer.android.com/reference/kotlin/android/net/http/UploadDataProvider) when a rewind succeeds.
