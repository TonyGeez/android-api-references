# ParcelFileDescriptor.OnCloseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCloseListener

Kotlin| [Java](https://developer.android.com/reference/android/os/ParcelFileDescriptor.OnCloseListener "View this page in Java") 

```
interface OnCloseListener
```

| [android.os.ParcelFileDescriptor.OnCloseListener](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener#) |

Callback indicating that a ParcelFileDescriptor has been closed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClose](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.OnCloseListener#onClose(java.io.IOException))`(`e:` ` [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!`)` Event indicating the ParcelFileDescriptor to which this listener was attached has been closed. |

## Public methods

### onClose

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClose(e: IOException!): Unit
```

Event indicating the ParcelFileDescriptor to which this listener was attached has been closed.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [IOException](https://developer.android.com/reference/kotlin/java/io/IOException.html#)!:error state, or`null`if closed cleanly. If the close event was the result of [ParcelFileDescriptor.detachFd()](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor#detachFd()), this will be a [FileDescriptorDetachedException](https://developer.android.com/reference/kotlin/android/os/ParcelFileDescriptor.FileDescriptorDetachedException). After detach the remote side may continue reading/writing to the underlying [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#), but they can no longer deliver reliable close/error events. |
