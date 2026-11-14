# AppWidgetHost

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetHost

Kotlin| [Java](https://developer.android.com/reference/android/appwidget/AppWidgetHost "View this page in Java") 
| --- | --- |

```
open class AppWidgetHost
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.appwidget.AppWidgetHost](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#) |

AppWidgetHost provides the interaction with the AppWidget service for apps, like the home screen, that want to embed AppWidgets in their UI.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppWidgetHost](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#AppWidgetHost(android.content.Context,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `hostId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [allocateAppWidgetId](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#allocateAppWidgetId())`()` Get a appWidgetId for a host in the calling process. |
| [AppWidgetHostView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHostView)! | [createView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#createView(android.content.Context,%20kotlin.Int,%20android.appwidget.AppWidgetProviderInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appWidget:` ` [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)!`)` Create the AppWidgetHostView for the given widget. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteAllHosts](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#deleteAllHosts())`()` Remove all records about all hosts for your package. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteAppWidgetId](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#deleteAppWidgetId(kotlin.Int))`(`appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Stop listening to changes for this AppWidget. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteHost](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#deleteHost())`()` Remove all records about this host from the AppWidget manager. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getAppWidgetIds](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#getAppWidgetIds())`()` Gets a list of all the appWidgetIds that are bound to the current host |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAppWidgetRemoved](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#onAppWidgetRemoved(kotlin.Int))`(`appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the app widget is removed for appWidgetId |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAppWidgetConfigureActivityForResult](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#startAppWidgetConfigureActivityForResult(android.app.Activity,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20android.os.Bundle))`(`activity:` ` [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#)`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intentFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?`)` Starts an app widget provider configure activity for result on behalf of the caller. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startListening](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#startListening())`()` Start receiving onAppWidgetChanged calls for your AppWidgets. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopListening](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#stopListening())`()` Stop receiving onAppWidgetChanged calls for your AppWidgets. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearViews](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#clearViews())`()` Clear the list of Views that have been created by this AppWidgetHost. |
| open [AppWidgetHostView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHostView)! | [onCreateView](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#onCreateView(android.content.Context,%20kotlin.Int,%20android.appwidget.AppWidgetProviderInfo))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appWidget:` ` [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)!`)` Called to create the AppWidgetHostView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProviderChanged](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#onProviderChanged(kotlin.Int,%20android.appwidget.AppWidgetProviderInfo))`(`appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appWidget:` ` [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)!`)` Called when the AppWidget provider for a AppWidget has been upgraded to a new apk. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvidersChanged](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost#onProvidersChanged())`()` Called when the set of available widgets changes (ie. widget containing packages are added, updated or removed, or widget components are enabled or disabled.) |

## Public constructors

### AppWidgetHost

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
AppWidgetHost(
    context: Context!, 
    hostId: Int)
```

## Public methods

### allocateAppWidgetId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun allocateAppWidgetId(): Int
```

Get a appWidgetId for a host in the calling process.

| Return ||
|----------------------------------------------------------------------------|---------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a appWidgetId |

### createView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun createView(
    context: Context!, 
    appWidgetId: Int, 
    appWidget: AppWidgetProviderInfo!
): AppWidgetHostView!
```

Create the AppWidgetHostView for the given widget. The AppWidgetHost retains a pointer to the newly-created View. 

### deleteAllHosts

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun deleteAllHosts(): Unit
```

Remove all records about all hosts for your package.

- Call this when initializing your database, as it might be because of a data wipe.
- Call this to have the AppWidget manager release all resources associated with your host. Any future calls about this host will cause the records to be re-allocated.

<br />

### deleteAppWidgetId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteAppWidgetId(appWidgetId: Int): Unit
```

Stop listening to changes for this AppWidget. 

### deleteHost

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun deleteHost(): Unit
```

Remove all records about this host from the AppWidget manager.

- Call this when initializing your database, as it might be because of a data wipe.
- Call this to have the AppWidget manager release all resources associated with your host. Any future calls about this host will cause the records to be re-allocated.

<br />

### getAppWidgetIds

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getAppWidgetIds(): IntArray!
```

Gets a list of all the appWidgetIds that are bound to the current host 

### onAppWidgetRemoved

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onAppWidgetRemoved(appWidgetId: Int): Unit
```

Called when the app widget is removed for appWidgetId

| Parameters ||
|---------------|-----------------------------------------------------------------------------|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): |

### startAppWidgetConfigureActivityForResult

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun startAppWidgetConfigureActivityForResult(
    activity: Activity, 
    appWidgetId: Int, 
    intentFlags: Int, 
    requestCode: Int, 
    options: Bundle?
): Unit
```

Starts an app widget provider configure activity for result on behalf of the caller. Use this method if the provider is in another profile as you are not allowed to start an activity in another profile. You can optionally provide a request code that is returned in [Activity.onActivityResult(int, int, android.content.Intent)](https://developer.android.com/reference/kotlin/android/app/Activity.html#onActivityResult(kotlin.Int,%20kotlin.Int,%20android.content.Intent))and an options bundle to be passed to the started activity.

Note that the provided app widget has to be bound for this method to work.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html#):The activity from which to start the configure one. This value cannot be`null`. |
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bound app widget whose provider's config activity to start. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional request code retuned with the result. |
| --- | --- |
| `intentFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional intent flags. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?:This value may be`null`. |

| Exceptions ||
|---------------------------------------------|-------------------------------|
| `android.content.ActivityNotFoundException` | If the activity is not found. |

**See Also**

- [android.appwidget.AppWidgetProviderInfo#getProfile()](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#getProfile()) 

### startListening

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun startListening(): Unit
```

Start receiving onAppWidgetChanged calls for your AppWidgets. Call this when your activity becomes visible, i.e. from onStart() in your Activity. 

### stopListening

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun stopListening(): Unit
```

Stop receiving onAppWidgetChanged calls for your AppWidgets. Call this when your activity is no longer visible, i.e. from onStop() in your Activity.

## Protected methods

### clearViews

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun clearViews(): Unit
```

Clear the list of Views that have been created by this AppWidgetHost. 

### onCreateView

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onCreateView(
    context: Context!, 
    appWidgetId: Int, 
    appWidget: AppWidgetProviderInfo!
): AppWidgetHostView!
```

Called to create the AppWidgetHostView. Override to return a custom subclass if you need it. {@more} 

### onProviderChanged

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onProviderChanged(
    appWidgetId: Int, 
    appWidget: AppWidgetProviderInfo!
): Unit
```

Called when the AppWidget provider for a AppWidget has been upgraded to a new apk. 

### onProvidersChanged

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun onProvidersChanged(): Unit
```

Called when the set of available widgets changes (ie. widget containing packages are added, updated or removed, or widget components are enabled or disabled.)
