# Window.OnRestrictedCaptionAreaChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRestrictedCaptionAreaChangedListener

Kotlin| [Java](https://developer.android.com/reference/android/view/Window.OnRestrictedCaptionAreaChangedListener "View this page in Java") 
| --- | --- |

```
interface OnRestrictedCaptionAreaChangedListener
```

| [android.view.Window.OnRestrictedCaptionAreaChangedListener](https://developer.android.com/reference/kotlin/android/view/Window.OnRestrictedCaptionAreaChangedListener#) |

Callback for clients that want to be aware of where caption draws content.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestrictedCaptionAreaChanged](https://developer.android.com/reference/kotlin/android/view/Window.OnRestrictedCaptionAreaChangedListener#onRestrictedCaptionAreaChanged(android.graphics.Rect))`(`rect:` ` [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!`)` Called when the area where caption draws content changes. |

## Public methods

### onRestrictedCaptionAreaChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRestrictedCaptionAreaChanged(rect: Rect!): Unit
```

Called when the area where caption draws content changes.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](https://developer.android.com/reference/kotlin/android/graphics/Rect.html#)!:The area where caption content is positioned, relative to the top view. |
