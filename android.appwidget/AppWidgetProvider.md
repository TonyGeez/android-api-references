# AppWidgetProvider

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetProvider

Kotlin| [Java](https://developer.android.com/reference/android/appwidget/AppWidgetProvider "View this page in Java") 

```
open class AppWidgetProvider : BroadcastReceiver
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.content.BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#) ||
| | ↳ | [android.appwidget.AppWidgetProvider](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#) |

A convenience class to aid in implementing an AppWidget provider. Everything you can do with AppWidgetProvider, you can do with a regular [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#). AppWidgetProvider merely parses the relevant fields out of the Intent that is received in [onReceive(Context,Intent)](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onReceive(android.content.Context,%20android.content.Intent)), and calls hook methods with the received extras.

Extend this class and override one or more of the [onUpdate](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onUpdate(android.content.Context,%20android.appwidget.AppWidgetManager,%20kotlin.IntArray)), [onDeleted](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onDeleted(android.content.Context,%20kotlin.IntArray)), [onEnabled](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onEnabled(android.content.Context))or [onDisabled](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onDisabled(android.content.Context))methods to implement your own AppWidget functionality.
|
| ### Developer Guides
|
| For more information about how to write an app widget provider, read the [App Widgets](https://developer.android.com/guide/topics/appwidgets/index.html#AppWidgetProvider) developer guide.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppWidgetProvider](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#AppWidgetProvider())`()` Constructor to initialize AppWidgetProvider. |

| Public methods ||
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAppWidgetOptionsChanged](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onAppWidgetOptionsChanged(android.content.Context,%20android.appwidget.AppWidgetManager,%20kotlin.Int,%20android.os.Bundle))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appWidgetManager:` ` [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager)!`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `newOptions:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_OPTIONS_CHANGED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_OPTIONS_CHANGED:kotlin.String) broadcast when this widget has been layed out at a new size or its options changed via [AppWidgetManager.updateAppWidgetOptions](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetOptions(kotlin.Int,%20android.os.Bundle)). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDeleted](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onDeleted(android.content.Context,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DELETED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DELETED:kotlin.String) broadcast when one or more AppWidget instances have been deleted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onDisabled](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onDisabled(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DISABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DISABLED:kotlin.String) broadcast, which is sent when the last AppWidget instance for this provider is deleted. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onEnabled](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onEnabled(android.content.Context))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_ENABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_ENABLED:kotlin.String) broadcast when the a AppWidget for this provider is instantiated. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReceive](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onReceive(android.content.Context,%20android.content.Intent))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `intent:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` Implements [BroadcastReceiver.onReceive](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent))to dispatch calls to the various other methods on AppWidgetProvider. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestored](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onRestored(android.content.Context,%20kotlin.IntArray,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `oldWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`, `newWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_RESTORED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String) broadcast when instances of this AppWidget provider have been restored from backup. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onUpdate](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onUpdate(android.content.Context,%20android.appwidget.AppWidgetManager,%20kotlin.IntArray))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appWidgetManager:` ` [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager)!`, `appWidgetIds:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Called in response to the [AppWidgetManager.ACTION_APPWIDGET_UPDATE](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String) and [AppWidgetManager.ACTION_APPWIDGET_RESTORED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String) broadcasts when this AppWidget provider is being asked to provide [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) for a set of AppWidgets. |

