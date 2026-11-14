# DialerKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# DialerKeyListener

Kotlin| [Java](../android/text/method/DialerKeyListener.md) 
| --- | --- |

```
open class DialerKeyListener : NumberKeyListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||||
| --- | --- | --- | --- | --- |
| ↳ | [android.text.method.MetaKeyKeyListener](../android/text/method/MetaKeyKeyListener.md) ||||
| | ↳ | [android.text.method.BaseKeyListener](../android/text/method/BaseKeyListener.md) |||
| | | ↳ | [android.text.method.NumberKeyListener](../android/text/method/NumberKeyListener.md) ||
| --- | --- | --- | --- | --- |
| | | | ↳ | [android.text.method.DialerKeyListener](../android/text/method/DialerKeyListener.md) |

For dialing-only text entry

<br />

As for all implementations of [KeyListener](../android/text/method/KeyListener.md), this class is only concerned with hardware keyboards. Software input methods have no obligation to trigger the methods in this class.

## Summary

| Inherited constants ||
|---|---|
| From class [MetaKeyKeyListener](../android/text/method/MetaKeyKeyListener.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_LOCKED](../android/text/method/MetaKeyKeyListener.md) <br /> Flag that indicates that the ALT key is locked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_ON](../android/text/method/MetaKeyKeyListener.md) <br /> Flag that indicates that the ALT key is on. Value equals [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_CAP_LOCKED](../android/text/method/MetaKeyKeyListener.md) <br /> Flag that indicates that the SHIFT key is locked in CAPS mode. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SHIFT_ON](../android/text/method/MetaKeyKeyListener.md) <br /> Flag that indicates that the SHIFT key is on. Value equals [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_LOCKED](../android/text/method/MetaKeyKeyListener.md) <br /> Flag that indicates that the SYM key is locked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_ON](../android/text/method/MetaKeyKeyListener.md) <br /> Flag that indicates that the SYM key is on. Value equals [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md). <br /> | ||

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------|---|
| [DialerKeyListener](../android/text/method/DialerKeyListener.md))`()` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](../android/text/method/DialerKeyListener.md))`()` <br /> |
| openstatic [DialerKeyListener](../android/text/method/DialerKeyListener.md)! | [getInstance](../android/text/method/DialerKeyListener.md))`()` <br /> |

| Protected methods ||
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html) | [getAcceptedChars](../android/text/method/DialerKeyListener.md))`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [lookup](../android/text/method/DialerKeyListener.md))`(`event:` ` [KeyEvent](../android/view/KeyEvent.md)!`, `content:` ` [Spannable](../android/text/Spannable.md)!`)` Overrides the superclass's lookup method to prefer the number field from the KeyEvent. |

| Inherited functions ||
|---|---|
| From class [MetaKeyKeyListener](../android/text/method/MetaKeyKeyListener.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustMetaAfterKeypress](../android/text/method/MetaKeyKeyListener.md))`(`content:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [adjustMetaAfterKeypress](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). Takes the current state, returns the new state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](../android/text/method/MetaKeyKeyListener.md))`(`view:` ` [View](../android/view/View.md)!`, `content:` ` [Editable](../android/text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearMetaKeyState](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Clears the state of the specified meta key if it is locked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](../android/text/method/MetaKeyKeyListener.md))`(`content:` ` [Editable](../android/text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Gets the state of the meta keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Gets the state of the meta keys for a specific key event. For input devices that use toggled key modifiers, the \`toggled' state is stored into the text buffer. This method retrieves the meta state for this event, accounting for the stored state. If the event has been created by a device that does not support toggled key modifiers, like a virtual device for example, the stored state is ignored. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state of a particular meta key. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Gets the state of a particular meta key to use with a particular key event. If the key event has been created by a device that does not support toggled key modifiers, like a virtual keyboard for example, only the meta state in the key event is considered. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Gets the state of the meta keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state of a particular meta key. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyDown](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Handles presses of the meta keys. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyUp](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Handles release of the meta keys. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetaTracker](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Returns true if this object is one that this class would use to keep track of any meta state in the specified text. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectingMetaTracker](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](../android/text/method/MetaKeyKeyListener.md))`(`view:` ` [View](../android/view/View.md)!`, `content:` ` [Editable](../android/text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Handles release of the meta keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetLockedMeta](../android/text/method/MetaKeyKeyListener.md))`(`content:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [resetLockedMeta](../android/text/method/MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetMetaState](../android/text/method/MetaKeyKeyListener.md))`(`text:` ` [Spannable](../android/text/Spannable.md)!`)` <br /> Resets all meta state to inactive. <br /> | ||
| From class [BaseKeyListener](../android/text/method/BaseKeyListener.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [backspace](../android/text/method/BaseKeyListener.md))`(`view:` ` [View](../android/view/View.md)!`, `content:` ` [Editable](../android/text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Performs the action that happens when you press the [KeyEvent.KEYCODE_DEL](../android/view/KeyEvent.md) key in a [TextView](../android/widget/TextView.md). If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+DEL deletes everything on the line the cursor is on. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [forwardDelete](../android/text/method/BaseKeyListener.md))`(`view:` ` [View](../android/view/View.md)!`, `content:` ` [Editable](../android/text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Performs the action that happens when you press the [KeyEvent.KEYCODE_FORWARD_DEL](../android/view/KeyEvent.md) key in a [TextView](../android/widget/TextView.md). If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+FORWARD_DEL deletes everything on the line the cursor is on. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](../android/text/method/BaseKeyListener.md))`(`view:` ` [View](../android/view/View.md)!`, `content:` ` [Editable](../android/text/Editable.md)!`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> Base implementation handles ACTION_MULTIPLE KEYCODE_UNKNOWN by inserting the event's text into the content. <br /> | ||
| From class [NumberKeyListener](../android/text/method/NumberKeyListener.md) |------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [filter](../android/text/method/NumberKeyListener.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Spanned](../android/text/Spanned.md)!`, `dstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [ok](../android/text/method/NumberKeyListener.md))`(`accept:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](../android/text/method/NumberKeyListener.md))`(`view:` ` [View](../android/view/View.md)!`, `content:` ` [Editable](../android/text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android/view/KeyEvent.md)!`)` <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| From class [KeyListener](../android/text/method/KeyListener.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](../android/text/method/KeyListener.md))`()` <br /> Return the type of text that this key listener is manipulating, as per [android.text.InputType](../android/text/InputType.md). This is used to determine the mode of the soft keyboard that is shown for the editor. If you return [android.text.InputType#TYPE_NULL](../android/text/InputType.md) then*no*soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard. If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)! | [CHARACTERS](../android/text/method/DialerKeyListener.md) The characters that are used. |

## Public constructors

### DialerKeyListener

```
DialerKeyListener()
```

## Public methods

### getInputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputType(): Int
```  

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): DialerKeyListener!
```

## Protected methods

### getAcceptedChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun getAcceptedChars(): CharArray
```

| Return ||
|-----------------------------------------------------------------------------------------|-----------------------------|
| [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html) | This value cannot be`null`. |

### lookup

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun lookup(
    event: KeyEvent!, 
    content: Spannable!
): Int
```

Overrides the superclass's lookup method to prefer the number field from the KeyEvent.

## Properties

### CHARACTERS

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CHARACTERS: CharArray!
```

The characters that are used. 
**See Also**

- [#getAcceptedChars](../android/text/method/DialerKeyListener.md))
