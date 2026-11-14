Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OutcomeReceiver

Kotlin | [Java](OutcomeReceiver.md)
| --- | --- |

```
interface OutcomeReceiver<R : Any!, E : Throwable!>
```

| [android.os.OutcomeReceiver](OutcomeReceiver.md) |

Callback interface intended for use when an asynchronous operation may result in a failure. This interface may be used in cases where an asynchronous API may complete either with a value or with a `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#` that indicates an error.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver#onError(android.os.OutcomeReceiver.E)(error: E)` Called when the asynchronous operation fails. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/OutcomeReceiver#onResult(android.os.OutcomeReceiver.R)(result: R)` Called when the asynchronous operation succeeds and delivers a result value. |

## Public methods

### onError

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onError(error: E): Unit
```

Called when the asynchronous operation fails. The mode of failure is indicated by the `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#` passed as an argument to this method.

| Parameters ||
|---|---|
| `error` | E: A subclass of `https://developer.android.com/reference/kotlin/java/lang/Throwable.html#` with more details about the error that occurred. This value cannot be `null`. |

### onResult

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onResult(result: R): Unit
```

Called when the asynchronous operation succeeds and delivers a result value.

| Parameters ||
|---|---|
| `result` | R: The value delivered by the asynchronous operation. |
