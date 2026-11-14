Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# AppWidgetManager

```
open class AppWidgetManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.appwidget.AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#) |

Updates AppWidget state; gets information about installed AppWidget providers and other AppWidget related state.

> [!NOTE]
>
> ### Developer Guides
>
> For more information about creating app widgets, read the [App Widgets](https://developer.android.com/guide/topics/appwidgets/index.html) developer guide.

. 
Requires the `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#FEATURE_APP_WIDGETS:kotlin.String` feature which can be detected using `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#hasSystemFeature(kotlin.String)`.

<br />

## Summary

| Constants ||
|---|---|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_BIND:kotlin.String` Activity action to launch from your `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost` activity when you want to bind an AppWidget to display and bindAppWidgetIdIfAllowed returns false. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_CONFIGURE:kotlin.String` Sent when it is time to configure your AppWidget while it is being added to a host. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DELETED:kotlin.String` Sent when an instance of an AppWidget is deleted from its host. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DISABLED:kotlin.String` Sent when the last AppWidget of this provider is removed from the last host. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_ENABLED:kotlin.String` Sent when an instance of an AppWidget is added to a host for the first time. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_HOST_RESTORED:kotlin.String` Sent to widget hosts after AppWidget state related to the host has been restored from backup. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_OPTIONS_CHANGED:kotlin.String` Sent when the custom extras for an AppWidget change. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_PICK:kotlin.String` Activity action to launch from your `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost` activity when you want to pick an AppWidget to display. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String` Sent to an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider` after AppWidget state related to that provider has been restored from backup. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` Sent when it is time to update your AppWidget. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String` An intent extra (int) that contains one appWidgetId. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_IDS:kotlin.String` An intent extra that contains multiple appWidgetIds. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_OLD_IDS:kotlin.String` An intent extra that contains multiple appWidgetIds. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_OPTIONS:kotlin.String` An intent extra which points to a bundle of extra information for a particular widget id. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_PREVIEW:kotlin.String` An extra that can be passed to `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#requestPinAppWidget(android.content.ComponentName,%20android.os.Bundle,%20android.app.PendingIntent)`. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_PROVIDER:kotlin.String` An intent extra that contains the component name of a AppWidget provider. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_PROVIDER_PROFILE:kotlin.String` An intent extra that contains the user handle of the profile under which an AppWidget provider is registered. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_CUSTOM_EXTRAS:kotlin.String` An intent extra to pass to the AppWidget picker containing a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` objects to mix in to the list of AppWidgets that are installed. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_CUSTOM_INFO:kotlin.String` An intent extra to pass to the AppWidget picker containing a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo` objects to mix in to the list of AppWidgets that are installed. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_HOST_ID:kotlin.String` An intent extra attached to the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_HOST_RESTORED:kotlin.String` broadcast, indicating the integer ID of the host whose widgets have just been restored. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#INVALID_APPWIDGET_ID:kotlin.Int` A sentinel value that the AppWidget manager will never return as a appWidgetId. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#META_DATA_APPWIDGET_PROVIDER:kotlin.String` Field for the manifest meta-data tag. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_DISPLAY_ID:kotlin.String` A bundle extra (int) that indicates which display the widget is currently being displayed on. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_HOST_CATEGORY:kotlin.String` A bundle extra that hints to the AppWidgetProvider the category of host that owns this this widget. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MAX_HEIGHT:kotlin.String` A bundle extra (int) that contains the upper bound on the current width, in dips, of a widget instance. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MAX_WIDTH:kotlin.String` A bundle extra (int) that contains the upper bound on the current width, in dips, of a widget instance. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MIN_HEIGHT:kotlin.String` A bundle extra (int) that contains the lower bound on the current height, in dips, of a widget instance. |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MIN_WIDTH:kotlin.String` A bundle extra (int) that contains the lower bound on the current width, in dips, of a widget instance. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_RESTORE_COMPLETED:kotlin.String` A bundle extra (boolean) that contains whether or not an app has finished restoring a widget. |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_SIZES:kotlin.String` A bundle extra (`List<SizeF>`) that contains the list of possible sizes, in dips, a widget instance can take. |
| --- | --- |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#bindAppWidgetIdIfAllowed(kotlin.Int,%20android.content.ComponentName)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Set the component for a given appWidgetId. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#bindAppWidgetIdIfAllowed(kotlin.Int,%20android.content.ComponentName,%20android.os.Bundle)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Set the component for a given appWidgetId. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#bindAppWidgetIdIfAllowed(kotlin.Int,%20android.os.UserHandle,%20android.content.ComponentName,%20android.os.Bundle)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, user: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#!, provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Set the provider for a given appWidgetId if the caller has a permission. |
| --- | --- |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getAppWidgetIds(android.content.ComponentName)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!)` Get the list of appWidgetIds that have been bound to the given AppWidget provider. |
| open [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getAppWidgetInfo(kotlin.Int)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo` for the specified AppWidget. |
| open [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getAppWidgetOptions(kotlin.Int)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the extras associated with a given widget instance. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)!\>! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getInstalledProviders()()` Return a list of the AppWidget providers that are currently installed. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)!\> | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getInstalledProvidersForPackage(kotlin.String,%20android.os.UserHandle)(packageName: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html, profile: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#?)` Gets the AppWidget providers for the given package and user profile. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppWidgetProviderInfo](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo)!\> | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getInstalledProvidersForProfile(android.os.UserHandle)(profile: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#?)` Gets the AppWidget providers for the given user profile. |
| --- | --- |
| open static [AppWidgetManager](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#)! | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getInstance(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` Get the AppWidgetManager instance to use for the supplied `https://developer.android.com/reference/kotlin/android/content/Context.html#` object. |
| open [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)? | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getWidgetPreview(android.content.ComponentName,%20android.os.UserHandle,%20kotlin.Int)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, profile: https://developer.android.com/reference/kotlin/android/os/UserHandle.html#?, widgetCategory: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get the RemoteViews previews for this widget. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#isRequestPinAppWidgetSupported()()` Returns `true` if the default launcher supports `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#requestPinAppWidget(android.content.ComponentName,%20android.os.Bundle,%20android.app.PendingIntent)`. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#notifyAppWidgetViewDataChanged(kotlin.Int,%20kotlin.Int)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, viewId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Notifies the specified collection view in the specified AppWidget instance to invalidate its data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#notifyAppWidgetViewDataChanged(kotlin.IntArray,%20kotlin.Int)(appWidgetIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, viewId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Notifies the specified collection view in all the specified AppWidget instances to invalidate their data. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.Int,%20android.widget.RemoteViews)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, views: https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#!)` Perform an incremental update or command on the widget specified by appWidgetId. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)(appWidgetIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, views: https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#!)` Perform an incremental update or command on the widget(s) specified by appWidgetIds. |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [AppWidgetEvent](https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent)!\> | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#queryAppWidgetEvents(kotlin.Long,%20kotlin.Long)(beginTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, endTime: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Query for app widget interaction events in the given time range. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#removeWidgetPreview(android.content.ComponentName,%20kotlin.Int)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, widgetCategories: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Remove this provider's preview for the specified widget categories. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#requestPinAppWidget(android.content.ComponentName,%20android.os.Bundle,%20android.app.PendingIntent)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, extras: https://developer.android.com/reference/kotlin/android/os/Bundle.html#?, successCallback: https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#?)` Request to pin an app widget on the current launcher. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#setWidgetPreview(android.content.ComponentName,%20kotlin.Int,%20android.widget.RemoteViews)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#, widgetCategories: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, preview: https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)` Set a preview for this widget. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(android.content.ComponentName,%20android.widget.RemoteViews)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, views: https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#!)` Set the RemoteViews to use for all AppWidget instances for the supplied AppWidget provider. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.Int,%20android.widget.RemoteViews)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, views: https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#!)` Set the RemoteViews to use for the specified appWidgetId. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)(appWidgetIds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html!, views: https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#!)` Set the RemoteViews to use for the specified appWidgetIds. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetOptions(kotlin.Int,%20android.os.Bundle)(appWidgetId: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, options: https://developer.android.com/reference/kotlin/android/os/Bundle.html#!)` Update the extras for a given widget instance. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetProviderInfo(android.content.ComponentName,%20kotlin.String)(provider: https://developer.android.com/reference/kotlin/android/content/ComponentName.html#!, metaDataKey: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html?)` Updates the info for the supplied AppWidget provider. |

## Constants

### ACTION_APPWIDGET_BIND

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_BIND: String
```

Activity action to launch from your `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost` activity when you want to bind an AppWidget to display and bindAppWidgetIdIfAllowed returns false.

You must supply the following extras:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String` | A newly allocated appWidgetId, which will be bound to the AppWidget provider you provide. |
| --- | --- |
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_PROVIDER:kotlin.String` | The BroadcastReceiver that will be the AppWidget provider for this AppWidget. |
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_PROVIDER_PROFILE:kotlin.String` | An optional handle to a user profile under which runs the provider for this AppWidget. |

The system will respond with an onActivityResult call with the following extras in the intent:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String` | The appWidgetId that you supplied in the original intent. |
| --- | --- |

When you receive the result from the AppWidget bind activity, if the resultCode is `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, the AppWidget has been bound. You should then check the AppWidgetProviderInfo for the returned AppWidget, and if it has one, launch its configuration activity. If `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` is returned, you should delete the appWidgetId.

 Value: "android.appwidget.action.APPWIDGET_BIND"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_CONFIGURE:kotlin.String`

### ACTION_APPWIDGET_CONFIGURE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_CONFIGURE: String
```

Sent when it is time to configure your AppWidget while it is being added to a host. This action is not sent as a broadcast to the AppWidget provider, but as a startActivity to the activity specified in the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo`.

The intent will contain the following extras:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String` | The appWidgetId to configure. |
| --- | --- |

If you return `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int` using android.app.Activity#setResult, the AppWidget will be added, and you will receive an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast for this AppWidget. If you return `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int`, the host will cancel the add and not display this AppWidget, and you will receive a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_DELETED:kotlin.String` broadcast.

 Value: "android.appwidget.action.APPWIDGET_CONFIGURE"

### ACTION_APPWIDGET_DELETED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_DELETED: String
```

Sent when an instance of an AppWidget is deleted from its host.

This is a protected intent that can only be sent by the system.

 Value: "android.appwidget.action.APPWIDGET_DELETED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onDeleted(android.content.Context,%20kotlin.IntArray)`

### ACTION_APPWIDGET_DISABLED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_DISABLED: String
```

Sent when the last AppWidget of this provider is removed from the last host.

This is a protected intent that can only be sent by the system.

 Value: "android.appwidget.action.APPWIDGET_DISABLED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onEnabled(android.content.Context)`

### ACTION_APPWIDGET_ENABLED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_ENABLED: String
```

Sent when an instance of an AppWidget is added to a host for the first time. This broadcast is sent at boot time if there is a AppWidgetHost installed with an instance for this provider.

This is a protected intent that can only be sent by the system.

 Value: "android.appwidget.action.APPWIDGET_ENABLED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onEnabled(android.content.Context)`

### ACTION_APPWIDGET_HOST_RESTORED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_HOST_RESTORED: String
```

Sent to widget hosts after AppWidget state related to the host has been restored from backup. The intent contains information about how to translate AppWidget ids from the restored data to their new equivalents. If an application maintains multiple separate widget host instances, it will receive this broadcast separately for each one.

The intent will contain the following extras:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_OLD_IDS:kotlin.String` | The set of appWidgetIds represented in a restored backup that have been successfully incorporated into the current environment. This may be all of the AppWidgets known to this application, or just a subset. Each entry in this array of appWidgetIds has a corresponding entry in the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_IDS:kotlin.String` extra. |
| --- | --- |
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_IDS:kotlin.String` | The set of appWidgetIds now valid for this application. The app should look at its restored widget configuration and translate each appWidgetId in the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_OLD_IDS:kotlin.String` array to its new value found at the corresponding index within this array. |
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_HOST_ID:kotlin.String` | The integer ID of the widget host instance whose state has just been restored. |

This is a protected intent that can only be sent by the system.

 Value: "android.appwidget.action.APPWIDGET_HOST_RESTORED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String`

### ACTION_APPWIDGET_OPTIONS_CHANGED

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_OPTIONS_CHANGED: String
```

Sent when the custom extras for an AppWidget change.

This is a protected intent that can only be sent by the system.

 Value: "android.appwidget.action.APPWIDGET_UPDATE_OPTIONS"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onAppWidgetOptionsChanged(android.content.Context,%20android.appwidget.AppWidgetManager,%20kotlin.Int,%20android.os.Bundle)`

### ACTION_APPWIDGET_PICK

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_PICK: String
```

Activity action to launch from your `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetHost` activity when you want to pick an AppWidget to display. The AppWidget picker activity will be launched.

You must supply the following extras:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String` | A newly allocated appWidgetId, which will be bound to the AppWidget provider once the user has selected one. |
| --- | --- |

The system will respond with an onActivityResult call with the following extras in the intent:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String` | The appWidgetId that you supplied in the original intent. |
| --- | --- |

When you receive the result from the AppWidget pick activity, if the resultCode is `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_OK:kotlin.Int`, an AppWidget has been selected. You should then check the AppWidgetProviderInfo for the returned AppWidget, and if it has one, launch its configuration activity. If `https://developer.android.com/reference/kotlin/android/app/Activity.html#RESULT_CANCELED:kotlin.Int` is returned, you should delete the appWidgetId.

 Value: "android.appwidget.action.APPWIDGET_PICK"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_CONFIGURE:kotlin.String`

### ACTION_APPWIDGET_RESTORED

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_RESTORED: String
```

Sent to an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider` after AppWidget state related to that provider has been restored from backup. The intent contains information about how to translate AppWidget ids from the restored data to their new equivalents.

The intent will contain the following extras:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_OLD_IDS:kotlin.String` | The set of appWidgetIds represented in a restored backup that have been successfully incorporated into the current environment. This may be all of the AppWidgets known to this application, or just a subset. Each entry in this array of appWidgetIds has a corresponding entry in the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_IDS:kotlin.String` extra. |
| --- | --- |
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_IDS:kotlin.String` | The set of appWidgetIds now valid for this application. The app should look at its restored widget configuration and translate each appWidgetId in the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_OLD_IDS:kotlin.String` array to its new value found at the corresponding index within this array. |

This is a protected intent that can only be sent by the system.

 Value: "android.appwidget.action.APPWIDGET_RESTORED"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_HOST_RESTORED:kotlin.String`

### ACTION_APPWIDGET_UPDATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val ACTION_APPWIDGET_UPDATE: String
```

Sent when it is time to update your AppWidget.

This may be sent in response to a new instance for this AppWidget provider having been instantiated, the requested `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#updatePeriodMillis:kotlin.Int` having lapsed, or the system booting.

The intent will contain the following extras:

| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_IDS:kotlin.String` | The appWidgetIds to update. This may be all of the AppWidgets created for this provider, or just a subset. The system tries to send updates for as few AppWidget instances as possible. |
| --- | --- |

 Value: "android.appwidget.action.APPWIDGET_UPDATE"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProvider#onUpdate(android.content.Context,%20android.appwidget.AppWidgetManager,%20kotlin.IntArray)`

### EXTRA_APPWIDGET_ID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_ID: String
```

An intent extra (int) that contains one appWidgetId.

The value will be an int that can be retrieved like this:

 Value: "appWidgetId"

### EXTRA_APPWIDGET_IDS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_IDS: String
```

An intent extra that contains multiple appWidgetIds.

The value will be an int array that can be retrieved like this:

 Value: "appWidgetIds"

### EXTRA_APPWIDGET_OLD_IDS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_OLD_IDS: String
```

An intent extra that contains multiple appWidgetIds. These are id values as they were provided to the application during a recent restore from backup. It is attached to the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_RESTORED:kotlin.String` broadcast intent.

The value will be an int array that can be retrieved like this:

 Value: "appWidgetOldIds"

### EXTRA_APPWIDGET_OPTIONS

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_OPTIONS: String
```

An intent extra which points to a bundle of extra information for a particular widget id. In particular this bundle can contain `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MIN_WIDTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MIN_HEIGHT:kotlin.String`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MAX_WIDTH:kotlin.String`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#OPTION_APPWIDGET_MAX_HEIGHT:kotlin.String`.

 Value: "appWidgetOptions"

### EXTRA_APPWIDGET_PREVIEW

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_PREVIEW: String
```

An extra that can be passed to `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#requestPinAppWidget(android.content.ComponentName,%20android.os.Bundle,%20android.app.PendingIntent)`. This would allow the launcher app to present a custom preview to the user.

The value should be a `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#` similar to what is used with #updateAppWidget calls.

 Value: "appWidgetPreview"

### EXTRA_APPWIDGET_PROVIDER

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_PROVIDER: String
```

An intent extra that contains the component name of a AppWidget provider.

The value will be an `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#`.

 Value: "appWidgetProvider"

### EXTRA_APPWIDGET_PROVIDER_PROFILE

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_APPWIDGET_PROVIDER_PROFILE: String
```

An intent extra that contains the user handle of the profile under which an AppWidget provider is registered.

The value will be a `https://developer.android.com/reference/kotlin/android/os/UserHandle.html#`.

 Value: "appWidgetProviderProfile"

### EXTRA_CUSTOM_EXTRAS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CUSTOM_EXTRAS: String
```

An intent extra to pass to the AppWidget picker containing a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/os/Bundle.html#` objects to mix in to the list of AppWidgets that are installed. It will be added to the extras object on the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` that is returned from the picker activity. {@more}

 Value: "customExtras"

### EXTRA_CUSTOM_INFO

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_CUSTOM_INFO: String
```

An intent extra to pass to the AppWidget picker containing a `https://developer.android.com/reference/kotlin/java/util/List.html#` of `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo` objects to mix in to the list of AppWidgets that are installed. (This is how the launcher shows the search widget).

 Value: "customInfo"

### EXTRA_HOST_ID

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val EXTRA_HOST_ID: String
```

An intent extra attached to the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_HOST_RESTORED:kotlin.String` broadcast, indicating the integer ID of the host whose widgets have just been restored.

 Value: "hostId"

### INVALID_APPWIDGET_ID

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val INVALID_APPWIDGET_ID: Int
```

A sentinel value that the AppWidget manager will never return as a appWidgetId.

 Value: 0

### META_DATA_APPWIDGET_PROVIDER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val META_DATA_APPWIDGET_PROVIDER: String
```

Field for the manifest meta-data tag.

 Value: "android.appwidget.provider"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo`

### OPTION_APPWIDGET_DISPLAY_ID

Added in [API level 37](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_DISPLAY_ID: String
```

A bundle extra (int) that indicates which display the widget is currently being displayed on. This can be used with `https://developer.android.com/reference/kotlin/android/hardware/display/DisplayManager.html#getDisplay(kotlin.Int)` to retrieve the `https://developer.android.com/reference/kotlin/android/view/Display.html#` and its corresponding `https://developer.android.com/reference/kotlin/android/util/DisplayMetrics.html#`.

 Value: "appWidgetDisplayId"

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/Display.html#getDisplayId()`

### OPTION_APPWIDGET_HOST_CATEGORY

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_HOST_CATEGORY: String
```

A bundle extra that hints to the AppWidgetProvider the category of host that owns this this widget. Can have the value `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_NOT_KEYGUARD:kotlin.Int`.

 Value: "appWidgetCategory"

### OPTION_APPWIDGET_MAX_HEIGHT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_MAX_HEIGHT: String
```

A bundle extra (int) that contains the upper bound on the current width, in dips, of a widget instance.

 Value: "appWidgetMaxHeight"

### OPTION_APPWIDGET_MAX_WIDTH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_MAX_WIDTH: String
```

A bundle extra (int) that contains the upper bound on the current width, in dips, of a widget instance.

 Value: "appWidgetMaxWidth"

### OPTION_APPWIDGET_MIN_HEIGHT

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_MIN_HEIGHT: String
```

A bundle extra (int) that contains the lower bound on the current height, in dips, of a widget instance.

 Value: "appWidgetMinHeight"

### OPTION_APPWIDGET_MIN_WIDTH

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_MIN_WIDTH: String
```

A bundle extra (int) that contains the lower bound on the current width, in dips, of a widget instance.

 Value: "appWidgetMinWidth"

### OPTION_APPWIDGET_RESTORE_COMPLETED

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_RESTORE_COMPLETED: String
```

A bundle extra (boolean) that contains whether or not an app has finished restoring a widget.

After restore, the app should set OPTION_APPWIDGET_RESTORE_COMPLETED to true on its widgets followed by calling #updateAppWidget to update the views.

 Value: "appWidgetRestoreCompleted"

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetOptions(kotlin.Int,%20android.os.Bundle)`

### OPTION_APPWIDGET_SIZES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val OPTION_APPWIDGET_SIZES: String
```

A bundle extra (`List<SizeF>`) that contains the list of possible sizes, in dips, a widget instance can take.

 Value: "appWidgetSizes"

## Public methods

### bindAppWidgetIdIfAllowed

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindAppWidgetIdIfAllowed(
    appWidgetId: Int, 
    provider: ComponentName!
): Boolean
```

Set the component for a given appWidgetId. If successful, the app widget provider will receive a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast.

You need the BIND_APPWIDGET permission or the user must have enabled binding widgets always for your component. Should be used by apps that host widgets; if this method returns false, call `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_BIND:kotlin.String` to request permission to bind

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget id under which to bind the provider. |
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: The `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` that will be the AppWidget provider for this AppWidget. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this component has permission to bind the AppWidget |

### bindAppWidgetIdIfAllowed

Added in [API level 17](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindAppWidgetIdIfAllowed(
    appWidgetId: Int, 
    provider: ComponentName!, 
    options: Bundle!
): Boolean
```

Set the component for a given appWidgetId. If successful, the app widget provider will receive a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast.

You need the BIND_APPWIDGET permission or the user must have enabled binding widgets always for your component. Should be used by apps that host widgets; if this method returns false, call `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_BIND:kotlin.String` to request permission to bind

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget id under which to bind the provider. |
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: The `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` that will be the AppWidget provider for this AppWidget. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: Bundle containing options for the AppWidget. See also `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetOptions(kotlin.Int,%20android.os.Bundle)` |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this component has permission to bind the AppWidget |

### bindAppWidgetIdIfAllowed

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun bindAppWidgetIdIfAllowed(
    appWidgetId: Int, 
    user: UserHandle!, 
    provider: ComponentName!, 
    options: Bundle!
): Boolean
```

Set the provider for a given appWidgetId if the caller has a permission. If successful, the app widget provider will receive a `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast.

**Note:** You need the `https://developer.android.com/reference/kotlin/android/Manifest.permission.html#BIND_APPWIDGET:kotlin.String` permission or the user must have enabled binding widgets always for your component. Should be used by apps that host widgets. If this method returns false, call `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_BIND:kotlin.String` to request permission to bind.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget id under which to bind the provider. |
| `user` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)!: The user id in which the provider resides. |
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: The component name of the provider. |
| --- | --- |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: An optional Bundle containing options for the AppWidget. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this component has permission to bind the AppWidget |

### getAppWidgetIds

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppWidgetIds(provider: ComponentName!): IntArray!
```

Get the list of appWidgetIds that have been bound to the given AppWidget provider.

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: The `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` that is the AppWidget provider to find appWidgetIds for. |

### getAppWidgetInfo

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppWidgetInfo(appWidgetId: Int): AppWidgetProviderInfo!
```

Returns the `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo` for the specified AppWidget.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo!` | Information regarding the provider of speficied widget, returns null if the appWidgetId has not been bound to a provider yet, or you don't have access to that widget. |

### getAppWidgetOptions

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAppWidgetOptions(appWidgetId: Int): Bundle!
```

Get the extras associated with a given widget instance.

The extras can be used to embed additional information about this widget to be accessed by the associated widget's AppWidgetProvider.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget instances for which to set the RemoteViews. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/os/Bundle.html#!` | The options associated with the given widget instance. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidgetOptions(kotlin.Int,%20android.os.Bundle)`

### getInstalledProviders

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledProviders(): MutableList<AppWidgetProviderInfo!>!
```

Return a list of the AppWidget providers that are currently installed.

### getInstalledProvidersForPackage

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledProvidersForPackage(
    packageName: String, 
    profile: UserHandle?
): MutableList<AppWidgetProviderInfo!>
```

Gets the AppWidget providers for the given package and user profile. User profile can only be the current user or a profile of the current user. For example, the current user may have a corporate profile. In this case the parent user profile has a child profile, the corporate one.

| Parameters ||
|---|---|
| `packageName` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html): The package for which to get providers. If null, this method is equivalent to `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getInstalledProvidersForProfile(android.os.UserHandle)`. |
| `profile` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)?: The profile for which to get providers. Passing null is equivalent to querying for only the calling user. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo!>` | The installed providers, or an empty list if none are found for the given package and user. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.NullPointerException` | if the provided package name is null |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Process.html#myUserHandle()`
- `https://developer.android.com/reference/kotlin/android/os/UserManager.html#getUserProfiles()`

