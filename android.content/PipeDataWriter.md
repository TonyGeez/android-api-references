# ContentProvider.PipeDataWriter

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# PipeDataWriter

Kotlin| [Java](../android/content/ContentProvider.PipeDataWriter.md) 
| --- | --- |

```
interface PipeDataWriter<T : Any!>
```

| [android.content.ContentProvider.PipeDataWriter](../android/content/ContentProvider.PipeDataWriter.md) |

Interface to write a stream of data to a pipe. Use with [ContentProvider.openPipeHelper](../android/content/ContentProvider.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeDataToPipe](../android/content/ContentProvider.PipeDataWriter.md))`(`output:` ` [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md)`, `uri:` ` [Uri](../android/net/Uri.md)`, `mimeType:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `opts:` ` [Bundle](../android/os/Bundle.md)?`, `args:` `T?`)` Called from a background thread to stream data out to a pipe. |

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
| `output` | [ParcelFileDescriptor](../android/os/ParcelFileDescriptor.md):The pipe where data should be written. This will be closed for you upon returning from this function. This value cannot be`null`. |
| `uri` | [Uri](../android/net/Uri.md):The URI whose data is to be written. This value cannot be`null`. |
| `mimeType` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The desired type of data to be written. This value cannot be`null`. |
| --- | --- |
| `opts` | [Bundle](../android/os/Bundle.md)?:Options supplied by caller. This value may be`null`. |
| `args` | T?:Your own custom arguments. This value may be`null`. |
