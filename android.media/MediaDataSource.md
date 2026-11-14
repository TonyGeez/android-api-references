# MediaDataSource

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaDataSource

Kotlin| [Java](https://developer.android.com/reference/android/media/MediaDataSource "View this page in Java") 

```
abstract class MediaDataSource : Closeable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.media.MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource#) |

For supplying media data to the framework. Implement this if your app has special requirements for the way media data is obtained.

Methods of this interface may be called on multiple different threads. There will be a thread synchronization point between each call to ensure that modifications to the state of your MediaDataSource are visible to future calls. This means you don't need to do your own synchronization unless you're modifying the MediaDataSource from another thread while it's being used by the framework.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------|---|
| [MediaDataSource](https://developer.android.com/reference/kotlin/android/media/MediaDataSource#MediaDataSource())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/media/MediaDataSource#getSize())`()` Called to get the size of the data source. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [readAt](https://developer.android.com/reference/kotlin/android/media/MediaDataSource#readAt(kotlin.Long,%20kotlin.ByteArray,%20kotlin.Int,%20kotlin.Int))`(`position:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `buffer:` ` [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!`, `offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `size:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called to request data from the given position. |

| Inherited functions ||
|---|---|
| From class [Closeable](https://developer.android.com/reference/kotlin/java/io/Closeable.html#) |------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](https://developer.android.com/reference/kotlin/java/io/Closeable.html#close())`()` <br /> Closes this stream and releases any system resources associated with it. If the stream is already closed then invoking this method has no effect. As noted in [AutoCloseable.close()](https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#close()), cases where the close may fail require careful attention. It is strongly advised to relinquish the underlying resources and to internally*mark* the`Closeable`as closed, prior to throwing the`IOException`. <br /> | ||

## Public constructors

### MediaDataSource

```
MediaDataSource()
```

## Public methods

### getSize

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getSize(): Long
```

Called to get the size of the data source.

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | the size of data source in bytes, or -1 if the size is unknown. |

| Exceptions ||
|-----------------------|-----------------|
| `java.io.IOException` | on fatal errors |

### readAt

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun readAt(
    position: Long, 
    buffer: ByteArray!, 
    offset: Int, 
    size: Int
): Int
```

Called to request data from the given position. Implementations should fill`buffer`with up to`size`bytes of data, and return the number of valid bytes in the buffer. Return`0`if size is zero (thus no bytes are read). Return`-1`to indicate that end of stream is reached.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------|
| `position` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the position in the data source to read from. |
| `buffer` | [ByteArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-byte-array/index.html)!:the buffer to read the data into. |
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset within buffer to read the data into. |
| `size` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the number of bytes to read. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of bytes read, or -1 if end of stream is reached. |

| Exceptions ||
|-----------------------|------------------|
| `java.io.IOException` | on fatal errors. |