### getInstalledProvidersForProfile

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInstalledProvidersForProfile(profile: UserHandle?): MutableList<AppWidgetProviderInfo!>
```

Gets the AppWidget providers for the given user profile. User profile can only be the current user or a profile of the current user. For example, the current user may have a corporate profile. In this case the parent user profile has a child profile, the corporate one.

| Parameters ||
|---|---|
| `profile` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)?: The profile for which to get providers. Passing null is equivalent to querying for only the calling user. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo!>` | The installed providers, or an empty list if none are found for the given user. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/os/Process.html#myUserHandle()`
- `https://developer.android.com/reference/kotlin/android/os/UserManager.html#getUserProfiles()`

### getInstance

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(context: Context!): AppWidgetManager!
```

Get the AppWidgetManager instance to use for the supplied `https://developer.android.com/reference/kotlin/android/content/Context.html#` object.

### getWidgetPreview

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getWidgetPreview(
    provider: ComponentName, 
    profile: UserHandle?, 
    widgetCategory: Int
): RemoteViews?
```

Get the RemoteViews previews for this widget.

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for the `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` provider for the AppWidget you intend to get a preview for. This value cannot be `null`. |
| `profile` | [UserHandle](https://developer.android.com/reference/kotlin/android/os/UserHandle.html#)?: The profile in which the provider resides. Passing null is equivalent to querying for only the calling user. |
| `widgetCategory` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The widget category for which you want to display previews. This should be a single category. If a combination of categories is provided, this function will return a preview that matches at least one of the categories. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_NOT_KEYGUARD:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#?` | The widget preview for the selected category, if available. This value may be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#generatedPreviewCategories:kotlin.Int`

