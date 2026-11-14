Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IkeSession

```
class IkeSession : AutoCloseable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.net.ipsec.ike.IkeSession](IkeSession.md) |

This class represents an IKE Session management object that allows for keying and management of `https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#`s.

An IKE/Child Session represents an IKE/Child SA as well as its rekeyed successors. A Child Session is bounded by the lifecycle of the IKE Session under which it is set up. Closing an IKE Session implicitly closes any remaining Child Sessions under it.

An IKE procedure is one or multiple IKE message exchanges that are used to create, delete or rekey an IKE Session or Child Session.

This class provides methods for initiating IKE procedures, such as the Creation and Deletion of a Child Session, or the Deletion of the IKE session. All procedures (except for IKE deletion) will be initiated sequentially after IKE Session is set up.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#IkeSession(android.content.Context,%20android.net.ipsec.ike.IkeSessionParams,%20android.net.ipsec.ike.ChildSessionParams,%20java.util.concurrent.Executor,%20android.net.ipsec.ike.IkeSessionCallback,%20android.net.ipsec.ike.ChildSessionCallback)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, ikeSessionParams: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams, firstChildSessionParams: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams, userCbExecutor: https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#, ikeSessionCallback: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback, firstChildSessionCallback: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback)` Constructs a new IKE session. |

| Public methods ||
|---|---|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#close()()` Close the IKE session gracefully. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#closeChildSession(android.net.ipsec.ike.ChildSessionCallback)(childSessionCallback: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback)` Delete a Child Session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#dump(java.io.PrintWriter)(pw: https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)` Dumps the state of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#` information for the clients |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#finalize()()` Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#kill()()` Terminate (forcibly close) the IKE session. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#openChildSession(android.net.ipsec.ike.ChildSessionParams,%20android.net.ipsec.ike.ChildSessionCallback)(childSessionParams: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams, childSessionCallback: https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback)` Request a new Child Session. |
| --- | --- |

## Public constructors

### IkeSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
IkeSession(
    context: Context, 
    ikeSessionParams: IkeSessionParams, 
    firstChildSessionParams: ChildSessionParams, 
    userCbExecutor: Executor, 
    ikeSessionCallback: IkeSessionCallback, 
    firstChildSessionCallback: ChildSessionCallback)
```

Constructs a new IKE session.

This method will immediately return an instance of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#` and asynchronously initiate the setup procedure of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#` as well as its first Child Session. Callers will be notified of these two setup results via the callback arguments.

FEATURE_IPSEC_TUNNELS is required for setting up a tunnel mode Child SA.

| Parameters ||
|---|---|
| `context` | [Context](../android.content/Context.md): a valid `https://developer.android.com/reference/kotlin/android/content/Context.html#` instance. This value cannot be `null`. |
| `ikeSessionParams` | [IkeSessionParams](IkeSessionParams.md): the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionParams` that contains a set of valid `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#` configurations. This value cannot be `null`. |
| `firstChildSessionParams` | [ChildSessionParams](ChildSessionParams.md): the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams` that contains a set of valid configurations for the first Child Session. This value cannot be `null`. |
| --- | --- |
| `userCbExecutor` | [Executor](../java.util.concurrent/Executor.md): the `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` upon which all callbacks will be posted. For security and consistency, the callbacks posted to this executor MUST be executed serially and in the order they were posted, as guaranteed by executors such as `https://developer.android.com/reference/kotlin/java/util/concurrent/Executors.html#newSingleThreadExecutor()` This value cannot be `null`. |
| `ikeSessionCallback` | [IkeSessionCallback](IkeSessionCallback.md): the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback` interface to notify callers of state changes within the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#`. This value cannot be `null`. |
| `firstChildSessionCallback` | [ChildSessionCallback](ChildSessionCallback.md): the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback` interface to notify callers of state changes within the first Child Session. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| | an instance of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#`. |

## Public methods

### close

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun close(): Unit
```

Close the IKE session gracefully.

Implements `https://developer.android.com/reference/kotlin/java/lang/AutoCloseable.html#close()`

Upon closure, `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onClosed()` or `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onClosedWithException(android.net.ipsec.ike.exceptions.IkeException)` will be fired.

