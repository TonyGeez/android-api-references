Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRouteActionProvider

Kotlin | [Java](MediaRouteActionProvider.md)
| --- | --- |

```
open class MediaRouteActionProvider : ActionProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.ActionProvider](../android.view/ActionProvider.md) ||
| | ↳ | [android.app.MediaRouteActionProvider](MediaRouteActionProvider.md) |

The media route action provider displays a MediaRouteButton in the application's ActionBar to allow the user to select routes and to control the currently selected route.

The application must specify the kinds of routes that the user should be allowed to select by specifying the route types with the setRouteTypes method.

Refer to MediaRouteButton for a description of the button that will appear in the action bar menu. Note that instead of disabling the button when no routes are available, the action provider will instead make the menu item invisible. In this way, the button will only be visible when it is possible for the user to discover and select a matching route.

## Summary

| Public constructors ||
|---|---|
| MediaRouteActionProvider <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | isVisible If overridesItemVisibility returns true, the return value of this method will help determine the visibility of the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to. |
| open [View](../android.view/View.md) | onCreateActionView Factory method called by the Android framework to create new action views. |
| open [View](../android.view/View.md) | onCreateActionView Factory method called by the Android framework to create new action views. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onPerformDefaultAction Performs an optional default action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | overridesItemVisibility The result of this method determines whether or not isVisible will be used by the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to help determine its visibility. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setExtendedSettingsClickListener <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setRouteTypes Sets the types of routes that will be shown in the media route chooser dialog launched by this button. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | hasSubMenu Determines if this ActionProvider has a submenu associated with it. Associated submenus will be shown when an action view is not. This provider instance will receive a call to onPrepareSubMenu after the call to onPerformDefaultAction and before a submenu is displayed to the user. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | onPrepareSubMenu Called to prepare an associated submenu for the menu item backed by this ActionProvider. if hasSubMenu returns true, this method will be called when the menu item is selected to prepare the submenu for presentation to the user. Apps may use this to create or alter submenu content right before display. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | refreshVisibility If this ActionProvider is associated with an item in a menu, refresh the visibility of the item based on overridesItemVisibility and isVisible. If overridesItemVisibility returns false, this call will have no effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | setVisibilityListener Set a listener to be notified when this ActionProvider's overridden visibility changes. This should only be used by MenuItem implementations. <br /> | ||

## Public constructors

### MediaRouteActionProvider

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
MediaRouteActionProvider(context: Context!)
```

## Public methods

### isVisible

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVisible(): Boolean
```

If overridesItemVisibility returns true, the return value of this method will help determine the visibility of the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to.

If the MenuItem's visibility is explicitly set to false by the application, the MenuItem will not be shown, even if this method returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the MenuItem this ActionProvider is bound to is visible, false if it is invisible. The default implementation returns true. |

### onCreateActionView

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateActionView(): View
```

Factory method called by the Android framework to create new action views.

This method has been deprecated in favor of onCreateActionView. Newer apps that wish to support platform versions prior to API 16 should also implement this method to return a valid action view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#` | A new action view. This value cannot be `null`. |

### onCreateActionView

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateActionView(item: MenuItem): View
```

Factory method called by the Android framework to create new action views. This method returns a new action view for the given MenuItem.

If your ActionProvider implementation overrides the deprecated no-argument overload onCreateActionView, overriding this method for devices running API 16 or later is recommended but optional. The default implementation calls onCreateActionView for compatibility with applications written for older platform versions.

| Parameters ||
|---|---|
| `forItem` | MenuItem to create the action view for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#` | the new action view. This value cannot be `null`. |

### onPerformDefaultAction

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPerformDefaultAction(): Boolean
```

Performs an optional default action.

For the case of an action provider placed in a menu item not shown as an action this method is invoked if previous callbacks for processing menu selection has handled the event.

A menu item selection is processed in the following order:

- Receiving a call to onMenuItemClick.
- Receiving a call to onOptionsItemSelected
- Receiving a call to onOptionsItemSelected
- Launching the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` set via setIntent
- Invoking this method.

<br />

The default implementation does not perform any action and returns false.

### overridesItemVisibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun overridesItemVisibility(): Boolean
```

The result of this method determines whether or not isVisible will be used by the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to help determine its visibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this ActionProvider overrides the visibility of the MenuItem it is bound to, false otherwise. The default implementation returns false. |

### setExtendedSettingsClickListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setExtendedSettingsClickListener(listener: View.OnClickListener!): Unit
```

### setRouteTypes

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setRouteTypes(types: Int): Unit
```

Sets the types of routes that will be shown in the media route chooser dialog launched by this button.

| Parameters ||
|---|---|
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The route types to match. |
