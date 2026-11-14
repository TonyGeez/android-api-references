Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# NumberKeyListener

Kotlin | [Java](NumberKeyListener.md)
| --- | --- |

```
abstract class NumberKeyListener : BaseKeyListener, InputFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.method.MetaKeyKeyListener](MetaKeyKeyListener.md) |||
| | ↳ | [android.text.method.BaseKeyListener](BaseKeyListener.md) ||
| | | ↳ | [android.text.method.NumberKeyListener](NumberKeyListener.md) |
| --- | --- | --- | --- |

| Known Direct Subclasses [DateKeyListener](DateKeyListener.md), [DateTimeKeyListener](DateTimeKeyListener.md), [DialerKeyListener](DialerKeyListener.md), [DigitsKeyListener](DigitsKeyListener.md), [TimeKeyListener](TimeKeyListener.md) |---|---| | [DateKeyListener](DateKeyListener.md) | For entering dates in a text field. | | [DateTimeKeyListener](DateTimeKeyListener.md) | For entering dates and times in the same text field. | | [DialerKeyListener](DialerKeyListener.md) | For dialing-only text entry | | [DigitsKeyListener](DigitsKeyListener.md) | For digits-only text entry | | [TimeKeyListener](TimeKeyListener.md) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

For numeric text entry

<br />

As for all implementations of KeyListener, this class is only concerned with hardware keyboards. Software input methods have no obligation to trigger the methods in this class.

## Summary

| Inherited constants ||
|---|---|
| From class MetaKeyKeyListener |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_LOCKED:kotlin.Int` Flag that indicates that the ALT key is locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_ON:kotlin.Int` Flag that indicates that the ALT key is on. Value equals `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_ALT_ON:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_CAP_LOCKED:kotlin.Int` Flag that indicates that the SHIFT key is locked in CAPS mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SHIFT_ON:kotlin.Int` Flag that indicates that the SHIFT key is on. Value equals `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SHIFT_ON:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_LOCKED:kotlin.Int` Flag that indicates that the SYM key is locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_ON:kotlin.Int` Flag that indicates that the SYM key is on. Value equals `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SYM_ON:kotlin.Int`. <br /> | ||

| Public constructors ||
|---|---|
| NumberKeyListener <br /> |

| Public methods ||
|---|---|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | filter This method is called when the buffer is going to replace the range `dstart ... dend` of `dest` with the new text from the range `start ... end` of `source`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | onKeyDown Handles presses of the meta keys. |

| Protected methods ||
|---|---|
| abstract [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html) | getAcceptedChars You can say which characters you can accept. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | lookup <br /> |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | ok <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class MetaKeyKeyListener |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | adjustMetaAfterKeypress Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | adjustMetaAfterKeypress Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). Takes the current state, returns the new state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clearMetaKeyState <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | clearMetaKeyState Clears the state of the specified meta key if it is locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | clearMetaKeyState <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMetaState Gets the state of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMetaState Gets the state of the meta keys for a specific key event. For input devices that use toggled key modifiers, the \`toggled' state is stored into the text buffer. This method retrieves the meta state for this event, accounting for the stored state. If the event has been created by a device that does not support toggled key modifiers, like a virtual device for example, the stored state is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMetaState Gets the state of a particular meta key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMetaState Gets the state of a particular meta key to use with a particular key event. If the key event has been created by a device that does not support toggled key modifiers, like a virtual keyboard for example, only the meta state in the key event is considered. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMetaState Gets the state of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getMetaState Gets the state of a particular meta key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | handleKeyDown Handles presses of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | handleKeyUp Handles release of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isMetaTracker Returns true if this object is one that this class would use to keep track of any meta state in the specified text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | isSelectingMetaTracker Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyUp Handles release of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | resetLockedMeta Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | resetLockedMeta Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | resetMetaState Resets all meta state to inactive. <br /> | ||
| From class BaseKeyListener |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | backspace Performs the action that happens when you press the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_DEL:kotlin.Int` key in a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+DEL deletes everything on the line the cursor is on. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | forwardDelete Performs the action that happens when you press the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_FORWARD_DEL:kotlin.Int` key in a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+FORWARD_DEL deletes everything on the line the cursor is on. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | onKeyOther Base implementation handles ACTION_MULTIPLE KEYCODE_UNKNOWN by inserting the event's text into the content. <br /> | ||
| From class KeyListener |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getInputType Return the type of text that this key listener is manipulating, as per `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. This is used to determine the mode of the soft keyboard that is shown for the editor. If you return `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` then *no* soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard. If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

## Public constructors

### NumberKeyListener

```
NumberKeyListener()
```

## Public methods

### filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun filter(
    source: CharSequence!, 
    start: Int, 
    end: Int, 
    dest: Spanned!, 
    dstart: Int, 
    dend: Int
): CharSequence!
```

This method is called when the buffer is going to replace the range `dstart ... dend` of `dest` with the new text from the range `start ... end` of `source`. Return the CharSequence that you would like to have placed there instead, including an empty string if appropriate, or `null` to accept the original replacement. Be careful to not to reject 0-length replacements, as this is what happens when you delete text. Also beware that you should not attempt to make any changes to `dest` from this method; you may only examine it for context. Note: If source is an instance of `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` or `https://developer.android.com/reference/kotlin/android/text/Spannable.html#`, the span objects in the source should be copied into the filtered result (i.e. the non-null return value). copySpansFrom can be used for convenience if the span boundary indices would be remaining identical relative to the source.

### onKeyDown

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun onKeyDown(
    view: View!, 
    content: Editable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```

Handles presses of the meta keys.

## Protected methods

### getAcceptedChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected abstract fun getAcceptedChars(): CharArray
```

You can say which characters you can accept.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html` | This value cannot be `null`. |

### lookup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun lookup(
    event: KeyEvent!, 
    content: Spannable!
): Int
```

### ok

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open static fun ok(
    accept: CharArray!, 
    c: Char
): Boolean
```
