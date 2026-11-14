# FragmentManager.OnBackStackChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackStackChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentManager.OnBackStackChangedListener "View this page in Java") 
| --- | --- |

```
interface OnBackStackChangedListener
```

| [android.app.FragmentManager.OnBackStackChangedListener](https://developer.android.com/reference/kotlin/android/app/FragmentManager.OnBackStackChangedListener#) |

| Known Direct Subclasses [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [FragmentBreadCrumbs](https://developer.android.com/reference/kotlin/android/app/FragmentBreadCrumbs) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentManager.OnBackStackChangedListener

Interface to watch for changes to the back stack.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackStackChanged](https://developer.android.com/reference/kotlin/android/app/FragmentManager.OnBackStackChangedListener#onBackStackChanged())`()` Called whenever the contents of the back stack change. |

## Public methods

### onBackStackChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBackStackChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the contents of the back stack change.
