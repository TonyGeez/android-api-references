# MessageQueue.OnFileDescriptorEventListener

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFileDescriptorEventListener

Kotlin| [Java](https://developer.android.com/reference/android/os/MessageQueue.OnFileDescriptorEventListener "View this page in Java") 
| --- | --- |

```
interface OnFileDescriptorEventListener
```

| [android.os.MessageQueue.OnFileDescriptorEventListener](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#) |

A listener which is invoked when file descriptor related events occur.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) File descriptor event: Indicates that the file descriptor encountered a fatal error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int) File descriptor event: Indicates that the file descriptor is ready for input operations, such as reading. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int) File descriptor event: Indicates that the file descriptor is ready for output operations, such as writing. |
| --- | --- |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [onFileDescriptorEvents](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#onFileDescriptorEvents(java.io.FileDescriptor,%20kotlin.Int))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `events:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a file descriptor receives events. |

## Constants

### EVENT_ERROR

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_ERROR: Int
```

File descriptor event: Indicates that the file descriptor encountered a fatal error.

File descriptor errors can occur for various reasons. One common error is when the remote peer of a socket or pipe closes its end of the connection.

This event may be generated at any time regardless of whether the [EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) event mask was specified when the listener was added. 

 Value: 4

### EVENT_INPUT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_INPUT: Int
```

File descriptor event: Indicates that the file descriptor is ready for input operations, such as reading.

The listener should read all available data from the file descriptor then return`true`to keep the listener active or`false`to remove the listener.

In the case of a socket, this event may be generated to indicate that there is at least one incoming connection that the listener should accept.

This event will only be generated if the [EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int) event mask was specified when the listener was added. 

 Value: 1

### EVENT_OUTPUT

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val EVENT_OUTPUT: Int
```

File descriptor event: Indicates that the file descriptor is ready for output operations, such as writing.

The listener should write as much data as it needs. If it could not write everything at once, then it should return`true`to keep the listener active. Otherwise, it should return`false`to remove the listener then re-register it later when it needs to write something else.

This event will only be generated if the [EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int) event mask was specified when the listener was added. 

 Value: 2

## Public methods

### onFileDescriptorEvents

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFileDescriptorEvents(
    fd: FileDescriptor, 
    events: Int
): Int
```

Called when a file descriptor receives events.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):The file descriptor. This value cannot be`null`. |
| `events` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of events that occurred: a combination of the [EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int), [EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int), and [EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) event masks. Value is either`0`or a combination of [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int), [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int), and [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The new set of events to watch, or 0 to unregister the listener. Value is either`0`or a combination of [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int), [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int), and [android.os.MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int) |

**See Also**

- [#EVENT_INPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_INPUT:kotlin.Int)
- [#EVENT_OUTPUT](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_OUTPUT:kotlin.Int)
- [#EVENT_ERROR](https://developer.android.com/reference/kotlin/android/os/MessageQueue.OnFileDescriptorEventListener#EVENT_ERROR:kotlin.Int)
