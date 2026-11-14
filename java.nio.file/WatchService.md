# WatchService

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WatchService

```
interface WatchService : Closeable
```

| [java.nio.file.WatchService](../java/nio/file/WatchService.md) |

A watch service that*watches*registered objects for changes and events. For example a file manager may use a watch service to monitor a directory for changes so that it can update its display of the list of files when files are created or deleted.

A [Watchable](../java/nio/file/Watchable.md) object is registered with a watch service by invoking its java.nio.file.Watchable#register method, returning a [WatchKey](../java/nio/file/WatchKey.md) to represent the registration. When an event for an object is detected the key is*signalled* , and if not currently signalled, it is queued to the watch service so that it can be retrieved by consumers that invoke the [poll](../java/nio/file/WatchService.md))or [take](../java/nio/file/WatchService.md))methods to retrieve keys and process events. Once the events have been processed the consumer invokes the key's [reset](../java/nio/file/WatchKey.md))method to reset the key which allows the key to be signalled and re-queued with further events.

Registration with a watch service is cancelled by invoking the key's [cancel](../java/nio/file/WatchKey.md))method. A key that is queued at the time that it is cancelled remains in the queue until it is retrieved. Depending on the object, a key may be cancelled automatically. For example, suppose a directory is watched and the watch service detects that it has been deleted or its file system is no longer accessible. When a key is cancelled in this manner it is signalled and queued, if not currently signalled. To ensure that the consumer is notified the return value from the`reset`method indicates if the key is valid.

A watch service is safe for use by multiple concurrent consumers. To ensure that only one consumer processes the events for a particular object at any time then care should be taken to ensure that the key's`reset`method is only invoked after its events have been processed. The #close method may be invoked at any time to close the service causing any threads waiting to retrieve keys, to throw`ClosedWatchServiceException`.

File systems may report events faster than they can be retrieved or processed and an implementation may impose an unspecified limit on the number of events that it may accumulate. Where an implementation*knowingly* discards events then it arranges for the key's [pollEvents](../java/nio/file/WatchKey.md))method to return an element with an event type of [OVERFLOW](../java/nio/file/StandardWatchEventKinds.md). This event can be used by the consumer as a trigger to re-examine the state of the object.

When an event is reported to indicate that a file in a watched directory has been modified then there is no guarantee that the program (or programs) that have modified the file have completed. Care should be taken to coordinate access with other programs that may be updating the file. The [FileChannel](../java/nio/channels/FileChannel.md) class defines methods to lock regions of a file against access by other programs.

## Platform dependencies

The implementation that observes events from the file system is intended to map directly on to the native file event notification facility where available, or to use a primitive mechanism, such as polling, when a native facility is not available. Consequently, many of the details on how events are detected, their timeliness, and whether their ordering is preserved are highly implementation specific. For example, when a file in a watched directory is modified then it may result in a single [ENTRY_MODIFY](../java/nio/file/StandardWatchEventKinds.md) event in some implementations but several events in other implementations. Short-lived files (meaning files that are deleted very quickly after they are created) may not be detected by primitive implementations that periodically poll the file system to detect changes.

If a watched file is not located on a local storage device then it is implementation specific if changes to the file can be detected. In particular, it is not required that changes to files carried out on remote systems be detected.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [close](../java/nio/file/WatchService.md))`()` Closes this watch service. |
| abstract [WatchKey](../java/nio/file/WatchKey.md)! | [poll](../java/nio/file/WatchService.md))`()` Retrieves and removes the next watch key, or`null`if none are present. |
| abstract [WatchKey](../java/nio/file/WatchKey.md)! | [poll](../java/nio/file/WatchService.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Retrieves and removes the next watch key, waiting if necessary up to the specified wait time if none are yet present. |
| --- | --- |
| abstract [WatchKey](../java/nio/file/WatchKey.md)! | [take](../java/nio/file/WatchService.md))`()` Retrieves and removes next watch key, waiting if none are yet present. |

## Public methods

### close

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun close(): Unit
```

Closes this watch service.

If a thread is currently blocked in the [take](../java/nio/file/WatchService.md))or [poll](../java/nio/file/WatchService.md))methods waiting for a key to be queued then it immediately receives a [ClosedWatchServiceException](../java/nio/file/ClosedWatchServiceException.md). Any valid keys associated with this watch service are [invalidated](../java/nio/file/WatchKey.md)).

After a watch service is closed, any further attempt to invoke operations upon it will throw [ClosedWatchServiceException](../java/nio/file/ClosedWatchServiceException.md). If this watch service is already closed then invoking this method has no effect.

| Exceptions ||
|-----------------------|-----------------------------------|
| `java.lang.Exception` | if this resource cannot be closed |
| `java.io.IOException` | if an I/O error occurs |

### poll

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(): WatchKey!
```

Retrieves and removes the next watch key, or`null`if none are present.

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [WatchKey](../java/nio/file/WatchKey.md)! | the next watch key, or`null` |

| Exceptions ||
|---------------------------------------------|---------------------------------|
| `java.nio.file.ClosedWatchServiceException` | if this watch service is closed |

### poll

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun poll(
    timeout: Long, 
    unit: TimeUnit!
): WatchKey!
```

Retrieves and removes the next watch key, waiting if necessary up to the specified wait time if none are yet present.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):how to wait before giving up, in units of unit |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:a`TimeUnit`determining how to interpret the timeout parameter |

| Return ||
|------------------------------------------------------------------------------------|------------------------------|
| [WatchKey](../java/nio/file/WatchKey.md)! | the next watch key, or`null` |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------|
| `java.nio.file.ClosedWatchServiceException` | if this watch service is closed, or it is closed while waiting for the next key |
| `java.lang.InterruptedException` | if interrupted while waiting |

### take

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun take(): WatchKey!
```

Retrieves and removes next watch key, waiting if none are yet present.

| Return ||
|------------------------------------------------------------------------------------|--------------------|
| [WatchKey](../java/nio/file/WatchKey.md)! | the next watch key |

| Exceptions ||
|---------------------------------------------|---------------------------------------------------------------------------------|
| `java.nio.file.ClosedWatchServiceException` | if this watch service is closed, or it is closed while waiting for the next key |
| `java.lang.InterruptedException` | if interrupted while waiting |
