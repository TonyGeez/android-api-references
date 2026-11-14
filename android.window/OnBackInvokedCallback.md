# OnBackInvokedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackInvokedCallback

Kotlin| [Java](https://developer.android.com/reference/android/window/OnBackInvokedCallback "View this page in Java") 

```
interface OnBackInvokedCallback
```

| [android.window.OnBackInvokedCallback](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback#) |

| Known Direct Subclasses [OnBackAnimationCallback](https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [OnBackAnimationCallback](https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback) | Interface for applications to register back animation callbacks along their custom back handling. | |

Callback allowing applications to handle back events in place of the system.

Callback instances can be added to and removed from [OnBackInvokedDispatcher](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedDispatcher), which is held at window level and accessible through [Activity.getOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/app/Activity.html#getOnBackInvokedDispatcher()), [Dialog.getOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/app/Dialog.html#getOnBackInvokedDispatcher()), [Window.getOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/view/Window.html#getOnBackInvokedDispatcher())and [View.findOnBackInvokedDispatcher()](https://developer.android.com/reference/kotlin/android/view/View.html#findOnBackInvokedDispatcher()).

When back is triggered, callbacks on the in-focus window are invoked in reverse order in which they are added within the same priority. Between different priorities, callbacks with higher priority are invoked first.

This replaces [Activity.onBackPressed()](https://developer.android.com/reference/kotlin/android/app/Activity.html#onBackPressed()), [Dialog.onBackPressed()](https://developer.android.com/reference/kotlin/android/app/Dialog.html#onBackPressed())and [android.view.KeyEvent#KEYCODE_BACK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_BACK:kotlin.Int)

If you want to customize back animation behaviors, in addition to handling back invocations, register its subclass instances [OnBackAnimationCallback](https://developer.android.com/reference/kotlin/android/window/OnBackAnimationCallback) instead.

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackInvoked](https://developer.android.com/reference/kotlin/android/window/OnBackInvokedCallback#onBackInvoked())`()` Called when a back gesture has been completed and committed, or back button pressed has been released and committed. |

## Public methods

### onBackInvoked

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBackInvoked(): Unit
```

Called when a back gesture has been completed and committed, or back button pressed has been released and committed.
