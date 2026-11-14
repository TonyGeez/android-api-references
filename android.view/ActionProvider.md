Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ActionProvider

Kotlin | [Java](../android/view/ActionProvider.md)
| --- | --- |

```
abstract class ActionProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ActionProvider](../android/view/ActionProvider.md) |

| Known Direct Subclasses [MediaRouteActionProvider](../android/app/MediaRouteActionProvider.md), [ShareActionProvider](../android/widget/ShareActionProvider.md) |---|---| | [MediaRouteActionProvider](../android/app/MediaRouteActionProvider.md) | The media route action provider displays a `https://developer.android.com/reference/kotlin/android/app/MediaRouteButton.html#` in the application's `https://developer.android.com/reference/kotlin/android/app/ActionBar.html#` to allow the user to select routes and to control the currently selected route. | | [ShareActionProvider](../android/widget/ShareActionProvider.md) | This is a provider for a share action. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

An ActionProvider defines rich menu interaction in a single component. ActionProvider can generate action views for use in the action bar, dynamically populate submenus of a MenuItem, and handle default menu item invocations.

An ActionProvider can be optionally specified for a `https://developer.android.com/reference/kotlin/android/view/MenuItem` and will be responsible for creating the action view that appears in the `https://developer.android.com/reference/kotlin/android/app/ActionBar.html#` in place of a simple button in the bar. When the menu item is presented in a way that does not allow custom action views, (e.g. in an overflow menu,) the ActionProvider can perform a default action.

There are two ways to use an action provider:

- Set the action provider on a `https://developer.android.com/reference/kotlin/android/view/MenuItem` directly by calling `https://developer.android.com/reference/kotlin/android/view/MenuItem#setActionProvider(android.view.ActionProvider)`.
- Declare the action provider in an XML menu resource. For example:

  ```kotlin
  <code>
      &lt;item android:id="@+id/my_menu_item"
        android:title="Title"
        android:icon="@drawable/my_menu_item_icon"
        android:showAsAction="ifRoom"
        android:actionProviderClass="foo.bar.SomeActionProvider" /&gt;
    </code>
  ```

<br />

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/view/ActionProvider.VisibilityListener` Listens to changes in visibility as reported by `https://developer.android.com/reference/kotlin/android/view/ActionProvider#refreshVisibility()`. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ActionProvider#ActionProvider(android.content.Context)(context: https://developer.android.com/reference/kotlin/android/content/Context.html#)` Creates a new instance. |

| Public methods ||
|---|---|
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#hasSubMenu()()` Determines if this ActionProvider has a submenu associated with it. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#isVisible()()` If `https://developer.android.com/reference/kotlin/android/view/ActionProvider#overridesItemVisibility()` returns true, the return value of this method will help determine the visibility of the `https://developer.android.com/reference/kotlin/android/view/MenuItem` this ActionProvider is bound to. |
| abstract [View](../android/view/View.md) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onCreateActionView()()` Factory method called by the Android framework to create new action views. |
| --- | --- |
| open [View](../android/view/View.md) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onCreateActionView(android.view.MenuItem)(forItem: https://developer.android.com/reference/kotlin/android/view/MenuItem)` Factory method called by the Android framework to create new action views. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onPerformDefaultAction()()` Performs an optional default action. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onPrepareSubMenu(android.view.SubMenu)(subMenu: https://developer.android.com/reference/kotlin/android/view/SubMenu)` Called to prepare an associated submenu for the menu item backed by this ActionProvider. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#overridesItemVisibility()()` The result of this method determines whether or not `https://developer.android.com/reference/kotlin/android/view/ActionProvider#isVisible()` will be used by the `https://developer.android.com/reference/kotlin/android/view/MenuItem` this ActionProvider is bound to help determine its visibility. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#refreshVisibility()()` If this ActionProvider is associated with an item in a menu, refresh the visibility of the item based on `https://developer.android.com/reference/kotlin/android/view/ActionProvider#overridesItemVisibility()` and `https://developer.android.com/reference/kotlin/android/view/ActionProvider#isVisible()`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ActionProvider#setVisibilityListener(android.view.ActionProvider.VisibilityListener)(listener: https://developer.android.com/reference/kotlin/android/view/ActionProvider.VisibilityListener?)` Set a listener to be notified when this ActionProvider's overridden visibility changes. |
| --- | --- |

## Public constructors

### ActionProvider

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ActionProvider(context: Context)
```

Creates a new instance. ActionProvider classes should always implement a constructor that takes a single Context parameter for inflating from menu XML.

| Parameters ||
|---|---|
| `context` | [Context](../android/content/Context.md): Context for accessing resources. This value cannot be `null`. |

## Public methods

### hasSubMenu

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun hasSubMenu(): Boolean
```

Determines if this ActionProvider has a submenu associated with it.

