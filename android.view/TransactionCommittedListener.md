# SurfaceControl.TransactionCommittedListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransactionCommittedListener

Kotlin| [Java](../android/view/SurfaceControl.TransactionCommittedListener.md) 
| --- | --- |

```
interface TransactionCommittedListener
```

| [android.view.SurfaceControl.TransactionCommittedListener](../android/view/SurfaceControl.TransactionCommittedListener.md) |

Interface to handle request to [SurfaceControl.Transaction.addTransactionCommittedListener(Executor, TransactionCommittedListener)](../android/view/SurfaceControl.Transaction.md))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransactionCommitted](../android/view/SurfaceControl.TransactionCommittedListener.md))`()` Invoked when the transaction has been committed in SurfaceFlinger. |

## Public methods

### onTransactionCommitted

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransactionCommitted(): Unit
```

Invoked when the transaction has been committed in SurfaceFlinger.
