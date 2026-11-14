Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WindowInsetsAnimationListener

```
interface WindowInsetsAnimationListener
```

| [android.view.ViewTreeObserver.WindowInsetsAnimationListener](../android/view/ViewTreeObserver.WindowInsetsAnimationListener.md) |

Interface definition for a callback to be invoked when window insets animations prepare or end.

A window insets animation listener can be registered to observe when window insets animations are about to start (prepare) and when they end. These callbacks are executed on the UI thread.

Unlike `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback`, which is designed for applications to synchronize their view layouts or draw frames with the animation on every frame, this listener only observes the preparation and completion of animations, but doesn't allow for frame-by-frame synchronization.

Because this listener does not perform frame-by-frame synchronization, registering only this listener without a corresponding `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback` on the view hierarchy allows the window insets animation to run off-thread on the background animation thread. This avoids the performance overhead of running the animation on the main UI thread.

This listener does not have an equivalent to `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback#onStart(android.view.WindowInsetsAnimation,%20android.view.WindowInsetsAnimation.Bounds)` or receive the animation bounds, because it is not intended for layout synchronization. To perform frame-synchronized layout changes or customize the animation bounds, register a `https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation.Callback` on the view hierarchy instead.

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.WindowInsetsAnimationListener#onEnd(android.view.WindowInsetsAnimation)(animation: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation)` Called after a window insets animation has ended. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/ViewTreeObserver.WindowInsetsAnimationListener#onPrepare(android.view.WindowInsetsAnimation)(animation: https://developer.android.com/reference/kotlin/android/view/WindowInsetsAnimation)` Called when an insets animation is about to start and before the views have been laid out in the end state of the animation. |

## Public methods

### onEnd

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onEnd(animation: WindowInsetsAnimation): Unit
```

Called after a window insets animation has ended.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](WindowInsetsAnimation.md): The animation that has ended. This value cannot be `null`. |

### onPrepare

Added in [API level 37.2](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onPrepare(animation: WindowInsetsAnimation): Unit
```

Called when an insets animation is about to start and before the views have been laid out in the end state of the animation.

This is called before the final insets are dispatched to the view hierarchy via `https://developer.android.com/reference/kotlin/android/view/View#onApplyWindowInsets(android.view.WindowInsets)` or `https://developer.android.com/reference/kotlin/android/view/View.OnApplyWindowInsetsListener`.

| Parameters ||
|---|---|
| `animation` | [WindowInsetsAnimation](WindowInsetsAnimation.md): The animation that is about to start. This value cannot be `null`. |
