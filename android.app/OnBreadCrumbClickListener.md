# FragmentBreadCrumbs.OnBreadCrumbClickListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBreadCrumbClickListener

Kotlin| [Java](../android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener.md) 
| --- | --- |

```
interface OnBreadCrumbClickListener
```

| [android.app.FragmentBreadCrumbs.OnBreadCrumbClickListener](../android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener.md) |

| **This interface was deprecated in API level 28.**
|
| This widget is no longer supported.

Interface to intercept clicks on the bread crumbs.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onBreadCrumbClick](../android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener.md))`(`backStack:` ` [FragmentManager.BackStackEntry](../android/app/FragmentManager.BackStackEntry.md)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a bread crumb is clicked. |

## Public methods

### onBreadCrumbClick

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBreadCrumbClick(
    backStack: FragmentManager.BackStackEntry!, 
    flags: Int
): Boolean
```

**Deprecated:** *Deprecated in Java.*

Called when a bread crumb is clicked.

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `backStack` | [FragmentManager.BackStackEntry](../android/app/FragmentManager.BackStackEntry.md)!:The BackStackEntry whose bread crumb was clicked. May be null, if this bread crumb is for the root of the back stack. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional information about the entry. Currently always 0. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true to consume this click. Return to false to allow the default action (popping back stack to this entry) to occur. |
