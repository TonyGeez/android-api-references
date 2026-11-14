# ActionProvider.VisibilityListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisibilityListener

Kotlin| [Java](https://developer.android.com/reference/android/view/ActionProvider.VisibilityListener "View this page in Java") 
| --- | --- |

```
interface VisibilityListener
```

| [android.view.ActionProvider.VisibilityListener](https://developer.android.com/reference/kotlin/android/view/ActionProvider.VisibilityListener#) |

Listens to changes in visibility as reported by [ActionProvider.refreshVisibility()](https://developer.android.com/reference/kotlin/android/view/ActionProvider#refreshVisibility()).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionProviderVisibilityChanged](https://developer.android.com/reference/kotlin/android/view/ActionProvider.VisibilityListener#onActionProviderVisibilityChanged(kotlin.Boolean))`(`isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

## Public methods

### onActionProviderVisibilityChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionProviderVisibilityChanged(isVisible: Boolean): Unit
```
