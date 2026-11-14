# CancellationSignal.OnCancelListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnCancelListener

Kotlin| [Java](../android/os/CancellationSignal.OnCancelListener.md) 
| --- | --- |

```
interface OnCancelListener
```

| [android.os.CancellationSignal.OnCancelListener](../android/os/CancellationSignal.OnCancelListener.md) |

Listens for cancellation.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancel](../android/os/CancellationSignal.OnCancelListener.md))`()` Called when [CancellationSignal.cancel](CancellationSignal.md))is invoked. |

## Public methods

### onCancel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCancel(): Unit
```

Called when [CancellationSignal.cancel](CancellationSignal.md))is invoked.
