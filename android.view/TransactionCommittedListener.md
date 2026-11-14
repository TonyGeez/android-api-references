# SurfaceControl.TransactionCommittedListener

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransactionCommittedListener

Kotlin| [Java](https://developer.android.com/reference/android/view/SurfaceControl.TransactionCommittedListener "View this page in Java") 

```
interface TransactionCommittedListener
```

| [android.view.SurfaceControl.TransactionCommittedListener](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.TransactionCommittedListener#) |

Interface to handle request to [SurfaceControl.Transaction.addTransactionCommittedListener(Executor, TransactionCommittedListener)](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.Transaction#addTransactionCommittedListener(java.util.concurrent.Executor,%20android.view.SurfaceControl.TransactionCommittedListener))

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTransactionCommitted](https://developer.android.com/reference/kotlin/android/view/SurfaceControl.TransactionCommittedListener#onTransactionCommitted())`()` Invoked when the transaction has been committed in SurfaceFlinger. |

## Public methods

### onTransactionCommitted

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTransactionCommitted(): Unit
```

Invoked when the transaction has been committed in SurfaceFlinger.
