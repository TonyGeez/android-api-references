Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# IBinder

```
interface IBinder
```

| [android.os.IBinder](IBinder.md) |

Known Direct Subclasses [Binder](Binder.md) [Binder](Binder.md) Base class for a remotable object, the core part of a lightweight remote procedure call mechanism defined by IBinder.

Base interface for a remotable object, the core part of a lightweight remote procedure call mechanism designed for high performance when performing in-process and cross-process calls. This interface describes the abstract protocol for interacting with a remotable object. Do not implement this interface directly, instead extend from Binder.

The key IBinder API is transact matched by onTransact. These methods allow you to send a call to an IBinder object and receive a call coming in to a Binder object, respectively. This transaction API is synchronous, such that a call to transact does not return until the target has returned from onTransact; this is the expected behavior when calling an object that exists in the local process, and the underlying inter-process communication (IPC) mechanism ensures that these same semantics apply when going across processes.

The data sent through transact() is a Parcel, a generic buffer of data that also maintains some meta-data about its contents. The meta data is used to manage IBinder object references in the buffer, so that those references can be maintained as the buffer moves across processes. This mechanism ensures that when an IBinder is written into a Parcel and sent to another process, if that other process sends a reference to that same IBinder back to the original process, then the original process will receive the same IBinder object back. These semantics allow IBinder/Binder objects to be used as a unique identity (to serve as a token or for other purposes) that can be managed across processes.

The system maintains a pool of transaction threads in each process that it runs in. These threads are used to dispatch all IPCs coming in from other processes. For example, when an IPC is made from process A to process B, the calling thread in A blocks in transact() as it sends the transaction to process B. The next available pool thread in B receives the incoming transaction, calls Binder.onTransact() on the target object, and replies with the result Parcel. Upon receiving its result, the thread in process A returns to allow its execution to continue. In effect, other processes appear to use as additional threads that you did not create executing in your own process.

The Binder system also supports recursion across processes. For example if process A performs a transaction to process B, and process B while handling that transaction calls transact() on an IBinder that is implemented in A, then the thread in A that is currently waiting for the original transaction to finish will take care of calling Binder.onTransact() on the object being called by B. This ensures that the recursion semantics when calling remote binder object are the same as when calling local objects.

When working with remote objects, you often want to find out when they are no longer valid. There are three ways this can be determined:

