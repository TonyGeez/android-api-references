# ActionBar.OnNavigationListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnNavigationListener

Kotlin| [Java](../android/app/ActionBar.OnNavigationListener.md) 
| --- | --- |

```
interface OnNavigationListener
```

| [android.app.ActionBar.OnNavigationListener](../android/app/ActionBar.OnNavigationListener.md) |

| **This interface was deprecated in API level 21.**
|
| Action bar navigation modes are deprecated and not supported by inline toolbar action bars. Consider using other [common navigation patterns](http://developer.android.com/design/patterns/navigation.html) instead.

Listener interface for ActionBar navigation events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onNavigationItemSelected](../android/app/ActionBar.OnNavigationListener.md))`(`itemPosition:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `itemId:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` This method is called whenever a navigation item in your action bar is selected. |

## Public methods

### onNavigationItemSelected

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onNavigationItemSelected(
    itemPosition: Int, 
    itemId: Long
): Boolean
```

**Deprecated:** *Deprecated in Java.*

This method is called whenever a navigation item in your action bar is selected.

| Parameters ||
|----------------|----------------------------------------------------------------------------------------------------------|
| `itemPosition` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Position of the item clicked. |
| `itemId` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):ID of the item clicked. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the event was handled, false otherwise. |
