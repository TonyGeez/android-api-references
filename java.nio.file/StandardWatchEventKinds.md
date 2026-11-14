# StandardWatchEventKinds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# StandardWatchEventKinds

```
class StandardWatchEventKinds
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [java.nio.file.StandardWatchEventKinds](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#) |

Defines the*standard*event kinds.

## Summary

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!\>! | [ENTRY_CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_CREATE:java.nio.file.WatchEvent.Kind) Directory entry created. |
| static [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!\>! | [ENTRY_DELETE](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_DELETE:java.nio.file.WatchEvent.Kind) Directory entry deleted. |
| static [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\< [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path)!\>! | [ENTRY_MODIFY](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_MODIFY:java.nio.file.WatchEvent.Kind) Directory entry modified. |
| --- | --- |
| static [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\< [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!\>! | [OVERFLOW](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#OVERFLOW:java.nio.file.WatchEvent.Kind) A special event to indicate that events may have been lost or discarded. |

## Properties

### ENTRY_CREATE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTRY_CREATE: WatchEvent.Kind<Path!>!
```

Directory entry created.

When a directory is registered for this event then the [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey) is queued when it is observed that an entry is created in the directory or renamed into the directory. The event [count](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#count())for this event is always`1`. 

### ENTRY_DELETE

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTRY_DELETE: WatchEvent.Kind<Path!>!
```

Directory entry deleted.

When a directory is registered for this event then the [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey) is queued when it is observed that an entry is deleted or renamed out of the directory. The event [count](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#count())for this event is always`1`. 

### ENTRY_MODIFY

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ENTRY_MODIFY: WatchEvent.Kind<Path!>!
```

Directory entry modified.

When a directory is registered for this event then the [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey) is queued when it is observed that an entry in the directory has been modified. The event [count](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#count())for this event is`1`or greater. 

### OVERFLOW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val OVERFLOW: WatchEvent.Kind<Any!>!
```

A special event to indicate that events may have been lost or discarded.

The [context](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#context())for this event is implementation specific and may be`null`. The event [count](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#count())may be greater than`1`. 
**See Also**

- [java.nio.file.WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)
