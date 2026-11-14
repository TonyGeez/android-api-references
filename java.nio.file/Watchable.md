Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Watchable

```
interface Watchable
```

| [java.nio.file.Watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable#) |

| Known Direct Subclasses [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) |---|---| | [Path](https://developer.android.com/reference/kotlin/java/nio/file/Path) | An object that may be used to locate a file in a file system. | |

An object that may be registered with a watch service so that it can be *watched* for changes and events.

This interface defines the #register method to register the object with a `https://developer.android.com/reference/kotlin/java/nio/file/WatchService` returning a `https://developer.android.com/reference/kotlin/java/nio/file/WatchKey` to represent the registration. An object may be registered with more than one watch service. Registration with a watch service is cancelled by invoking the key's `https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#cancel()` method.

## Summary

| Public methods ||
|---|---|
| abstract [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey)! | `https://developer.android.com/reference/kotlin/java/nio/file/Watchable#register(java.nio.file.WatchService,%20java.nio.file.WatchEvent.Kind)(watcher: https://developer.android.com/reference/kotlin/java/nio/file/WatchService!, vararg events: https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind<*>!)` Registers an object with a watch service. |
| abstract [WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey)! | `https://developer.android.com/reference/kotlin/java/nio/file/Watchable#register(java.nio.file.WatchService,%20kotlin.Array,%20java.nio.file.WatchEvent.Modifier)(watcher: https://developer.android.com/reference/kotlin/java/nio/file/WatchService!, events: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind<*>!>!, vararg modifiers: https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Modifier!)` Registers an object with a watch service. |

## Public methods

### register

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun register(
    watcher: WatchService!, 
    vararg events: WatchEvent.Kind<*>!
): WatchKey!
```

Registers an object with a watch service.

An invocation of this method behaves in exactly the same way as the invocation

```kotlin
watchable.<code><a docref="java.nio.file.Watchable$register(java.nio.file.WatchService, kotlin.Array((java.nio.file.WatchEvent.Kind((kotlin.Any)))), kotlin.Array((java.nio.file.WatchEvent.Modifier)))">register</a></code>(watcher, events, new WatchEvent.Modifier[0]);
  
```

| Parameters ||
|---|---|
| `watcher` | [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)!: the watch service to which this object is to be registered |
| `events` | [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\<\*\>!: the events for which this object should be registered |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/WatchKey!` | a key representing the registration of this object with the given watch service |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if an invalid of combination of events are specified |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission required to monitor this object. Implementations of this interface should specify the permission checks. |
| `java.lang.UnsupportedOperationException` | if unsupported events are specified |
| `java.nio.file.ClosedWatchServiceException` | if the watch service is closed |

### register

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun register(
    watcher: WatchService!, 
    events: Array<WatchEvent.Kind<*>!>!, 
    vararg modifiers: WatchEvent.Modifier!
): WatchKey!
```

Registers an object with a watch service.

If the file system object identified by this object is currently registered with the watch service then the watch key, representing that registration, is returned after changing the event set or modifiers to those specified by the `events` and `modifiers` parameters. Changing the event set does not cause pending events for the object to be discarded. Objects are automatically registered for the `https://developer.android.com/reference/kotlin/java/nio/file/StandardWatchEventKinds#OVERFLOW:java.nio.file.WatchEvent.Kind` event. This event is not required to be present in the array of events.

Otherwise the file system object has not yet been registered with the given watch service, so it is registered and the resulting new key is returned.

Implementations of this interface should specify the events they support.

| Parameters ||
|---|---|
| `watcher` | [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService)!: the watch service to which this object is to be registered |
| `events` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [WatchEvent.Kind](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Kind)\<\*\>!\>!: the events for which this object should be registered |
| `modifiers` | [WatchEvent.Modifier](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent.Modifier)!: the modifiers, if any, that modify how the object is registered |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/nio/file/WatchKey!` | a key representing the registration of this object with the given watch service |

| Exceptions ||
|---|---|
| `java.io.IOException` | if an I/O error occurs |
| `java.lang.IllegalArgumentException` | if an invalid of combination of events are modifiers are specified |
| `java.lang.SecurityException` | if a security manager is installed and it denies an unspecified permission required to monitor this object. Implementations of this interface should specify the permission checks. |
| `java.lang.UnsupportedOperationException` | if unsupported events or modifiers are specified |
| `java.nio.file.ClosedWatchServiceException` | if the watch service is closed |
