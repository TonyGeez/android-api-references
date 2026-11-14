# PendingIntent.OnFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFinished

Kotlin| [Java](../android/app/PendingIntent.OnFinished.md) 
| --- | --- |

```
interface OnFinished
```

| [android.app.PendingIntent.OnFinished](../android/app/PendingIntent.OnFinished.md) |

Callback interface for discovering when a send operation has completed. Primarily for use with a PendingIntent that is performing a broadcast, this provides the same information as calling [Context.sendBroadcast()](../android.content/Context.md))with a final BroadcastReceiver.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSendFinished](../android/app/PendingIntent.OnFinished.md))`(`pendingIntent:` ` [PendingIntent](PendingIntent.md)!`, `intent:` ` [Intent](../android.content/Intent.md)!`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultExtras:` ` [Bundle](../android.os/Bundle.md)!`)` Called when a send operation as completed. |

## Public methods

### onSendFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSendFinished(
    pendingIntent: PendingIntent!, 
    intent: Intent!, 
    resultCode: Int, 
    resultData: String!, 
    resultExtras: Bundle!
): Unit
```

Called when a send operation as completed.

| Parameters ||
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `pendingIntent` | [PendingIntent](PendingIntent.md)!:The PendingIntent this operation was sent through. |
| `intent` | [Intent](../android.content/Intent.md)!:The original Intent that was sent. |
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The final result code determined by the send. |
| --- | --- |
| `resultData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The final data collected by a broadcast. |
| `resultExtras` | [Bundle](../android.os/Bundle.md)!:The final extras collected by a broadcast. |
