# MessageQueue.IdleHandler

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IdleHandler

Kotlin| [Java](../android/os/MessageQueue.IdleHandler.md) 
| --- | --- |

```
interface IdleHandler
```

| [android.os.MessageQueue.IdleHandler](../android/os/MessageQueue.IdleHandler.md) |

Callback interface for discovering when a thread is going to block waiting for more messages.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [queueIdle](../android/os/MessageQueue.IdleHandler.md))`()` Called when the message queue has run out of messages and will now wait for more. |

## Public methods

### queueIdle

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun queueIdle(): Boolean
```

Called when the message queue has run out of messages and will now wait for more. Return true to keep your idle handler active, false to have it removed. This may be called if there are still messages pending in the queue, but they are all scheduled to be dispatched after the current time.
