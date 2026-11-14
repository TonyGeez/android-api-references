# KeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyListener

Kotlin| [Java](KeyListener.md) 
| --- | --- |

```
interface KeyListener
```

| [android.text.method.KeyListener](KeyListener.md) |

| Known Direct Subclasses [BaseKeyListener](BaseKeyListener.md) |-------------------------------------------------------------------------------------------------------|----------------------------------------| | [BaseKeyListener](BaseKeyListener.md) | Abstract base class for key listeners. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DateKeyListener](DateKeyListener.md), [DateTimeKeyListener](DateTimeKeyListener.md), [DialerKeyListener](DialerKeyListener.md), [DigitsKeyListener](DigitsKeyListener.md), [MultiTapKeyListener](MultiTapKeyListener.md), [NumberKeyListener](NumberKeyListener.md), [QwertyKeyListener](QwertyKeyListener.md), [TextKeyListener](TextKeyListener.md), [TimeKeyListener](TimeKeyListener.md) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [DateKeyListener](DateKeyListener.md) | For entering dates in a text field. | | [DateTimeKeyListener](DateTimeKeyListener.md) | For entering dates and times in the same text field. | | [DialerKeyListener](DialerKeyListener.md) | For dialing-only text entry | | [DigitsKeyListener](DigitsKeyListener.md) | For digits-only text entry | | [MultiTapKeyListener](MultiTapKeyListener.md) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [NumberKeyListener](NumberKeyListener.md) | For numeric text entry | | [QwertyKeyListener](QwertyKeyListener.md) | This is the standard key listener for alphabetic input on qwerty keyboards. | | [TextKeyListener](TextKeyListener.md) | This is the key listener for typing normal text. | | [TimeKeyListener](TimeKeyListener.md) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Interface for converting text key events into edit operations on an Editable class. Note that for most cases this interface has been superceded by general soft input methods as defined by [android.view.inputmethod.InputMethod](../android.view.inputmethod/InputMethod.md); it should only be used for cases where an application has its own on-screen keypad and also wants to process hard keyboard events to match it.

<br />

Key presses on soft input methods are not required to trigger the methods in this listener, and are in fact discouraged to do so. The default android keyboard will not trigger these for any key to any application targetting Jelly Bean or later, and will only deliver it for some key presses to applications targetting Ice Cream Sandwich or earlier.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](KeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Remove the given shift states from the edited text. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](KeyListener.md))`()` Return the type of text that this key listener is manipulating, as per [android.text.InputType](../android.text/InputType.md). |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](KeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `text:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` If the key listener wants to handle this key, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |
| --- | --- |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](KeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `text:` ` [Editable](../android.text/Editable.md)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` If the key listener wants to other kinds of key events, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](KeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `text:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` If the key listener wants to handle this key release, return true, otherwise return false and the caller (i.e. the widget host) will handle the key. |

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

Return the type of text that this key listener is manipulating, as per [android.text.InputType](../android.text/InputType.md). This is used to determine the mode of the soft keyboard that is shown for the editor.

If you return [android.text.InputType#TYPE_NULL](../android.text/InputType.md) then*no*soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard.

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