### isRequestPinAppWidgetSupported

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isRequestPinAppWidgetSupported(): Boolean
```

Returns `true` if the default launcher supports `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#requestPinAppWidget(android.content.ComponentName,%20android.os.Bundle,%20android.app.PendingIntent)`.

Returns `false` if the default launcher does not support pinning, or if App Lock is currently enabled for the calling app. App Lock is a feature that allows users to require authentication before opening apps (see `https://developer.android.com/reference/kotlin/android/content/pm/PackageManager.html#getEnableAppLockIntentForPackage(kotlin.String,%20kotlin.Boolean)`). Applications presenting UI options to add widgets to the home screen should re-query this method when returning to the foreground (e.g. in `https://developer.android.com/reference/kotlin/android/app/Activity.html#onResume()`) to update option visibility.

### notifyAppWidgetViewDataChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyAppWidgetViewDataChanged(
    appWidgetId: Int, 
    viewId: Int
): Unit
```

**Deprecated:** *The corresponding API `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setRemoteAdapter(kotlin.Int,%20android.content.Intent)` associated with this method has been deprecated. Moving forward please use `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setRemoteAdapter(kotlin.Int,%20android.widget.RemoteViews.RemoteCollectionItems)` instead to set `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteCollectionItems.html#` for the remote adapter and update the widget views by calling `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.Int,%20android.widget.RemoteViews)`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(android.content.ComponentName,%20android.widget.RemoteViews)`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`, or `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.Int,%20android.widget.RemoteViews)`, whichever applicable.*

