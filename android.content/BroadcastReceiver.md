# BroadcastReceiver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# BroadcastReceiver

Kotlin| [Java](../android/content/BroadcastReceiver.md) 
| --- | --- |

```
abstract class BroadcastReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.content.BroadcastReceiver](../android/content/BroadcastReceiver.md) |

| Known Direct Subclasses [AppWidgetProvider](../android/appwidget/AppWidgetProvider.md), [DelegatedAdminReceiver](../android/app/admin/DelegatedAdminReceiver.md), [DeviceAdminReceiver](../android/app/admin/DeviceAdminReceiver.md), [MbmsDownloadReceiver](../android/telephony/mbms/MbmsDownloadReceiver.md), [PolicyUpdateReceiver](../android/app/admin/PolicyUpdateReceiver.md), [RestrictionsReceiver](../android/service/restrictions/RestrictionsReceiver.md) |--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AppWidgetProvider](../android/appwidget/AppWidgetProvider.md) | A convenience class to aid in implementing an AppWidget provider. | | [DelegatedAdminReceiver](../android/app/admin/DelegatedAdminReceiver.md) | Base class for delegated apps to handle callbacks related to their delegated capabilities. | | [DeviceAdminReceiver](../android/app/admin/DeviceAdminReceiver.md) | Base class for implementing a device administration component. | | [MbmsDownloadReceiver](../android/telephony/mbms/MbmsDownloadReceiver.md) | The [BroadcastReceiver](../android/content/BroadcastReceiver.md) responsible for handling intents sent from the middleware. | | [PolicyUpdateReceiver](../android/app/admin/PolicyUpdateReceiver.md) | Base class for implementing a policy update receiver. | | [RestrictionsReceiver](../android/service/restrictions/RestrictionsReceiver.md) | Abstract implementation of a Restrictions Provider BroadcastReceiver. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Base class for code that receives and handles broadcast intents sent by [android.content.Context#sendBroadcast(Intent)](../android/content/Context.md)).

You can either dynamically register an instance of this class with android.content.Context#registerReceiver or statically declare an implementation with the [<receiver>](../android/R.styleable.md) tag in your`AndroidManifest.xml`.
|
| ### Developer Guides
|
| For more information about using BroadcastReceiver, read the [Broadcasts](https://developer.android.com/guide/components/broadcasts.html) developer guide.

## Summary

| Nested classes ||
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PendingResult](../android/content/BroadcastReceiver.PendingResult.md) State for a result that is pending for a broadcast receiver. |

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------|---|
| [BroadcastReceiver](../android/content/BroadcastReceiver.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abortBroadcast](../android/content/BroadcastReceiver.md))`()` Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAbortBroadcast](../android/content/BroadcastReceiver.md))`()` Clears the flag indicating that this receiver should abort the current broadcast. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAbortBroadcast](../android/content/BroadcastReceiver.md))`()` Returns the flag indicating whether or not this receiver should abort the current broadcast. |
| --- | --- |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDebugUnregister](../android/content/BroadcastReceiver.md))`()` Return the last value given to [setDebugUnregister](../android/content/BroadcastReceiver.md)). |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](../android/content/BroadcastReceiver.md))`()` Retrieve the current result code, as set by the previous receiver. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResultData](../android/content/BroadcastReceiver.md))`()` Retrieve the current result data, as set by the previous receiver. |
| --- | --- |
| [Bundle](../android/os/Bundle.md)! | [getResultExtras](../android/content/BroadcastReceiver.md))`(`makeMap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Retrieve the current result extra data, as set by the previous receiver. |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSentFromPackage](../android/content/BroadcastReceiver.md))`()` Returns the package name of the app that initially sent this broadcast. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSentFromUid](../android/content/BroadcastReceiver.md))`()` Returns the uid of the app that initially sent this broadcast. |
| --- | --- |
| [BroadcastReceiver.PendingResult](../android/content/BroadcastReceiver.PendingResult.md)! | [goAsync](../android/content/BroadcastReceiver.md))`()` This can be called by an application in [onReceive](../android/content/BroadcastReceiver.md))to allow it to keep the broadcast active after returning from that function. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialStickyBroadcast](../android/content/BroadcastReceiver.md))`()` Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOrderedBroadcast](../android/content/BroadcastReceiver.md))`()` Returns true if the receiver is currently processing an ordered broadcast. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceive](../android/content/BroadcastReceiver.md))`(`context:` ` [Context](../android/content/Context.md)!`, `intent:` ` [Intent](../android/content/Intent.md)!`)` This method is called when the BroadcastReceiver is receiving an Intent broadcast. |
| open [IBinder](../android/os/IBinder.md)! | [peekService](../android/content/BroadcastReceiver.md))`(`myContext:` ` [Context](../android/content/Context.md)!`, `service:` ` [Intent](../android/content/Intent.md)!`)` Provide a binder to an already-bound service. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDebugUnregister](../android/content/BroadcastReceiver.md))`(`debug:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Control inclusion of debugging help for mismatched calls to [Context.registerReceiver()](../android/content/Context.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrderedHint](../android/content/BroadcastReceiver.md))`(`isOrdered:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResult](../android/content/BroadcastReceiver.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](../android/os/Bundle.md)!`)` Change all of the result data returned from this broadcasts; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultCode](../android/content/BroadcastReceiver.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Change the current result code of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultData](../android/content/BroadcastReceiver.md))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Change the current result data of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultExtras](../android/content/BroadcastReceiver.md))`(`extras:` ` [Bundle](../android/os/Bundle.md)!`)` Change the current result extras of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). |

## Public constructors

### BroadcastReceiver

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
BroadcastReceiver()
```

## Public methods

### abortBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun abortBroadcast(): Unit
```

Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). This will prevent any other broadcast receivers from receiving the broadcast. It will still call [onReceive](../android/content/BroadcastReceiver.md))of the BroadcastReceiver that the caller of [Context.sendOrderedBroadcast](../android/content/Context.md))passed in.

**This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))** 

### clearAbortBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun clearAbortBroadcast(): Unit
```

Clears the flag indicating that this receiver should abort the current broadcast. 

### getAbortBroadcast

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getAbortBroadcast(): Boolean
```

Returns the flag indicating whether or not this receiver should abort the current broadcast.

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the broadcast should be aborted. |

### getDebugUnregister

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getDebugUnregister(): Boolean
```

Return the last value given to [setDebugUnregister](../android/content/BroadcastReceiver.md)). 

### getResultCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultCode(): Int
```

Retrieve the current result code, as set by the previous receiver.

| Return ||
|----------------------------------------------------------------------------|------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | int The current result code. |

### getResultData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultData(): String!
```

Retrieve the current result data, as set by the previous receiver. Often this is null.

| Return ||
|-----------------------------------------------------------------------------------|----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | String The current result data; may be null. |

### getResultExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getResultExtras(makeMap: Boolean): Bundle!
```

Retrieve the current result extra data, as set by the previous receiver. Any changes you make to the returned Map will be propagated to the next receiver.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `makeMap` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):If true then a new empty Map will be made for you if the current Map is null; if false you should be prepared to receive a null Map. |

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android/os/Bundle.md)! | Map The current extras map. |

### getSentFromPackage

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSentFromPackage(): String?
```

Returns the package name of the app that initially sent this broadcast.

| Return ||
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | the package name of the broadcasting app or`null`if the current receiver cannot access the identity of the broadcasting app |

### getSentFromUid

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSentFromUid(): Int
```

Returns the uid of the app that initially sent this broadcast.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the uid of the broadcasting app or [Process.INVALID_UID](../android/os/Process.md) if the current receiver cannot access the identity of the broadcasting app |

### goAsync

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun goAsync(): BroadcastReceiver.PendingResult!
```

This can be called by an application in [onReceive](../android/content/BroadcastReceiver.md))to allow it to keep the broadcast active after returning from that function. This does*not*change the expectation of being relatively responsive to the broadcast, but does allow the implementation to move work related to it over to another thread to avoid glitching the main UI thread due to disk IO.

