# PendingIntent.OnFinished

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFinished

Kotlin| [Java](https://developer.android.com/reference/android/app/PendingIntent.OnFinished "View this page in Java") 

```
interface OnFinished
```

| [android.app.PendingIntent.OnFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished#) |

Callback interface for discovering when a send operation has completed. Primarily for use with a PendingIntent that is performing a broadcast, this provides the same information as calling [Context.sendBroadcast()](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle))with a final BroadcastReceiver.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSendFinished](https://developer.android.com/reference/kotlin/android/app/PendingIntent.OnFinished#onSendFinished(android.app.PendingIntent,%20android.content.Intent,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle))`(`pendingIntent:` ` [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultExtras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called when a send operation as completed. |

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
| `pendingIntent` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent)!:The PendingIntent this operation was sent through. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The original Intent that was sent. |
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The final result code determined by the send. |
| `resultData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The final data collected by a broadcast. |
| `resultExtras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The final extras collected by a broadcast. |
