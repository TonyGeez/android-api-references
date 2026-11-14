# CancellationSignal.OnCancelListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCancelListener

Kotlin| [Java](https://developer.android.com/reference/android/os/CancellationSignal.OnCancelListener "View this page in Java") 
| --- | --- |

```
interface OnCancelListener
```

| [android.os.CancellationSignal.OnCancelListener](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.OnCancelListener#) |

Listens for cancellation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancel](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.OnCancelListener#onCancel())`()` Called when [CancellationSignal.cancel](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#cancel())is invoked. |

## Public methods

### onCancel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCancel(): Unit
```

Called when [CancellationSignal.cancel](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#cancel())is invoked.