Notifies the specified collection view in the specified AppWidget instance to invalidate its data.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget instance to notify of view data changes. |
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The collection view id. |

### notifyAppWidgetViewDataChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun notifyAppWidgetViewDataChanged(
    appWidgetIds: IntArray!, 
    viewId: Int
): Unit
```

**Deprecated:** *The corresponding API `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setRemoteAdapter(kotlin.Int,%20android.content.Intent)` associated with this method has been deprecated. Moving forward please use `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setRemoteAdapter(kotlin.Int,%20android.widget.RemoteViews.RemoteCollectionItems)` instead to set `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteCollectionItems.html#` for the remote adapter and update the widget views by calling `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.Int,%20android.widget.RemoteViews)`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(android.content.ComponentName,%20android.widget.RemoteViews)`, `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`, or `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.Int,%20android.widget.RemoteViews)`, whichever applicable.*

Notifies the specified collection view in all the specified AppWidget instances to invalidate their data.

| Parameters ||
|---|---|
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The AppWidget instances to notify of view data changes. |
| `viewId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The collection view id. |

### partiallyUpdateAppWidget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun partiallyUpdateAppWidget(
    appWidgetId: Int, 
    views: RemoteViews!
): Unit
```

Perform an incremental update or command on the widget specified by appWidgetId.

