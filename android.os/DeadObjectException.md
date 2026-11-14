# DeadObjectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DeadObjectException

Kotlin| [Java](../android/os/DeadObjectException.md) 
| --- | --- |

```
open class DeadObjectException : RemoteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [android.util.AndroidException](../android/util/AndroidException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.RemoteException](../android/os/RemoteException.md) ||
| | | | | ↳ | [android.os.DeadObjectException](../android/os/DeadObjectException.md) |

| Known Direct Subclasses [DeadSystemException](../android/os/DeadSystemException.md) |------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [DeadSystemException](../android/os/DeadSystemException.md) | The core Android system has died and is going through a runtime restart. | |
| --- | --- | --- | --- | --- | --- | --- |

The object you are calling has died, because its hosting process no longer exists, or there has been a low-level binder error. If you get this exception from a system service, the error is usually nonrecoverable as the framework will restart. If you receive this error from an app, at a minimum, you should recover by resetting the connection. For instance, you should drop the binder, clean up associated state, and reset your connection to the service which threw this error. In order to simplify your error recovery paths, you may also want to "simply" restart your process. However, this may not be an option if the service you are talking to is unreliable or crashes frequently. If this isn't from a service death and is instead from a low-level binder error, it will be from:

- a one-way call queue filling up (too many one-way calls)
- from the binder buffer being filled up, so that the transaction is rejected.

In these cases, more information about the error will be logged. However, there isn't a good way to differentiate this information at runtime. So, you should handle the error, as if the service died.

<br />

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DeadObjectException](../android/os/DeadObjectException.md))`()` <br /> |
| [DeadObjectException](../android/os/DeadObjectException.md))`(`message:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [RemoteException](../android/os/RemoteException.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RuntimeException](../java/lang/RuntimeException.md) | [rethrowAsRuntimeException](../android/os/RemoteException.md))`()` <br /> Rethrow this as an unchecked runtime exception. Apps making calls into other processes may end up persisting internal state or making security decisions based on the perceived success or failure of a call, or any default values returned. For this reason, we want to strongly throw when there was trouble with the transaction. <br /> | | [RuntimeException](../java/lang/RuntimeException.md) | [rethrowFromSystemServer](../android/os/RemoteException.md))`()` <br /> Rethrow this exception when we know it came from the system server. This gives us an opportunity to throw a nice clean`DeadSystemRuntimeException`signal to avoid spamming logs with misleading stack traces. Apps making calls into the system server may end up persisting internal state or making security decisions based on the perceived success or failure of a call, or any default values returned. For this reason, we want to strongly throw when there was trouble with the transaction. <br /> | ||

## Public constructors

### DeadObjectException

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeadObjectException()
```  

### DeadObjectException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
DeadObjectException(message: String!)
```
