# ViewOutlineProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewOutlineProvider

Kotlin| [Java](../android/view/ViewOutlineProvider.md) 
| --- | --- |

```
abstract class ViewOutlineProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewOutlineProvider](../android/view/ViewOutlineProvider.md) |

| Known Direct Subclasses [RemoteViews.RemoteViewOutlineProvider](../android/widget/RemoteViews.RemoteViewOutlineProvider.md) |----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RemoteViews.RemoteViewOutlineProvider](../android/widget/RemoteViews.RemoteViewOutlineProvider.md) | OutlineProvider for a view with a radius set by [setViewOutlinePreferredRadius(int,float,int)](../android/widget/RemoteViews.md)). | |
| --- | --- | --- | --- | --- | --- | --- |

Interface by which a View builds its [Outline](../android/graphics/Outline.md), used for shadow casting and clipping.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [ViewOutlineProvider](../android/view/ViewOutlineProvider.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](../android/view/ViewOutlineProvider.md))`(`view:` ` [View](../android/view/View.md)!`, `outline:` ` [Outline](../android/graphics/Outline.md)!`)` Called to get the provider to populate the Outline. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ViewOutlineProvider](../android/view/ViewOutlineProvider.md)! | [BACKGROUND](../android/view/ViewOutlineProvider.md) Default outline provider for Views, which queries the Outline from the View's background, or generates a 0 alpha, rectangular Outline the size of the View if a background isn't present. |
| static [ViewOutlineProvider](../android/view/ViewOutlineProvider.md)! | [BOUNDS](../android/view/ViewOutlineProvider.md) Maintains the outline of the View to match its rectangular bounds, at`1.0f`alpha. |
| static [ViewOutlineProvider](../android/view/ViewOutlineProvider.md)! | [PADDED_BOUNDS](../android/view/ViewOutlineProvider.md) Maintains the outline of the View to match its rectangular padded bounds, at`1.0f`alpha. |
| --- | --- |

## Public constructors

### ViewOutlineProvider

```
ViewOutlineProvider()
```

## Public methods

### getOutline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getOutline(
    view: View!, 
    outline: Outline!
): Unit
```

Called to get the provider to populate the Outline. This method will be called by a View when its owned Drawables are invalidated, when the View's size changes, or if [View.invalidateOutline()](../android/view/View.md))is called explicitly. The input outline is empty and has an alpha of`1.0f`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md)!:The view building the outline. |
| `outline` | [Outline](../android/graphics/Outline.md)!:The empty outline to be populated. |

## Properties

### BACKGROUND

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BACKGROUND: ViewOutlineProvider!
```

Default outline provider for Views, which queries the Outline from the View's background, or generates a 0 alpha, rectangular Outline the size of the View if a background isn't present. 
**See Also**

- [android.graphics.drawable.Drawable#getOutline(Outline)](../android/graphics/drawable/Drawable.md)) 

### BOUNDS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BOUNDS: ViewOutlineProvider!
```

Maintains the outline of the View to match its rectangular bounds, at`1.0f`alpha. This can be used to enable Views that are opaque but lacking a background cast a shadow. 

### PADDED_BOUNDS

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PADDED_BOUNDS: ViewOutlineProvider!
```

Maintains the outline of the View to match its rectangular padded bounds, at`1.0f`alpha. This can be used to enable Views that are opaque but lacking a background cast a shadow.
