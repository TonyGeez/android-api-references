# CollapsibleActionView

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CollapsibleActionView

Kotlin| [Java](CollapsibleActionView.md) 
| --- | --- |

```
interface CollapsibleActionView
```

| [android.view.CollapsibleActionView](CollapsibleActionView.md) |

| Known Direct Subclasses [SearchView](../android.widget/SearchView.md) |----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------| | [SearchView](../android.widget/SearchView.md) | A widget that provides a user interface for the user to enter a search query and submit a request to a search provider. | |
| --- | --- | --- | --- | --- | --- | --- |

When a [View](View.md) implements this interface it will receive callbacks when expanded or collapsed as an action view alongside the optional, app-specified callbacks to [OnActionExpandListener](../android/view/MenuItem.OnActionExpandListener.md).

See [MenuItem](MenuItem.md) for more information about action views. See [android.app.ActionBar](../android.app/ActionBar.md) for more information about the action bar.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionViewCollapsed](CollapsibleActionView.md))`()` Called when this view is collapsed as an action view. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionViewExpanded](CollapsibleActionView.md))`()` Called when this view is expanded as an action view. |

## Public methods

### onActionViewCollapsed

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionViewCollapsed(): Unit
```

Called when this view is collapsed as an action view. See [MenuItem.collapseActionView()](MenuItem.md)). 

### onActionViewExpanded

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionViewExpanded(): Unit
```

Called when this view is expanded as an action view. See [MenuItem.expandActionView()](MenuItem.md)).
