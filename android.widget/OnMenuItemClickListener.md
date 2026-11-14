# ActionMenuView.OnMenuItemClickListener

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnMenuItemClickListener

Kotlin| [Java](../android/widget/ActionMenuView.OnMenuItemClickListener.md) 
| --- | --- |

```
interface OnMenuItemClickListener
```

| [android.widget.ActionMenuView.OnMenuItemClickListener](../android/widget/ActionMenuView.OnMenuItemClickListener.md) |

Interface responsible for receiving menu item click events if the items themselves do not have individual item click listeners.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onMenuItemClick](../android/widget/ActionMenuView.OnMenuItemClickListener.md))`(`item:` ` [MenuItem](../android.view/MenuItem.md)!`)` This method will be invoked when a menu item is clicked if the item itself did not already handle the event. |

## Public methods

### onMenuItemClick

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMenuItemClick(item: MenuItem!): Boolean
```

This method will be invoked when a menu item is clicked if the item itself did not already handle the event.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `item` | [MenuItem](../android.view/MenuItem.md)!: [MenuItem](../android.view/MenuItem.md) that was clicked |

| Return ||
|------------------------------------------------------------------------------------|--------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the event was handled,`false`otherwise. |