As a general rule, broadcast receivers are allowed to run for up to 10 seconds before the system will consider them non-responsive and ANR the app. Since these usually execute on the app's main thread, they are already bound by the \~5 second time limit of various operations that can happen there (not to mention just avoiding UI jank), so the receive limit is generally not of concern. However, once you use`goAsync`, though able to be off the main thread, the broadcast execution limit still applies, and that includes the time spent between calling this method and ultimately [PendingResult.finish()](../android/content/BroadcastReceiver.PendingResult.md)).

If you are taking advantage of this method to have more time to execute, it is useful to know that the available time can be longer in certain situations. In particular, if the broadcast you are receiving is not a foreground broadcast (that is, the sender has not used [Intent.FLAG_RECEIVER_FOREGROUND](../android/content/Intent.md)), then more time is allowed for the receivers to run, allowing them to execute for 30 seconds or even a bit more. This is something that receivers should rarely take advantage of (long work should be punted to another system facility such as [android.app.job.JobScheduler](../android/app/job/JobScheduler.md), [android.app.Service](../android/app/Service.md), or see especially androidx.core.app.JobIntentService), but can be useful in certain rare cases where it is necessary to do some work as soon as the broadcast is delivered. Keep in mind that the work you do here will block further broadcasts until it completes, so taking advantage of this at all excessively can be counter-productive and cause later events to be received more slowly.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BroadcastReceiver.PendingResult](../android/content/BroadcastReceiver.PendingResult.md)! | Returns a [PendingResult](../android/content/BroadcastReceiver.PendingResult.md) representing the result of the active broadcast. The BroadcastRecord itself is no longer active; all data and other interaction must go through [PendingResult](../android/content/BroadcastReceiver.PendingResult.md) APIs. The [PendingResult.finish()](../android/content/BroadcastReceiver.PendingResult.md))method must be called once processing of the broadcast is done. |

### isInitialStickyBroadcast

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isInitialStickyBroadcast(): Boolean
```

Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now. 

### isOrderedBroadcast

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isOrderedBroadcast(): Boolean
```

Returns true if the receiver is currently processing an ordered broadcast. 

