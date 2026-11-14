Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackAnimationCallback

Kotlin | [Java](https://developer.android.com/reference/android/window/OnBackAnimationCallback "View this page in Java")
| --- | --- |

```
interface OnBackAnimationCallback : OnBackInvokedCallback
```

| [android.window.OnBackAnimationCallback](https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback#) |

Interface for applications to register back animation callbacks along their custom back handling.

This allows the client to customize various back behaviors by overriding the corresponding callback methods.

Callback instances can be added to and removed from `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher`, which is held at window level and accessible through `https://developer.android.com/reference/kotlin/android/app/Activity.html#getOnBackInvokedDispatcher()`, `https://developer.android.com/reference/kotlin/android/app/Dialog.html#getOnBackInvokedDispatcher()`, `https://developer.android.com/reference/kotlin/android/view/Window.html#getOnBackInvokedDispatcher()` and `https://developer.android.com/reference/kotlin/android/view/View.html#findOnBackInvokedDispatcher()`.

When back is triggered, callbacks on the in-focus window are invoked in reverse order in which they are added within the same priority. Between different priorities, callbacks with higher priority are invoked first.

<br />

## Summary

| Public methods ||
|---|---|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback#onBackCancelled()()` Called when a back gesture or back button press has been cancelled. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback#onBackProgressed(android.window.BackEvent)(backEvent: https://developer.android.com/reference/kotlin/android/window/BackEvent)` Called when a back gesture progresses. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback#onBackStarted(android.window.BackEvent)(backEvent: https://developer.android.com/reference/kotlin/android/window/BackEvent)` Called when a back gesture has been started, or back button has been pressed down. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback#onBackInvoked()()` Called when a back gesture has been completed and committed, or back button pressed has been released and committed. <br /> | ||

## Public methods

### onBackCancelled

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBackCancelled(): Unit
```

Called when a back gesture or back button press has been cancelled.

### onBackProgressed

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBackProgressed(backEvent: BackEvent): Unit
```

Called when a back gesture progresses.

| Parameters ||
|---|---|
| `backEvent` | [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent): An `https://developer.android.com/reference/kotlin/android/window/BackEvent` object describing the progress event. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/window/BackEvent`

### onBackStarted

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onBackStarted(backEvent: BackEvent): Unit
```

Called when a back gesture has been started, or back button has been pressed down.

| Parameters ||
|---|---|
| `backEvent` | [BackEvent](https://developer.android.com/reference/kotlin/android/window/BackEvent): The `https://developer.android.com/reference/kotlin/android/window/BackEvent` containing information about the touch or button press. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/window/BackEvent`
