# WindowInsetsAnimationControlListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsAnimationControlListener

Kotlin| [Java](WindowInsetsAnimationControlListener.md) 
| --- | --- |

```
interface WindowInsetsAnimationControlListener
```

| [android.view.WindowInsetsAnimationControlListener](WindowInsetsAnimationControlListener.md) |

Listener that encapsulates a request to [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md)).

Insets can be controlled with the supplied [WindowInsetsAnimationController](WindowInsetsAnimationController.md) from [onReady](WindowInsetsAnimationControlListener.md))until either [onFinished](WindowInsetsAnimationControlListener.md))or [onCancelled](WindowInsetsAnimationControlListener.md)).

Once the control over insets is finished or cancelled, it will not be regained until a new request to [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md))is made.

The request to control insets can fail immediately. In that case [onCancelled](WindowInsetsAnimationControlListener.md))will be invoked without a preceding [onReady](WindowInsetsAnimationControlListener.md)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancelled](WindowInsetsAnimationControlListener.md))`(`controller:` ` [WindowInsetsAnimationController](WindowInsetsAnimationController.md)?`)` Called when the request for control over the insets has been cancelled, either because the [android.os.CancellationSignal](../android.os/CancellationSignal.md) associated with the [request](WindowInsetsController.md))has been invoked, or the window has lost control over the insets (e.g. because it lost focus). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](WindowInsetsAnimationControlListener.md))`(`controller:` ` [WindowInsetsAnimationController](WindowInsetsAnimationController.md)`)` Called when the request for control over the insets has [finished](WindowInsetsAnimationController.md)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReady](WindowInsetsAnimationControlListener.md))`(`controller:` ` [WindowInsetsAnimationController](WindowInsetsAnimationController.md)`, `types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the animation is ready to be controlled. |
| --- | --- |

## Public methods

### onCancelled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCancelled(controller: WindowInsetsAnimationController?): Unit
```

Called when the request for control over the insets has been cancelled, either because the [android.os.CancellationSignal](../android.os/CancellationSignal.md) associated with the [request](WindowInsetsController.md))has been invoked, or the window has lost control over the insets (e.g. because it lost focus). Once this callback is invoked, the supplied [WindowInsetsAnimationController](WindowInsetsAnimationController.md) is no longer [ready](WindowInsetsAnimationController.md)). Control will not be regained until a new request to [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md))is made.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [WindowInsetsAnimationController](WindowInsetsAnimationController.md)?:the controller which has been cancelled, or null if the request was cancelled before [onReady](WindowInsetsAnimationControlListener.md))was invoked. |

**See Also**

- [android.view.WindowInsetsAnimationController#isCancelled](WindowInsetsAnimationController.md)) 

### onFinished

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFinished(controller: WindowInsetsAnimationController): Unit
```

Called when the request for control over the insets has [finished](WindowInsetsAnimationController.md)). Once this callback is invoked, the supplied [WindowInsetsAnimationController](WindowInsetsAnimationController.md) is no longer [ready](WindowInsetsAnimationController.md)). Control will not be regained until a new request to [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md))is made.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [WindowInsetsAnimationController](WindowInsetsAnimationController.md):the controller which has finished. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsAnimationController#isFinished](WindowInsetsAnimationController.md)) 

### onReady

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onReady(
    controller: WindowInsetsAnimationController, 
    types: Int
): Unit
```

Called when the animation is ready to be controlled. This may be delayed when the IME needs to redraw because of an [EditorInfo](../android.view.inputmethod/EditorInfo.md) change, or when the window is starting up.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [WindowInsetsAnimationController](WindowInsetsAnimationController.md):The controller to control the inset animation. This value cannot be`null`. |
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [WindowInsets.Type](../android/view/WindowInsets.Type.md) s it was able to gain control over. Note that this may be different than the types passed into [WindowInsetsController.controlWindowInsetsAnimation](WindowInsetsController.md))in case the window wasn't able to gain the controls because it wasn't the IME target or not currently the window that's controlling the system bars. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

**See Also**

- [android.view.WindowInsetsAnimationController#isReady](WindowInsetsAnimationController.md))
