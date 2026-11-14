# TextView.OnEditorActionListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnEditorActionListener

Kotlin| [Java](https://developer.android.com/reference/android/widget/TextView.OnEditorActionListener "View this page in Java") 
| --- | --- |

```
interface OnEditorActionListener
```

| [android.widget.TextView.OnEditorActionListener](https://developer.android.com/reference/kotlin/android/widget/TextView.OnEditorActionListener#) |

Interface definition for a callback to be invoked when an action is performed on the editor.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onEditorAction](https://developer.android.com/reference/kotlin/android/widget/TextView.OnEditorActionListener#onEditorAction(android.widget.TextView,%20kotlin.Int,%20android.view.KeyEvent))`(`v:` ` [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)!`, `actionId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Called when an action is being performed. |

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
| `v` | [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView)!:The view that was clicked. |
| `actionId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Identifier of the action. This will be either the identifier you supplied, or [EditorInfo.IME_NULL](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#IME_NULL:kotlin.Int) if being called due to the enter key being pressed. Starting from Android 14, the action identifier will also be included when triggered by an enter key if the input is constrained to a single line. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:If triggered by an enter key, this is the event; otherwise, this is null. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|----------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | Return true if you have consumed the action, else false. |
