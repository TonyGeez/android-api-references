# ActionMenuView.OnMenuItemClickListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnMenuItemClickListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/ActionMenuView.OnMenuItemClickListener "View this page in Java") 
| --- | --- |

```
interface OnMenuItemClickListener
```

| [android.widget.ActionMenuView.OnMenuItemClickListener](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.OnMenuItemClickListener#) |

Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuItemClick](https://developer.android.com/reference/kotlin/android/widget/ActionMenuView.OnMenuItemClickListener#onMenuItemClick(android.view.MenuItem))`(`item:` ` [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!`)` This method will be invoked when a menu item is clicked if the item itself did not already handle the event. |

## Public methods

### onMenuItemClick

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMenuItemClick(item: MenuItem!): Boolean
```

This method will be invoked when a menu item is clicked if the item itself did not already handle the event.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#)!: [MenuItem](https://developer.android.com/reference/kotlin/android/view/MenuItem.html#) that was clicked |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the event was handled,`false`otherwise. |
