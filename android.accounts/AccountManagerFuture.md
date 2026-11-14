# AccountManagerFuture

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AccountManagerFuture

Kotlin| [Java](../android/accounts/AccountManagerFuture.md) 
| --- | --- |

```
interface AccountManagerFuture<V : Any!>
```

| [android.accounts.AccountManagerFuture](../android/accounts/AccountManagerFuture.md) |

A AccountManagerFuture represents the result of an asynchronous [AccountManager](../android/accounts/AccountManager.md) call. Methods are provided to check if the computation is complete, to wait for its completion, and to retrieve the result of the computation. The result can only be retrieved using method get when the computation has completed, blocking if necessary until it is ready. Cancellation is performed by the cancel method. Additional methods are provided to determine if the task completed normally or was cancelled. Once a computation has completed, the computation cannot be cancelled. If you would like to use a Future for the sake of cancellability but not provide a usable result, you can declare types of the form Future\<?\> and return null as a result of the underlying task.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [cancel](../android/accounts/AccountManagerFuture.md))`(`mayInterruptIfRunning:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Attempts to cancel execution of this task. |
| abstractV | [getResult](../android/accounts/AccountManagerFuture.md))`()` Accessor for the future result the [AccountManagerFuture](../android/accounts/AccountManagerFuture.md) represents. |
| abstractV | [getResult](../android/accounts/AccountManagerFuture.md))`(`timeout:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `unit:` ` [TimeUnit](../java/util/concurrent/TimeUnit.md)!`)` Accessor for the future result the [AccountManagerFuture](../android/accounts/AccountManagerFuture.md) represents. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isCancelled](../android/accounts/AccountManagerFuture.md))`()` Returns true if this task was cancelled before it completed normally. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isDone](../android/accounts/AccountManagerFuture.md))`()` Returns true if this task completed. |

## Public methods

### cancel

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun cancel(mayInterruptIfRunning: Boolean): Boolean
```

Attempts to cancel execution of this task. This attempt will fail if the task has already completed, has already been cancelled, or could not be cancelled for some other reason. If successful, and this task has not started when cancel is called, this task should never run. If the task has already started, then the mayInterruptIfRunning parameter determines whether the thread executing this task should be interrupted in an attempt to stop the task.

After this method returns, subsequent calls to [isDone](../android/accounts/AccountManagerFuture.md))will always return true. Subsequent calls to [isCancelled](../android/accounts/AccountManagerFuture.md))will always return true if this method returned true.

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

Accessor for the future result the [AccountManagerFuture](../android/accounts/AccountManagerFuture.md) represents. This call will block until the result is available. In order to check if the result is available without blocking, one may call [isDone()](../android/accounts/AccountManagerFuture.md))and [isCancelled()](../android/accounts/AccountManagerFuture.md)). If the request that generated this result fails or is canceled then an exception will be thrown rather than the call returning normally.

| Return ||
|---|-------------------|
| V | the actual result |

| Exceptions ||
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.accounts.OperationCanceledException` | if the request was canceled for any reason (including if it is forbidden by policy to modify an account (of that type)) |
| `android.accounts.AuthenticatorException` | if there was an error communicating with the authenticator or if the authenticator returned an invalid response |
| `java.io.IOException` | if the authenticator returned an error response that indicates that it encountered an IOException while communicating with the authentication server |
| --- | --- |

### getResult

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getResult(
    timeout: Long, 
    unit: TimeUnit!
): V
```

Accessor for the future result the [AccountManagerFuture](../android/accounts/AccountManagerFuture.md) represents. This call will block until the result is available. In order to check if the result is available without blocking, one may call [isDone()](../android/accounts/AccountManagerFuture.md))and [isCancelled()](../android/accounts/AccountManagerFuture.md)). If the request that generated this result fails or is canceled then an exception will be thrown rather than the call returning normally. If a timeout is specified then the request will automatically be canceled if it does not complete in that amount of time.

| Parameters ||
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `timeout` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the maximum time to wait |
| `unit` | [TimeUnit](../java/util/concurrent/TimeUnit.md)!:the time unit of the timeout argument. This must not be null. |

| Return ||
|---|-------------------|
| V | the actual result |

| Exceptions ||
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| `android.accounts.OperationCanceledException` | if the request was canceled for any reason |
| `android.accounts.AuthenticatorException` | if there was an error communicating with the authenticator or if the authenticator returned an invalid response |
| `java.io.IOException` | if the authenticator returned an error response that indicates that it encountered an IOException while communicating with the authentication server |
| --- | --- |

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