- The transact method will throw a RemoteException exception if you try to call it on an IBinder whose process no longer exists.
- The pingBinder method can be called, and will return false if the remote process no longer exists.
- The linkToDeath method can be used to register a `https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient` with the IBinder, which will be called when its containing process goes away.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient` Interface for receiving a callback when the process hosting an IBinder has gone away. |
| abstract | `https://developer.android.com/reference/kotlin/android/os/IBinder.FrozenStateChangeCallback` A callback interface for receiving frozen state change events. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#DUMP_TRANSACTION:kotlin.Int` IBinder protocol transaction code: dump internal state. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#FIRST_CALL_TRANSACTION:kotlin.Int` The first transaction code available for user commands. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#FLAG_ONEWAY:kotlin.Int` Flag to transact: this is a one-way call, meaning that the caller returns immediately, without waiting for a result from the callee. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#INTERFACE_TRANSACTION:kotlin.Int` IBinder protocol transaction code: interrogate the recipient side of the transaction for its canonical interface descriptor. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#LAST_CALL_TRANSACTION:kotlin.Int` The last transaction code available for user commands. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#LIKE_TRANSACTION:kotlin.Int` IBinder protocol transaction code: tell an app asynchronously that the caller likes it. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#PING_TRANSACTION:kotlin.Int` IBinder protocol transaction code: pingBinder(). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/IBinder#TWEET_TRANSACTION:kotlin.Int` IBinder protocol transaction code: send a tweet to the target object. |

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | addFrozenStateChangeCallback This method provides a callback mechanism to notify about process frozen/unfrozen events. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dump Print the object's state into the given stream. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | dumpAsync Like dump but always executes asynchronously. |
| --- | --- |
| abstract [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | getInterfaceDescriptor Get the canonical name of the interface supported by this binder. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getSuggestedMaxIpcSizeBytes Limit that should be placed on IPC sizes, in bytes, to keep them safely under the transaction buffer limit. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isBinderAlive Check to see if the process that the binder is in is still alive. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | linkToDeath Register the recipient for a notification if this binder goes away. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | pingBinder Check to see if the object still exists. |
| abstract [IInterface](IInterface.md)? | queryLocalInterface Attempt to retrieve a local implementation of an interface for this Binder object. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | removeFrozenStateChangeCallback Unregister a `https://developer.android.com/reference/kotlin/android/os/IBinder.FrozenStateChangeCallback`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | transact Perform a generic operation with the object. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | unlinkToDeath Remove a previously registered death notification. |
| --- | --- |

## Constants

### DUMP_TRANSACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val DUMP_TRANSACTION: Int
```

IBinder protocol transaction code: dump internal state.

 Value: 1598311760

### FIRST_CALL_TRANSACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FIRST_CALL_TRANSACTION: Int
```

The first transaction code available for user commands.

 Value: 1

### FLAG_ONEWAY

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_ONEWAY: Int
```

Flag to transact: this is a one-way call, meaning that the caller returns immediately, without waiting for a result from the callee. Applies only if the caller and callee are in different processes.

The system provides special ordering semantics for multiple oneway calls being made to the same IBinder object: these calls will be dispatched in the other process one at a time, with the same order as the original calls. These are still dispatched by the IPC thread pool, so may execute on different threads, but the next one will not be dispatched until the previous one completes. This ordering is not guaranteed for calls on different IBinder objects or when mixing oneway and non-oneway calls on the same IBinder object.

 Value: 1

### INTERFACE_TRANSACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INTERFACE_TRANSACTION: Int
```

IBinder protocol transaction code: interrogate the recipient side of the transaction for its canonical interface descriptor.

 Value: 1598968902

### LAST_CALL_TRANSACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LAST_CALL_TRANSACTION: Int
```

The last transaction code available for user commands.

 Value: 16777215

### LIKE_TRANSACTION

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val LIKE_TRANSACTION: Int
```

IBinder protocol transaction code: tell an app asynchronously that the caller likes it. The app is responsible for incrementing and maintaining its own like counter, and may display this value to the user to indicate the quality of the app. This is an optional command that applications do not need to handle, so the default implementation is to do nothing.

There is no response returned and nothing about the system will be functionally affected by it, but it will improve the app's self-esteem.

 Value: 1598835019

### PING_TRANSACTION

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val PING_TRANSACTION: Int
```

IBinder protocol transaction code: pingBinder().

 Value: 1599098439

### TWEET_TRANSACTION

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val TWEET_TRANSACTION: Int
```

IBinder protocol transaction code: send a tweet to the target object. The data in the parcel is intended to be delivered to a shared messaging service associated with the object; it can be anything, as long as it is not more than 130 UTF-8 characters to conservatively fit within common messaging services. As part of `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#HONEYCOMB_MR2:kotlin.Int`, all Binder objects are expected to support this protocol for fully integrated tweeting across the platform. To support older code, the default implementation logs the tweet to the main log as a simple emulation of broadcasting it publicly over the Internet.

Also, upon completing the dispatch, the object must make a cup of tea, return it to the caller, and exclaim "jolly good message old boy!".

 Value: 1599362900

## Public methods

### addFrozenStateChangeCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun addFrozenStateChangeCallback(
    executor: Executor, 
    callback: IBinder.FrozenStateChangeCallback
): Unit
```

This method provides a callback mechanism to notify about process frozen/unfrozen events. Upon registration and any subsequent state changes, the callback is invoked with the latest process frozen state.

If the listener process (the one using this API) is itself frozen, state change events might be combined into a single one with the latest frozen state. This single event would then be delivered when the listener process becomes unfrozen. Similarly, if an event happens before the previous event is consumed, they might be combined. This means the callback might not be called for every single state change, so don't rely on this API to count how many times the state has changed.

The callback is automatically removed when all references to the binder proxy are dropped.

You will only receive state change notifications for remote binders, as local binders by definition can't be frozen without you being frozen too.

| Parameters ||
|---|---|
| `executor` | [Executor](../java.util.concurrent/Executor.md): The executor on which to run the callback. This value cannot be `null`. Callback and listener events are dispatched through this `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#`, providing an easy way to control which thread is used. To dispatch events through the main thread of your application, you can use getMainExecutor. Otherwise, provide an `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#` that dispatches to an appropriate thread. |
| `callback` | [IBinder.FrozenStateChangeCallback](../android/os/IBinder.FrozenStateChangeCallback.md): The callback used to deliver state change notifications. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if the kernel binder driver does not support this feature. |

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun dump(
    fd: FileDescriptor, 
    args: Array<String!>?
): Unit
```

Print the object's state into the given stream.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md): The raw file descriptor that the dump is being sent to. This value cannot be `null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: additional arguments to the dump request. This value may be `null`. |

