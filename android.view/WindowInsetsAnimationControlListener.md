# WindowInsetsAnimationControlListener

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsAnimationControlListener

Kotlin| [Java](https://developer.android.com/reference/android/view/WindowInsetsAnimationControlListener "View this page in Java") 

```
interface WindowInsetsAnimationControlListener
```

| [android.view.WindowInsetsAnimationControlListener](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#) |

Listener that encapsulates a request to [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener)).

Insets can be controlled with the supplied [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController) from [onReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onReady(android.view.WindowInsetsAnimationController,%20kotlin.Int))until either [onFinished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onFinished(android.view.WindowInsetsAnimationController))or [onCancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onCancelled(android.view.WindowInsetsAnimationController)).

Once the control over insets is finished or cancelled, it will not be regained until a new request to [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))is made.

The request to control insets can fail immediately. In that case [onCancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onCancelled(android.view.WindowInsetsAnimationController))will be invoked without a preceding [onReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onReady(android.view.WindowInsetsAnimationController,%20kotlin.Int)).

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onCancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onCancelled(android.view.WindowInsetsAnimationController))`(`controller:` ` [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController)?`)` Called when the request for control over the insets has been cancelled, either because the [android.os.CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) associated with the [request](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))has been invoked, or the window has lost control over the insets (e.g. because it lost focus). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onFinished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onFinished(android.view.WindowInsetsAnimationController))`(`controller:` ` [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController)`)` Called when the request for control over the insets has [finished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean)). |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onReady(android.view.WindowInsetsAnimationController,%20kotlin.Int))`(`controller:` ` [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController)`, `types:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the animation is ready to be controlled. |

## Public methods

### onCancelled

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onCancelled(controller: WindowInsetsAnimationController?): Unit
```

Called when the request for control over the insets has been cancelled, either because the [android.os.CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) associated with the [request](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))has been invoked, or the window has lost control over the insets (e.g. because it lost focus). Once this callback is invoked, the supplied [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController) is no longer [ready](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isReady()). Control will not be regained until a new request to [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))is made.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController)?:the controller which has been cancelled, or null if the request was cancelled before [onReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationControlListener#onReady(android.view.WindowInsetsAnimationController,%20kotlin.Int))was invoked. |

**See Also**

- [android.view.WindowInsetsAnimationController#isCancelled](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isCancelled()) 

### onFinished

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onFinished(controller: WindowInsetsAnimationController): Unit
```

Called when the request for control over the insets has [finished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#finish(kotlin.Boolean)). Once this callback is invoked, the supplied [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController) is no longer [ready](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isReady()). Control will not be regained until a new request to [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))is made.

| Parameters ||
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController):the controller which has finished. This value cannot be`null`. |

**See Also**

- [android.view.WindowInsetsAnimationController#isFinished](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isFinished()) 

### onReady

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onReady(
    controller: WindowInsetsAnimationController, 
    types: Int
): Unit
```

Called when the animation is ready to be controlled. This may be delayed when the IME needs to redraw because of an [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo) change, or when the window is starting up.

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `controller` | [WindowInsetsAnimationController](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController):The controller to control the inset animation. This value cannot be`null`. |
| `types` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The [WindowInsets.Type](https://developer.android.com/reference/kotlin/android/view/WindowInsets.Type) s it was able to gain control over. Note that this may be different than the types passed into [WindowInsetsController.controlWindowInsetsAnimation](https://developer.android.com/reference/kotlin/android/view/WindowInsetsController#controlWindowInsetsAnimation(kotlin.Int,%20kotlin.Long,%20android.view.animation.Interpolator,%20android.os.CancellationSignal,%20android.view.WindowInsetsAnimationControlListener))in case the window wasn't able to gain the controls because it wasn't the IME target or not currently the window that's controlling the system bars. Value is either`0`or a combination of android.view.WindowInsets.Type.STATUS_BARS, android.view.WindowInsets.Type.NAVIGATION_BARS, android.view.WindowInsets.Type.CAPTION_BAR, android.view.WindowInsets.Type.IME, android.view.WindowInsets.Type.SYSTEM_GESTURES, android.view.WindowInsets.Type.MANDATORY_SYSTEM_GESTURES, android.view.WindowInsets.Type.TAPPABLE_ELEMENT, android.view.WindowInsets.Type.DISPLAY_CUTOUT, and android.view.WindowInsets.Type.SYSTEM_OVERLAYS |

**See Also**

- [android.view.WindowInsetsAnimationController#isReady](https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimationController#isReady())
