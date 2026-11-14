# View.OnUnhandledKeyEventListener

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnUnhandledKeyEventListener

Kotlin| [Java](../android/view/View.OnUnhandledKeyEventListener.md) 
| --- | --- |

```
interface OnUnhandledKeyEventListener
```

| [android.view.View.OnUnhandledKeyEventListener](../android/view/View.OnUnhandledKeyEventListener.md) |

Interface definition for a callback to be invoked when a hardware key event hasn't been handled by the view hierarchy.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onUnhandledKeyEvent](../android/view/View.OnUnhandledKeyEventListener.md))`(`v:` ` [View](View.md)!`, `event:` ` [KeyEvent](KeyEvent.md)!`)` Called when a hardware key is dispatched to a view after being unhandled during normal [KeyEvent](KeyEvent.md) dispatch. |

## Public methods

### onUnhandledKeyEvent

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onUnhandledKeyEvent(
    v: View!, 
    event: KeyEvent!
): Boolean
```

Called when a hardware key is dispatched to a view after being unhandled during normal [KeyEvent](KeyEvent.md) dispatch.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](View.md)!:The view the key has been dispatched to. |
| `event` | [KeyEvent](KeyEvent.md)!:The KeyEvent object containing information about the event. |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if the listener has consumed the event,`false`otherwise. |
