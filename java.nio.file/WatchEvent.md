# WatchEvent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WatchEvent

```
interface WatchEvent<T : Any!>
```

| [java.nio.file.WatchEvent](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#) |

An event or a repeated event for an object that is registered with a [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService).

An event is classified by its [kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#kind())and has a [count](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#count())to indicate the number of times that the event has been observed. This allows for efficient representation of repeated events. The [context](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#context())method returns any context associated with the event. In the case of a repeated event then the context is the same for all events.

Watch events are immutable and safe for use by multiple concurrent threads.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind) An event kind, for the purposes of identification. |
| abstract | [Modifier](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Modifier) An event modifier that qualifies how a [Watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable) is registered with a [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| abstractT | [context](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#context())`()` Returns the context for the event. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#count())`()` Returns the event count. |
| abstract [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\<T\>! | [kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent#kind())`()` Returns the event kind. |
| --- | --- |

## Public methods

### context

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun context(): T
```

Returns the context for the event.

In the case of [ENTRY_CREATE](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_CREATE:java.nio.file.WatchEvent.Kind), [ENTRY_DELETE](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_DELETE:java.nio.file.WatchEvent.Kind), and [ENTRY_MODIFY](https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#ENTRY_MODIFY:java.nio.file.WatchEvent.Kind) events the context is a`Path`that is the [relative](https://developer.android.com/reference/kotlin/java/nio/file/Path#relativize(java.nio.file.Path))path between the directory registered with the watch service, and the entry that is created, deleted, or modified.

| Return ||
|---|---------------------------------|
| T | the event context; may be`null` |

### count

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun count(): Int
```

Returns the event count. If the event count is greater than`1`then this is a repeated event.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the event count |

### kind

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun kind(): WatchEvent.Kind<T>!
```

Returns the event kind.

| Return ||
|-----------------------------------------------------------------------------------------------------|----------------|
| [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)<T>! | the event kind |
