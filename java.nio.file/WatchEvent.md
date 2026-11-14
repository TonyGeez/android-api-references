# WatchEvent

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WatchEvent

```
interface WatchEvent<T : Any!>
```

| [java.nio.file.WatchEvent](WatchEvent.md) |

An event or a repeated event for an object that is registered with a [WatchService](WatchService.md).

An event is classified by its [kind](WatchEvent.md))and has a [count](WatchEvent.md))to indicate the number of times that the event has been observed. This allows for efficient representation of repeated events. The [context](WatchEvent.md))method returns any context associated with the event. In the case of a repeated event then the context is the same for all events.

Watch events are immutable and safe for use by multiple concurrent threads.

## Summary

| Nested classes ||
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [Kind](../java/nio/file/WatchEvent.Kind.md) An event kind, for the purposes of identification. |
| abstract | [Modifier](../java/nio/file/WatchEvent.Modifier.md) An event modifier that qualifies how a [Watchable](Watchable.md) is registered with a [WatchService](WatchService.md). |

| Public methods ||
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| abstractT | [context](WatchEvent.md))`()` Returns the context for the event. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [count](WatchEvent.md))`()` Returns the event count. |
| abstract [WatchEvent.Kind](../java/nio/file/WatchEvent.Kind.md)\<T\>! | [kind](WatchEvent.md))`()` Returns the event kind. |
| --- | --- |

## Public methods

### context

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun context(): T
```

Returns the context for the event.

In the case of [ENTRY_CREATE](StandardWatchEventKinds.md), [ENTRY_DELETE](StandardWatchEventKinds.md), and [ENTRY_MODIFY](StandardWatchEventKinds.md) events the context is a`Path`that is the [relative](Path.md))path between the directory registered with the watch service, and the entry that is created, deleted, or modified.

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
| [WatchEvent.Kind](../java/nio/file/WatchEvent.Kind.md)<T>! | the event kind |
