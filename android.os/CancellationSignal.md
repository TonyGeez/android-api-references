# CancellationSignal

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CancellationSignal

Kotlin| [Java](https://developer.android.com/reference/android/os/CancellationSignal "View this page in Java") 

```
class CancellationSignal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#) |

Provides the ability to cancel an operation in progress.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnCancelListener](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.OnCancelListener) Listens for cancellation. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#CancellationSignal())`()` Creates a cancellation signal, initially not canceled. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#cancel())`()` Cancels the operation and signals the cancellation listener. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCanceled](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#isCanceled())`()` Returns true if the operation has been canceled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#setOnCancelListener(android.os.CancellationSignal.OnCancelListener))`(`listener:` ` [CancellationSignal.OnCancelListener](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.OnCancelListener)!`)` Sets the cancellation listener to be called when canceled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [throwIfCanceled](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#throwIfCanceled())`()` Throws [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException) if the operation has been canceled. |

## Public constructors

### CancellationSignal

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
CancellationSignal()
```

Creates a cancellation signal, initially not canceled.

## Public methods

### cancel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun cancel(): Unit
```

Cancels the operation and signals the cancellation listener. If the operation has not yet started, then it will be canceled as soon as it does. 

### isCanceled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isCanceled(): Boolean
```

Returns true if the operation has been canceled.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the operation has been canceled. |

### setOnCancelListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOnCancelListener(listener: CancellationSignal.OnCancelListener!): Unit
```

Sets the cancellation listener to be called when canceled. This method is intended to be used by the recipient of a cancellation signal such as a database or a content provider to handle cancellation requests while performing a long-running operation. This method is not intended to be used by applications themselves. If [CancellationSignal.cancel](https://developer.android.com/reference/kotlin/android/os/CancellationSignal#cancel())has already been called, then the provided listener is invoked immediately. This method is guaranteed that the listener will not be called after it has been removed.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [CancellationSignal.OnCancelListener](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.OnCancelListener)!:The cancellation listener, or null to remove the current listener. |

### throwIfCanceled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun throwIfCanceled(): Unit
```

Throws [OperationCanceledException](https://developer.android.com/reference/kotlin/android/os/OperationCanceledException) if the operation has been canceled.

| Exceptions ||
|-----------------------------------------|-------------------------------------|
| `android.os.OperationCanceledException` | if the operation has been canceled. |
