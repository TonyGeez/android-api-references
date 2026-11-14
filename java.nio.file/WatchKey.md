# WatchKey

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WatchKey

```
interface WatchKey
```

| [java.nio.file.WatchKey](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#) |

A token representing the registration of a [watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable) object with a [WatchService](https://developer.android.com/reference/kotlin/java/nio/file/WatchService).

A watch key is created when a watchable object is registered with a watch service. The key remains [valid](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#isValid())until:

1. It is cancelled, explicitly, by invoking its [cancel](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#cancel())method, or
2. Cancelled implicitly, because the object is no longer accessible, or
3. By java.nio.file.WatchService#close the watch service.

A watch key has a state. When initially created the key is said to be*ready* . When an event is detected then the key is*signalled* and queued so that it can be retrieved by invoking the watch service's [poll](https://developer.android.com/reference/kotlin/java/nio/file/WatchService#poll())or [take](https://developer.android.com/reference/kotlin/java/nio/file/WatchService#take())methods. Once signalled, a key remains in this state until its [reset](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#reset())method is invoked to return the key to the ready state. Events detected while the key is in the signalled state are queued but do not cause the key to be re-queued for retrieval from the watch service. Events are retrieved by invoking the key's [pollEvents](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#pollEvents())method. This method retrieves and removes all events accumulated for the object. When initially created, a watch key has no pending events. Typically events are retrieved when the key is in the signalled state leading to the following idiom: 

```kotlin
for (;;) {
          // retrieve key
          WatchKey key = watcher.take();
 
          // process events
          for (WatchEvent<?> event: key.pollEvents()) {
              :
          }
 
          // reset the key
          boolean valid = key.reset();
          if (!valid) {
              // object no longer registered
          }
      }
  
```

Watch keys are safe for use by multiple concurrent threads. Where there are several threads retrieving signalled keys from a watch service then care should be taken to ensure that the`reset`method is only invoked after the events for the object have been processed. This ensures that one thread is processing the events for an object at any time.

## Summary

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#cancel())`()` Cancels the registration with the watch service. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isValid](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#isValid())`()` Tells whether or not this watch key is valid. |
| abstract [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [WatchEvent](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent)\<\*\>!\>! | [pollEvents](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#pollEvents())`()` Retrieves and removes all pending events for this watch key, returning a`List`of the events that were retrieved. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [reset](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#reset())`()` Resets this watch key. |
| abstract [Watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable)! | [watchable](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#watchable())`()` Returns the object for which this watch key was created. |

## Public methods

### cancel

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(): Unit
```

Cancels the registration with the watch service. Upon return the watch key will be invalid. If the watch key is enqueued, waiting to be retrieved from the watch service, then it will remain in the queue until it is removed. Pending events, if any, remain pending and may be retrieved by invoking the [pollEvents](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#pollEvents())method after the key is cancelled.

If this watch key has already been cancelled then invoking this method has no effect. Once cancelled, a watch key remains forever invalid. 

### isValid

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isValid(): Boolean
```

Tells whether or not this watch key is valid.

A watch key is valid upon creation and remains until it is cancelled, or its watch service is closed.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if, and only if, this watch key is valid |

### pollEvents

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun pollEvents(): MutableList<WatchEvent<*>!>!
```

Retrieves and removes all pending events for this watch key, returning a`List`of the events that were retrieved.

Note that this method does not wait if there are no events pending.

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [WatchEvent](https://developer.android.com/reference/kotlin/java/nio/file/WatchEvent)<*>!>! | the list of the events retrieved; may be empty |

### reset

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun reset(): Boolean
```

Resets this watch key.

If this watch key has been cancelled or this watch key is already in the ready state then invoking this method has no effect. Otherwise if there are pending events for the object then this watch key is immediately re-queued to the watch service. If there are no pending events then the watch key is put into the ready state and will remain in that state until an event is detected or the watch key is cancelled.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the watch key is valid and has been reset, and`false`if the watch key could not be reset because it is no longer [valid](https://developer.android.com/reference/kotlin/java/nio/file/WatchKey#isValid()) |

### watchable

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun watchable(): Watchable!
```

Returns the object for which this watch key was created. This method will continue to return the object even after the key is cancelled.

As the`WatchService`is intended to map directly on to the native file event notification facility (where available) then many of details on how registered objects are watched is highly implementation specific. When watching a directory for changes for example, and the directory is moved or renamed in the file system, there is no guarantee that the watch key will be cancelled and so the object returned by this method may no longer be a valid path to the directory.

| Return ||
|--------------------------------------------------------------------------------------|-------------------------------------------------|
| [Watchable](https://developer.android.com/reference/kotlin/java/nio/file/Watchable)! | the object for which this watch key was created |