| Inherited functions ||
|---|---|
| From class [BroadcastReceiver](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#) |------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [abortBroadcast](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#abortBroadcast())`()` <br /> Sets the flag indicating that this receiver should abort the current broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)). This will prevent any other broadcast receivers from receiving the broadcast. It will still call [onReceive](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent))of the BroadcastReceiver that the caller of [Context.sendOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String))passed in. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearAbortBroadcast](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#clearAbortBroadcast())`()` <br /> Clears the flag indicating that this receiver should abort the current broadcast. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getAbortBroadcast](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getAbortBroadcast())`()` <br /> Returns the flag indicating whether or not this receiver should abort the current broadcast. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getDebugUnregister](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getDebugUnregister())`()` <br /> Return the last value given to [setDebugUnregister](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setDebugUnregister(kotlin.Boolean)). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getResultCode](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getResultCode())`()` <br /> Retrieve the current result code, as set by the previous receiver. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | [getResultData](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getResultData())`()` <br /> Retrieve the current result data, as set by the previous receiver. Often this is null. <br /> | | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | [getResultExtras](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getResultExtras(kotlin.Boolean))`(`makeMap:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Retrieve the current result extra data, as set by the previous receiver. Any changes you make to the returned Map will be propagated to the next receiver. <br /> | | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getSentFromPackage](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromPackage())`()` <br /> Returns the package name of the app that initially sent this broadcast. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSentFromUid](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#getSentFromUid())`()` <br /> Returns the uid of the app that initially sent this broadcast. <br /> | | [BroadcastReceiver.PendingResult](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.PendingResult.html#)! | [goAsync](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#goAsync())`()` <br /> This can be called by an application in [onReceive](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent))to allow it to keep the broadcast active after returning from that function. This does*not*change the expectation of being relatively responsive to the broadcast, but does allow the implementation to move work related to it over to another thread to avoid glitching the main UI thread due to disk IO. As a general rule, broadcast receivers are allowed to run for up to 10 seconds before the system will consider them non-responsive and ANR the app. Since these usually execute on the app's main thread, they are already bound by the \~5 second time limit of various operations that can happen there (not to mention just avoiding UI jank), so the receive limit is generally not of concern. However, once you use`goAsync`, though able to be off the main thread, the broadcast execution limit still applies, and that includes the time spent between calling this method and ultimately [PendingResult.finish()](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.PendingResult.html#finish()). If you are taking advantage of this method to have more time to execute, it is useful to know that the available time can be longer in certain situations. In particular, if the broadcast you are receiving is not a foreground broadcast (that is, the sender has not used [Intent.FLAG_RECEIVER_FOREGROUND](https://developer.android.com/reference/kotlin/android/content/Intent.html#FLAG_RECEIVER_FOREGROUND:kotlin.Int)), then more time is allowed for the receivers to run, allowing them to execute for 30 seconds or even a bit more. This is something that receivers should rarely take advantage of (long work should be punted to another system facility such as [android.app.job.JobScheduler](https://developer.android.com/reference/kotlin/android/app/job/JobScheduler.html#), [android.app.Service](https://developer.android.com/reference/kotlin/android/app/Service.html#), or see especially androidx.core.app.JobIntentService), but can be useful in certain rare cases where it is necessary to do some work as soon as the broadcast is delivered. Keep in mind that the work you do here will block further broadcasts until it completes, so taking advantage of this at all excessively can be counter-productive and cause later events to be received more slowly. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isInitialStickyBroadcast](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#isInitialStickyBroadcast())`()` <br /> Returns true if the receiver is currently processing the initial value of a sticky broadcast -- that is, the value that was last broadcast and is currently held in the sticky cache, so this is not directly the result of a broadcast right now. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#isOrderedBroadcast())`()` <br /> Returns true if the receiver is currently processing an ordered broadcast. <br /> | | [IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#)! | [peekService](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#peekService(android.content.Context,%20android.content.Intent))`(`myContext:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `service:` ` [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!`)` <br /> Provide a binder to an already-bound service. This method is synchronous and will not start the target service if it is not present, so it is safe to call from [onReceive](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent)). For peekService() to return a non null [android.os.IBinder](https://developer.android.com/reference/kotlin/android/os/IBinder.html#) interface the service must have published it before. In other words some component must have called [android.content.Context#bindService(Intent, ServiceConnection, int)](https://developer.android.com/reference/kotlin/android/content/Context.html#bindService(android.content.Intent,%20android.content.ServiceConnection,%20kotlin.Int))on it. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setDebugUnregister](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setDebugUnregister(kotlin.Boolean))`(`debug:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> Control inclusion of debugging help for mismatched calls to [Context.registerReceiver()](https://developer.android.com/reference/kotlin/android/content/Context.html#registerReceiver(android.content.BroadcastReceiver,%20android.content.IntentFilter)). If called with true, before given to registerReceiver(), then the callstack of the following [Context.unregisterReceiver()](https://developer.android.com/reference/kotlin/android/content/Context.html#unregisterReceiver(android.content.BroadcastReceiver))call is retained, to be printed if a later incorrect unregister call is made. Note that doing this requires retaining information about the BroadcastReceiver for the lifetime of the app, resulting in a leak -- this should only be used for debugging. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setOrderedHint](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setOrderedHint(kotlin.Boolean))`(`isOrdered:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> For internal use, sets the hint about whether this BroadcastReceiver is running in ordered mode. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResult](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResult(kotlin.Int,%20kotlin.String,%20android.os.Bundle))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`, `extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Change all of the result data returned from this broadcasts; only works with broadcasts sent through [Context.sendOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)). All current result data is replaced by the value given to this method. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultCode](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultCode(kotlin.Int))`(`code:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Change the current result code of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)). Often uses the Activity [android.app.Activity#RESULT_CANCELED](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int) and [android.app.Activity#RESULT_OK](https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int) constants, though the actual meaning of this value is ultimately up to the broadcaster. This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent)) <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultData](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultData(kotlin.String))`(`data:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` <br /> Change the current result data of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)). This is an arbitrary string whose interpretation is up to the broadcaster. **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))** <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setResultExtras](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#setResultExtras(android.os.Bundle))`(`extras:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!`)` <br /> Change the current result extras of this broadcast; only works with broadcasts sent through [Context.sendOrderedBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendOrderedBroadcast(android.content.Intent,%20kotlin.String)). This is a Bundle holding arbitrary data, whose interpretation is up to the broadcaster. Can be set to null. Calling this method completely replaces the current map (if any). **This method does not work with non-ordered broadcasts such as those sent with [Context.sendBroadcast](https://developer.android.com/reference/kotlin/android/content/Context.html#sendBroadcast(android.content.Intent))** <br /> | ||

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

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_OPTIONS_CHANGED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_OPTIONS_CHANGED:kotlin.String) broadcast when this widget has been layed out at a new size or its options changed via [AppWidgetManager.updateAppWidgetOptions](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetOptions(kotlin.Int,%20android.os.Bundle)). {@more}

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which this receiver is running. |
| `appWidgetManager` | [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager)!:A [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager) object you can call android.appwidget.AppWidgetManager#updateAppWidget on. |
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The appWidgetId of the widget whose size changed. |
| `newOptions` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!:The new options of the changed widget. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_OPTIONS_CHANGED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_OPTIONS_CHANGED:kotlin.String) 

