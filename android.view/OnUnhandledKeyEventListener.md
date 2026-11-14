# View.OnUnhandledKeyEventListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnUnhandledKeyEventListener

Kotlin| [Java](https://developer.android.com/reference/android/view/View.OnUnhandledKeyEventListener "View this page in Java") 

```
interface OnUnhandledKeyEventListener
```

| [android.view.View.OnUnhandledKeyEventListener](https://developer.android.com/reference/kotlin/android/view/View.OnUnhandledKeyEventListener#) |

Interface definition for a callback to be invoked when a hardware key event hasn't been handled by the view hierarchy.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onUnhandledKeyEvent](https://developer.android.com/reference/kotlin/android/view/View.OnUnhandledKeyEventListener#onUnhandledKeyEvent(android.view.View,%20android.view.KeyEvent))`(`v:` ` [View](https://developer.android.com/reference/kotlin/android/view/View)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!`)` Called when a hardware key is dispatched to a view after being unhandled during normal [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent) dispatch. |

## Public methods

### onUnhandledKeyEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUnhandledKeyEvent(
    v: View!, 
    event: KeyEvent!
): Boolean
```

Called when a hardware key is dispatched to a view after being unhandled during normal [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent) dispatch.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](https://developer.android.com/reference/kotlin/android/view/View)!:The view the key has been dispatched to. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent)!:The KeyEvent object containing information about the event. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the listener has consumed the event,`false`otherwise. |
