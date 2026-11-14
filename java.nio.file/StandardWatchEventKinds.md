# StandardWatchEventKinds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardWatchEventKinds

```
class StandardWatchEventKinds
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.StandardWatchEventKinds](StandardWatchEventKinds.md) |

Defines the*standard*event kinds.

## Summary

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [WatchEvent.Kind](../java/nio/file/WatchEvent.Kind.md)\< [Path](Path.md)!\>! | [ENTRY_CREATE](StandardWatchEventKinds.md) Directory entry created. |
| static [WatchEvent.Kind](../java/nio/file/WatchEvent.Kind.md)\< [Path](Path.md)!\>! | [ENTRY_DELETE](StandardWatchEventKinds.md) Directory entry deleted. |
| static [WatchEvent.Kind](../java/nio/file/WatchEvent.Kind.md)\< [Path](Path.md)!\>! | [ENTRY_MODIFY](StandardWatchEventKinds.md) Directory entry modified. |
| --- | --- |
| static [WatchEvent.Kind](../java/nio/file/WatchEvent.Kind.md)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [OVERFLOW](StandardWatchEventKinds.md) A special event to indicate that events may have been lost or discarded. |

## Properties

### ENTRY_CREATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTRY_CREATE: WatchEvent.Kind<Path!>!
```

Directory entry created.

When a directory is registered for this event then the [WatchKey](WatchKey.md) is queued when it is observed that an entry is created in the directory or renamed into the directory. The event [count](WatchEvent.md))for this event is always`1`. 

### ENTRY_DELETE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTRY_DELETE: WatchEvent.Kind<Path!>!
```

Directory entry deleted.

When a directory is registered for this event then the [WatchKey](WatchKey.md) is queued when it is observed that an entry is deleted or renamed out of the directory. The event [count](WatchEvent.md))for this event is always`1`. 

### ENTRY_MODIFY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTRY_MODIFY: WatchEvent.Kind<Path!>!
```

Directory entry modified.

When a directory is registered for this event then the [WatchKey](WatchKey.md) is queued when it is observed that an entry in the directory has been modified. The event [count](WatchEvent.md))for this event is`1`or greater. 

### OVERFLOW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERFLOW: WatchEvent.Kind<Any!>!
```

A special event to indicate that events may have been lost or discarded.

The [context](WatchEvent.md))for this event is implementation specific and may be`null`. The event [count](WatchEvent.md))may be greater than`1`. 
**See Also**

- [java.nio.file.WatchService](WatchService.md)
