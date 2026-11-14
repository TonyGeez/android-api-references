# View.OnKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnKeyListener

Kotlin| [Java](../android/view/View.OnKeyListener.md) 
| --- | --- |

```
interface OnKeyListener
```

| [android.view.View.OnKeyListener](../android/view/View.OnKeyListener.md) |

Interface definition for a callback to be invoked when a hardware key event is dispatched to this view. The callback will be invoked before the key event is given to the view. This is only useful for hardware keyboards; a software input method has no obligation to trigger this listener.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKey](../android/view/View.OnKeyListener.md))`(`v:` ` [View](../android/view/View.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` Called when a hardware key is dispatched to a view. |

## Public methods

### onKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKey(
    v: View!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Called when a hardware key is dispatched to a view. This allows listeners to get a chance to respond before the target view.

Key presses in software keyboards will generally NOT trigger this method, although some may elect to do so in some situations. Do not assume a software input method has to be key-based; even if it is, it may use key presses in a different way than you expect, so there is no way to reliably catch soft input key presses.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [View](../android/view/View.md)!:The view the key has been dispatched to. |
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The code for the physical key that was pressed |
| `event` | [KeyEvent](../android/view/KeyEvent.md)!:The KeyEvent object containing full information about the event. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the listener has consumed the event, false otherwise. |
