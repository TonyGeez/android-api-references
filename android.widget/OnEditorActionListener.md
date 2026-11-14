# TextView.OnEditorActionListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEditorActionListener

Kotlin| [Java](../android/widget/TextView.OnEditorActionListener.md) 
| --- | --- |

```
interface OnEditorActionListener
```

| [android.widget.TextView.OnEditorActionListener](../android/widget/TextView.OnEditorActionListener.md) |

Interface definition for a callback to be invoked when an action is performed on the editor.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onEditorAction](../android/widget/TextView.OnEditorActionListener.md))`(`v:` ` [TextView](TextView.md)!`, `actionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Called when an action is being performed. |

## Public methods

### onEditorAction

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onEditorAction(
    v: TextView!, 
    actionId: Int, 
    event: KeyEvent!
): Boolean
```

Called when an action is being performed.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `v` | [TextView](TextView.md)!:The view that was clicked. |
| `actionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the action. This will be either the identifier you supplied, or [EditorInfo.IME_NULL](../android.view.inputmethod/EditorInfo.md) if being called due to the enter key being pressed. Starting from Android 14, the action identifier will also be included when triggered by an enter key if the input is constrained to a single line. |
| `event` | [KeyEvent](../android.view/KeyEvent.md)!:If triggered by an enter key, this is the event; otherwise, this is null. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true if you have consumed the action, else false. |
