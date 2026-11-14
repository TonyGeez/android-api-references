# FragmentContainer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentContainer

Kotlin| [Java](https://developer.android.com/reference/android/app/FragmentContainer "View this page in Java") 
| --- | --- |

```
abstract class FragmentContainer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.FragmentContainer](https://developer.android.com/reference/kotlin/android/app/FragmentContainer#) |

| Known Direct Subclasses [FragmentHostCallback](https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback) |---------------------------------------------------------------------------------------------------------|--------------------------------------------| | [FragmentHostCallback](https://developer.android.com/reference/kotlin/android/app/FragmentHostCallback) | Integration points with the Fragment host. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentContainer.

Callbacks to a [Fragment](https://developer.android.com/reference/kotlin/android/app/Fragment)'s container.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------|---|
| [FragmentContainer](https://developer.android.com/reference/kotlin/android/app/FragmentContainer#FragmentContainer())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT? | [onFindViewById](https://developer.android.com/reference/kotlin/android/app/FragmentContainer#onFindViewById(kotlin.Int))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the view with the given resource ID. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onHasView](https://developer.android.com/reference/kotlin/android/app/FragmentContainer#onHasView())`()` Return`true`if the container holds any view. |

## Public constructors

### FragmentContainer

```
FragmentContainer()
```

## Public methods

### onFindViewById

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun <T : View!> onFindViewById(id: Int): T?
```

**Deprecated:** *Deprecated in Java.*

Return the view with the given resource ID. May return`null`if the view is not a child of this container. 

### onHasView

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onHasView(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Return`true`if the container holds any view.
