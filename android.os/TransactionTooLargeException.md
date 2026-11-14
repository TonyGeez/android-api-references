# TransactionTooLargeException

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TransactionTooLargeException

Kotlin| [Java](../android/os/TransactionTooLargeException.md) 
| --- | --- |

```
open class TransactionTooLargeException : RemoteException
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||||
| --- | --- | --- | --- | --- | --- |
| ↳ | [kotlin.Throwable](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-throwable/index.html) |||||
| | ↳ | [java.lang.Exception](../java/lang/Exception.md) ||||
| | | ↳ | [android.util.AndroidException](../android/util/AndroidException.md) |||
| --- | --- | --- | --- | --- | --- |
| | | | ↳ | [android.os.RemoteException](../android/os/RemoteException.md) ||
| | | | | ↳ | [android.os.TransactionTooLargeException](../android/os/TransactionTooLargeException.md) |

The Binder transaction failed because it was too large.

During a remote procedure call, the arguments and the return value of the call are transferred as [Parcel](../android/os/Parcel.md) objects stored in the Binder transaction buffer. If the arguments or the return value are too large to fit in the transaction buffer, then the call will fail. [TransactionTooLargeException](../android/os/TransactionTooLargeException.md) is thrown as a heuristic when a transaction is large, and it fails, since these are the transactions which are most likely to overfill the transaction buffer.

The Binder transaction buffer has a limited fixed size, currently 1MB, which is shared by all transactions in progress for the process. Consequently this exception can be thrown when there are many transactions in progress even when most of the individual transactions are of moderate size.

There are two possible outcomes when a remote procedure call throws [TransactionTooLargeException](../android/os/TransactionTooLargeException.md). Either the client was unable to send its request to the service (most likely if the arguments were too large to fit in the transaction buffer), or the service was unable to send its response back to the client (most likely if the return value was too large to fit in the transaction buffer). It is not possible to tell which of these outcomes actually occurred. The client should assume that a partial failure occurred.

The key to avoiding [TransactionTooLargeException](../android/os/TransactionTooLargeException.md) is to keep all transactions relatively small. Try to minimize the amount of memory needed to create a [Parcel](../android/os/Parcel.md) for the arguments and the return value of the remote procedure call. Avoid transferring huge arrays of strings or large bitmaps. If possible, try to break up big requests into smaller pieces.

If you are implementing a service, it may help to impose size or complexity constraints on the queries that clients can perform. For example, if the result set could become large, then don't allow the client to request more than a few records at a time. Alternately, instead of returning all of the available data all at once, return the essential information first and make the client ask for additional information later as needed.

## Summary

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TransactionTooLargeException](../android/os/TransactionTooLargeException.md))`()` <br /> |
| [TransactionTooLargeException](../android/os/TransactionTooLargeException.md))`(`msg:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [RemoteException](../android/os/RemoteException.md) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RuntimeException](../java/lang/RuntimeException.md) | [rethrowAsRuntimeException](../android/os/RemoteException.md))`()` <br /> Rethrow this as an unchecked runtime exception. Apps making calls into other processes may end up persisting internal state or making security decisions based on the perceived success or failure of a call, or any default values returned. For this reason, we want to strongly throw when there was trouble with the transaction. <br /> | | [RuntimeException](../java/lang/RuntimeException.md) | [rethrowFromSystemServer](../android/os/RemoteException.md))`()` <br /> Rethrow this exception when we know it came from the system server. This gives us an opportunity to throw a nice clean`DeadSystemRuntimeException`signal to avoid spamming logs with misleading stack traces. Apps making calls into the system server may end up persisting internal state or making security decisions based on the perceived success or failure of a call, or any default values returned. For this reason, we want to strongly throw when there was trouble with the transaction. <br /> | ||

## Public constructors

### TransactionTooLargeException

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransactionTooLargeException()
```  

### TransactionTooLargeException

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TransactionTooLargeException(msg: String!)
```
