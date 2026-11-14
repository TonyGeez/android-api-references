# AccountManagerFuture

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccountManagerFuture

Kotlin| [Java](https://developer.android.com/reference/android/accounts/AccountManagerFuture "View this page in Java") 

```
interface AccountManagerFuture<V : Any!>
```

| [android.accounts.AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#) |

A AccountManagerFuture represents the result of an asynchronous [AccountManager](https://developer.android.com/reference/kotlin/android/accounts/AccountManager) call. Methods are provided to check if the computation is complete, to wait for its completion, and to retrieve the result of the computation. The result can only be retrieved using method get when the computation has completed, blocking if necessary until it is ready. Cancellation is performed by the cancel method. Additional methods are provided to determine if the task completed normally or was cancelled. Once a computation has completed, the computation cannot be cancelled. If you would like to use a Future for the sake of cancellability but not provide a usable result, you can declare types of the form Future\<?\> and return null as a result of the underlying task.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#cancel(kotlin.Boolean))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to cancel execution of this task. |
| abstractV | [getResult](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult())`()` Accessor for the future result the [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#) represents. |
| abstractV | [getResult](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#getResult(kotlin.Long,%20java.util.concurrent.TimeUnit))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!`)` Accessor for the future result the [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#) represents. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isCancelled())`()` Returns true if this task was cancelled before it completed normally. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isDone())`()` Returns true if this task completed. |

## Public methods

### cancel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

Attempts to cancel execution of this task. This attempt will fail if the task has already completed, has already been cancelled, or could not be cancelled for some other reason. If successful, and this task has not started when cancel is called, this task should never run. If the task has already started, then the mayInterruptIfRunning parameter determines whether the thread executing this task should be interrupted in an attempt to stop the task.

After this method returns, subsequent calls to [isDone](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isDone())will always return true. Subsequent calls to [isCancelled](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isCancelled())will always return true if this method returned true.

| Parameters ||
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `mayInterruptIfRunning` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):true if the thread executing this task should be interrupted; otherwise, in-progress tasks are allowed to complete |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | false if the task could not be cancelled, typically because it has already completed normally; true otherwise |

### getResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResult(): V
```

Accessor for the future result the [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#) represents. This call will block until the result is available. In order to check if the result is available without blocking, one may call [isDone()](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isDone())and [isCancelled()](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isCancelled()). If the request that generated this result fails or is canceled then an exception will be thrown rather than the call returning normally.

| Return ||
|---|-------------------|
| V | the actual result |

| Exceptions ||
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.accounts.OperationCanceledException` | if the request was canceled for any reason (including if it is forbidden by policy to modify an account (of that type)) |
| `android.accounts.AuthenticatorException` | if there was an error communicating with the authenticator or if the authenticator returned an invalid response |
| `java.io.IOException` | if the authenticator returned an error response that indicates that it encountered an IOException while communicating with the authentication server |

### getResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResult(
    timeout: Long, 
    unit: TimeUnit!
): V
```

Accessor for the future result the [AccountManagerFuture](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#) represents. This call will block until the result is available. In order to check if the result is available without blocking, one may call [isDone()](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isDone())and [isCancelled()](https://developer.android.com/reference/kotlin/android/accounts/AccountManagerFuture#isCancelled()). If the request that generated this result fails or is canceled then an exception will be thrown rather than the call returning normally. If a timeout is specified then the request will automatically be canceled if it does not complete in that amount of time.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](https://developer.android.com/reference/kotlin/java/util/concurrent/TimeUnit.html#)!:the time unit of the timeout argument. This must not be null. |

| Return ||
|---|-------------------|
| V | the actual result |

| Exceptions ||
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.accounts.OperationCanceledException` | if the request was canceled for any reason |
| `android.accounts.AuthenticatorException` | if there was an error communicating with the authenticator or if the authenticator returned an invalid response |
| `java.io.IOException` | if the authenticator returned an error response that indicates that it encountered an IOException while communicating with the authentication server |

### isCancelled

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isCancelled(): Boolean
```

Returns true if this task was cancelled before it completed normally.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this task was cancelled before it completed |

### isDone

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isDone(): Boolean
```

Returns true if this task completed. Completion may be due to normal termination, an exception, or cancellation -- in all of these cases, this method will return true.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | true if this task completed |
