# FragmentContainer

Added in [API level 23](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# FragmentContainer

Kotlin| [Java](FragmentContainer.md) 
| --- | --- |

```
abstract class FragmentContainer
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.app.FragmentContainer](FragmentContainer.md) |

| Known Direct Subclasses [FragmentHostCallback](FragmentHostCallback.md) |---------------------------------------------------------------------------------------------------------|--------------------------------------------| | [FragmentHostCallback](FragmentHostCallback.md) | Integration points with the Fragment host. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 28.**
|
| Use the [Support Library](https://developer.android.com/tools/extras/support-library.html) androidx.fragment.app.FragmentContainer.

Callbacks to a [Fragment](Fragment.md)'s container.

## Summary

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------|---|
| [FragmentContainer](FragmentContainer.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstractT? | [onFindViewById](FragmentContainer.md))`(`id:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the view with the given resource ID. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onHasView](FragmentContainer.md))`()` Return`true`if the container holds any view. |

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
