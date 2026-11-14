# ActionBar.OnMenuVisibilityListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnMenuVisibilityListener

Kotlin| [Java](https://developer.android.com/reference/android/app/ActionBar.OnMenuVisibilityListener "View this page in Java") 

```
interface OnMenuVisibilityListener
```

| [android.app.ActionBar.OnMenuVisibilityListener](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener#) |

Listener for receiving events when action bar menus are shown or hidden.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onMenuVisibilityChanged](https://developer.android.com/reference/kotlin/android/app/ActionBar.OnMenuVisibilityListener#onMenuVisibilityChanged(kotlin.Boolean))`(`isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when an action bar menu is shown or hidden. |

## Public methods

### onMenuVisibilityChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onMenuVisibilityChanged(isVisible: Boolean): Unit
```

Called when an action bar menu is shown or hidden. Applications may want to use this to tune auto-hiding behavior for the action bar or pause/resume video playback, gameplay, or other activity within the main content area.

| Parameters ||
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `isVisible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):True if an action bar menu is now visible, false if no action bar menus are visible. |
