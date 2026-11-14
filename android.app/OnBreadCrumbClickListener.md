# FragmentBreadCrumbs.OnBreadCrumbClickListener

Added in [API level 12](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBreadCrumbClickListener

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener "View this page in Java") 

```
interface OnBreadCrumbClickListener
```

| [android.app.FragmentBreadCrumbs.OnBreadCrumbClickListener](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener#) |

| **This interface was deprecated in API level 28.**
|
| This widget is no longer supported.

Interface to intercept clicks on the bread crumbs.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onBreadCrumbClick](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs.OnBreadCrumbClickListener#onBreadCrumbClick(android.app.FragmentManager.BackStackEntry,%20kotlin.Int))`(`backStack:` ` [FragmentManager.BackStackEntry](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry)!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when a bread crumb is clicked. |

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
| `backStack` | [FragmentManager.BackStackEntry](https://developer.android.com/reference/kotlin/android/app/FragmentManager.BackStackEntry)!:The BackStackEntry whose bread crumb was clicked. May be null, if this bread crumb is for the root of the back stack. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional information about the entry. Currently always 0. |

| Return ||
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true to consume this click. Return to false to allow the default action (popping back stack to this entry) to occur. |
