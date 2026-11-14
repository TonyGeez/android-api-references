# ViewOutlineProvider

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewOutlineProvider

Kotlin| [Java](https://developer.android.com/reference/android/view/ViewOutlineProvider "View this page in Java") 

```
abstract class ViewOutlineProvider
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#) |

| Known Direct Subclasses [RemoteViews.RemoteViewOutlineProvider](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteViewOutlineProvider.html#) |----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [RemoteViews.RemoteViewOutlineProvider](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.RemoteViewOutlineProvider.html#) | OutlineProvider for a view with a radius set by [setViewOutlinePreferredRadius(int,float,int)](https://developer.android.com/reference/kotlin/android/widget/RemoteViews.html#setViewOutlinePreferredRadius(kotlin.Int,%20kotlin.Float,%20kotlin.Int)). | |

Interface by which a View builds its [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#), used for shadow casting and clipping.

## Summary

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------|---|
| [ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#ViewOutlineProvider())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getOutline](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#getOutline(android.view.View,%20android.graphics.Outline))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `outline:` ` [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)!`)` Called to get the provider to populate the Outline. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#)! | [BACKGROUND](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#BACKGROUND:android.view.ViewOutlineProvider) Default outline provider for Views, which queries the Outline from the View's background, or generates a 0 alpha, rectangular Outline the size of the View if a background isn't present. |
| static [ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#)! | [BOUNDS](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#BOUNDS:android.view.ViewOutlineProvider) Maintains the outline of the View to match its rectangular bounds, at`1.0f`alpha. |
| static [ViewOutlineProvider](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#)! | [PADDED_BOUNDS](https://developer.android.com/reference/kotlin/android/view/ViewOutlineProvider#PADDED_BOUNDS:android.view.ViewOutlineProvider) Maintains the outline of the View to match its rectangular padded bounds, at`1.0f`alpha. |

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

Called to get the provider to populate the Outline. This method will be called by a View when its owned Drawables are invalidated, when the View's size changes, or if [View.invalidateOutline()](https://developer.android.com/reference/kotlin/android/view/View#invalidateOutline())is called explicitly. The input outline is empty and has an alpha of`1.0f`.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view building the outline. |
| `outline` | [Outline](https://developer.android.com/reference/kotlin/android/graphics/Outline.html#)!:The empty outline to be populated. |

## Properties

### BACKGROUND

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BACKGROUND: ViewOutlineProvider!
```

Default outline provider for Views, which queries the Outline from the View's background, or generates a 0 alpha, rectangular Outline the size of the View if a background isn't present. 
**See Also**

- [android.graphics.drawable.Drawable#getOutline(Outline)](https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#getOutline(android.graphics.Outline)) 

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
