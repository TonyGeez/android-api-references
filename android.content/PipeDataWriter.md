# ContentProvider.PipeDataWriter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PipeDataWriter

Kotlin| [Java](https://developer.android.com/reference/android/content/ContentProvider.PipeDataWriter "View this page in Java") 
| --- | --- |

```
interface PipeDataWriter<T : Any!>
```

| [android.content.ContentProvider.PipeDataWriter](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter#) |

Interface to write a stream of data to a pipe. Use with [ContentProvider.openPipeHelper](https://developer.android.com/reference/kotlin/android/content/ContentProvider#openPipeHelper(android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.openPipeHelper.T,%20android.content.ContentProvider.PipeDataWriter)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeDataToPipe](https://developer.android.com/reference/kotlin/android/content/ContentProvider.PipeDataWriter#writeDataToPipe(android.os.ParcelFileDescriptor,%20android.net.Uri,%20kotlin.String,%20android.os.Bundle,%20android.content.ContentProvider.PipeDataWriter.T))`(`output:` ` [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#)`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`, `args:` `T?`)` Called from a background thread to stream data out to a pipe. |

## Public methods

### writeDataToPipe

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun writeDataToPipe(
    output: ParcelFileDescriptor, 
    uri: Uri, 
    mimeType: String, 
    opts: Bundle?, 
    args: T?
): Unit
```

Called from a background thread to stream data out to a pipe. Note that the pipe is blocking, so this thread can block on writes for an arbitrary amount of time if the client is slow at reading.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `output` | [ParcelFileDescriptor](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.html#):The pipe where data should be written. This will be closed for you upon returning from this function. This value cannot be`null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):The URI whose data is to be written. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The desired type of data to be written. This value cannot be`null`. |
| --- | --- |
| `opts` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:Options supplied by caller. This value may be`null`. |
| `args` | T?:Your own custom arguments. This value may be`null`. |