This update differs from `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.Int,%20android.widget.RemoteViews)` in that the RemoteViews object which is passed is understood to be an incomplete representation of the widget, and hence is not cached by the AppWidgetService. Note that because these updates are not cached, any state that they modify that is not restored by restoreInstanceState will not persist in the case that the widgets are restored using the cached version in AppWidgetService. Use with `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#showNext(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#showPrevious(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setScrollPosition(kotlin.Int,%20kotlin.Int)` and similar commands.

It is okay to call this method both inside an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast, and outside of the handler. This method will only work when called from the uid that owns the AppWidget provider.

This method will be ignored if a widget has not received a full update via `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget instance for which to set the RemoteViews. |
| `views` | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)!: The RemoteViews object containing the incremental update / command. |

### partiallyUpdateAppWidget

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun partiallyUpdateAppWidget(
    appWidgetIds: IntArray!, 
    views: RemoteViews!
): Unit
```

Perform an incremental update or command on the widget(s) specified by appWidgetIds.

This update differs from `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)` in that the RemoteViews object which is passed is understood to be an incomplete representation of the widget, and hence does not replace the cached representation of the widget. As of API level 17, the new properties set within the views objects will be appended to the cached representation of the widget, and hence will persist. Use with `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#showNext(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#showPrevious(kotlin.Int)`, `https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setScrollPosition(kotlin.Int,%20kotlin.Int)` and similar commands.

