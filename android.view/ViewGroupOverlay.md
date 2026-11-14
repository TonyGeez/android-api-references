# ViewGroupOverlay

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewGroupOverlay

Kotlin| [Java](../android/view/ViewGroupOverlay.md) 
| --- | --- |

```
open class ViewGroupOverlay : ViewOverlay
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.ViewOverlay](../android/view/ViewOverlay.md) ||
| | ↳ | [android.view.ViewGroupOverlay](../android/view/ViewGroupOverlay.md) |

A group overlay is an extra layer that sits on top of a ViewGroup (the "host view") which is drawn after all other content in that view (including the view group's children). Interaction with the overlay layer is done by adding and removing views and drawables.

ViewGroupOverlay is a subclass of [ViewOverlay](../android/view/ViewOverlay.md), adding the ability to manage views for overlays on ViewGroups, in addition to the drawable support in ViewOverlay.

## Summary

| Public methods ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](../android/view/ViewGroupOverlay.md))`(`view:` ` [View](../android/view/View.md)`)` Adds a`View`to the overlay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](../android/view/ViewGroupOverlay.md))`(`view:` ` [View](../android/view/View.md)`)` Removes the specified`View`from the overlay. |

| Inherited functions ||
|---|---|
| From class [ViewOverlay](../android/view/ViewOverlay.md) |------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [add](../android/view/ViewOverlay.md))`(`drawable:` ` [Drawable](../android/graphics/drawable/Drawable.md)`)` <br /> Adds a [Drawable](../android/graphics/drawable/Drawable.md) to the overlay. The bounds of the drawable should be relative to the host view. Any drawable added to the overlay should be removed when it is no longer needed or no longer visible. Adding an already existing [Drawable](../android/graphics/drawable/Drawable.md) is a no-op. Passing`null`parameter will result in an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) being thrown. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](../android/view/ViewOverlay.md))`()` <br /> Removes all content from the overlay. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [remove](../android/view/ViewOverlay.md))`(`drawable:` ` [Drawable](../android/graphics/drawable/Drawable.md)`)` <br /> Removes the specified [Drawable](../android/graphics/drawable/Drawable.md) from the overlay. Removing a [Drawable](../android/graphics/drawable/Drawable.md) that was not added with [add(android.graphics.drawable.Drawable)](../android/view/ViewOverlay.md))is a no-op. Passing`null`parameter will result in an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) being thrown. <br /> | ||

## Public methods

### add

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun add(view: View): Unit
```

Adds a`View`to the overlay. The bounds of the added view should be relative to the host view. Any view added to the overlay should be removed when it is no longer needed or no longer visible.

Views in the overlay are visual-only; they do not receive input events and do not participate in focus traversal. Overlay views are intended to be transient, such as might be needed by a temporary animation effect.

If the view has a parent, the view will be removed from that parent before being added to the overlay. Also, if that parent is attached in the current view hierarchy, the view will be repositioned such that it is in the same relative location inside the activity. For example, if the view's current parent lies 100 pixels to the right and 200 pixels down from the origin of the overlay's host view, then the view will be offset by (100, 200).

`View`s added with this API will be drawn in the order they were added. Drawing of the overlay views will happen before drawing of any of the`Drawable`s added with [add(android.graphics.drawable.Drawable)](../android/view/ViewOverlay.md))API even if a call to this API happened after the call to [add(android.graphics.drawable.Drawable)](../android/view/ViewOverlay.md)).

Passing`null`parameter will result in an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) being thrown.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):The`View`to be added to the overlay. The added view will be drawn when the overlay is drawn. This value cannot be`null`. |

**See Also**

- [#remove(View)](../android/view/ViewGroupOverlay.md))
- [android.view.ViewOverlay#add(Drawable)](../android/view/ViewOverlay.md)) 

### remove

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun remove(view: View): Unit
```

Removes the specified`View`from the overlay. Passing`null`parameter will result in an [IllegalArgumentException](../java/lang/IllegalArgumentException.md) being thrown.

| Parameters ||
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `view` | [View](../android/view/View.md):The`View`to be removed from the overlay. This value cannot be`null`. |

**See Also**

- [#add(View)](../android/view/ViewGroupOverlay.md))
- [android.view.ViewOverlay#remove(Drawable)](../android/view/ViewOverlay.md))
