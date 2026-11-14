# AppWidgetHost

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetHost

Kotlin| [Java](AppWidgetHost.md) 
| --- | --- |

```
open class AppWidgetHost
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.appwidget.AppWidgetHost](AppWidgetHost.md) |

AppWidgetHost provides the interaction with the AppWidget service for apps, like the home screen, that want to embed AppWidgets in their UI.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [AppWidgetHost](AppWidgetHost.md))`(`context:` ` [Context](../android.content/Context.md)!`, `hostId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [allocateAppWidgetId](AppWidgetHost.md))`()` Get a appWidgetId for a host in the calling process. |
| [AppWidgetHostView](AppWidgetHostView.md)! | [createView](AppWidgetHost.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appWidget:` ` [AppWidgetProviderInfo](AppWidgetProviderInfo.md)!`)` Create the AppWidgetHostView for the given widget. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteAllHosts](AppWidgetHost.md))`()` Remove all records about all hosts for your package. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteAppWidgetId](AppWidgetHost.md))`(`appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Stop listening to changes for this AppWidget. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [deleteHost](AppWidgetHost.md))`()` Remove all records about this host from the AppWidget manager. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | [getAppWidgetIds](AppWidgetHost.md))`()` Gets a list of all the appWidgetIds that are bound to the current host |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onAppWidgetRemoved](AppWidgetHost.md))`(`appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the app widget is removed for appWidgetId |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startAppWidgetConfigureActivityForResult](AppWidgetHost.md))`(`activity:` ` [Activity](../android.app/Activity.md)`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `intentFlags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `requestCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `options:` ` [Bundle](../android.os/Bundle.md)?`)` Starts an app widget provider configure activity for result on behalf of the caller. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [startListening](AppWidgetHost.md))`()` Start receiving onAppWidgetChanged calls for your AppWidgets. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [stopListening](AppWidgetHost.md))`()` Stop receiving onAppWidgetChanged calls for your AppWidgets. |

| Protected methods ||
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearViews](AppWidgetHost.md))`()` Clear the list of Views that have been created by this AppWidgetHost. |
| open [AppWidgetHostView](AppWidgetHostView.md)! | [onCreateView](AppWidgetHost.md))`(`context:` ` [Context](../android.content/Context.md)!`, `appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appWidget:` ` [AppWidgetProviderInfo](AppWidgetProviderInfo.md)!`)` Called to create the AppWidgetHostView. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProviderChanged](AppWidgetHost.md))`(`appWidgetId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `appWidget:` ` [AppWidgetProviderInfo](AppWidgetProviderInfo.md)!`)` Called when the AppWidget provider for a AppWidget has been upgraded to a new apk. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onProvidersChanged](AppWidgetHost.md))`()` Called when the set of available widgets changes (ie. widget containing packages are added, updated or removed, or widget components are enabled or disabled.) |

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

Starts an app widget provider configure activity for result on behalf of the caller. Use this method if the provider is in another profile as you are not allowed to start an activity in another profile. You can optionally provide a request code that is returned in [Activity.onActivityResult(int, int, android.content.Intent)](../android.app/Activity.md))and an options bundle to be passed to the started activity.

Note that the provided app widget has to be bound for this method to work.

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `activity` | [Activity](../android.app/Activity.md):The activity from which to start the configure one. This value cannot be`null`. |
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The bound app widget whose provider's config activity to start. |
| `requestCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional request code retuned with the result. |
| --- | --- |
| `intentFlags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Optional intent flags. |
| `options` | [Bundle](../android.os/Bundle.md)?:This value may be`null`. |

| Exceptions ||
|---------------------------------------------|-------------------------------|
| `android.content.ActivityNotFoundException` | If the activity is not found. |

**See Also**

- [android.appwidget.AppWidgetProviderInfo#getProfile()](AppWidgetProviderInfo.md)) 

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