It is okay to call this method both inside an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast, and outside of the handler. This method will only work when called from the uid that owns the AppWidget provider.

This method will be ignored if a widget has not received a full update via `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#updateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`.

| Parameters ||
|---|---|
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The AppWidget instances for which to set the RemoteViews. |
| `views` | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)!: The RemoteViews object containing the incremental update / command. |

### queryAppWidgetEvents

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun queryAppWidgetEvents(
    beginTime: Long, 
    endTime: Long
): MutableList<AppWidgetEvent!>
```

Query for app widget interaction events in the given time range. Events are only kept by the system for a few days. This method only returns events for widgets provided by the calling package and does not require any additional permissions.

| Parameters ||
|---|---|
| `beginTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The inclusive beginning of the range of events to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |
| `endTime` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The exclusive end of the range of events to include in the results. Defined in terms of "Unix time", see `https://developer.android.com/reference/kotlin/java/lang/System.html#currentTimeMillis()`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent!>` | An array of `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetEvent` objects. This value cannot be `null`. |

### removeWidgetPreview

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun removeWidgetPreview(
    provider: ComponentName, 
    widgetCategories: Int
): Unit
```

Remove this provider's preview for the specified widget categories. If the provider does not have a preview for the specified widget category, this is a no-op.

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The AppWidgetProvider to remove previews for. This value cannot be `null`. |
| `widgetCategories` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The categories of the preview to remove. For example, removing the preview for WIDGET_CATEGORY_HOME_SCREEN | WIDGET_CATEGORY_KEYGUARD will remove the previews for both categories. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_NOT_KEYGUARD:kotlin.Int` |

### requestPinAppWidget

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun requestPinAppWidget(
    provider: ComponentName, 
    extras: Bundle?, 
    successCallback: PendingIntent?
): Boolean
```

