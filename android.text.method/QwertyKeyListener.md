# QwertyKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# QwertyKeyListener

Kotlin| [Java](QwertyKeyListener.md) 
| --- | --- |

```
open class QwertyKeyListener : BaseKeyListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.method.MetaKeyKeyListener](MetaKeyKeyListener.md) |||
| | ↳ | [android.text.method.BaseKeyListener](BaseKeyListener.md) ||
| | | ↳ | [android.text.method.QwertyKeyListener](QwertyKeyListener.md) |
| --- | --- | --- | --- |

This is the standard key listener for alphabetic input on qwerty keyboards. You should generally not need to instantiate this yourself; TextKeyListener will do it for you.

<br />

As for all implementations of [KeyListener](KeyListener.md), this class is only concerned with hardware keyboards. Software input methods have no obligation to trigger the methods in this class.

## Summary

| Inherited constants ||
|---|---|
| From class [MetaKeyKeyListener](MetaKeyKeyListener.md) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_LOCKED](MetaKeyKeyListener.md) <br /> Flag that indicates that the ALT key is locked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_ON](MetaKeyKeyListener.md) <br /> Flag that indicates that the ALT key is on. Value equals [KeyEvent.META_ALT_ON](../android.view/KeyEvent.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_CAP_LOCKED](MetaKeyKeyListener.md) <br /> Flag that indicates that the SHIFT key is locked in CAPS mode. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SHIFT_ON](MetaKeyKeyListener.md) <br /> Flag that indicates that the SHIFT key is on. Value equals [KeyEvent.META_SHIFT_ON](../android.view/KeyEvent.md). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_LOCKED](MetaKeyKeyListener.md) <br /> Flag that indicates that the SYM key is locked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_ON](MetaKeyKeyListener.md) <br /> Flag that indicates that the SYM key is on. Value equals [KeyEvent.META_SYM_ON](../android.view/KeyEvent.md). <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [QwertyKeyListener](QwertyKeyListener.md))`(`cap:` ` [TextKeyListener.Capitalize](../android/text/method/TextKeyListener.Capitalize.md)!`, `autoText:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` <br /> |

| Public methods ||
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](QwertyKeyListener.md))`()` <br /> |
| openstatic [QwertyKeyListener](QwertyKeyListener.md)! | [getInstance](QwertyKeyListener.md))`(`autoText:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cap:` ` [TextKeyListener.Capitalize](../android/text/method/TextKeyListener.Capitalize.md)!`)` Returns a new or existing instance with the specified capitalization and correction properties. |
| openstatic [QwertyKeyListener](QwertyKeyListener.md)! | [getInstanceForFullKeyboard](QwertyKeyListener.md))`()` Gets an instance of the listener suitable for use with full keyboards. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [markAsReplaced](QwertyKeyListener.md))`(`content:` ` [Spannable](../android.text/Spannable.md)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `original:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Marks the specified region of`content`as having contained`original`prior to AutoText replacement. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](QwertyKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> |

| Inherited functions ||
|---|---|
| From class [MetaKeyKeyListener](MetaKeyKeyListener.md) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustMetaAfterKeypress](MetaKeyKeyListener.md))`(`content:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [adjustMetaAfterKeypress](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). Takes the current state, returns the new state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](MetaKeyKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearMetaKeyState](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Clears the state of the specified meta key if it is locked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](MetaKeyKeyListener.md))`(`content:` ` [Editable](../android.text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Gets the state of the meta keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Gets the state of the meta keys for a specific key event. For input devices that use toggled key modifiers, the \`toggled' state is stored into the text buffer. This method retrieves the meta state for this event, accounting for the stored state. If the event has been created by a device that does not support toggled key modifiers, like a virtual device for example, the stored state is ignored. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state of a particular meta key. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Gets the state of a particular meta key to use with a particular key event. If the key event has been created by a device that does not support toggled key modifiers, like a virtual keyboard for example, only the meta state in the key event is considered. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Gets the state of the meta keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state of a particular meta key. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyDown](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Handles presses of the meta keys. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyUp](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Handles release of the meta keys. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetaTracker](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Returns true if this object is one that this class would use to keep track of any meta state in the specified text. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectingMetaTracker](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](MetaKeyKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Handles release of the meta keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetLockedMeta](MetaKeyKeyListener.md))`(`content:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [resetLockedMeta](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetMetaState](MetaKeyKeyListener.md))`(`text:` ` [Spannable](../android.text/Spannable.md)!`)` <br /> Resets all meta state to inactive. <br /> | ||
| From class [BaseKeyListener](BaseKeyListener.md) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [backspace](BaseKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Performs the action that happens when you press the [KeyEvent.KEYCODE_DEL](../android.view/KeyEvent.md) key in a [TextView](../android.widget/TextView.md). If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+DEL deletes everything on the line the cursor is on. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [forwardDelete](BaseKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Performs the action that happens when you press the [KeyEvent.KEYCODE_FORWARD_DEL](../android.view/KeyEvent.md) key in a [TextView](../android.widget/TextView.md). If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+FORWARD_DEL deletes everything on the line the cursor is on. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](BaseKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` <br /> Base implementation handles ACTION_MULTIPLE KEYCODE_UNKNOWN by inserting the event's text into the content. <br /> | ||
| From class [KeyListener](KeyListener.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](KeyListener.md))`()` <br /> Return the type of text that this key listener is manipulating, as per [android.text.InputType](../android.text/InputType.md). This is used to determine the mode of the soft keyboard that is shown for the editor. If you return [android.text.InputType#TYPE_NULL](../android.text/InputType.md) then*no*soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard. If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

## Public constructors

### QwertyKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
QwertyKeyListener(
    cap: TextKeyListener.Capitalize!, 
    autoText: Boolean)
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
open static fun getInstance(
    autoText: Boolean, 
    cap: TextKeyListener.Capitalize!
): QwertyKeyListener!
```

Returns a new or existing instance with the specified capitalization and correction properties. 

### getInstanceForFullKeyboard

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstanceForFullKeyboard(): QwertyKeyListener!
```

Gets an instance of the listener suitable for use with full keyboards. Disables auto-capitalization, auto-text and long-press initiated on-screen character pickers. 

### markAsReplaced

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun markAsReplaced(
    content: Spannable!, 
    start: Int, 
    end: Int, 
    original: String!
): Unit
```

Marks the specified region of`content`as having contained`original`prior to AutoText replacement. Call this method when you have done or are about to do an AutoText-style replacement on a region of text and want to let the same mechanism (the user pressing DEL immediately after the change) undo the replacement.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `content` | [Spannable](../android.text/Spannable.md)!:the Editable text where the replacement was made |
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the start of the replaced region |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the end of the replaced region; the location of the cursor |
| --- | --- |
| `original` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:the text to be restored if the user presses DEL |

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
