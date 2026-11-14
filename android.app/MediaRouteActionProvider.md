Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MediaRouteActionProvider

Kotlin | [Java](https://developer.android.com/reference/android/app/MediaRouteActionProvider "View this page in Java")

```
open class MediaRouteActionProvider : ActionProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.view.ActionProvider](https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#) ||
| | ↳ | [android.app.MediaRouteActionProvider](https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#) |

The media route action provider displays a `https://developer.android.com/reference/kotlin/android/app/MediaRouteButton` in the application's `https://developer.android.com/reference/kotlin/android/app/ActionBar` to allow the user to select routes and to control the currently selected route.

The application must specify the kinds of routes that the user should be allowed to select by specifying the route types with the `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#setRouteTypes(kotlin.Int)` method.

Refer to `https://developer.android.com/reference/kotlin/android/app/MediaRouteButton` for a description of the button that will appear in the action bar menu. Note that instead of disabling the button when no routes are available, the action provider will instead make the menu item invisible. In this way, the button will only be visible when it is possible for the user to discover and select a matching route.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#MediaRouteActionProvider(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#!)` <br /> |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#isVisible()()` If `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#overridesItemVisibility()` returns true, the return value of this method will help determine the visibility of the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#onCreateActionView()()` Factory method called by the Android framework to create new action views. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#onCreateActionView(android.view.MenuItem)(item: https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)` Factory method called by the Android framework to create new action views. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#onPerformDefaultAction()()` Performs an optional default action. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#overridesItemVisibility()()` The result of this method determines whether or not `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#isVisible()` will be used by the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to help determine its visibility. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#setExtendedSettingsClickListener(android.view.View.OnClickListener)(listener: https://developer.android.com/reference/kotlin/android/view/View.OnClickListener.html#!)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/app/MediaRouteActionProvider#setRouteTypes(kotlin.Int)(types: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Sets the types of routes that will be shown in the media route chooser dialog launched by this button. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#hasSubMenu()()` Determines if this ActionProvider has a submenu associated with it. Associated submenus will be shown when an action view is not. This provider instance will receive a call to `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#onPrepareSubMenu(android.view.SubMenu)` after the call to `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#onPerformDefaultAction()` and before a submenu is displayed to the user. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#onPrepareSubMenu(android.view.SubMenu)(subMenu: https://developer.android.com/reference/kotlin/android/view/SubMenu.html#)` Called to prepare an associated submenu for the menu item backed by this ActionProvider. if `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#hasSubMenu()` returns true, this method will be called when the menu item is selected to prepare the submenu for presentation to the user. Apps may use this to create or alter submenu content right before display. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#refreshVisibility()()` If this ActionProvider is associated with an item in a menu, refresh the visibility of the item based on `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#overridesItemVisibility()` and `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#isVisible()`. If `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#overridesItemVisibility()` returns false, this call will have no effect. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#setVisibilityListener(android.view.ActionProvider.VisibilityListener)(listener: https://developer.android.com/reference/kotlin/android/view/ActionProvider.VisibilityListener.html#?)` Set a listener to be notified when this ActionProvider's overridden visibility changes. This should only be used by MenuItem implementations. <br /> | ||

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

If `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#overridesItemVisibility()` returns true, the return value of this method will help determine the visibility of the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to.

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

This method has been deprecated in favor of `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#onCreateActionView(android.view.MenuItem)`. Newer apps that wish to support platform versions prior to API 16 should also implement this method to return a valid action view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#` | A new action view. This value cannot be `null`. |

### onCreateActionView

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateActionView(item: MenuItem): View
```

Factory method called by the Android framework to create new action views. This method returns a new action view for the given MenuItem.

If your ActionProvider implementation overrides the deprecated no-argument overload `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#onCreateActionView()`, overriding this method for devices running API 16 or later is recommended but optional. The default implementation calls `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#onCreateActionView()` for compatibility with applications written for older platform versions.

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

- Receiving a call to `https://developer.android.com/reference/kotlin/android/view/MenuItem.OnMenuItemClickListener.html#onMenuItemClick(android.view.MenuItem)`.
- Receiving a call to `https://developer.android.com/reference/kotlin/android/app/Activity#onOptionsItemSelected(android.view.MenuItem)`
- Receiving a call to `https://developer.android.com/reference/kotlin/android/app/Fragment#onOptionsItemSelected(android.view.MenuItem)`
- Launching the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` set via `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#setIntent(android.content.Intent)`
- Invoking this method.

<br />

The default implementation does not perform any action and returns false.

### overridesItemVisibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun overridesItemVisibility(): Boolean
```

The result of this method determines whether or not `https://developer.android.com/reference/kotlin/android/view/ActionProvider.html#isVisible()` will be used by the `https://developer.android.com/reference/kotlin/android/view/MenuItem.html#` this ActionProvider is bound to help determine its visibility.

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