### onReceive

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onReceive(
    context: Context!, 
    intent: Intent!
): Unit
```

This method is called when the BroadcastReceiver is receiving an Intent broadcast. During this time you can use the other methods on BroadcastReceiver to view/modify the current result values. This method is always called within the main thread of its process, unless you explicitly asked for it to be scheduled on a different thread using [android.content.Context#registerReceiver(BroadcastReceiver, * IntentFilter, String, android.os.Handler)](../android/content/Context.md)). When it runs on the main thread you should never perform long-running operations in it (there is a timeout of 10 seconds that the system allows before considering the receiver to be blocked and a candidate to be killed). You cannot launch a popup dialog in your implementation of onReceive().

**If this BroadcastReceiver was launched through a \<receiver\> tag, then the object is no longer alive after returning from this function.** This means you should not perform any operations that return a result to you asynchronously. If you need to perform any follow up background work, schedule a [android.app.job.JobService](../android/app/job/JobService.md) with [android.app.job.JobScheduler](../android/app/job/JobScheduler.md). If you wish to interact with a service that is already running and previously bound using [bindService()](../android/content/Context.md)), you can use [peekService](../android/content/BroadcastReceiver.md)).

The Intent filters used in android.content.Context#registerReceiver and in application manifests are*not* guaranteed to be exclusive. They are hints to the operating system about how to find suitable recipients. It is possible for senders to force delivery to specific recipients, bypassing filter resolution. For this reason, [onReceive()](../android/content/BroadcastReceiver.md))implementations should respond only to known actions, ignoring any unexpected Intents that they may receive.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android/content/Context.md)!:The Context in which the receiver is running. |
| `intent` | [Intent](../android/content/Intent.md)!:The Intent being received. |

### peekService

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun peekService(
    myContext: Context!, 
    service: Intent!
): IBinder!
```

Provide a binder to an already-bound service. This method is synchronous and will not start the target service if it is not present, so it is safe to call from [onReceive](../android/content/BroadcastReceiver.md)). For peekService() to return a non null [android.os.IBinder](../android/os/IBinder.md) interface the service must have published it before. In other words some component must have called [android.content.Context#bindService(Intent, ServiceConnection, int)](../android/content/Context.md))on it.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `myContext` | [Context](../android/content/Context.md)!:The Context that had been passed to [onReceive(android.content.Context,android.content.Intent)](../android/content/BroadcastReceiver.md)) |
| `service` | [Intent](../android/content/Intent.md)!:Identifies the already-bound service you wish to use. See [android.content.Context#bindService(Intent, ServiceConnection, int)](../android/content/Context.md))for more information. |

### setDebugUnregister

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setDebugUnregister(debug: Boolean): Unit
```

Control inclusion of debugging help for mismatched calls to [Context.registerReceiver()](../android/content/Context.md)). If called with true, before given to registerReceiver(), then the callstack of the following [Context.unregisterReceiver()](../android/content/Context.md))call is retained, to be printed if a later incorrect unregister call is made. Note that doing this requires retaining information about the BroadcastReceiver for the lifetime of the app, resulting in a leak -- this should only be used for debugging. 

### setOrderedHint

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setOrderedHint(isOrdered: Boolean): Unit
```

For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode. 

### setResult

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setResult(
    code: Int, 
    data: String!, 
    extras: Bundle!
): Unit
```

Change all of the result data returned from this broadcasts; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). All current result data is replaced by the value given to this method.

**This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))**

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new result code. Often uses the Activity [android.app.Activity#RESULT_CANCELED](../android/app/Activity.md) and [android.app.Activity#RESULT_OK](../android/app/Activity.md) constants, though the actual meaning of this value is ultimately up to the broadcaster. |
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new result data. This is an arbitrary string whose interpretation is up to the broadcaster; may be null. |
| `extras` | [Bundle](../android/os/Bundle.md)!:The new extra data map. This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. This completely replaces the current map (if any). |
| --- | --- |

### setResultCode

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setResultCode(code: Int): Unit
```

Change the current result code of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). Often uses the Activity [android.app.Activity#RESULT_CANCELED](../android/app/Activity.md) and [android.app.Activity#RESULT_OK](../android/app/Activity.md) constants, though the actual meaning of this value is ultimately up to the broadcaster.

This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------|
| `code` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new result code. |

**See Also**

- [#setResult(int, String, Bundle)](../android/content/BroadcastReceiver.md)) 

### setResultData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setResultData(data: String!): Unit
```

Change the current result data of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). This is an arbitrary string whose interpretation is up to the broadcaster.

**This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))**

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------|
| `data` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:The new result data; may be null. |

**See Also**

- [#setResult(int, String, Bundle)](../android/content/BroadcastReceiver.md)) 

### setResultExtras

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun setResultExtras(extras: Bundle!): Unit
```

Change the current result extras of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android/content/Context.md)). This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. Calling this method completely replaces the current map (if any).

**This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android/content/Context.md))**

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------|
| `extras` | [Bundle](../android/os/Bundle.md)!:The new extra data map; may be null. |

**See Also**

- [#setResult(int, String, Bundle)](../android/content/BroadcastReceiver.md))
