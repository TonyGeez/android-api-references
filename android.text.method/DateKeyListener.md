Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DateKeyListener

Kotlin | [Java](https://developer.android.com/reference/android/text/method/DateKeyListener "View this page in Java")

```
open class DateKeyListener : NumberKeyListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| ↳ | [android.text.method.MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener) ||||
| | ↳ | [android.text.method.BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) |||
| | | ↳ | [android.text.method.NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener) ||
| | | | ↳ | [android.text.method.DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#) |

For entering dates in a text field.

<br />

As for all implementations of `https://developer.android.com/reference/kotlin/android/text/method/KeyListener`, this class is only concerned with hardware keyboards. Software input methods have no obligation to trigger the methods in this class.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_LOCKED:kotlin.Int` Flag that indicates that the ALT key is locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_ON:kotlin.Int` Flag that indicates that the ALT key is on. Value equals `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_ALT_ON:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_CAP_LOCKED:kotlin.Int` Flag that indicates that the SHIFT key is locked in CAPS mode. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SHIFT_ON:kotlin.Int` Flag that indicates that the SHIFT key is on. Value equals `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SHIFT_ON:kotlin.Int`. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_LOCKED:kotlin.Int` Flag that indicates that the SYM key is locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_ON:kotlin.Int` Flag that indicates that the SYM key is on. Value equals `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SYM_ON:kotlin.Int`. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#DateKeyListener()()` <br /> |
| `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#DateKeyListener(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#?)` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getInputType()()` Return the type of text that this key listener is manipulating, as per `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. |
| open static [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#) | `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getInstance()()` <br /> |
| open static [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#) | `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getInstance(java.util.Locale)(locale: https://developer.android.com/reference/kotlin/java/util/Locale.html#?)` Returns an instance of DateKeyListener appropriate for the given locale. |

| Protected methods ||
|---|---|
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html) | `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getAcceptedChars()()` You can say which characters you can accept. |

| Inherited functions ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#adjustMetaAfterKeypress(android.text.Spannable)(content: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#adjustMetaAfterKeypress(kotlin.Long)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). Takes the current state, returns the new state. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(android.view.View,%20android.text.Editable,%20kotlin.Int)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(kotlin.Long,%20kotlin.Int)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, which: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Clears the state of the specified meta key if it is locked. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(android.text.Editable,%20kotlin.Int)(content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, states: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!)` Gets the state of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20android.view.KeyEvent)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Gets the state of the meta keys for a specific key event. For input devices that use toggled key modifiers, the \`toggled' state is stored into the text buffer. This method retrieves the meta state for this event, accounting for the stored state. If the event has been created by a device that does not support toggled key modifiers, like a virtual device for example, the stored state is ignored. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, meta: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the state of a particular meta key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int,%20android.view.KeyEvent)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, meta: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Gets the state of a particular meta key to use with a particular key event. If the key event has been created by a device that does not support toggled key modifiers, like a virtual keyboard for example, only the meta state in the key event is considered. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Gets the state of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long,%20kotlin.Int)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, meta: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the state of a particular meta key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyDown(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Handles presses of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyUp(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Handles release of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#isMetaTracker(kotlin.CharSequence,%20kotlin.Any)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns true if this object is one that this class would use to keep track of any meta state in the specified text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#isSelectingMetaTracker(kotlin.CharSequence,%20kotlin.Any)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, what: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html!)` Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#onKeyUp(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Handles release of the meta keys. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetLockedMeta(android.text.Spannable)(content: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetLockedMeta(kotlin.Long)(state: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetMetaState(android.text.Spannable)(text: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` Resets all meta state to inactive. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener#backspace(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Performs the action that happens when you press the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_DEL:kotlin.Int` key in a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+DEL deletes everything on the line the cursor is on. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener#forwardDelete(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Performs the action that happens when you press the `https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_FORWARD_DEL:kotlin.Int` key in a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+FORWARD_DEL deletes everything on the line the cursor is on. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener#onKeyOther(android.view.View,%20android.text.Editable,%20android.view.KeyEvent)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Base implementation handles ACTION_MULTIPLE KEYCODE_UNKNOWN by inserting the event's text into the content. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | `https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener#filter(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.text.Spanned,%20kotlin.Int,%20kotlin.Int)(source: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!, start: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, end: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dest: https://developer.android.com/reference/kotlin/android/text/Spanned.html#!, dstart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, dend: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` This method is called when the buffer is going to replace the range `dstart ... dend` of `dest` with the new text from the range `start ... end` of `source`. Return the CharSequence that you would like to have placed there instead, including an empty string if appropriate, or `null` to accept the original replacement. Be careful to not to reject 0-length replacements, as this is what happens when you delete text. Also beware that you should not attempt to make any changes to `dest` from this method; you may only examine it for context. Note: If source is an instance of `https://developer.android.com/reference/kotlin/android/text/Spanned.html#` or `https://developer.android.com/reference/kotlin/android/text/Spannable.html#`, the span objects in the source should be copied into the filtered result (i.e. the non-null return value). `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#copySpansFrom(android.text.Spanned,%20kotlin.Int,%20kotlin.Int,%20java.lang.Class,%20android.text.Spannable,%20kotlin.Int)` can be used for convenience if the span boundary indices would be remaining identical relative to the source. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener#lookup(android.view.KeyEvent,%20android.text.Spannable)(event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!, content: https://developer.android.com/reference/kotlin/android/text/Spannable.html#!)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener#ok(kotlin.CharArray,%20kotlin.Char)(accept: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html!, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)` <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener#onKeyDown(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent)(view: https://developer.android.com/reference/kotlin/android/view/View.html#!, content: https://developer.android.com/reference/kotlin/android/text/Editable.html#!, keyCode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, event: https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#!)` Handles presses of the meta keys. <br /> | ||
| From class `https://developer.android.com/reference/kotlin/android/text/method/KeyListener` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/method/KeyListener#getInputType()()` Return the type of text that this key listener is manipulating, as per `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. This is used to determine the mode of the soft keyboard that is shown for the editor. If you return `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` then *no* soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard. If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here. <br /> | ||

| Properties ||
|---|---|
| static [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#CHARACTERS:kotlin.CharArray` This field used to list the characters that were used. |

## Public constructors

### DateKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DateKeyListener()
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#DateKeyListener(java.util.Locale)` instead.*

### DateKeyListener

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
DateKeyListener(locale: Locale?)
```

| Parameters ||
|---|---|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)?: This value may be `null`. |

## Public methods

### getInputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInputType(): Int
```

Return the type of text that this key listener is manipulating, as per `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. This is used to determine the mode of the soft keyboard that is shown for the editor.

If you return `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int` then *no* soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard.

If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here.

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(): DateKeyListener
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getInstance(java.util.Locale)` instead.*

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#` | This value cannot be `null`. |

### getInstance

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open static fun getInstance(locale: Locale?): DateKeyListener
```

Returns an instance of DateKeyListener appropriate for the given locale.

| Parameters ||
|---|---|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)?: This value may be `null`. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#` | This value cannot be `null`. |

## Protected methods

### getAcceptedChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
protected open fun getAcceptedChars(): CharArray
```

You can say which characters you can accept.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html` | This value cannot be `null`. |

## Properties

### CHARACTERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CHARACTERS: CharArray!
```

**Deprecated:** *Use `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getAcceptedChars()` instead.*

This field used to list the characters that were used. But is now a fixed data field that is the list of code units used for the deprecated case where the class is instantiated with null or no input parameter.
**See Also**

- `https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener#getAcceptedChars()`
