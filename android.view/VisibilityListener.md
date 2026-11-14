# ActionProvider.VisibilityListener

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# VisibilityListener

Kotlin| [Java](../android/view/ActionProvider.VisibilityListener.md) 
| --- | --- |

```
interface VisibilityListener
```

| [android.view.ActionProvider.VisibilityListener](../android/view/ActionProvider.VisibilityListener.md) |

Listens to changes in visibility as reported by [ActionProvider.refreshVisibility()](../android/view/ActionProvider.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onActionProviderVisibilityChanged](../android/view/ActionProvider.VisibilityListener.md))`(`isVisible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

## Public methods

### onActionProviderVisibilityChanged

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onActionProviderVisibilityChanged(isVisible: Boolean): Unit
```
