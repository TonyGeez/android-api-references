# OnBackInvokedCallback

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnBackInvokedCallback

Kotlin| [Java](OnBackInvokedCallback.md) 
| --- | --- |

```
interface OnBackInvokedCallback
```

| [android.window.OnBackInvokedCallback](OnBackInvokedCallback.md) |

| Known Direct Subclasses [OnBackAnimationCallback](OnBackAnimationCallback.md) |------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------| | [OnBackAnimationCallback](OnBackAnimationCallback.md) | Interface for applications to register back animation callbacks along their custom back handling. | |
| --- | --- | --- | --- | --- | --- | --- |

Callback allowing applications to handle back events in place of the system.

Callback instances can be added to and removed from [OnBackInvokedDispatcher](OnBackInvokedDispatcher.md), which is held at window level and accessible through [Activity.getOnBackInvokedDispatcher()](../android.app/Activity.md)), [Dialog.getOnBackInvokedDispatcher()](../android.app/Dialog.md)), [Window.getOnBackInvokedDispatcher()](../android.view/Window.md))and [View.findOnBackInvokedDispatcher()](../android.view/View.md)).

When back is triggered, callbacks on the in-focus window are invoked in reverse order in which they are added within the same priority. Between different priorities, callbacks with higher priority are invoked first.

This replaces [Activity.onBackPressed()](../android.app/Activity.md)), [Dialog.onBackPressed()](../android.app/Dialog.md))and [android.view.KeyEvent#KEYCODE_BACK](../android.view/KeyEvent.md)

If you want to customize back animation behaviors, in addition to handling back invocations, register its subclass instances [OnBackAnimationCallback](OnBackAnimationCallback.md) instead.

<br />

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onBackInvoked](OnBackInvokedCallback.md))`()` Called when a back gesture has been completed and committed, or back button pressed has been released and committed. |

## Public methods

### onBackInvoked

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onBackInvoked(): Unit
```

Called when a back gesture has been completed and committed, or back button pressed has been released and committed.
