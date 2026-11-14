# FileObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FileObserver

Kotlin| [Java](FileObserver.md) 
| --- | --- |

```
abstract class FileObserver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.FileObserver](FileObserver.md) |

Monitors files (using [inotify](http://en.wikipedia.org/wiki/Inotify)) to fire an event after files are accessed or changed by any process on the device (including this one). FileObserver is an abstract class; subclasses must implement the event handler [onEvent(int,java.lang.String)](FileObserver.md)).

Each FileObserver instance can monitor multiple files or directories. If a directory is monitored, events will be triggered for all files and subdirectories inside the monitored directory.

An event mask is used to specify which changes or actions to report. Event type constants are used to describe the possible changes in the event mask as well as what actually happened in event callbacks.

**Warning**: If a FileObserver is garbage collected, it will stop sending events. To ensure you keep receiving events, you must keep a reference to the FileObserver instance from some other live object.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ACCESS](FileObserver.md) Event type: Data was read from a file |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALL_EVENTS](FileObserver.md) Event mask: All valid event types, combined Value is either`0`or a combination of [android.os.FileObserver#ACCESS](FileObserver.md), [android.os.FileObserver#MODIFY](FileObserver.md), [android.os.FileObserver#ATTRIB](FileObserver.md), [android.os.FileObserver#CLOSE_WRITE](FileObserver.md), [android.os.FileObserver#CLOSE_NOWRITE](FileObserver.md), [android.os.FileObserver#OPEN](FileObserver.md), [android.os.FileObserver#MOVED_FROM](FileObserver.md), [android.os.FileObserver#MOVED_TO](FileObserver.md), [android.os.FileObserver#CREATE](FileObserver.md), [android.os.FileObserver#DELETE](FileObserver.md), [android.os.FileObserver#DELETE_SELF](FileObserver.md), and [android.os.FileObserver#MOVE_SELF](FileObserver.md) |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ATTRIB](FileObserver.md) Event type: Metadata (permissions, owner, timestamp) was changed explicitly |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_NOWRITE](FileObserver.md) Event type: Someone had a file or directory open read-only, and closed it |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CLOSE_WRITE](FileObserver.md) Event type: Someone had a file or directory open for writing, and closed it |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CREATE](FileObserver.md) Event type: A new file or subdirectory was created under the monitored directory |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DELETE](FileObserver.md) Event type: A file was deleted from the monitored directory |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DELETE_SELF](FileObserver.md) Event type: The monitored file or directory was deleted; monitoring effectively stops |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODIFY](FileObserver.md) Event type: Data was written to a file |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MOVED_FROM](FileObserver.md) Event type: A file or subdirectory was moved from the monitored directory |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MOVED_TO](FileObserver.md) Event type: A file or subdirectory was moved to the monitored directory |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MOVE_SELF](FileObserver.md) Event type: The monitored file or directory was moved; monitoring continues |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [OPEN](FileObserver.md) Event type: A file or directory was opened |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FileObserver](FileObserver.md))`(`file:` ` [File](../java.io/File.md)`)` Equivalent to FileObserver(file, FileObserver.ALL_EVENTS). |
| [FileObserver](FileObserver.md))`(`file:` ` [File](../java.io/File.md)`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new file observer for a certain file or directory. |
| [FileObserver](FileObserver.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Equivalent to FileObserver(path, FileObserver.ALL_EVENTS). |
| [FileObserver](FileObserver.md))`(`path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new file observer for a certain file or directory. |
| [FileObserver](FileObserver.md))`(`files:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [File](../java.io/File.md)!>`)` Equivalent to FileObserver(paths, FileObserver.ALL_EVENTS). |
| [FileObserver](FileObserver.md))`(`files:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [File](../java.io/File.md)!>`, `mask:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Version of [FileObserver(java.io.File,int)](FileObserver.md))that allows callers to monitor multiple files or directories. |

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEvent](FileObserver.md))`(`event:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `path:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` The event handler, which must be implemented by subclasses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startWatching](FileObserver.md))`()` Start watching for events. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopWatching](FileObserver.md))`()` Stop watching for events. |
| --- | --- |

