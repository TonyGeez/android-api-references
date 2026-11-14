# IntentSender.OnFinished

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFinished

Kotlin | [Java](https://developer.android.com/reference/android/content/IntentSender.OnFinished "View this page in Java") 

```
interface OnFinished
```

| [android.content.IntentSender.OnFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished#) |

Callback interface for discovering when a send operation has completed. Primarily for use with a IntentSender that is performing a broadcast, this provides the same information as calling [Context.sendBroadcast()](https://developer.android.com/reference/kotlin/android/content/Context#sendOrderedBroadcast(android.content.Intent,%20kotlin.String,%20android.content.BroadcastReceiver,%20android.os.Handler,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle)) with a final BroadcastReceiver.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSendFinished](https://developer.android.com/reference/kotlin/android/content/IntentSender.OnFinished#onSendFinished(android.content.IntentSender,%20android.content.Intent,%20kotlin.Int,%20kotlin.String,%20android.os.Bundle))`(`IntentSender:` ` [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)!`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultExtras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called when a send operation as completed. |

## Public methods

### onSendFinished

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onSendFinished(
    IntentSender: IntentSender!, 
    intent: Intent!, 
    resultCode: Int, 
    resultData: String!, 
    resultExtras: Bundle!
): Unit
```

Called when a send operation as completed.

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `IntentSender` | [IntentSender](https://developer.android.com/reference/kotlin/android/content/IntentSender)!: The IntentSender this operation was sent through. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent)!: The original Intent that was sent. |
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The final result code determined by the send. |
| `resultData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The final data collected by a broadcast. |
| `resultExtras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: The final extras collected by a broadcast. |
