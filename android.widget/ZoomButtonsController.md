Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ZoomButtonsController

```
open class ZoomButtonsController : View.OnTouchListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.widget.ZoomButtonsController](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#) |

> [!CAUTION]
> **This class was deprecated in API level 26.**
>
> This functionality and UI is better handled with custom views and layouts rather than a dedicated zoom-control widget

The `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#` handles showing and hiding the zoom controls and positioning it relative to an owner view. It also gives the client access to the zoom controls container, allowing for additional accessory buttons to be shown in the zoom controls window.

Typically, clients should call `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setVisible(kotlin.Boolean)` on a touch down or move (no need to call `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setVisible(kotlin.Boolean)` since it will time out on its own). Also, whenever the owner cannot be zoomed further, the client should update `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setZoomInEnabled(kotlin.Boolean)` and `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setZoomOutEnabled(kotlin.Boolean)`.

If you are using this with a custom View, please call `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setVisible(kotlin.Boolean)` from `https://developer.android.com/reference/kotlin/android/view/View.html#onDetachedFromWindow()` and from `https://developer.android.com/reference/kotlin/android/view/View.html#onVisibilityChanged(android.view.View,%20kotlin.Int)` when `visibility != View.VISIBLE`.

## Summary

| Nested classes ||
|---|---|
| abstract | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.OnZoomListener` Interface that will be called when the user performs an interaction that triggers some action, for example zooming. |

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#ZoomButtonsController(android.view.View)(ownerView: https://developer.android.com/reference/kotlin/android/view/View.html#!)` Constructor for the `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#`. |

| Public methods ||
|---|---|
| open [ViewGroup](https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#)! | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#getContainer()()` Gets the container that is the parent of the zoom controls. |
| open [View](https://developer.android.com/reference/kotlin/android/view/View.html#)! | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#getZoomControls()()` Gets the view for the zoom controls. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#isAutoDismissed()()` Whether the zoom controls will be automatically dismissed after showing. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#isVisible()()` Whether the zoom controls are visible to the user. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#onTouch(android.view.View,%20android.view.MotionEvent)(v: https://developer.android.com/reference/kotlin/android/view/View.html#!, event: https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#!)` The ZoomButtonsController implements the OnTouchListener, but this does not need to be shown in its public API. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setAutoDismissed(kotlin.Boolean)(autoDismiss: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the zoom controls will be automatically dismissed after showing. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setFocusable(kotlin.Boolean)(focusable: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the zoom controls should be focusable. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setOnZoomListener(android.widget.ZoomButtonsController.OnZoomListener)(listener: https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.OnZoomListener!)` Sets the `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.OnZoomListener` listener that receives callbacks to zoom. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setVisible(kotlin.Boolean)(visible: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Sets whether the zoom controls should be visible to the user. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setZoomInEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to enable the zoom in control. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setZoomOutEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Whether to enable the zoom out control. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#setZoomSpeed(kotlin.Long)(speed: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Sets the delay between zoom callbacks as the user holds a zoom button. |

## Public constructors

### ZoomButtonsController

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
ZoomButtonsController(ownerView: View!)
```

Constructor for the `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController#`.

| Parameters ||
|---|---|
| `ownerView` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view that is being zoomed by the zoom controls. The zoom controls will be displayed aligned with this view. |

## Public methods

### getContainer

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getContainer(): ViewGroup!
```

**Deprecated:** *Deprecated in Java.*

Gets the container that is the parent of the zoom controls.

The client can add other views to this container to link them with the zoom controls.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/ViewGroup.html#!` | The container of the zoom controls. It will be a layout that respects the gravity of a child's layout parameters. |

### getZoomControls

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getZoomControls(): View!
```

**Deprecated:** *Deprecated in Java.*

Gets the view for the zoom controls.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/View.html#!` | The zoom controls view. |

### isAutoDismissed

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isAutoDismissed(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Whether the zoom controls will be automatically dismissed after showing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the zoom controls will be auto dismissed after showing. |

### isVisible

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isVisible(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Whether the zoom controls are visible to the user.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | Whether the zoom controls are visible to the user. |

### onTouch

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onTouch(
    v: View!, 
    event: MotionEvent!
): Boolean
```

**Deprecated:** *Deprecated in Java.*

The ZoomButtonsController implements the OnTouchListener, but this does not need to be shown in its public API.

| Parameters ||
|---|---|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!: The view the touch event has been dispatched to. |
| `event` | [MotionEvent](https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#)!: The MotionEvent object containing full information about the event. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | True if the listener has consumed the event, false otherwise. |

### setAutoDismissed

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutoDismissed(autoDismiss: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether the zoom controls will be automatically dismissed after showing.

### setFocusable

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setFocusable(focusable: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether the zoom controls should be focusable. If the controls are focusable, then trackball and arrow key interactions are possible. Otherwise, only touch interactions are possible.

| Parameters ||
|---|---|
| `focusable` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the zoom controls should be focusable. |

### setOnZoomListener

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setOnZoomListener(listener: ZoomButtonsController.OnZoomListener!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the `https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.OnZoomListener` listener that receives callbacks to zoom.

| Parameters ||
|---|---|
| `listener` | [ZoomButtonsController.OnZoomListener](https://developer.android.com/reference/kotlin/android/widget/ZoomButtonsController.OnZoomListener)!: The listener that will be told to zoom. |

### setVisible

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setVisible(visible: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets whether the zoom controls should be visible to the user.

| Parameters ||
|---|---|
| `visible` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether the zoom controls should be visible to the user. |

### setZoomInEnabled

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setZoomInEnabled(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Whether to enable the zoom in control.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to enable the zoom in control. |

### setZoomOutEnabled

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setZoomOutEnabled(enabled: Boolean): Unit
```

**Deprecated:** *Deprecated in Java.*

Whether to enable the zoom out control.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): Whether to enable the zoom out control. |

### setZoomSpeed

Added in [API level 4](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setZoomSpeed(speed: Long): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the delay between zoom callbacks as the user holds a zoom button.

| Parameters ||
|---|---|
| `speed` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html): The delay in milliseconds between zoom callbacks. |