| Protected methods ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](FileObserver.md))`()` <br /> |

## Constants

### ACCESS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACCESS: Int
```

Event type: Data was read from a file 

 Value: 1

### ALL_EVENTS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALL_EVENTS: Int
```

Event mask: All valid event types, combined 
Value is either`0`or a combination of [android.os.FileObserver#ACCESS](FileObserver.md), [android.os.FileObserver#MODIFY](FileObserver.md), [android.os.FileObserver#ATTRIB](FileObserver.md), [android.os.FileObserver#CLOSE_WRITE](FileObserver.md), [android.os.FileObserver#CLOSE_NOWRITE](FileObserver.md), [android.os.FileObserver#OPEN](FileObserver.md), [android.os.FileObserver#MOVED_FROM](FileObserver.md), [android.os.FileObserver#MOVED_TO](FileObserver.md), [android.os.FileObserver#CREATE](FileObserver.md), [android.os.FileObserver#DELETE](FileObserver.md), [android.os.FileObserver#DELETE_SELF](FileObserver.md), and [android.os.FileObserver#MOVE_SELF](FileObserver.md) 

 Value: 4095

### ATTRIB

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ATTRIB: Int
```

Event type: Metadata (permissions, owner, timestamp) was changed explicitly 

 Value: 4

### CLOSE_NOWRITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLOSE_NOWRITE: Int
```

Event type: Someone had a file or directory open read-only, and closed it 

 Value: 16

### CLOSE_WRITE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CLOSE_WRITE: Int
```

Event type: Someone had a file or directory open for writing, and closed it 

 Value: 8

### CREATE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATE: Int
```

Event type: A new file or subdirectory was created under the monitored directory 

 Value: 256

### DELETE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELETE: Int
```

Event type: A file was deleted from the monitored directory 

 Value: 512

### DELETE_SELF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DELETE_SELF: Int
```

Event type: The monitored file or directory was deleted; monitoring effectively stops 

 Value: 1024

### MODIFY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODIFY: Int
```

Event type: Data was written to a file 

 Value: 2

### MOVED_FROM

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MOVED_FROM: Int
```

Event type: A file or subdirectory was moved from the monitored directory 

 Value: 64

### MOVED_TO

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MOVED_TO: Int
```

Event type: A file or subdirectory was moved to the monitored directory 

 Value: 128

### MOVE_SELF

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MOVE_SELF: Int
```

Event type: The monitored file or directory was moved; monitoring continues 

 Value: 2048

### OPEN

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OPEN: Int
```

Event type: A file or directory was opened 

 Value: 32

## Public constructors

### FileObserver

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileObserver(file: File)
```

Equivalent to FileObserver(file, FileObserver.ALL_EVENTS).

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------|
| `file` | [File](../java.io/File.md):This value cannot be`null`. |

### FileObserver

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileObserver(
    file: File, 
    mask: Int)
```

Create a new file observer for a certain file or directory. Monitoring does not start on creation! You must call [startWatching()](FileObserver.md))before you will receive events.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `file` | [File](../java.io/File.md):The file or directory to monitor This value cannot be`null`. |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event or events (added together) to watch for Value is either`0`or a combination of [android.os.FileObserver#ACCESS](FileObserver.md), [android.os.FileObserver#MODIFY](FileObserver.md), [android.os.FileObserver#ATTRIB](FileObserver.md), [android.os.FileObserver#CLOSE_WRITE](FileObserver.md), [android.os.FileObserver#CLOSE_NOWRITE](FileObserver.md), [android.os.FileObserver#OPEN](FileObserver.md), [android.os.FileObserver#MOVED_FROM](FileObserver.md), [android.os.FileObserver#MOVED_TO](FileObserver.md), [android.os.FileObserver#CREATE](FileObserver.md), [android.os.FileObserver#DELETE](FileObserver.md), [android.os.FileObserver#DELETE_SELF](FileObserver.md), and [android.os.FileObserver#MOVE_SELF](FileObserver.md) |

### FileObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileObserver(path: String!)
```

**Deprecated:** *use [FileObserver(java.io.File)](FileObserver.md))instead.*