Associated submenus will be shown when an action view is not. This provider instance will receive a call to `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onPrepareSubMenu(android.view.SubMenu)` after the call to `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onPerformDefaultAction()` and before a submenu is displayed to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the item backed by this provider should have an associated submenu |

### isVisible

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVisible(): Boolean
```

If `https://developer.android.com/reference/kotlin/android/view/ActionProvider#overridesItemVisibility()` returns true, the return value of this method will help determine the visibility of the `https://developer.android.com/reference/kotlin/android/view/MenuItem` this ActionProvider is bound to.

If the MenuItem's visibility is explicitly set to false by the application, the MenuItem will not be shown, even if this method returns true.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if the MenuItem this ActionProvider is bound to is visible, false if it is invisible. The default implementation returns true. |

### onCreateActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
abstract fun onCreateActionView(): View
```

**Deprecated:** *use `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onCreateActionView(android.view.MenuItem)`*

Factory method called by the Android framework to create new action views.

This method has been deprecated in favor of `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onCreateActionView(android.view.MenuItem)`. Newer apps that wish to support platform versions prior to API 16 should also implement this method to return a valid action view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View` | A new action view. This value cannot be `null`. |

### onCreateActionView

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onCreateActionView(forItem: MenuItem): View
```

Factory method called by the Android framework to create new action views. This method returns a new action view for the given MenuItem.

If your ActionProvider implementation overrides the deprecated no-argument overload `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onCreateActionView()`, overriding this method for devices running API 16 or later is recommended but optional. The default implementation calls `https://developer.android.com/reference/kotlin/android/view/ActionProvider#onCreateActionView()` for compatibility with applications written for older platform versions.

| Parameters ||
|---|---|
| `forItem` | [MenuItem](../android/view/MenuItem.md): MenuItem to create the action view for. This value cannot be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View` | the new action view. This value cannot be `null`. |

### onPerformDefaultAction

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPerformDefaultAction(): Boolean
```

Performs an optional default action.

For the case of an action provider placed in a menu item not shown as an action this method is invoked if previous callbacks for processing menu selection has handled the event.

A menu item selection is processed in the following order:

- Receiving a call to `https://developer.android.com/reference/kotlin/android/view/MenuItem.OnMenuItemClickListener#onMenuItemClick(android.view.MenuItem)`.
- Receiving a call to `https://developer.android.com/reference/kotlin/android/app/Activity.html#onOptionsItemSelected(android.view.MenuItem)`
- Receiving a call to `https://developer.android.com/reference/kotlin/android/app/Fragment.html#onOptionsItemSelected(android.view.MenuItem)`
- Launching the `https://developer.android.com/reference/kotlin/android/content/Intent.html#` set via `https://developer.android.com/reference/kotlin/android/view/MenuItem#setIntent(android.content.Intent)`
- Invoking this method.

<br />

The default implementation does not perform any action and returns false.

### onPrepareSubMenu

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPrepareSubMenu(subMenu: SubMenu): Unit
```

Called to prepare an associated submenu for the menu item backed by this ActionProvider.

if `https://developer.android.com/reference/kotlin/android/view/ActionProvider#hasSubMenu()` returns true, this method will be called when the menu item is selected to prepare the submenu for presentation to the user. Apps may use this to create or alter submenu content right before display.

| Parameters ||
|---|---|
| `subMenu` | [SubMenu](../android/view/SubMenu.md): Submenu that will be displayed. This value cannot be `null`. |

### overridesItemVisibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun overridesItemVisibility(): Boolean
```

The result of this method determines whether or not `https://developer.android.com/reference/kotlin/android/view/ActionProvider#isVisible()` will be used by the `https://developer.android.com/reference/kotlin/android/view/MenuItem` this ActionProvider is bound to help determine its visibility.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | true if this ActionProvider overrides the visibility of the MenuItem it is bound to, false otherwise. The default implementation returns false. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ActionProvider#isVisible()`

### refreshVisibility

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun refreshVisibility(): Unit
```

If this ActionProvider is associated with an item in a menu, refresh the visibility of the item based on `https://developer.android.com/reference/kotlin/android/view/ActionProvider#overridesItemVisibility()` and `https://developer.android.com/reference/kotlin/android/view/ActionProvider#isVisible()`. If `https://developer.android.com/reference/kotlin/android/view/ActionProvider#overridesItemVisibility()` returns false, this call will have no effect.

### setVisibilityListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisibilityListener(listener: ActionProvider.VisibilityListener?): Unit
```

Set a listener to be notified when this ActionProvider's overridden visibility changes. This should only be used by MenuItem implementations.

| Parameters ||
|---|---|
| `listener` | [ActionProvider.VisibilityListener](../android/view/ActionProvider.VisibilityListener.md)?: listener to set. This value may be `null`. |
