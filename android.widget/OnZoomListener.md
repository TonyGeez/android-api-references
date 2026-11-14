# ZoomButtonsController.OnZoomListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnZoomListener

Kotlin | [Java](../android/widget/ZoomButtonsController.OnZoomListener.md) 
| --- | --- |

```
interface OnZoomListener
```

| [android.widget.ZoomButtonsController.OnZoomListener](../android/widget/ZoomButtonsController.OnZoomListener.md) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Interface that will be called when the user performs an interaction that triggers some action, for example zooming.

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onVisibilityChanged](../android/widget/ZoomButtonsController.OnZoomListener.md))`(`visible:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the zoom controls' visibility changes. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onZoom](../android/widget/ZoomButtonsController.OnZoomListener.md))`(`zoomIn:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Called when the owner view needs to be zoomed. |

## Public methods

### onVisibilityChanged

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onVisibilityChanged(visible: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the zoom controls' visibility changes.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the zoom controls are visible. |

### onZoom

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onZoom(zoomIn: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the owner view needs to be zoomed.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `zoomIn` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): The direction of the zoom: true to zoom in, false to zoom out. |
