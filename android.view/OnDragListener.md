# View.OnDragListener

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnDragListener

Kotlin | [Java](../android/view/View.OnDragListener.md) 
| --- | --- |

```
interface OnDragListener
```

| [android.view.View.OnDragListener](../android/view/View.OnDragListener.md) |

Interface definition for a listener that's invoked when a drag event is dispatched to this view. The listener is invoked before the view's own [onDragEvent(android.view.DragEvent)](View.md)) method. To fall back to the view's `onDragEvent(DragEvent)` behavior, return `false` from the listener method.
|
| ### Developer Guides
|
| For a guide to implementing drag and drop features, see the [Drag and drop](https://developer.android.com/guide/topics/ui/drag-drop.html) developer guide.

<br />

## Summary

| Public methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onDrag](../android/view/View.OnDragListener.md))`(`v:` ` [View](View.md)!`, `event:` ` [DragEvent](DragEvent.md)!`)` Called when a drag event is dispatched to a view. |

## Public methods

### onDrag

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onDrag(
    v: View!, 
    event: DragEvent!
): Boolean
```

Called when a drag event is dispatched to a view. Enables listeners to override the base behavior provided by [onDragEvent(android.view.DragEvent)](View.md)).

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md)!: The `View` that received the drag event. |
| `event` | [DragEvent](DragEvent.md)!: The event object for the drag event. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if the drag event was handled successfully; `false`, if the drag event was not handled. **Note:** A `false` return value triggers the view's [onDragEvent(android.view.DragEvent)](View.md)) handler. |
