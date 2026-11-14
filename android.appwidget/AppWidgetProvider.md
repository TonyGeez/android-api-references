# AppWidgetProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetProvider

Kotlin| [Java](AppWidgetProvider.md) 
| --- | --- |

```
open class AppWidgetProvider : BroadcastReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.content.BroadcastReceiver](../android.content/BroadcastReceiver.md) ||
| | ↳ | [android.appwidget.AppWidgetProvider](AppWidgetProvider.md) |

A convenience class to aid in implementing an AppWidget provider. Everything you can do with AppWidgetProvider, you can do with a regular [BroadcastReceiver](../android.content/BroadcastReceiver.md). AppWidgetProvider merely parses the relevant fields out of the Intent that is received in [onReceive(Context,Intent)](AppWidgetProvider.md)), and calls hook methods with the received extras.

Extend this class and override one or more of the [onUpdate](AppWidgetProvider.md)), [onDeleted](AppWidgetProvider.md)), [onEnabled](AppWidgetProvider.md))or [onDisabled](AppWidgetProvider.md))methods to implement your own AppWidget functionality.
|
| ### Developer Guides
|
| For more information about how to write an app widget provider, read the [App Widgets](https://developer.android.com/guide/topics/appwidgets/index.html#AppWidgetProvider) developer guide.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppWidgetProvider](AppWidgetProvider.md))`()` Constructor to initialize AppWidgetProvider. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAppWidgetOptionsChanged](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appWidgetManager:` ` [AppWidgetManager](AppWidgetManager.md)!`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newOptions:` ` [Bundle](../android.os/Bundle.md)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_OPTIONS_CHANGED](AppWidgetManager.md) broadcast when this widget has been layed out at a new size or its options changed via [AppWidgetManager.updateAppWidgetOptions](AppWidgetManager.md)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeleted](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DELETED](AppWidgetManager.md) broadcast when one or more AppWidget instances have been deleted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisabled](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DISABLED](AppWidgetManager.md) broadcast, which is sent when the last AppWidget instance for this provider is deleted. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEnabled](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_ENABLED](AppWidgetManager.md) broadcast when the a AppWidget for this provider is instantiated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceive](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`, `intent:` ` [Intent](../android.content/Intent.md)!`)` Implements [BroadcastReceiver.onReceive](../android.content/BroadcastReceiver.md))to dispatch calls to the various other methods on AppWidgetProvider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestored](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`, `oldWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `newWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_RESTORED](AppWidgetManager.md) broadcast when instances of this AppWidget provider have been restored from backup. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdate](AppWidgetProvider.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appWidgetManager:` ` [AppWidgetManager](AppWidgetManager.md)!`, `appWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_UPDATE](AppWidgetManager.md) and [AppWidgetManager.ACTION_APPWIDGET_RESTORED](AppWidgetManager.md) broadcasts when this AppWidget provider is being asked to provide [RemoteViews](../android.widget/RemoteViews.md) for a set of AppWidgets. |

| Inherited functions ||
|---|---|
| From class [BroadcastReceiver](../android.content/BroadcastReceiver.md) |------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abortBroadcast](../android.content/BroadcastReceiver.md))`()` <br /> Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android.content/Context.md)). This will prevent any other broadcast receivers from receiving the broadcast. It will still call [onReceive](../android.content/BroadcastReceiver.md))of the BroadcastReceiver that the caller of [Context.sendOrderedBroadcast](../android.content/Context.md))passed in. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android.content/Context.md))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAbortBroadcast](../android.content/BroadcastReceiver.md))`()` <br /> Clears the flag indicating that this receiver should abort the current broadcast. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAbortBroadcast](../android.content/BroadcastReceiver.md))`()` <br /> Returns the flag indicating whether or not this receiver should abort the current broadcast. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDebugUnregister](../android.content/BroadcastReceiver.md))`()` <br /> Return the last value given to [setDebugUnregister](../android.content/BroadcastReceiver.md)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](../android.content/BroadcastReceiver.md))`()` <br /> Retrieve the current result code, as set by the previous receiver. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResultData](../android.content/BroadcastReceiver.md))`()` <br /> Retrieve the current result data, as set by the previous receiver. Often this is null. <br /> | | [Bundle](../android.os/Bundle.md)! | [getResultExtras](../android.content/BroadcastReceiver.md))`(`makeMap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Retrieve the current result extra data, as set by the previous receiver. Any changes you make to the returned Map will be propagated to the next receiver. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSentFromPackage](../android.content/BroadcastReceiver.md))`()` <br /> Returns the package name of the app that initially sent this broadcast. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSentFromUid](../android.content/BroadcastReceiver.md))`()` <br /> Returns the uid of the app that initially sent this broadcast. <br /> | | [BroadcastReceiver.PendingResult](../android/content/BroadcastReceiver.PendingResult.md)! | [goAsync](../android.content/BroadcastReceiver.md))`()` <br /> This can be called by an application in [onReceive](../android.content/BroadcastReceiver.md))to allow it to keep the broadcast active after returning from that function. This does*not*change the expectation of being relatively responsive to the broadcast, but does allow the implementation to move work related to it over to another thread to avoid glitching the main UI thread due to disk IO. As a general rule, broadcast receivers are allowed to run for up to 10 seconds before the system will consider them non-responsive and ANR the app. Since these usually execute on the app's main thread, they are already bound by the \~5 second time limit of various operations that can happen there (not to mention just avoiding UI jank), so the receive limit is generally not of concern. However, once you use`goAsync`, though able to be off the main thread, the broadcast execution limit still applies, and that includes the time spent between calling this method and ultimately [PendingResult.finish()](../android/content/BroadcastReceiver.PendingResult.md)). If you are taking advantage of this method to have more time to execute, it is useful to know that the available time can be longer in certain situations. In particular, if the broadcast you are receiving is not a foreground broadcast (that is, the sender has not used [Intent.FLAG_RECEIVER_FOREGROUND](../android.content/Intent.md)), then more time is allowed for the receivers to run, allowing them to execute for 30 seconds or even a bit more. This is something that receivers should rarely take advantage of (long work should be punted to another system facility such as [android.app.job.JobScheduler](../android.app.job/JobScheduler.md), [android.app.Service](../android.app/Service.md), or see especially androidx.core.app.JobIntentService), but can be useful in certain rare cases where it is necessary to do some work as soon as the broadcast is delivered. Keep in mind that the work you do here will block further broadcasts until it completes, so taking advantage of this at all excessively can be counter-productive and cause later events to be received more slowly. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialStickyBroadcast](../android.content/BroadcastReceiver.md))`()` <br /> Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOrderedBroadcast](../android.content/BroadcastReceiver.md))`()` <br /> Returns true if the receiver is currently processing an ordered broadcast. <br /> | | [IBinder](../android.os/IBinder.md)! | [peekService](../android.content/BroadcastReceiver.md))`(`myContext:` ` [Context](../android.content/Context.md)!`, `service:` ` [Intent](../android.content/Intent.md)!`)` <br /> Provide a binder to an already-bound service. This method is synchronous and will not start the target service if it is not present, so it is safe to call from [onReceive](../android.content/BroadcastReceiver.md)). For peekService() to return a non null [android.os.IBinder](../android.os/IBinder.md) interface the service must have published it before. In other words some component must have called [android.content.Context#bindService(Intent, ServiceConnection, int)](../android.content/Context.md))on it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDebugUnregister](../android.content/BroadcastReceiver.md))`(`debug:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control inclusion of debugging help for mismatched calls to [Context.registerReceiver()](../android.content/Context.md)). If called with true, before given to registerReceiver(), then the callstack of the following [Context.unregisterReceiver()](../android.content/Context.md))call is retained, to be printed if a later incorrect unregister call is made. Note that doing this requires retaining information about the BroadcastReceiver for the lifetime of the app, resulting in a leak -- this should only be used for debugging. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrderedHint](../android.content/BroadcastReceiver.md))`(`isOrdered:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResult](../android.content/BroadcastReceiver.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Change all of the result data returned from this broadcasts; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android.content/Context.md)). All current result data is replaced by the value given to this method. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android.content/Context.md))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultCode](../android.content/BroadcastReceiver.md))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the current result code of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android.content/Context.md)). Often uses the Activity [android.app.Activity#RESULT_CANCELED](../android.app/Activity.md) and [android.app.Activity#RESULT_OK](../android.app/Activity.md) constants, though the actual meaning of this value is ultimately up to the broadcaster. This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android.content/Context.md)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultData](../android.content/BroadcastReceiver.md))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Change the current result data of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android.content/Context.md)). This is an arbitrary string whose interpretation is up to the broadcaster. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android.content/Context.md))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultExtras](../android.content/BroadcastReceiver.md))`(`extras:` ` [Bundle](../android.os/Bundle.md)!`)` <br /> Change the current result extras of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](../android.content/Context.md)). This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. Calling this method completely replaces the current map (if any). **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](../android.content/Context.md))** <br /> | ||

## Public constructors

### AppWidgetProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AppWidgetProvider()
```

Constructor to initialize AppWidgetProvider.

## Public methods

### onAppWidgetOptionsChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAppWidgetOptionsChanged(
    context: Context!, 
    appWidgetManager: AppWidgetManager!, 
    appWidgetId: Int, 
    newOptions: Bundle!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_OPTIONS_CHANGED](AppWidgetManager.md) broadcast when this widget has been layed out at a new size or its options changed via [AppWidgetManager.updateAppWidgetOptions](AppWidgetManager.md)). {@more}

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The [Context](../android.content/Context.md) in which this receiver is running. |
| `appWidgetManager` | [AppWidgetManager](AppWidgetManager.md)!:A [AppWidgetManager](AppWidgetManager.md) object you can call android.appwidget.AppWidgetManager#updateAppWidget on. |
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The appWidgetId of the widget whose size changed. |
| --- | --- |
| `newOptions` | [Bundle](../android.os/Bundle.md)!:The new options of the changed widget. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_OPTIONS_CHANGED](AppWidgetManager.md) 

### onDeleted

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDeleted(
    context: Context!, 
    appWidgetIds: IntArray!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DELETED](AppWidgetManager.md) broadcast when one or more AppWidget instances have been deleted. Override this method to implement your own AppWidget functionality. {@more}

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The [Context](../android.content/Context.md) in which this receiver is running. |
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The appWidgetIds that have been deleted from their host. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_DELETED](AppWidgetManager.md) 

### onDisabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDisabled(context: Context!): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DISABLED](AppWidgetManager.md) broadcast, which is sent when the last AppWidget instance for this provider is deleted. Override this method to implement your own AppWidget functionality. {@more}

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The [Context](../android.content/Context.md) in which this receiver is running. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_DISABLED](AppWidgetManager.md) 

### onEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onEnabled(context: Context!): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_ENABLED](AppWidgetManager.md) broadcast when the a AppWidget for this provider is instantiated. Override this method to implement your own AppWidget functionality. {@more} When the last AppWidget for this provider is deleted, [AppWidgetManager.ACTION_APPWIDGET_DISABLED](AppWidgetManager.md) is sent by the AppWidget manager, and [onDisabled](AppWidgetProvider.md))is called. If after that, an AppWidget for this provider is created again, onEnabled() will be called again.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The [Context](../android.content/Context.md) in which this receiver is running. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_ENABLED](AppWidgetManager.md) 

### onReceive

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceive(
    context: Context!, 
    intent: Intent!
): Unit
```

Implements [BroadcastReceiver.onReceive](../android.content/BroadcastReceiver.md))to dispatch calls to the various other methods on AppWidgetProvider.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The Context in which the receiver is running. |
| `intent` | [Intent](../android.content/Intent.md)!:The Intent being received. |

### onRestored

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRestored(
    context: Context!, 
    oldWidgetIds: IntArray!, 
    newWidgetIds: IntArray!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_RESTORED](AppWidgetManager.md) broadcast when instances of this AppWidget provider have been restored from backup. If your provider maintains any persistent data about its widget instances, override this method to remap the old AppWidgetIds to the new values and update any other app state that may be relevant.

This callback will be followed immediately by a call to [onUpdate](AppWidgetProvider.md))so your provider can immediately generate new RemoteViews suitable for its newly-restored set of instances.

In addition, you should set [AppWidgetManager.OPTION_APPWIDGET_RESTORE_COMPLETED](AppWidgetManager.md) to true indicate if a widget has been restored successfully from the provider's side. {@more}

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!: |
| `oldWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: |
| `newWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: |
| --- | --- |

### onUpdate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUpdate(
    context: Context!, 
    appWidgetManager: AppWidgetManager!, 
    appWidgetIds: IntArray!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_UPDATE](AppWidgetManager.md) and [AppWidgetManager.ACTION_APPWIDGET_RESTORED](AppWidgetManager.md) broadcasts when this AppWidget provider is being asked to provide [RemoteViews](../android.widget/RemoteViews.md) for a set of AppWidgets. Override this method to implement your own AppWidget functionality. {@more}

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](../android.content/Context.md)!:The [Context](../android.content/Context.md) in which this receiver is running. |
| `appWidgetManager` | [AppWidgetManager](AppWidgetManager.md)!:A [AppWidgetManager](AppWidgetManager.md) object you can call android.appwidget.AppWidgetManager#updateAppWidget on. |
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The appWidgetIds for which an update is needed. Note that this may be all of the AppWidget instances for this provider, or just a subset of them. |
| --- | --- |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_UPDATE](AppWidgetManager.md)
