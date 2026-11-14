# FragmentManager.OnBackStackChangedListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackStackChangedListener

Kotlin| [Java](../android/app/FragmentManager.OnBackStackChangedListener.md) 
| --- | --- |

```
interface OnBackStackChangedListener
```

| [android.app.FragmentManager.OnBackStackChangedListener](../android/app/FragmentManager.OnBackStackChangedListener.md) |

| Known Direct Subclasses [FragmentBreadCrumbs](../android/app/FragmentBreadCrumbs.md) |-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------| | [FragmentBreadCrumbs](../android/app/FragmentBreadCrumbs.md) | Helper class for showing "bread crumbs" representing the fragment stack in an activity. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This interface was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentManager.OnBackStackChangedListener

Interface to watch for changes to the back stack.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackStackChanged](../android/app/FragmentManager.OnBackStackChangedListener.md))`()` Called whenever the contents of the back stack change. |

## Public methods

### onBackStackChanged

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBackStackChanged(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever the contents of the back stack change.