### onDeleted

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDeleted(
    context: Context!, 
    appWidgetIds: IntArray!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DELETED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DELETED:kotlin.String) broadcast when one or more AppWidget instances have been deleted. Override this method to implement your own AppWidget functionality. {@more}

| Parameters ||
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which this receiver is running. |
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The appWidgetIds that have been deleted from their host. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_DELETED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DELETED:kotlin.String) 

### onDisabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onDisabled(context: Context!): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_DISABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DISABLED:kotlin.String) broadcast, which is sent when the last AppWidget instance for this provider is deleted. Override this method to implement your own AppWidget functionality. {@more}

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which this receiver is running. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_DISABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DISABLED:kotlin.String) 

### onEnabled

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onEnabled(context: Context!): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_ENABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_ENABLED:kotlin.String) broadcast when the a AppWidget for this provider is instantiated. Override this method to implement your own AppWidget functionality. {@more} When the last AppWidget for this provider is deleted, [AppWidgetManager.ACTION_APPWIDGET_DISABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DISABLED:kotlin.String) is sent by the AppWidget manager, and [onDisabled](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onDisabled(android.content.Context))is called. If after that, an AppWidget for this provider is created again, onEnabled() will be called again.

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which this receiver is running. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_ENABLED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_ENABLED:kotlin.String) 

### onReceive

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onReceive(
    context: Context!, 
    intent: Intent!
): Unit
```

Implements [BroadcastReceiver.onReceive](https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#onReceive(android.content.Context,%20android.content.Intent))to dispatch calls to the various other methods on AppWidgetProvider.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The Context in which the receiver is running. |
| `intent` | [Intent](https://developer.android.com/reference/kotlin/android/content/Intent.html#)!:The Intent being received. |

### onRestored

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onRestored(
    context: Context!, 
    oldWidgetIds: IntArray!, 
    newWidgetIds: IntArray!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_RESTORED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String) broadcast when instances of this AppWidget provider have been restored from backup. If your provider maintains any persistent data about its widget instances, override this method to remap the old AppWidgetIds to the new values and update any other app state that may be relevant.

This callback will be followed immediately by a call to [onUpdate](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onUpdate(android.content.Context,%20android.appwidget.AppWidgetManager,%20kotlin.IntArray))so your provider can immediately generate new RemoteViews suitable for its newly-restored set of instances.

In addition, you should set [AppWidgetManager.OPTION_APPWIDGET_RESTORE_COMPLETED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_RESTORE_COMPLETED:kotlin.String) to true indicate if a widget has been restored successfully from the provider's side. {@more}

| Parameters ||
|----------------|-------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!: |
| `oldWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: |
| `newWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: |

### onUpdate

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onUpdate(
    context: Context!, 
    appWidgetManager: AppWidgetManager!, 
    appWidgetIds: IntArray!
): Unit
```

Called in response to the [AppWidgetManager.ACTION_APPWIDGET_UPDATE](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String) and [AppWidgetManager.ACTION_APPWIDGET_RESTORED](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String) broadcasts when this AppWidget provider is being asked to provide [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#) for a set of AppWidgets. Override this method to implement your own AppWidget functionality. {@more}

| Parameters ||
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:The [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#) in which this receiver is running. |
| `appWidgetManager` | [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager)!:A [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager) object you can call android.appwidget.AppWidgetManager#updateAppWidget on. |
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:The appWidgetIds for which an update is needed. Note that this may be all of the AppWidget instances for this provider, or just a subset of them. |

**See Also**

- [android.appwidget.AppWidgetManager#ACTION_APPWIDGET_UPDATE](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String)
