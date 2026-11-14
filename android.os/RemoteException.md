# RemoteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteException

Kotlin| [Java](RemoteException.md) 
| --- | --- |

```
open class RemoteException : AndroidException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) ||||
| | ↳ | [java.lang.Exception](../java.lang/Exception.md) |||
| | | ↳ | [android.util.AndroidException](../android.util/AndroidException.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.RemoteException](RemoteException.md) |

| Known Direct Subclasses [DeadObjectException](DeadObjectException.md), [TransactionTooLargeException](TransactionTooLargeException.md) |------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------| | [DeadObjectException](DeadObjectException.md) | The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error. | | [TransactionTooLargeException](TransactionTooLargeException.md) | The Binder transaction failed because it was too large. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DeadSystemException](DeadSystemException.md) |------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [DeadSystemException](DeadSystemException.md) | The core Android system has died and is going through a runtime restart. | |
| --- | --- | --- | --- | --- | --- | --- |

Parent exception for all Binder remote-invocation errors Note: not all exceptions from binder services will be subclasses of this. For instance, RuntimeException and several subclasses of it may be thrown as well as OutOfMemoryException. One common subclass is [DeadObjectException](DeadObjectException.md).

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [RemoteException](RemoteException.md))`()` <br /> |
| [RemoteException](RemoteException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Public methods ||
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [RuntimeException](../java.lang/RuntimeException.md) | [rethrowAsRuntimeException](RemoteException.md))`()` Rethrow this as an unchecked runtime exception. |
| open [RuntimeException](../java.lang/RuntimeException.md) | [rethrowFromSystemServer](RemoteException.md))`()` Rethrow this exception when we know it came from the system server. |

## Public constructors

### RemoteException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RemoteException()
```  

### RemoteException

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
RemoteException(message: String!)
```

## Public methods

### rethrowAsRuntimeException

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rethrowAsRuntimeException(): RuntimeException
```

Rethrow this as an unchecked runtime exception.

Apps making calls into other processes may end up persisting internal state or making security decisions based on the perceived success or failure of a call, or any default values returned. For this reason, we want to strongly throw when there was trouble with the transaction.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [RuntimeException](../java.lang/RuntimeException.md) | This value cannot be`null`. |

| Exceptions ||
|------------------------------|---|
| `java.lang.RuntimeException` | |

### rethrowFromSystemServer

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun rethrowFromSystemServer(): RuntimeException
```

Rethrow this exception when we know it came from the system server. This gives us an opportunity to throw a nice clean`DeadSystemRuntimeException`signal to avoid spamming logs with misleading stack traces.

Apps making calls into the system server may end up persisting internal state or making security decisions based on the perceived success or failure of a call, or any default values returned. For this reason, we want to strongly throw when there was trouble with the transaction.

| Return ||
|-----------------------------------------------------------------------------------------------------|-----------------------------|
| [RuntimeException](../java.lang/RuntimeException.md) | This value cannot be`null`. |

| Exceptions ||
|------------------------------|---|
| `java.lang.RuntimeException` | |
