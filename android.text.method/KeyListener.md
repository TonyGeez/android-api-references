# KeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyListener

Kotlin| [Java](https://developer.android.com/reference/android/text/method/KeyListener "View this page in Java") 
| --- | --- |

```
interface KeyListener
```

| [android.text.method.KeyListener](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#) |

| Known Direct Subclasses [BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) |-------------------------------------------------------------------------------------------------------|----------------------------------------| | [BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) | Abstract base class for key listeners. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener), [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener), [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener), [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener), [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener), [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener), [QwertyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/QwertyKeyListener), [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener), [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener) | For entering dates in a text field. | | [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener) | For entering dates and times in the same text field. | | [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener) | For dialing-only text entry | | [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener) | For digits-only text entry | | [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener) | For numeric text entry | | [QwertyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/QwertyKeyListener) | This is the standard key listener for alphabetic input on qwerty keyboards. | | [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) | This is the key listener for typing normal text. | | [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface for converting text key events into edit operations on an Editable class. Note that for most cases this interface has been superceded by general soft input methods as defined by [android.view.inputmethod.InputMethod](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethod.html#); it should only be used for cases where an application has its own on-screen keypad and also wants to process hard keyboard events to match it.

<br />

Key presses on soft input methods are not required to trigger the methods in this listener, and are in fact discouraged to do so. The default android keyboard will not trigger these for any key to any application targetting Jelly Bean or later, and will only deliver it for some key presses to applications targetting Ice Cream Sandwich or earlier.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#clearMetaKeyState(android.view.View,%20android.text.Editable,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove the given shift states from the edited text. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#getInputType())`()` Return the type of text that this key listener is manipulating, as per [android.text.InputType](https://developer.android.com/reference/kotlin/android/text/InputType.html#). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#onKeyDown(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `text:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` If the key listener wants to handle this key, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#onKeyOther(android.view.View,%20android.text.Editable,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `text:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#onKeyUp(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `text:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` If the key listener wants to handle this key release, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |

## Public methods

### clearMetaKeyState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun clearMetaKeyState(
    view: View!, 
    content: Editable!, 
    states: Int
): Unit
```

Remove the given shift states from the edited text. 

### getInputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getInputType(): Int
```

Return the type of text that this key listener is manipulating, as per [android.text.InputType](https://developer.android.com/reference/kotlin/android/text/InputType.html#). This is used to determine the mode of the soft keyboard that is shown for the editor.

If you return [android.text.InputType#TYPE_NULL](https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int) then*no*soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard.

If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here. 

### onKeyDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyDown(
    view: View!, 
    text: Editable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

If the key listener wants to handle this key, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. 

### onKeyOther

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyOther(
    view: View!, 
    text: Editable!, 
    event: KeyEvent!
): Boolean
```

If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. 

### onKeyUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKeyUp(
    view: View!, 
    text: Editable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

If the key listener wants to handle this key release, return true, otherwise return false and the caller (i.e. the widget host) will handle the key.