### dumpAsync

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun dumpAsync(
    fd: FileDescriptor, 
    args: Array<String!>?
): Unit
```

Like dump but always executes asynchronously. If the object is local, a new thread is created to perform the dump.

| Parameters ||
|---|---|
| `fd` | [FileDescriptor](../java.io/FileDescriptor.md): The raw file descriptor that the dump is being sent to. This value cannot be `null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?: additional arguments to the dump request. This value may be `null`. |

### getInterfaceDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun getInterfaceDescriptor(): String?
```

Get the canonical name of the interface supported by this binder.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | This value may be `null`. |

### getSuggestedMaxIpcSizeBytes

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getSuggestedMaxIpcSizeBytes(): Int
```

Limit that should be placed on IPC sizes, in bytes, to keep them safely under the transaction buffer limit.

### isBinderAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun isBinderAlive(): Boolean
```

Check to see if the process that the binder is in is still alive.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | false if the process is not alive. Note that if it returns true, the process may have died while the call is returning. |

### linkToDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun linkToDeath(
    recipient: IBinder.DeathRecipient, 
    flags: Int
): Unit
```

Register the recipient for a notification if this binder goes away. If this binder object unexpectedly goes away (typically because its hosting process has been killed), then the given `https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient`'s android.os.IBinder.DeathRecipient#binderDied method will be called.

This will automatically be unlinked when all references to the linked binder proxy are dropped.

You will only receive death notifications for remote binders, as local binders by definition can't die without you dying as well.

| Parameters ||
|---|---|
| `recipient` | [IBinder.DeathRecipient](../android/os/IBinder.DeathRecipient.md): This value cannot be `null`. |

| Exceptions ||
|---|---|
| `android.os.RemoteException` | if the target IBinder's process has already died. |

**See Also**

- unlinkToDeath

### pingBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun pingBinder(): Boolean
```

Check to see if the object still exists.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns false if the hosting process is gone, otherwise the result (always by default true) returned by the pingBinder() implementation on the other side. |

### queryLocalInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun queryLocalInterface(descriptor: String): IInterface?
```

Attempt to retrieve a local implementation of an interface for this Binder object. If null is returned, you will need to instantiate a proxy class to marshall calls through the transact() method.

| Parameters ||
|---|---|
| `descriptor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): This value cannot be `null`. |

### removeFrozenStateChangeCallback

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeFrozenStateChangeCallback(callback: IBinder.FrozenStateChangeCallback): Boolean
```

Unregister a `https://developer.android.com/reference/kotlin/android/os/IBinder.FrozenStateChangeCallback`. The callback will no longer be invoked when the hosting process changes its frozen state.

| Parameters ||
|---|---|
| `callback` | [IBinder.FrozenStateChangeCallback](../android/os/IBinder.FrozenStateChangeCallback.md): This value cannot be `null`. |

### transact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun transact(
    code: Int, 
    data: Parcel, 
    reply: Parcel?, 
    flags: Int
): Boolean
```

Perform a generic operation with the object.

| Parameters ||
|---|---|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The action to perform. This should be a number between `https://developer.android.com/reference/kotlin/android/os/IBinder#FIRST_CALL_TRANSACTION:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/os/IBinder#LAST_CALL_TRANSACTION:kotlin.Int`. |
| `data` | [Parcel](Parcel.md): Marshalled data to send to the target. Must not be null. If you are not sending any data, you must create an empty Parcel that is given here. |
| `reply` | [Parcel](Parcel.md)?: Marshalled data to be received from the target. May be null if you are not interested in the return value. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional operation flags. Either 0 for a normal RPC, or `https://developer.android.com/reference/kotlin/android/os/IBinder#FLAG_ONEWAY:kotlin.Int` for a one-way RPC. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns the result from onTransact. A successful call generally returns true; false generally means the transaction code was not understood. For a oneway call to a different process false should never be returned. If a oneway call is made to code in the same process (usually to a C++ or Rust implementation), then there are no oneway semantics, and false can still be returned. |

### unlinkToDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun unlinkToDeath(
    recipient: IBinder.DeathRecipient, 
    flags: Int
): Boolean
```

Remove a previously registered death notification. The recipient will no longer be called if this object dies.

| Parameters ||
|---|---|
| `recipient` | [IBinder.DeathRecipient](../android/os/IBinder.DeathRecipient.md): This value cannot be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the recipient is successfully unlinked, assuring you that its android.os.IBinder.DeathRecipient#binderDied method will not be called; `false` if the target IBinder has already died, meaning the method has been (or soon will be) called. |

| Exceptions ||
|---|---|
| `java.util.NoSuchElementException` | if the given recipient has not been registered with the IBinder, and the IBinder is still alive. Note that if the recipient was never registered, but the IBinder has already died, then this exception will *not* be thrown, and you will receive a false return value instead. |
