# CancellationSignal

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CancellationSignal

Kotlin| [Java](../android/os/CancellationSignal.md) 
| --- | --- |

```
class CancellationSignal
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.os.CancellationSignal](../android/os/CancellationSignal.md) |

Provides the ability to cancel an operation in progress.

## Summary

| Nested classes ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| abstract | [OnCancelListener](../android/os/CancellationSignal.OnCancelListener.md) Listens for cancellation. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [CancellationSignal](../android/os/CancellationSignal.md))`()` Creates a cancellation signal, initially not canceled. |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [cancel](../android/os/CancellationSignal.md))`()` Cancels the operation and signals the cancellation listener. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCanceled](../android/os/CancellationSignal.md))`()` Returns true if the operation has been canceled. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOnCancelListener](../android/os/CancellationSignal.md))`(`listener:` ` [CancellationSignal.OnCancelListener](../android/os/CancellationSignal.OnCancelListener.md)!`)` Sets the cancellation listener to be called when canceled. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [throwIfCanceled](../android/os/CancellationSignal.md))`()` Throws [OperationCanceledException](../android/os/OperationCanceledException.md) if the operation has been canceled. |

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

Sets the cancellation listener to be called when canceled. This method is intended to be used by the recipient of a cancellation signal such as a database or a content provider to handle cancellation requests while performing a long-running operation. This method is not intended to be used by applications themselves. If [CancellationSignal.cancel](../android/os/CancellationSignal.md))has already been called, then the provided listener is invoked immediately. This method is guaranteed that the listener will not be called after it has been removed.

| Parameters ||
|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `listener` | [CancellationSignal.OnCancelListener](../android/os/CancellationSignal.OnCancelListener.md)!:The cancellation listener, or null to remove the current listener. |

### throwIfCanceled

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun throwIfCanceled(): Unit
```

Throws [OperationCanceledException](../android/os/OperationCanceledException.md) if the operation has been canceled.

| Exceptions ||
|-----------------------------------------|-------------------------------------|
| `android.os.OperationCanceledException` | if the operation has been canceled. |
