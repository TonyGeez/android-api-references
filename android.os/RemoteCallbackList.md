Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RemoteCallbackList

```
open class RemoteCallbackList<E : IInterface!>
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.os.RemoteCallbackList](https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#) |

Takes care of the grunt work of maintaining a list of remote interfaces, typically for the use of performing callbacks from a `https://developer.android.com/reference/kotlin/android/app/Service.html#` to its clients. In particular, this:

- Keeps track of a set of registered `https://developer.android.com/reference/kotlin/android/os/IInterface` objects, taking care to identify them through their underlying unique `https://developer.android.com/reference/kotlin/android/os/IBinder` (by calling `https://developer.android.com/reference/kotlin/android/os/IInterface#asBinder()`.
- Attaches a `https://developer.android.com/reference/kotlin/android/os/IBinder.DeathRecipient` to each registered interface, so that it can be cleaned out of the list if its process goes away.
- Performs locking of the underlying list of interfaces to deal with multithreaded incoming calls, and a thread-safe way to iterate over a snapshot of the list without holding its lock.

<br />

To use this class, simply create a single instance along with your service, and call its #register and `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)` methods as client register and unregister with your service. To call back on to the registered clients, use `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`, `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)`, and `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#finishBroadcast()`.

If a registered interface's process goes away, this class will take care of automatically removing it from the list. If you want to do additional work in this situation, you can create a subclass that implements the #onCallbackDied method.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList.Builder` Builder for `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_DROP:kotlin.Int` When the callback recipient's process is frozen, callbacks are suppressed as if they never happened. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_ENQUEUE_ALL:kotlin.Int` When the callback recipient's process is frozen, callbacks are enqueued so they're invoked after the recipient is unfrozen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_ENQUEUE_MOST_RECENT:kotlin.Int` When the callback recipient's process is frozen, only the most recent callback is enqueued, which is later invoked after the recipient is unfrozen. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_UNSET:kotlin.Int` Callbacks are invoked immediately regardless of the frozen state of the target process. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#RemoteCallbackList()()` Creates a RemoteCallbackList with `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_UNSET:kotlin.Int`. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()()` Use instead to ensure proper handling of frozen processes. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#broadcast(java.util.function.Consumer)(callback: https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#<E>)` Performs `callback` on each registered interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#finishBroadcast()()` Clean up the state of a broadcast previously initiated by calling `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastCookie(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve the cookie associated with the item returned by `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)`. |
| open E | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Retrieve an item in the active broadcast that was previously started with `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`. |
| open [Executor](https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#)? | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getExecutor()()` Returns the executor used when invoking callbacks asynchronously. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getFrozenCalleePolicy()()` Returns the frozen callee policy. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getMaxQueueSize()()` Returns the max queue size. |
| open [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)! | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getRegisteredCallbackCookie(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return any cookie associated with a currently registered interface. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getRegisteredCallbackCount()()` Returns the number of registered interfaces. |
| open E | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getRegisteredCallbackItem(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Return a currently registered interface. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#kill()()` Disable this interface list. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#onCallbackDied(android.os.RemoteCallbackList.E)(callbackInterface: E)` Old version of `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#onCallbackDied(android.os.RemoteCallbackList.E,%20kotlin.Any)` that does not provide a cookie. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#onCallbackDied(android.os.RemoteCallbackList.E,%20kotlin.Any)(callbackInterface: E, cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Called when the process hosting an interface in the list has gone away. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#register(android.os.RemoteCallbackList.E)(callbackInterface: E)` Simple version of `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#register(android.os.RemoteCallbackList.E,%20kotlin.Any)` that does not take a cookie object. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#register(android.os.RemoteCallbackList.E,%20kotlin.Any)(callbackInterface: E, cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Add a new interface to the list. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)(callbackInterface: E)` Remove from the list an interface that was previously added with #register. |

## Constants

### FROZEN_CALLEE_POLICY_DROP

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FROZEN_CALLEE_POLICY_DROP: Int
```

When the callback recipient's process is frozen, callbacks are suppressed as if they never happened. This could be useful in the case where the recipient wishes to react to callbacks only when they occur while the recipient is not frozen. For example, certain network events are only worth responding to if the response can be immediate. Another example is recipients having another way of getting the latest state once it's unfrozen. Therefore there is no need to save callbacks that happened while the recipient was frozen.

 Value: 3

### FROZEN_CALLEE_POLICY_ENQUEUE_ALL

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FROZEN_CALLEE_POLICY_ENQUEUE_ALL: Int
```

When the callback recipient's process is frozen, callbacks are enqueued so they're invoked after the recipient is unfrozen. This is commonly used when the recipient wants to receive all callbacks without losing any history, e.g. the recipient maintains a running count of events that occurred. Queued callbacks are invoked in the order they were originally broadcasted.

 Value: 1

### FROZEN_CALLEE_POLICY_ENQUEUE_MOST_RECENT

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FROZEN_CALLEE_POLICY_ENQUEUE_MOST_RECENT: Int
```

When the callback recipient's process is frozen, only the most recent callback is enqueued, which is later invoked after the recipient is unfrozen. This can be used when only the most recent state matters, for instance when clients are listening to screen brightness changes.

 Value: 2

### FROZEN_CALLEE_POLICY_UNSET

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FROZEN_CALLEE_POLICY_UNSET: Int
```

Callbacks are invoked immediately regardless of the frozen state of the target process. Not recommended. Only exists for backward-compatibility. This represents the behavior up to SDK 35. Starting with SDK 36, clients should set a policy to govern callback invocations when recipients are frozen.

 Value: 0

## Public constructors

### RemoteCallbackList

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
RemoteCallbackList()
```

Creates a RemoteCallbackList with `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_UNSET:kotlin.Int`. This is equivalent to

```kotlin
new RemoteCallbackList.Build(RemoteCallbackList.FROZEN_CALLEE_POLICY_UNSET).build()
  
```

<br />

## Public methods

### beginBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun beginBroadcast(): Int
```

Use instead to ensure proper handling of frozen processes. Prepare to start making calls to the currently registered interfaces. This creates a copy of the interface list, which you can retrieve items from using `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)`. Note that only one broadcast can be active at a time, so you must be sure to always call this from the same thread (usually by scheduling with `https://developer.android.com/reference/kotlin/android/os/Handler`) or do your own synchronization. You must call `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#finishBroadcast()` when done.

A typical loop delivering a broadcast looks like this:

```kotlin
int i = interfaces.beginBroadcast();
  while (i > 0) {
      i--;
      try {
          interfaces.getBroadcastItem(i).somethingHappened();
      } catch (RemoteException e) {
          // The RemoteCallbackList will take care of removing
          // the dead object for us.
      }
  }
  interfaces.finishBroadcast();
```
Note that this method is only supported for `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_UNSET:kotlin.Int`. For other policies use `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#broadcast(java.util.function.Consumer)` instead.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | Returns the number of interfaces in the broadcast, to be used with `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)` to determine the range of indices you can supply. |

| Exceptions ||
|---|---|
| `java.lang.UnsupportedOperationException` | if an frozen callee policy is set. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#finishBroadcast()`

### broadcast

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun broadcast(callback: Consumer<E>): Unit
```

Performs `callback` on each registered interface. This is equivalent to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`, followed by iterating over the items using `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)` and then `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#finishBroadcast()`, except that this method supports frozen callee policies.

| Parameters ||
|---|---|
| `callback` | [Consumer](https://developer.android.com/reference/kotlin/java/util/function/Consumer.html#)\<E\>: This value cannot be `null`. |

### finishBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun finishBroadcast(): Unit
```

Clean up the state of a broadcast previously initiated by calling `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`. This must always be called when you are done with a broadcast.
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`

### getBroadcastCookie

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBroadcastCookie(index: Int): Any!
```

Retrieve the cookie associated with the item returned by `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)`

### getBroadcastItem

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getBroadcastItem(index: Int): E
```

Retrieve an item in the active broadcast that was previously started with `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`. This can *only* be called after the broadcast is started, and its data is no longer valid after calling `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#finishBroadcast()`.

Note that it is possible for the process of one of the returned interfaces to go away before you call it, so you will need to catch `https://developer.android.com/reference/kotlin/android/os/RemoteException` when calling on to the returned object. The interface list itself, however, will take care of unregistering these objects once it detects that it is no longer valid, so you can handle such an exception by simply ignoring it.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Which of the registered interfaces you would like to retrieve. Ranges from 0 to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`-1, inclusive. |

| Return ||
|---|---|
| `E` | Returns the interface that you can call. This will always be non-null. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()`

### getExecutor

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getExecutor(): Executor?
```

Returns the executor used when invoking callbacks asynchronously.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/java/util/concurrent/Executor.html#?` | The executor. This value may be `null`. |

### getFrozenCalleePolicy

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getFrozenCalleePolicy(): Int
```

Returns the frozen callee policy.

Note that if the list silently fell back to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_UNSET:kotlin.Int` behavior (e.g., due to lack of kernel support), this method will still return the originally configured policy.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The frozen callee policy. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_UNSET:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_ENQUEUE_ALL:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_ENQUEUE_MOST_RECENT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#FROZEN_CALLEE_POLICY_DROP:kotlin.Int` |

### getMaxQueueSize

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getMaxQueueSize(): Int
```

Returns the max queue size.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The max queue size. |

### getRegisteredCallbackCookie

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRegisteredCallbackCookie(index: Int): Any!
```

Return any cookie associated with a currently registered interface. Note that this is *not* the same as `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastCookie(kotlin.Int)` and should not be used interchangeably with it. This method returns the current cookie registered at the given index, not the current broadcast state. This means that it is not itself thread-safe: any call to #register or `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)` will change these indices, so you must do your own thread safety between these to protect from such changes.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index of which registration cookie to return, from 0 to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getRegisteredCallbackCount()` - 1. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!` | Returns whatever cookie object is associated with this index, or null if `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#kill()` has been called. |

### getRegisteredCallbackCount

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRegisteredCallbackCount(): Int
```

Returns the number of registered interfaces. Note that the number of registered interfaces may differ from the value returned by `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#beginBroadcast()` since the former returns the number of interfaces registered at the time of the call and the second the number of interfaces to which the broadcast will be delivered.

This function is useful to decide whether to schedule a broadcast if this requires doing some work which otherwise would not be performed.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The size. |

### getRegisteredCallbackItem

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getRegisteredCallbackItem(index: Int): E
```

Return a currently registered interface. Note that this is *not* the same as `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getBroadcastItem(kotlin.Int)` and should not be used interchangeably with it. This method returns the registered interface at the given index, not the current broadcast state. This means that it is not itself thread-safe: any call to #register or `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)` will change these indices, so you must do your own thread safety between these to protect from such changes.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Index of which interface registration to return, from 0 to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#getRegisteredCallbackCount()` - 1. |

| Return ||
|---|---|
| `E` | Returns whatever interface is associated with this index, or null if `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#kill()` has been called. |

### kill

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun kill(): Unit
```

Disable this interface list. All registered interfaces are unregistered, and the list is disabled so that future calls to #register will fail. This should be used when a Service is stopping, to prevent clients from registering interfaces after it is stopped.
**See Also**

### onCallbackDied

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallbackDied(callbackInterface: E): Unit
```

Old version of `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#onCallbackDied(android.os.RemoteCallbackList.E,%20kotlin.Any)` that does not provide a cookie.

### onCallbackDied

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCallbackDied(
    callbackInterface: E, 
    cookie: Any!
): Unit
```

Called when the process hosting an interface in the list has gone away. The default implementation calls `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#onCallbackDied(android.os.RemoteCallbackList.E)` for backwards compatibility.

| Parameters ||
|---|---|
| `callbackInterface` | E: The interface whose process has died. Note that, since its process has died, you can not make any calls on to this interface. You can, however, retrieve its IBinder and compare it with another IBinder to see if it is the same object. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: The cookie object original provided to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#register(android.os.RemoteCallbackList.E,%20kotlin.Any)`. |

**See Also**

### register

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun register(callbackInterface: E): Boolean
```

Simple version of `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#register(android.os.RemoteCallbackList.E,%20kotlin.Any)` that does not take a cookie object.

### register

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun register(
    callbackInterface: E, 
    cookie: Any!
): Boolean
```

Add a new interface to the list. This interface will remain in the list until a corresponding call to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)` or its hosting process goes away. If the interface was already registered (determined by checking to see if the `https://developer.android.com/reference/kotlin/android/os/IInterface#asBinder()` object is already in the list), then it will be replaced with the new interface. Registrations are not counted; a single call to `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)` will remove an interface after any number calls to register it.

| Parameters ||
|---|---|
| `callbackInterface` | E: The callback interface to be added to the list. Must not be null -- passing null here will cause a NullPointerException. Most services will want to check for null before calling this with an object given from a client, so that clients can't crash the service with bad data. |
| `cookie` | [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!: Optional additional data to be associated with this interface. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the interface was successfully added to the list. Returns false if it was not added, either because `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#kill()` had previously been called or the interface's process has gone away. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#unregister(android.os.RemoteCallbackList.E)`
- `https://developer.android.com/reference/kotlin/android/os/RemoteCallbackList#kill()`

### unregister

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun unregister(callbackInterface: E): Boolean
```

Remove from the list an interface that was previously added with #register. This uses the `https://developer.android.com/reference/kotlin/android/os/IInterface#asBinder()` object to correctly find the previous registration. Registrations are not counted; a single unregister call will remove an interface after any number calls to #register for it.

| Parameters ||
|---|---|
| `callbackInterface` | E: The interface to be removed from the list. Passing null here will cause a NullPointerException, so you will generally want to check for null before calling. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Returns true if the interface was found and unregistered. Returns false if the given interface was not found on the list. |

**See Also**
