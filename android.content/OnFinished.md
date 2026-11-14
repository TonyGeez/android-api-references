# IntentSender.OnFinished

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnFinished

Kotlin | [Java](../android/content/IntentSender.OnFinished.md) 
| --- | --- |

```
interface OnFinished
```

| [android.content.IntentSender.OnFinished](../android/content/IntentSender.OnFinished.md) |

Callback interface for discovering when a send operation has completed. Primarily for use with a IntentSender that is performing a broadcast, this provides the same information as calling [Context.sendBroadcast()](../android/content/Context.md)) with a final BroadcastReceiver.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSendFinished](../android/content/IntentSender.OnFinished.md))`(`IntentSender:` ` [IntentSender](../android/content/IntentSender.md)!`, `intent:` ` [Intent](../android/content/Intent.md)!`, `resultCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `resultData:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `resultExtras:` ` [Bundle](../android/os/Bundle.md)!`)` Called when a send operation as completed. |

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
| `IntentSender` | [IntentSender](../android/content/IntentSender.md)!: The IntentSender this operation was sent through. |
| `intent` | [Intent](../android/content/Intent.md)!: The original Intent that was sent. |
| `resultCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The final result code determined by the send. |
| --- | --- |
| `resultData` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!: The final data collected by a broadcast. |
| `resultExtras` | [Bundle](../android/os/Bundle.md)!: The final extras collected by a broadcast. |
