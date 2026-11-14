# ActionBar.TabListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TabListener

Kotlin| [Java](../android/app/ActionBar.TabListener.md) 
| --- | --- |

```
interface TabListener
```

| [android.app.ActionBar.TabListener](../android/app/ActionBar.TabListener.md) |

| **This interface was deprecated in API level 21.**
|
| Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.

Callback interface invoked when a tab is focused, unfocused, added, or removed.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTabReselected](../android/app/ActionBar.TabListener.md))`(`tab:` ` [ActionBar.Tab](../android/app/ActionBar.Tab.md)!`, `ft:` ` [FragmentTransaction](../android/app/FragmentTransaction.md)!`)` Called when a tab that is already selected is chosen again by the user. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTabSelected](../android/app/ActionBar.TabListener.md))`(`tab:` ` [ActionBar.Tab](../android/app/ActionBar.Tab.md)!`, `ft:` ` [FragmentTransaction](../android/app/FragmentTransaction.md)!`)` Called when a tab enters the selected state. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onTabUnselected](../android/app/ActionBar.TabListener.md))`(`tab:` ` [ActionBar.Tab](../android/app/ActionBar.Tab.md)!`, `ft:` ` [FragmentTransaction](../android/app/FragmentTransaction.md)!`)` Called when a tab exits the selected state. |
| --- | --- |

## Public methods

### onTabReselected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTabReselected(
    tab: ActionBar.Tab!, 
    ft: FragmentTransaction!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a tab that is already selected is chosen again by the user. Some applications may use this action to return to the top level of a category.

| Parameters ||
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tab` | [ActionBar.Tab](../android/app/ActionBar.Tab.md)!:The tab that was reselected. |
| `ft` | [FragmentTransaction](../android/app/FragmentTransaction.md)!:A [FragmentTransaction](../android/app/FragmentTransaction.md) for queuing fragment operations to execute once this method returns. This FragmentTransaction does not support being added to the back stack. |

### onTabSelected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTabSelected(
    tab: ActionBar.Tab!, 
    ft: FragmentTransaction!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a tab enters the selected state.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tab` | [ActionBar.Tab](../android/app/ActionBar.Tab.md)!:The tab that was selected |
| `ft` | [FragmentTransaction](../android/app/FragmentTransaction.md)!:A [FragmentTransaction](../android/app/FragmentTransaction.md) for queuing fragment operations to execute during a tab switch. The previous tab's unselect and this tab's select will be executed in a single transaction. This FragmentTransaction does not support being added to the back stack. |

### onTabUnselected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onTabUnselected(
    tab: ActionBar.Tab!, 
    ft: FragmentTransaction!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when a tab exits the selected state.

| Parameters ||
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `tab` | [ActionBar.Tab](../android/app/ActionBar.Tab.md)!:The tab that was unselected |
| `ft` | [FragmentTransaction](../android/app/FragmentTransaction.md)!:A [FragmentTransaction](../android/app/FragmentTransaction.md) for queuing fragment operations to execute during a tab switch. This tab's unselect and the newly selected tab's select will be executed in a single transaction. This FragmentTransaction does not support being added to the back stack. |
