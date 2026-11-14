# Binder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Binder

Kotlin| [Java](https://developer.android.com/reference/android/os/Binder "View this page in Java") 

```
open class Binder : IBinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.Binder](https://developer.android.com/reference/kotlin/android/os/Binder#) |

Base class for a remotable object, the core part of a lightweight remote procedure call mechanism defined by [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder). This class is an implementation of IBinder that provides standard local implementation of such an object.

Most developers will not implement this class directly, instead using the [aidl](https://developer.android.com/guide/components/aidl.html) tool to describe the desired interface, having it generate the appropriate Binder subclass. You can, however, derive directly from Binder to implement your own custom RPC protocol or simply instantiate a raw Binder object directly to use as a token that can be shared across processes.

This class is just a basic IPC primitive; it has no impact on an application's lifecycle, and is valid only as long as the process that created it continues to run. To use this correctly, you must be doing so within the context of a top-level application component (a [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#), [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#), or [android.content.ContentProvider](https://developer.android.com/reference/kotlin/android/content/ContentProvider.html#)) that lets the system know your process should remain running.

You must keep in mind the situations in which your process could go away, and thus require that you later re-create a new Binder and re-attach it when the process starts again. For example, if you are using this within an [android.app.Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#), your activity's process may be killed any time the activity is not started; if the activity is later re-created you will need to create a new Binder and hand it back to the correct place again; you need to be aware that your process may be started for another reason (for example to receive a broadcast) that will not involve re-creating the activity and thus run its code to create a new Binder.

## Summary

| Inherited constants ||
|---|---|
| From class [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DUMP_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#DUMP_TRANSACTION:kotlin.Int) <br /> IBinder protocol transaction code: dump internal state. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FIRST_CALL_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#FIRST_CALL_TRANSACTION:kotlin.Int) <br /> The first transaction code available for user commands. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_ONEWAY](https://developer.android.com/reference/kotlin/android/os/IBinder#FLAG_ONEWAY:kotlin.Int) <br /> Flag to [transact](https://developer.android.com/reference/kotlin/android/os/IBinder#transact(kotlin.Int,%20android.os.Parcel,%20android.os.Parcel,%20kotlin.Int)): this is a one-way call, meaning that the caller returns immediately, without waiting for a result from the callee. Applies only if the caller and callee are in different processes. The system provides special ordering semantics for multiple oneway calls being made to the same IBinder object: these calls will be dispatched in the other process one at a time, with the same order as the original calls. These are still dispatched by the IPC thread pool, so may execute on different threads, but the next one will not be dispatched until the previous one completes. This ordering is not guaranteed for calls on different IBinder objects or when mixing oneway and non-oneway calls on the same IBinder object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [INTERFACE_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#INTERFACE_TRANSACTION:kotlin.Int) <br /> IBinder protocol transaction code: interrogate the recipient side of the transaction for its canonical interface descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LAST_CALL_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#LAST_CALL_TRANSACTION:kotlin.Int) <br /> The last transaction code available for user commands. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [LIKE_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#LIKE_TRANSACTION:kotlin.Int) <br /> IBinder protocol transaction code: tell an app asynchronously that the caller likes it. The app is responsible for incrementing and maintaining its own like counter, and may display this value to the user to indicate the quality of the app. This is an optional command that applications do not need to handle, so the default implementation is to do nothing. There is no response returned and nothing about the system will be functionally affected by it, but it will improve the app's self-esteem. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PING_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#PING_TRANSACTION:kotlin.Int) <br /> IBinder protocol transaction code: pingBinder(). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TWEET_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#TWEET_TRANSACTION:kotlin.Int) <br /> IBinder protocol transaction code: send a tweet to the target object. The data in the parcel is intended to be delivered to a shared messaging service associated with the object; it can be anything, as long as it is not more than 130 UTF-8 characters to conservatively fit within common messaging services. As part of [Build.VERSION_CODES.HONEYCOMB_MR2](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES#HONEYCOMB_MR2:kotlin.Int), all Binder objects are expected to support this protocol for fully integrated tweeting across the platform. To support older code, the default implementation logs the tweet to the main log as a simple emulation of broadcasting it publicly over the Internet. Also, upon completing the dispatch, the object must make a cup of tea, return it to the caller, and exclaim "jolly good message old boy!". <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [Binder](https://developer.android.com/reference/kotlin/android/os/Binder#Binder())`()` Default constructor just initializes the object. |
| [Binder](https://developer.android.com/reference/kotlin/android/os/Binder#Binder(kotlin.String))`(`descriptor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Constructor for creating a raw Binder object (token) along with a descriptor. |

| Public methods ||
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [attachInterface](https://developer.android.com/reference/kotlin/android/os/Binder#attachInterface(android.os.IInterface,%20kotlin.String))`(`owner:` ` [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface)?`, `descriptor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?`)` Convenience method for associating a specific interface with the Binder. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingIdentity())`()` Reset the identity of the incoming IPC on the current thread. |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearCallingWorkSource](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingWorkSource())`()` Clears the work source on this thread. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/os/Binder#dump(java.io.FileDescriptor,%20kotlin.Array))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Implemented to call the more convenient version[dump(java.io.FileDescriptor,java.io.PrintWriter,java.lang.String[])](https://developer.android.com/reference/kotlin/android/os/Binder#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dumpAsync](https://developer.android.com/reference/kotlin/android/os/Binder#dumpAsync(java.io.FileDescriptor,%20kotlin.Array))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Like[dump(java.io.FileDescriptor,java.lang.String[])](https://developer.android.com/reference/kotlin/android/os/Binder#dump(java.io.FileDescriptor,%20kotlin.Array)), but ensures the target executes asynchronously. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [flushPendingCommands](https://developer.android.com/reference/kotlin/android/os/Binder#flushPendingCommands())`()` Flush any Binder commands pending in the current thread to the kernel driver. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallingPid](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingPid())`()` Return the ID of the process that sent you the current transaction that is being processed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallingUid](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingUid())`()` Return the Linux UID assigned to the process that sent you the current transaction that is being processed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallingUidOrThrow](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingUidOrThrow())`()` Return the Linux UID assigned to the process that sent the transaction currently being processed. |
| static [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle) | [getCallingUserHandle](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingUserHandle())`()` Return the UserHandle assigned to the process that sent you the current transaction that is being processed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCallingWorkSourceUid](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingWorkSourceUid())`()` Returns the work source set by the caller. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getInterfaceDescriptor](https://developer.android.com/reference/kotlin/android/os/Binder#getInterfaceDescriptor())`()` Default implementation returns an empty interface name. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isBinderAlive](https://developer.android.com/reference/kotlin/android/os/Binder#isBinderAlive())`()` Check to see if the process that the binder is in is still alive. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [joinThreadPool](https://developer.android.com/reference/kotlin/android/os/Binder#joinThreadPool())`()` Add the calling thread to the IPC thread pool. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [linkToDeath](https://developer.android.com/reference/kotlin/android/os/Binder#linkToDeath(android.os.IBinder.DeathRecipient,%20kotlin.Int))`(`recipient:` ` [IBinder.DeathRecipient](https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Local implementation is a no-op. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [pingBinder](https://developer.android.com/reference/kotlin/android/os/Binder#pingBinder())`()` Default implementation always returns true -- if you got here, the object is alive. |
| open [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface)? | [queryLocalInterface](https://developer.android.com/reference/kotlin/android/os/Binder#queryLocalInterface(kotlin.String))`(`descriptor:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Use information supplied to [attachInterface()](https://developer.android.com/reference/kotlin/android/os/Binder#attachInterface(android.os.IInterface,%20kotlin.String))to return the associated [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface) if it matches the requested descriptor. |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreCallingIdentity](https://developer.android.com/reference/kotlin/android/os/Binder#restoreCallingIdentity(kotlin.Long))`(`token:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingIdentity()). |
| static [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [restoreCallingWorkSource](https://developer.android.com/reference/kotlin/android/os/Binder#restoreCallingWorkSource(kotlin.Long))`(`token:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Restores the work source on this thread using a token returned by [setCallingWorkSourceUid(int)](https://developer.android.com/reference/kotlin/android/os/Binder#setCallingWorkSourceUid(kotlin.Int))or [clearCallingWorkSource()](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingWorkSource()). |
| static [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [setCallingWorkSourceUid](https://developer.android.com/reference/kotlin/android/os/Binder#setCallingWorkSourceUid(kotlin.Int))`(`workSource:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the work source for this thread. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [transact](https://developer.android.com/reference/kotlin/android/os/Binder#transact(kotlin.Int,%20android.os.Parcel,%20android.os.Parcel,%20kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `reply:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)?`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Default implementation rewinds the parcels and calls onTransact. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [unlinkToDeath](https://developer.android.com/reference/kotlin/android/os/Binder#unlinkToDeath(android.os.IBinder.DeathRecipient,%20kotlin.Int))`(`recipient:` ` [IBinder.DeathRecipient](https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Local implementation is a no-op. |

| Protected methods ||
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [dump](https://developer.android.com/reference/kotlin/android/os/Binder#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array))`(`fd:` ` [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#)`, `fout:` ` [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#)`, `args:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>?`)` Print the object's state into the given stream. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onTransact](https://developer.android.com/reference/kotlin/android/os/Binder#onTransact(kotlin.Int,%20android.os.Parcel,%20android.os.Parcel,%20kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)`, `reply:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)?`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Default implementation is a stub that returns false. |

| Inherited functions ||
|---|---|
| From class [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder) |------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [addFrozenStateChangeCallback](https://developer.android.com/reference/kotlin/android/os/IBinder#addFrozenStateChangeCallback(java.util.concurrent.Executor,%20android.os.IBinder.FrozenStateChangeCallback))`(`executor:` ` [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)`, `callback:` ` [IBinder.FrozenStateChangeCallback](https://developer.android.com/reference/kotlin/android/os/IBinder.FrozenStateChangeCallback)`)` <br /> This method provides a callback mechanism to notify about process frozen/unfrozen events. Upon registration and any subsequent state changes, the callback is invoked with the latest process frozen state. If the listener process (the one using this API) is itself frozen, state change events might be combined into a single one with the latest frozen state. This single event would then be delivered when the listener process becomes unfrozen. Similarly, if an event happens before the previous event is consumed, they might be combined. This means the callback might not be called for every single state change, so don't rely on this API to count how many times the state has changed. The callback is automatically removed when all references to the binder proxy are dropped. You will only receive state change notifications for remote binders, as local binders by definition can't be frozen without you being frozen too. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [removeFrozenStateChangeCallback](https://developer.android.com/reference/kotlin/android/os/IBinder#removeFrozenStateChangeCallback(android.os.IBinder.FrozenStateChangeCallback))`(`callback:` ` [IBinder.FrozenStateChangeCallback](https://developer.android.com/reference/kotlin/android/os/IBinder.FrozenStateChangeCallback)`)` <br /> Unregister a [FrozenStateChangeCallback](https://developer.android.com/reference/kotlin/android/os/IBinder.FrozenStateChangeCallback). The callback will no longer be invoked when the hosting process changes its frozen state. <br /> | ||

## Public constructors

### Binder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Binder()
```

Default constructor just initializes the object.

If you're creating a Binder token (a Binder object without an attached interface), you should use [Binder(java.lang.String)](https://developer.android.com/reference/kotlin/android/os/Binder#Binder(kotlin.String))instead. 

### Binder

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
Binder(descriptor: String?)
```

Constructor for creating a raw Binder object (token) along with a descriptor.

The descriptor of binder objects usually specifies the interface they are implementing. In case of binder tokens, no interface is implemented, and the descriptor can be used as a sort of tag to help identify the binder token. This will help identify remote references to these objects more easily when debugging.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `descriptor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:Used to identify the creator of this token, for example the class name. Instead of creating multiple tokens with the same descriptor, consider adding a suffix to help identify them. This value may be`null`. |

## Public methods

### attachInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun attachInterface(
    owner: IInterface?, 
    descriptor: String?
): Unit
```

Convenience method for associating a specific interface with the Binder. After calling, [queryLocalInterface()](https://developer.android.com/reference/kotlin/android/os/Binder#queryLocalInterface(kotlin.String))will be implemented for you to return the given owner IInterface when the corresponding descriptor is requested.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------|
| `owner` | [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface)?:This value may be`null`. |
| `descriptor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?:This value may be`null`. |

### clearCallingIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun clearCallingIdentity(): Long
```

Reset the identity of the incoming IPC on the current thread. This can be useful if, while handling an incoming call, you will be calling on interfaces of other objects that may be local to your process and need to do permission checks on the calls coming into them (so they will check the permission of your own local process, and not whatever process originally called you).

| Return ||
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | Returns an opaque token that can be used to restore the original calling identity by passing it to [restoreCallingIdentity(long)](https://developer.android.com/reference/kotlin/android/os/Binder#restoreCallingIdentity(kotlin.Long)). |

**See Also**

- <https://developer.android.com/reference/kotlin/android/os/Binder#getCallingPid()>
- <https://developer.android.com/reference/kotlin/android/os/Binder#getCallingUid()>
- [#restoreCallingIdentity(long)](https://developer.android.com/reference/kotlin/android/os/Binder#restoreCallingIdentity(kotlin.Long)) 

### clearCallingWorkSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun clearCallingWorkSource(): Long
```

Clears the work source on this thread.

The work source will be propagated for future outgoing binder transactions executed on this thread.

[restoreCallingWorkSource(long)](https://developer.android.com/reference/kotlin/android/os/Binder#restoreCallingWorkSource(kotlin.Long))must always be called after clearing the worksource.

A typical use case would be 

```kotlin
long token = Binder.clearCallingWorkSource();
  try {
    // Call an API.
  } finally {
    Binder.restoreCallingWorkSource(token);
  }
  
```

| Return ||
|------------------------------------------------------------------------------|----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | token to restore original work source. |

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dump(
    fd: FileDescriptor, 
    args: Array<String!>?
): Unit
```

Implemented to call the more convenient version[dump(java.io.FileDescriptor,java.io.PrintWriter,java.lang.String[])](https://developer.android.com/reference/kotlin/android/os/Binder#dump(java.io.FileDescriptor,%20java.io.PrintWriter,%20kotlin.Array)).

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):This value cannot be`null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

### dumpAsync

Added in [API level 13](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun dumpAsync(
    fd: FileDescriptor, 
    args: Array<String!>?
): Unit
```

Like[dump(java.io.FileDescriptor,java.lang.String[])](https://developer.android.com/reference/kotlin/android/os/Binder#dump(java.io.FileDescriptor,%20kotlin.Array)), but ensures the target executes asynchronously.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):This value cannot be`null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:This value may be`null`. |

### flushPendingCommands

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun flushPendingCommands(): Unit
```

Flush any Binder commands pending in the current thread to the kernel driver. This can be useful to call before performing an operation that may block for a long time, to ensure that any pending object references have been released in order to prevent the process from holding on to objects longer than it needs to. 

### getCallingPid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCallingPid(): Int
```

Return the ID of the process that sent you the current transaction that is being processed. This PID can be used with higher-level system services to determine its identity and check permissions. If the current thread is not currently executing an incoming transaction, then its own PID is returned. Warning do not use this as a security identifier! PID is unreliable as it may be re-used. This should mostly be used for debugging. oneway transactions do not receive PID. Even if you expect a transaction to be synchronous, a misbehaving client could send it as a asynchronous call and result in a 0 PID here. Additionally, if there is a race and the calling process dies, the PID may still be 0 for a synchronous call. 

### getCallingUid

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCallingUid(): Int
```

Return the Linux UID assigned to the process that sent you the current transaction that is being processed. This UID can be used with higher-level system services to determine its identity and check permissions. If the current thread is not currently executing an incoming transaction, then its own UID is returned. 

### getCallingUidOrThrow

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCallingUidOrThrow(): Int
```

Return the Linux UID assigned to the process that sent the transaction currently being processed.

| Exceptions ||
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.lang.IllegalStateException` | if the current thread is not currently executing an incoming transaction and the calling identity has not been explicitly set with [clearCallingIdentity()](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingIdentity()) |

### getCallingUserHandle

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCallingUserHandle(): UserHandle
```

Return the UserHandle assigned to the process that sent you the current transaction that is being processed. This is the user of the caller. It is distinct from [getCallingUid()](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingUid())in that a particular user will have multiple distinct apps running under it each with their own UID. If the current thread is not currently executing an incoming transaction, then its own UserHandle is returned.

| Return ||
|------------------------------------------------------------------------------------|-----------------------------|
| [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle) | This value cannot be`null`. |

**See Also**

- [android.os.UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle) 

### getCallingWorkSourceUid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getCallingWorkSourceUid(): Int
```

Returns the work source set by the caller.

Unlike [getCallingUid()](https://developer.android.com/reference/kotlin/android/os/Binder#getCallingUid()), this result of this method cannot be trusted. The caller can set the value to whatever they want. Only use this value if you trust the calling UID.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The original UID responsible for the binder transaction. |

### getInterfaceDescriptor

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInterfaceDescriptor(): String?
```

Default implementation returns an empty interface name.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### isBinderAlive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isBinderAlive(): Boolean
```

Check to see if the process that the binder is in is still alive. Note that if you're calling on a local binder, this always returns true because your process is alive if you're calling it.

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | false if the process is not alive. Note that if it returns true, the process may have died while the call is returning. |

### joinThreadPool

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun joinThreadPool(): Unit
```

Add the calling thread to the IPC thread pool. This function does not return until the current process is exiting. 

### linkToDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun linkToDeath(
    recipient: IBinder.DeathRecipient, 
    flags: Int
): Unit
```

Local implementation is a no-op.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `recipient` | [IBinder.DeathRecipient](https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient):This value cannot be`null`. |

| Exceptions ||
|------------------------------|---------------------------------------------------|
| `android.os.RemoteException` | if the target IBinder's process has already died. |

### pingBinder

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun pingBinder(): Boolean
```

Default implementation always returns true -- if you got here, the object is alive.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns false if the hosting process is gone, otherwise the result (always by default true) returned by the pingBinder() implementation on the other side. |

### queryLocalInterface

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun queryLocalInterface(descriptor: String): IInterface?
```

Use information supplied to [attachInterface()](https://developer.android.com/reference/kotlin/android/os/Binder#attachInterface(android.os.IInterface,%20kotlin.String))to return the associated [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface) if it matches the requested descriptor.

| Parameters ||
|--------------|--------------------------------------------------------------------------------------------------------------|
| `descriptor` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

| Return ||
|-------------------------------------------------------------------------------------|--------------------------|
| [IInterface](https://developer.android.com/reference/kotlin/android/os/IInterface)? | This value may be`null`. |

### restoreCallingIdentity

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun restoreCallingIdentity(token: Long): Unit
```

Restore the identity of the incoming IPC on the current thread back to a previously identity that was returned by [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingIdentity()).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `token` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):The opaque token that was previously returned by [clearCallingIdentity](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingIdentity()). |

**See Also**

- [#clearCallingIdentity](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingIdentity()) 

### restoreCallingWorkSource

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun restoreCallingWorkSource(token: Long): Unit
```

Restores the work source on this thread using a token returned by [setCallingWorkSourceUid(int)](https://developer.android.com/reference/kotlin/android/os/Binder#setCallingWorkSourceUid(kotlin.Int))or [clearCallingWorkSource()](https://developer.android.com/reference/kotlin/android/os/Binder#clearCallingWorkSource()).

A typical use case would be 

```kotlin
long token = Binder.setCallingWorkSourceUid(uid);
  try {
    // Call an API.
  } finally {
    Binder.restoreCallingWorkSource(token);
  }
  
```  

### setCallingWorkSourceUid

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun setCallingWorkSourceUid(workSource: Int): Long
```

Sets the work source for this thread.

All the following binder calls on this thread will use the provided work source. If this is called during an on-going binder transaction, all the following binder calls will use the work source until the end of the transaction.

The concept of worksource is similar to [WorkSource](https://developer.android.com/reference/kotlin/android/os/WorkSource). However, for performance reasons, we only support one UID. This UID represents the original user responsible for the binder calls.

[restoreCallingWorkSource(long)](https://developer.android.com/reference/kotlin/android/os/Binder#restoreCallingWorkSource(kotlin.Long))must always be called after setting the worksource.

A typical use case would be 

```kotlin
long token = Binder.setCallingWorkSourceUid(uid);
  try {
    // Call an API.
  } finally {
    Binder.restoreCallingWorkSource(token);
  }
  
```

The work source will be propagated for future outgoing binder transactions executed on this thread.

| Parameters ||
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| `workSource` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The original UID responsible for the binder call. |

| Return ||
|------------------------------------------------------------------------------|----------------------------------------|
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | token to restore original work source. |

### transact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun transact(
    code: Int, 
    data: Parcel, 
    reply: Parcel?, 
    flags: Int
): Boolean
```

Default implementation rewinds the parcels and calls onTransact. On the remote side, transact calls into the binder to do the IPC.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action to perform. This should be a number between [FIRST_CALL_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#FIRST_CALL_TRANSACTION:kotlin.Int) and [LAST_CALL_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#LAST_CALL_TRANSACTION:kotlin.Int). |
| `data` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel):This value cannot be`null`. |
| `reply` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)?:This value may be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional operation flags. Either 0 for a normal RPC, or [FLAG_ONEWAY](https://developer.android.com/reference/kotlin/android/os/IBinder#FLAG_ONEWAY:kotlin.Int) for a one-way RPC. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Returns the result from [Binder.onTransact](https://developer.android.com/reference/kotlin/android/os/Binder#onTransact(kotlin.Int,%20android.os.Parcel,%20android.os.Parcel,%20kotlin.Int)). A successful call generally returns true; false generally means the transaction code was not understood. For a oneway call to a different process false should never be returned. If a oneway call is made to code in the same process (usually to a C++ or Rust implementation), then there are no oneway semantics, and false can still be returned. |

### unlinkToDeath

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun unlinkToDeath(
    recipient: IBinder.DeathRecipient, 
    flags: Int
): Boolean
```

Local implementation is a no-op.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------|
| `recipient` | [IBinder.DeathRecipient](https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the recipient is successfully unlinked, assuring you that its android.os.IBinder.DeathRecipient#binderDied method will not be called;`false`if the target IBinder has already died, meaning the method has been (or soon will be) called. |

| Exceptions ||
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `java.util.NoSuchElementException` | if the given recipient has not been registered with the IBinder, and the IBinder is still alive. Note that if the recipient was never registered, but the IBinder has already died, then this exception will*not*be thrown, and you will receive a false return value instead. |

## Protected methods

### dump

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun dump(
    fd: FileDescriptor, 
    fout: PrintWriter, 
    args: Array<String!>?
): Unit
```

Print the object's state into the given stream.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `fd` | [FileDescriptor](https://developer.android.com/reference/kotlin/java/io/FileDescriptor.html#):The raw file descriptor that the dump is being sent to. This value cannot be`null`. |
| `fout` | [PrintWriter](https://developer.android.com/reference/kotlin/java/io/PrintWriter.html#):The file to which you should dump your state. This will be closed for you after you return. This value cannot be`null`. |
| `args` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>?:additional arguments to the dump request. This value may be`null`. |

### onTransact

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onTransact(
    code: Int, 
    data: Parcel, 
    reply: Parcel?, 
    flags: Int
): Boolean
```

Default implementation is a stub that returns false. You will want to override this to do the appropriate unmarshalling of transactions.

If you want to call this, call transact().

Implementations that are returning a result should generally use [Parcel.writeNoException](https://developer.android.com/reference/kotlin/android/os/Parcel#writeNoException())and [Parcel.writeException](https://developer.android.com/reference/kotlin/android/os/Parcel#writeException(java.lang.Exception))to propagate exceptions back to the caller.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The action to perform. This should be a number between [FIRST_CALL_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#FIRST_CALL_TRANSACTION:kotlin.Int) and [LAST_CALL_TRANSACTION](https://developer.android.com/reference/kotlin/android/os/IBinder#LAST_CALL_TRANSACTION:kotlin.Int). |
| `data` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel):Marshalled data being received from the caller. This value cannot be`null`. |
| `reply` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel)?:If the caller is expecting a result back, it should be marshalled in to here. This value may be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional operation flags. Either 0 for a normal RPC, or [FLAG_ONEWAY](https://developer.android.com/reference/kotlin/android/os/IBinder#FLAG_ONEWAY:kotlin.Int) for a one-way RPC. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true on a successful call; returning false is generally used to indicate that you did not understand the transaction code. |