Request to pin an app widget on the current launcher. It's up to the launcher to accept this request (optionally showing a user confirmation). If the request is accepted, the caller will get a confirmation with extra `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_ID:kotlin.String`.

When a request is denied by the user, the caller app will not get any response.

Only apps with a foreground activity or a foreground service can call it. Otherwise it'll throw `https://developer.android.com/reference/kotlin/java/lang/IllegalStateException.html#`.

It's up to the launcher how to handle previous pending requests when the same package calls this API multiple times in a row. It may ignore the previous requests, for example.

Launcher will not show the configuration activity associated with the provider in this case. The app could either show the configuration activity as a response to the callback, or show if before calling the API (various configurations can be encapsulated in `successCallback` to avoid persisting them before the widgetId is known).

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for the `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` provider for your AppWidget. This value cannot be `null`. |
| `extras` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)?: IF not null, this is passed to the launcher app. e.g. `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#EXTRA_APPWIDGET_PREVIEW:kotlin.String` can be used for a custom preview. |
| `successCallback` | [PendingIntent](https://developer.android.com/reference/kotlin/android/app/PendingIntent.html#)?: If not null, this intent will be sent when the widget is created. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if the launcher supports this feature. Note the API will return without waiting for the user to respond, so getting `true` from this API does \*not\* mean the shortcut is pinned. `false` if the launcher doesn't support this feature or if calling app belongs to a user-profile with items restricted on home screen. If App Lock is enabled for the calling app, this method will fail and return `false`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalStateException` | The caller doesn't have a foreground activity or a foreground service or when the user is locked. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#isRequestPinShortcutSupported()`
- `https://developer.android.com/reference/kotlin/android/content/pm/ShortcutManager.html#requestPinShortcut(android.content.pm.ShortcutInfo,%20android.content.IntentSender)`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#isRequestPinAppWidgetSupported()`

### setWidgetPreview

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWidgetPreview(
    provider: ComponentName, 
    widgetCategories: Int, 
    preview: RemoteViews
): Boolean
```

Set a preview for this widget. This preview will be used instead of the provider's `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#previewLayout:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#previewImage:kotlin.Int` for previewing the widget in the widget picker and pin app widget flow.

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#): The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for the `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` provider for the AppWidget you intend to provide a preview for. This value cannot be `null`. |
| `widgetCategories` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The categories that this preview should be used for. This can be a single category or combination of categories. If multiple categories are specified, then this preview will be used for each of those categories. For example, if you set a preview for WIDGET_CATEGORY_HOME_SCREEN | WIDGET_CATEGORY_KEYGUARD, the preview will be used when picking widgets for the home screen and keyguard. Note: You should only use the widget categories that the provider supports, as defined in `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#widgetCategory:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_NOT_KEYGUARD:kotlin.Int` |
| `preview` | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#): This preview will be used for previewing the provider when picking widgets for the selected categories. This value cannot be `null`. |
| --- | --- |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the call was successful, false if it was rate-limited. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_HOME_SCREEN:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_KEYGUARD:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetProviderInfo#WIDGET_CATEGORY_SEARCHBOX:kotlin.Int`

### updateAppWidget

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAppWidget(
    provider: ComponentName!, 
    views: RemoteViews!
): Unit
```

Set the RemoteViews to use for all AppWidget instances for the supplied AppWidget provider.

It is okay to call this method both inside an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast, and outside of the handler. This method will only work when called from the uid that owns the AppWidget provider.

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: The `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for the `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` provider for your AppWidget. |
| `views` | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)!: The RemoteViews object to show. |

