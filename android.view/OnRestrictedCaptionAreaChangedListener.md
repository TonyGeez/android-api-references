# Window.OnRestrictedCaptionAreaChangedListener

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnRestrictedCaptionAreaChangedListener

Kotlin| [Java](../android/view/Window.OnRestrictedCaptionAreaChangedListener.md) 
| --- | --- |

```
interface OnRestrictedCaptionAreaChangedListener
```

| [android.view.Window.OnRestrictedCaptionAreaChangedListener](../android/view/Window.OnRestrictedCaptionAreaChangedListener.md) |

Callback for clients that want to be aware of where caption draws content.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRestrictedCaptionAreaChanged](../android/view/Window.OnRestrictedCaptionAreaChangedListener.md))`(`rect:` ` [Rect](../android/graphics/Rect.md)!`)` Called when the area where caption draws content changes. |

## Public methods

### onRestrictedCaptionAreaChanged

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRestrictedCaptionAreaChanged(rect: Rect!): Unit
```

Called when the area where caption draws content changes.

| Parameters ||
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `rect` | [Rect](../android/graphics/Rect.md)!:The area where caption content is positioned, relative to the top view. |