Closing an IKE Session implicitly closes any remaining Child Sessions negotiated under it. Users SHOULD stop all outbound traffic that uses these Child Sessions (`https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#` pairs) before calling this method. Otherwise IPsec packets will be dropped due to the lack of a valid `https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#`.

Closure of an IKE session will take priority over, and cancel other procedures waiting in the queue (but will wait for ongoing locally initiated procedures to complete). After sending the Delete request, the IKE library will wait until a Delete response is received or retransmission timeout occurs.

| Exceptions ||
|---|---|
| `java.lang.Exception` | if this resource cannot be closed |

### closeChildSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun closeChildSession(childSessionCallback: ChildSessionCallback): Unit
```

Delete a Child Session.

Upon closure, `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onClosed()` will be fired.

| Parameters ||
|---|---|
| `childSessionCallback` | [ChildSessionCallback](ChildSessionCallback.md): The `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback` instance that uniquely identify the Child Session. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if no Child Session found bound with this callback. |

### dump

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun dump(pw: PrintWriter): Unit
```

Dumps the state of `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#` information for the clients

| Parameters ||
|---|---|
| `pw` | [PrintWriter](../java.io/PrintWriter.md): Print writer. This value cannot be `null`. |

### finalize

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun finalize(): Unit
```

Called by the garbage collector on an object when garbage collection determines that there are no more references to the object. A subclass overrides the `finalize` method to dispose of system resources or to perform other cleanup.

The general contract of `finalize` is that it is invoked if and when the Java virtual machine has determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, except as a result of an action taken by the finalization of some other object or class which is ready to be finalized. The `finalize` method may take any action, including making this object available again to other threads; the usual purpose of `finalize`, however, is to perform cleanup actions before the object is irrevocably discarded. For example, the finalize method for an object that represents an input/output connection might perform explicit I/O transactions to break the connection before the object is permanently discarded.

The `finalize` method of class `Object` performs no special action; it simply returns normally. Subclasses of `Object` may override this definition.

The Java programming language does not guarantee which thread will invoke the `finalize` method for any given object. It is guaranteed, however, that the thread that invokes finalize will not be holding any user-visible synchronization locks when finalize is invoked. If an uncaught exception is thrown by the finalize method, the exception is ignored and finalization of that object terminates.

After the `finalize` method has been invoked for an object, no further action is taken until the Java virtual machine has again determined that there is no longer any means by which this object can be accessed by any thread that has not yet died, including possible actions by other objects or classes which are ready to be finalized, at which point the object may be discarded.

The `finalize` method is never invoked more than once by a Java virtual machine for any given object.

Any exception thrown by the `finalize` method causes the finalization of this object to be halted, but is otherwise ignored.

| Exceptions ||
|---|---|
| `java.lang.Throwable` | the `Exception` raised by this method |

### kill

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun kill(): Unit
```

Terminate (forcibly close) the IKE session.

Upon closing, `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSessionCallback#onClosed()` will be fired.

Closing an IKE Session implicitly closes any remaining Child Sessions negotiated under it. Users SHOULD stop all outbound traffic that uses these Child Sessions (`https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#` pairs) before calling this method. Otherwise IPsec packets will be dropped due to the lack of a valid `https://developer.android.com/reference/kotlin/android/net/IpSecTransform.html#`.

Forcible closure of an IKE session will take priority over, and cancel other procedures waiting in the queue. It will also interrupt any ongoing locally initiated procedure.

### openChildSession

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun openChildSession(
    childSessionParams: ChildSessionParams, 
    childSessionCallback: ChildSessionCallback
): Unit
```

Request a new Child Session.

Users MUST provide a unique `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback` instance for each new Child Session.

Upon setup, `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback#onOpened(android.net.ipsec.ike.ChildSessionConfiguration)` will be fired.

FEATURE_IPSEC_TUNNELS is required for setting up a tunnel mode Child SA.

| Parameters ||
|---|---|
| `childSessionParams` | [ChildSessionParams](ChildSessionParams.md): the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionParams` that contains the Child Session configurations to negotiate. This value cannot be `null`. |
| `childSessionCallback` | [ChildSessionCallback](ChildSessionCallback.md): the `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/ChildSessionCallback` interface to notify users the state changes of the Child Session. It will be posted to the callback `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` of this `https://developer.android.com/reference/kotlin/android/net/ipsec/ike/IkeSession#`. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the ChildSessionCallback is already in use. |