### updateAppWidget

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAppWidget(
    appWidgetId: Int, 
    views: RemoteViews!
): Unit
```

Set the RemoteViews to use for the specified appWidgetId.

Note that the RemoteViews parameter will be cached by the AppWidgetService, and hence should contain a complete representation of the widget. For performing partial widget updates, see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.Int,%20android.widget.RemoteViews)`.

It is okay to call this method both inside an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast, and outside of the handler. This method will only work when called from the uid that owns the AppWidget provider.

The combined memory used by the Bitmaps and Icons in the RemoteViews object must not exceed memory that is required to fill the screen 1.5 times, ie. (screen width x screen height x 4 x 1.5) bytes. Starting in Android 17 (SDK 37) an error will be thrown.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget instance for which to set the RemoteViews. |
| `views` | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)!: The RemoteViews object to show. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the combined memory used by Bitmaps and Icons in `views` exceeds the maximum limit. |

### updateAppWidget

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAppWidget(
    appWidgetIds: IntArray!, 
    views: RemoteViews!
): Unit
```

Set the RemoteViews to use for the specified appWidgetIds.

Note that the RemoteViews parameter will be cached by the AppWidgetService, and hence should contain a complete representation of the widget. For performing partial widget updates, see `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#partiallyUpdateAppWidget(kotlin.IntArray,%20android.widget.RemoteViews)`.

It is okay to call this method both inside an `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#ACTION_APPWIDGET_UPDATE:kotlin.String` broadcast, and outside of the handler. This method will only work when called from the uid that owns the AppWidget provider.

The combined memory used by the Bitmaps and Icons in the RemoteViews object must not exceed memory that is required to fill the screen 1.5 times, ie. (screen width x screen height x 4 x 1.5) bytes. Starting in Android 17 (SDK 37) an error will be thrown.

| Parameters ||
|---|---|
| `appWidgetIds` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The AppWidget instances for which to set the RemoteViews. |
| `views` | [RemoteViews](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#)!: The RemoteViews object to show. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the combined memory used by Bitmaps and Icons in `views` exceeds the maximum limit. |

### updateAppWidgetOptions

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAppWidgetOptions(
    appWidgetId: Int, 
    options: Bundle!
): Unit
```

Update the extras for a given widget instance.

The extras can be used to embed additional information about this widget to be accessed by the associated widget's AppWidgetProvider.

The new options are merged into existing options using android.os.Bundle#putAll semantics.

| Parameters ||
|---|---|
| `appWidgetId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The AppWidget instances for which to set the RemoteViews. |
| `options` | [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)!: The options to associate with this widget |

**See Also**

- `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#getAppWidgetOptions(kotlin.Int)`

### updateAppWidgetProviderInfo

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun updateAppWidgetProviderInfo(
    provider: ComponentName!, 
    metaDataKey: String?
): Unit
```

Updates the info for the supplied AppWidget provider. Apps can use this to change the default behavior of the widget based on the state of the app (for e.g., if the user is logged in or not). Calling this API completely replaces the previous definition.

The manifest entry of the provider should contain an additional meta-data tag similar to `https://developer.android.com/reference/kotlin/android/appwidget/AppWidgetManager#META_DATA_APPWIDGET_PROVIDER:kotlin.String` which should point to any alternative definitions for the provider.

This is persisted across device reboots and app updates. If this meta-data key is not present in the manifest entry, the info reverts to default.

| Parameters ||
|---|---|
| `provider` | [ComponentName](https://developer.android.com/reference/kotlin/android/content/ComponentName.html#)!: `https://developer.android.com/reference/kotlin/android/content/ComponentName.html#` for the `https://developer.android.com/reference/kotlin/android/content/BroadcastReceiver.html#` provider for your AppWidget. |
| `metaDataKey` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)?: key for the meta-data tag pointing to the new provider info. Use null to reset any previously set info. |
