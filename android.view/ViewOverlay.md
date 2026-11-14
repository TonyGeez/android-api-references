Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ViewOverlay

Kotlin | [Java](ViewOverlay.md)
| --- | --- |

```
open class ViewOverlay
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.ViewOverlay](ViewOverlay.md) |

| Known Direct Subclasses [ViewGroupOverlay](ViewGroupOverlay.md) |---|---| | [ViewGroupOverlay](ViewGroupOverlay.md) | A group overlay is an extra layer that sits on top of a ViewGroup (the "host view") which is drawn after all other content in that view (including the view group's children). | |
| --- | --- | --- | --- | --- | --- | --- |

An overlay is an extra layer that sits on top of a View (the "host view") which is drawn after all other content in that view (including children, if the view is a ViewGroup). Interaction with the overlay layer is done by adding and removing drawables.

An overlay requested from a ViewGroup is of type `https://developer.android.com/reference/kotlin/android/view/ViewGroupOverlay`, which also supports adding and removing views.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewOverlay#add(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)` Adds a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to the overlay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewOverlay#clear()()` Removes all content from the overlay. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewOverlay#remove(android.graphics.drawable.Drawable)(drawable: https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#)` Removes the specified `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` from the overlay. |
| --- | --- |

## Public methods

### add

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun add(drawable: Drawable): Unit
```

Adds a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to the overlay. The bounds of the drawable should be relative to the host view. Any drawable added to the overlay should be removed when it is no longer needed or no longer visible. Adding an already existing `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` is a no-op. Passing `null` parameter will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` being thrown.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to be added to the overlay. This drawable will be drawn when the view redraws its overlay. `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#`s will be drawn in the order that they were added. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewOverlay#remove(android.graphics.drawable.Drawable)`

### clear

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun clear(): Unit
```

Removes all content from the overlay.

### remove

Added in [API level 18](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun remove(drawable: Drawable): Unit
```

Removes the specified `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` from the overlay. Removing a `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` that was not added with `https://developer.android.com/reference/kotlin/android/view/ViewOverlay#add(android.graphics.drawable.Drawable)` is a no-op. Passing `null` parameter will result in an `https://developer.android.com/reference/kotlin/java/lang/IllegalArgumentException.html#` being thrown.

| Parameters ||
|---|---|
| `drawable` | [Drawable](../android.graphics.drawable/Drawable.md): The `https://developer.android.com/reference/kotlin/android/graphics/drawable/Drawable.html#` to be removed from the overlay. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/ViewOverlay#add(android.graphics.drawable.Drawable)`
