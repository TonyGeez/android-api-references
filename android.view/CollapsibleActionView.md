# CollapsibleActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollapsibleActionView

Kotlin| [Java](https://developer.android.com/reference/android/view/CollapsibleActionView "View this page in Java") 

```
interface CollapsibleActionView
```

| [android.view.CollapsibleActionView](https://developer.android.com/reference/kotlin/android/view/CollapsibleActionView#) |

| Known Direct Subclasses [SearchView](https://developer.android.com/reference/kotlin/android/widget/SearchView.html#) |----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------| | [SearchView](https://developer.android.com/reference/kotlin/android/widget/SearchView.html#) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. | |

When a [View](https://developer.android.com/reference/kotlin/android/view/View) implements this interface it will receive callbacks when expanded or collapsed as an action view alongside the optional, app-specified callbacks to [OnActionExpandListener](https://developer.android.com/reference/kotlin/android/view/MenuItem.OnActionExpandListener).

See [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem) for more information about action views. See [android.app.ActionBar](https://developer.android.com/reference/kotlin/android/app/ActionBar.html#) for more information about the action bar.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionViewCollapsed](https://developer.android.com/reference/kotlin/android/view/CollapsibleActionView#onActionViewCollapsed())`()` Called when this view is collapsed as an action view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionViewExpanded](https://developer.android.com/reference/kotlin/android/view/CollapsibleActionView#onActionViewExpanded())`()` Called when this view is expanded as an action view. |

## Public methods

### onActionViewCollapsed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionViewCollapsed(): Unit
```

Called when this view is collapsed as an action view. See [MenuItem.collapseActionView()](https://developer.android.com/reference/kotlin/android/view/MenuItem#collapseActionView()). 

### onActionViewExpanded

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionViewExpanded(): Unit
```

Called when this view is expanded as an action view. See [MenuItem.expandActionView()](https://developer.android.com/reference/kotlin/android/view/MenuItem#expandActionView()).
