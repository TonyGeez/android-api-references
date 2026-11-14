# View.OnDragListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDragListener

Kotlin | [Java](https://developer.android.com/reference/android/view/View.OnDragListener "View this page in Java") 
| --- | --- |

```
interface OnDragListener
```

| [android.view.View.OnDragListener](https://developer.android.com/reference/kotlin/android/view/View.OnDragListener#) |

Interface definition for a listener that's invoked when a drag event is dispatched to this view. The listener is invoked before the view's own [onDragEvent(android.view.DragEvent)](https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)) method. To fall back to the view's `onDragEvent(DragEvent)` behavior, return `false` from the listener method.
|
| ### Developer Guides
|
| For a guide to implementing drag and drop features, see the [Drag and drop](https://developer.android.com/guide/topics/ui/drag-drop.html) developer guide.

<br />

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDrag](https://developer.android.com/reference/kotlin/android/view/View.OnDragListener#onDrag(android.view.View,%20android.view.DragEvent))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `event:` ` [DragEvent](https://developer.android.com/reference/kotlin/android/view/DragEvent)!`)` Called when a drag event is dispatched to a view. |

## Public methods

### onDrag

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrag(
    v: View!, 
    event: DragEvent!
): Boolean
```

Called when a drag event is dispatched to a view. Enables listeners to override the base behavior provided by [onDragEvent(android.view.DragEvent)](https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!: The `View` that received the drag event. |
| `event` | [DragEvent](https://developer.android.com/reference/kotlin/android/view/DragEvent)!: The event object for the drag event. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the drag event was handled successfully; `false`, if the drag event was not handled. **Note:** A `false` return value triggers the view's [onDragEvent(android.view.DragEvent)](https://developer.android.com/reference/kotlin/android/view/View#onDragEvent(android.view.DragEvent)) handler. |
