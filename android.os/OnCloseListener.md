# ParcelFileDescriptor.OnCloseListener

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCloseListener

Kotlin| [Java](../android/os/ParcelFileDescriptor.OnCloseListener.md) 
| --- | --- |

```
interface OnCloseListener
```

| [android.os.ParcelFileDescriptor.OnCloseListener](../android/os/ParcelFileDescriptor.OnCloseListener.md) |

Callback indicating that a ParcelFileDescriptor has been closed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onClose](../android/os/ParcelFileDescriptor.OnCloseListener.md))`(`e:` ` [IOException](../java.io/IOException.md)!`)` Event indicating the ParcelFileDescriptor to which this listener was attached has been closed. |

## Public methods

### onClose

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onClose(e: IOException!): Unit
```

Event indicating the ParcelFileDescriptor to which this listener was attached has been closed.

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [IOException](../java.io/IOException.md)!:error state, or`null`if closed cleanly. If the close event was the result of [ParcelFileDescriptor.detachFd()](ParcelFileDescriptor.md)), this will be a [FileDescriptorDetachedException](../android/os/ParcelFileDescriptor.FileDescriptorDetachedException.md). After detach the remote side may continue reading/writing to the underlying [FileDescriptor](../java.io/FileDescriptor.md), but they can no longer deliver reliable close/error events. |