Equivalent to FileObserver(path, FileObserver.ALL_EVENTS). 

### FileObserver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileObserver(
    path: String!, 
    mask: Int)
```

**Deprecated:** *use [FileObserver(java.io.File,int)](FileObserver.md))instead.*

Create a new file observer for a certain file or directory. Monitoring does not start on creation! You must call [startWatching()](FileObserver.md))before you will receive events.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The file or directory to monitor |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event or events (added together) to watch for Value is either`0`or a combination of [android.os.FileObserver#ACCESS](FileObserver.md), [android.os.FileObserver#MODIFY](FileObserver.md), [android.os.FileObserver#ATTRIB](FileObserver.md), [android.os.FileObserver#CLOSE_WRITE](FileObserver.md), [android.os.FileObserver#CLOSE_NOWRITE](FileObserver.md), [android.os.FileObserver#OPEN](FileObserver.md), [android.os.FileObserver#MOVED_FROM](FileObserver.md), [android.os.FileObserver#MOVED_TO](FileObserver.md), [android.os.FileObserver#CREATE](FileObserver.md), [android.os.FileObserver#DELETE](FileObserver.md), [android.os.FileObserver#DELETE_SELF](FileObserver.md), and [android.os.FileObserver#MOVE_SELF](FileObserver.md) |

### FileObserver

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileObserver(files: MutableList<File!>)
```

Equivalent to FileObserver(paths, FileObserver.ALL_EVENTS).

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `files` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [File](../java.io/File.md)!\>:The files or directories to monitor This value cannot be`null`. |

### FileObserver

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
FileObserver(
    files: MutableList<File!>, 
    mask: Int)
```

Version of [FileObserver(java.io.File,int)](FileObserver.md))that allows callers to monitor multiple files or directories.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `files` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [File](../java.io/File.md)!\>:The files or directories to monitor This value cannot be`null`. |
| `mask` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The event or events (added together) to watch for Value is either`0`or a combination of [android.os.FileObserver#ACCESS](FileObserver.md), [android.os.FileObserver#MODIFY](FileObserver.md), [android.os.FileObserver#ATTRIB](FileObserver.md), [android.os.FileObserver#CLOSE_WRITE](FileObserver.md), [android.os.FileObserver#CLOSE_NOWRITE](FileObserver.md), [android.os.FileObserver#OPEN](FileObserver.md), [android.os.FileObserver#MOVED_FROM](FileObserver.md), [android.os.FileObserver#MOVED_TO](FileObserver.md), [android.os.FileObserver#CREATE](FileObserver.md), [android.os.FileObserver#DELETE](FileObserver.md), [android.os.FileObserver#DELETE_SELF](FileObserver.md), and [android.os.FileObserver#MOVE_SELF](FileObserver.md) |

## Public methods

### onEvent

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEvent(
    event: Int, 
    path: String?
): Unit
```

The event handler, which must be implemented by subclasses.

This method is invoked on a special FileObserver thread. It runs independently of any threads, so take care to use appropriate synchronization! Consider using [Handler.post(Runnable)](Handler.md))to shift event handling work to the main thread to avoid concurrency problems.

Event handlers must not throw exceptions.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `event` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The type of event which happened |
| `path` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:The path, relative to the main monitored file or directory, of the file or directory which triggered the event. This value can be`null`for certain events, such as [MOVE_SELF](FileObserver.md). |

### startWatching

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startWatching(): Unit
```

Start watching for events. The monitored file or directory must exist at this time, or else no events will be reported (even if it appears later). If monitoring is already started, this call has no effect. 

### stopWatching

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopWatching(): Unit
```

Stop watching for events. Some events may be in process, so events may continue to be reported even after this method completes. If monitoring is already stopped, this call has no effect.

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|-------------------------------------|
| `java.lang.Throwable` | the`Exception`raised by this method |
