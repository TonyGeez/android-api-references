Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DelegatedAdminReceiver

```
open class DelegatedAdminReceiver : BroadcastReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.content.BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#) ||
| | ↳ | [android.app.admin.DelegatedAdminReceiver](https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#) |

Base class for delegated apps to handle callbacks related to their delegated capabilities.

Delegated apps are apps that receive additional capabilities from the profile owner or device owner apps. Some of these capabilities involve the framework calling into the apps. To receive these callbacks, delegated apps should subclass this class and override the appropriate methods here. The subclassed receiver needs to be published in the app's manifest, with appropriate intent filters to mark which callbacks the receiver is interested in. An app can have multiple receivers as long as they listen for disjoint set of callbacks. For the manifest definitions, it must be protected by the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_DEVICE_ADMIN:kotlin.String` permission to ensure only the system can trigger these callbacks.

The callback methods happen on the main thread of the process. Thus long running operations must be done on another thread. Note that because a receiver is done once returning from its onReceive function, such long-running operations should probably be done in a `https://developer.android.com/reference/kotlin/android/app/Service.html#`.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#DelegatedAdminReceiver()()` <br /> |

| Public methods ||
|---|---|
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onChoosePrivateKeyAlias(android.content.Context,%20android.content.Intent,%20kotlin.Int,%20android.net.Uri,%20kotlin.String)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, uid: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, uri: https://developer.android.com/reference/kotlin/android/net/Uri.html#?, alias: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Allows this receiver to select the alias for a private key and certificate pair for authentication. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onNetworkLogsAvailable(android.content.Context,%20android.content.Intent,%20kotlin.Long,%20kotlin.Int)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#, batchToken: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, networkLogsCount: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Called each time a new batch of network logs can be retrieved. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Intercept delegated device administrator broadcasts. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onSecurityLogsAvailable(android.content.Context,%20android.content.Intent)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#, intent: https://developer.android.com/reference/kotlin/android/content/Intent.html#)` Called each time a new batch of security logs can be retrieved. |

Inherited functions From class `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#abortBroadcast()()`

Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`. This will prevent any other broadcast receivers from receiving the broadcast. It will still call `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` of the BroadcastReceiver that the caller of `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)` passed in.

**This method does not work with non-ordered broadcasts such as those sent with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`**

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#clearAbortBroadcast()()`

Clears the flag indicating that this receiver should abort the current broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getAbortBroadcast()()`

Returns the flag indicating whether or not this receiver should abort the current broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getDebugUnregister()()`

Return the last value given to `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setDebugUnregister(kotlin.Boolean)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getResultCode()()`

