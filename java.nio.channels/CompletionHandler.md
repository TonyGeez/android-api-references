# CompletionHandler

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CompletionHandler

```
interface CompletionHandler<V : Any!, A : Any!>
```

| [java.nio.channels.CompletionHandler](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler#) |

A handler for consuming the result of an asynchronous I/O operation.

The asynchronous channels defined in this package allow a completion handler to be specified to consume the result of an asynchronous operation. The [completed](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler#completed(java.nio.channels.CompletionHandler.V,%20java.nio.channels.CompletionHandler.A))method is invoked when the I/O operation completes successfully. The [failed](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler#failed(kotlin.Throwable,%20java.nio.channels.CompletionHandler.A))method is invoked if the I/O operations fails. The implementations of these methods should complete in a timely manner so as to avoid keeping the invoking thread from dispatching to other completion handlers.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [completed](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler#completed(java.nio.channels.CompletionHandler.V,%20java.nio.channels.CompletionHandler.A))`(`result:` `V`, `attachment:` `A`)` Invoked when an operation has completed. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [failed](https://developer.android.com/reference/kotlin/java/nio/channels/CompletionHandler#failed(kotlin.Throwable,%20java.nio.channels.CompletionHandler.A))`(`exc:` ` [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!`, `attachment:` `A`)` Invoked when an operation fails. |

## Public methods

### completed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun completed(
    result: V, 
    attachment: A
): Unit
```

Invoked when an operation has completed.

| Parameters ||
|--------------|-------------------------------------------------------------------|
| `result` | V:The result of the I/O operation. |
| `attachment` | A:The object attached to the I/O operation when it was initiated. |

### failed

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun failed(
    exc: Throwable!, 
    attachment: A
): Unit
```

Invoked when an operation fails.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `exc` | [Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html)!:The exception to indicate why the I/O operation failed |
| `attachment` | A:The object attached to the I/O operation when it was initiated. |