Retrieve the current result code, as set by the previous receiver.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getResultData()()`

Retrieve the current result data, as set by the previous receiver. Often this is null.

<br />

`https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getResultExtras(kotlin.Boolean)(makeMap: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Retrieve the current result extra data, as set by the previous receiver. Any changes you make to the returned Map will be propagated to the next receiver.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromPackage()()`

Returns the package name of the app that initially sent this broadcast.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromUid()()`

Returns the uid of the app that initially sent this broadcast.

<br />

`https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.PendingResult.html#!` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#goAsync()()`

This can be called by an application in `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)` to allow it to keep the broadcast active after returning from that function. This does *not* change the expectation of being relatively responsive to the broadcast, but does allow the implementation to move work related to it over to another thread to avoid glitching the main UI thread due to disk IO.

As a general rule, broadcast receivers are allowed to run for up to 10 seconds before the system will consider them non-responsive and ANR the app. Since these usually execute on the app's main thread, they are already bound by the \~5 second time limit of various operations that can happen there (not to mention just avoiding UI jank), so the receive limit is generally not of concern. However, once you use `goAsync`, though able to be off the main thread, the broadcast execution limit still applies, and that includes the time spent between calling this method and ultimately `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.PendingResult.html#finish()`.

If you are taking advantage of this method to have more time to execute, it is useful to know that the available time can be longer in certain situations. In particular, if the broadcast you are receiving is not a foreground broadcast (that is, the sender has not used `https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_FOREGROUND:kotlin.Int`), then more time is allowed for the receivers to run, allowing them to execute for 30 seconds or even a bit more. This is something that receivers should rarely take advantage of (long work should be punted to another system facility such as `https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#`, `https://developer.android.com/reference/kotlin/android/app/Service.html#`, or see especially androidx.core.app.JobIntentService), but can be useful in certain rare cases where it is necessary to do some work as soon as the broadcast is delivered. Keep in mind that the work you do here will block further broadcasts until it completes, so taking advantage of this at all excessively can be counter-productive and cause later events to be received more slowly.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#isInitialStickyBroadcast()()`

Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#isOrderedBroadcast()()`

Returns true if the receiver is currently processing an ordered broadcast.

<br />

`https://developer.android.com/reference/kotlin/android/os/IBinder.html#!` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#peekService(android.content.Context,%20android.content.Intent)(myContext: https://developer.android.com/reference/kotlin/android/content/Context.html#!, service: https://developer.android.com/reference/kotlin/android/content/Intent.html#!)`

Provide a binder to an already-bound service. This method is synchronous and will not start the target service if it is not present, so it is safe to call from `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)`. For peekService() to return a non null `https://developer.android.com/reference/kotlin/android/os/IBinder.html#` interface the service must have published it before. In other words some component must have called `https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int)` on it.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setDebugUnregister(kotlin.Boolean)(debug: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

Control inclusion of debugging help for mismatched calls to `https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)`. If called with true, before given to registerReceiver(), then the callstack of the following `https://developer.android.com/reference/kotlin/android/content/Context.html#unregisterReceiver(android.content.BroadcastReceiver)` call is retained, to be printed if a later incorrect unregister call is made. Note that doing this requires retaining information about the BroadcastReceiver for the lifetime of the app, resulting in a leak -- this should only be used for debugging.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setOrderedHint(kotlin.Boolean)(isOrdered: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`

For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResult(kotlin.Int,%20kotlin.String,%20android.os.Bundle)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Change all of the result data returned from this broadcasts; only works with broadcasts sent through `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`. All current result data is replaced by the value given to this method.

**This method does not work with non-ordered broadcasts such as those sent with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`**

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultCode(kotlin.Int)(code: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`

Change the current result code of this broadcast; only works with broadcasts sent through `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`. Often uses the Activity `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` constants, though the actual meaning of this value is ultimately up to the broadcaster.

This method does not work with non-ordered broadcasts such as those sent with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultData(kotlin.String)(data: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)`

Change the current result data of this broadcast; only works with broadcasts sent through `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`. This is an arbitrary string whose interpretation is up to the broadcaster.

**This method does not work with non-ordered broadcasts such as those sent with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`**

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultExtras(android.os.Bundle)(extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)`

Change the current result extras of this broadcast; only works with broadcasts sent through `https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)`. This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. Calling this method completely replaces the current map (if any).

**This method does not work with non-ordered broadcasts such as those sent with `https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)`**

<br />

## Public constructors

### DelegatedAdminReceiver

```
DelegatedAdminReceiver()
```

## Public methods

### onChoosePrivateKeyAlias

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onChoosePrivateKeyAlias(
    context: Context, 
    intent: Intent, 
    uid: Int, 
    uri: Uri?, 
    alias: String?
): String?
```

Allows this receiver to select the alias for a private key and certificate pair for authentication. If this method returns null, the default `https://developer.android.com/reference/kotlin/android/app/Activity.html#` will be shown that lets the user pick a private key and certificate pair. If this method returns `https://developer.android.com/reference/kotlin/android/security/KeyChain.html#KEY_ALIAS_SELECTION_DENIED:kotlin.String`, the default `https://developer.android.com/reference/kotlin/android/app/Activity.html#` will not be shown and the user will not be allowed to pick anything. And the app, that called android.security.KeyChain#choosePrivateKeyAlias, will receive `null` back.

This callback is only applicable if the delegated app has `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#DELEGATION_CERT_SELECTION:kotlin.String` capability. Additionally, it must declare an intent filter for `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_CHOOSE_PRIVATE_KEY_ALIAS:kotlin.String` in the receiver's manifest in order to receive this callback. The default implementation simply throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The running context as per `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)`. This value cannot be `null`. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The received intent as per `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)`. This value cannot be `null`. |
| `uid` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The uid of the app asking for the private key and certificate pair. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)?: The URI to authenticate, may be null. |
| `alias` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: The alias preselected by the client, or null. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?` | The private key alias to return and grant access to. |

**See Also**

### onNetworkLogsAvailable

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onNetworkLogsAvailable(
    context: Context, 
    intent: Intent, 
    batchToken: Long, 
    networkLogsCount: Int
): Unit
```

Called each time a new batch of network logs can be retrieved. This callback method will only ever be called when network logging is enabled. The logs can only be retrieved while network logging is enabled.

If a secondary user or profile is created, this callback won't be received until all users become affiliated again (even if network logging is enabled). It will also no longer be possible to retrieve the network logs batch with the most recent `batchToken` provided by this callback. See `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAffiliationIds(android.content.ComponentName,%20kotlin.collections.MutableSet)`.

This callback is only applicable if the delegated app has `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#DELEGATION_NETWORK_LOGGING:kotlin.String` capability. Additionally, it must declare an intent filter for `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_NETWORK_LOGS_AVAILABLE:kotlin.String` in the receiver's manifest in order to receive this callback. The default implementation simply throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

This callback is triggered by a foreground broadcast and the app should ensure that any long-running work is not executed synchronously inside the callback.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The running context as per `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)`. This value cannot be `null`. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The received intent as per `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)`. This value cannot be `null`. |
| `batchToken` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The token representing the current batch of network logs. |
| `networkLogsCount` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The total count of events in the current batch of network logs. Value is 1 or greater |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#retrieveNetworkLogs(android.content.ComponentName,%20kotlin.Long)`

### onReceive

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun onReceive(
    context: Context, 
    intent: Intent
): Unit
```

Intercept delegated device administrator broadcasts. Implementations should not override this method; implement the convenience callbacks for each action instead.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): This value cannot be `null`. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): This value cannot be `null`. |

### onSecurityLogsAvailable

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onSecurityLogsAvailable(
    context: Context, 
    intent: Intent
): Unit
```

Called each time a new batch of security logs can be retrieved. This callback method will only ever be called when security logging is enabled. The logs can only be retrieved while security logging is enabled.

If a secondary user or profile is created, this callback won't be received until all users become affiliated again (even if security logging is enabled). It will also no longer be possible to retrieve the security logs. See `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#setAffiliationIds(android.content.ComponentName,%20kotlin.collections.MutableSet)`.

This callback is only applicable if the delegated app has `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#DELEGATION_SECURITY_LOGGING:kotlin.String` capability. Additionally, it must declare an intent filter for `https://developer.android.com/reference/kotlin/android/app/admin/DeviceAdminReceiver#ACTION_SECURITY_LOGS_AVAILABLE:kotlin.String` in the receiver's manifest in order to receive this callback. The default implementation simply throws `https://developer.android.com/reference/kotlin/java/lang/UnsupportedOperationException.html#`.

This callback is triggered by a foreground broadcast and the app should ensure that any long-running work is not executed synchronously inside the callback.

| Parameters ||
|---|---|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#): The running context as per `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)`. This value cannot be `null`. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#): The received intent as per `https://developer.android.com/reference/kotlin/android/app/admin/DelegatedAdminReceiver#onReceive(android.content.Context,%20android.content.Intent)`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/app/admin/DevicePolicyManager#retrieveSecurityLogs(android.content.ComponentName)`
