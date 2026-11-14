# TextKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextKeyListener

Kotlin| [Java](https://developer.android.com/reference/android/text/method/TextKeyListener "View this page in Java") 
| --- | --- |

```
open class TextKeyListener : BaseKeyListener, SpanWatcher
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.text.method.MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener) |||
| | ↳ | [android.text.method.BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) ||
| | | ↳ | [android.text.method.TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#) |
| --- | --- | --- | --- |

This is the key listener for typing normal text. It delegates to other key listeners appropriate to the current keyboard and language.

<br />

As for all implementations of [KeyListener](https://developer.android.com/reference/kotlin/android/text/method/KeyListener), this class is only concerned with hardware keyboards. Software input methods have no obligation to trigger the methods in this class.

## Summary

| Nested classes ||
|---|--------------------------------------------------------------------------------------------------------------------|
| | [Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize) <br /> |

| Inherited constants ||
|---|---|
| From class [MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener) |----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_LOCKED](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_LOCKED:kotlin.Int) <br /> Flag that indicates that the ALT key is locked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_ON:kotlin.Int) <br /> Flag that indicates that the ALT key is on. Value equals [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_ALT_ON:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_CAP_LOCKED](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_CAP_LOCKED:kotlin.Int) <br /> Flag that indicates that the SHIFT key is locked in CAPS mode. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SHIFT_ON:kotlin.Int) <br /> Flag that indicates that the SHIFT key is on. Value equals [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SHIFT_ON:kotlin.Int). <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_LOCKED](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_LOCKED:kotlin.Int) <br /> Flag that indicates that the SYM key is locked. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_ON:kotlin.Int) <br /> Flag that indicates that the SYM key is on. Value equals [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SYM_ON:kotlin.Int). <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#TextKeyListener(android.text.method.TextKeyListener.Capitalize,%20kotlin.Boolean))`(`cap:` ` [TextKeyListener.Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize)!`, `autotext:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`)` Creates a new TextKeyListener with the specified capitalization and correction properties. |

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clear](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#clear(android.text.Editable))`(`e:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`)` Clear all the input state (autotext, autocap, multitap, undo) from the specified Editable, going beyond Editable. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#getInputType())`()` <br /> |
| openstatic [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#getInstance())`()` Returns a new or existing instance with no automatic capitalization or correction. |
| --- | --- |
| openstatic [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#)! | [getInstance](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#getInstance(kotlin.Boolean,%20android.text.method.TextKeyListener.Capitalize))`(`autotext:` ` [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, `cap:` ` [TextKeyListener.Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize)!`)` Returns a new or existing instance with the specified capitalization and correction properties. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#onKeyDown(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyOther](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#onKeyOther(android.view.View,%20android.text.Editable,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#onKeyUp(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpanAdded](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#onSpanAdded(android.text.Spannable,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpanChanged](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#onSpanChanged(android.text.Spannable,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `st:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `en:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onSpanRemoved](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#onSpanRemoved(android.text.Spannable,%20kotlin.Any,%20kotlin.Int,%20kotlin.Int))`(`s:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [release](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#release())`()` <br /> |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [shouldCap](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener#shouldCap(android.text.method.TextKeyListener.Capitalize,%20kotlin.CharSequence,%20kotlin.Int))`(`cap:` ` [TextKeyListener.Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize)!`, `cs:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `off:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns whether it makes sense to automatically capitalize at the specified position in the specified text, with the specified rules. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener) |------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustMetaAfterKeypress](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#adjustMetaAfterKeypress(android.text.Spannable))`(`content:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [adjustMetaAfterKeypress](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#adjustMetaAfterKeypress(kotlin.Long))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). Takes the current state, returns the new state. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(android.view.View,%20android.text.Editable,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(kotlin.Long,%20kotlin.Int))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Clears the state of the specified meta key if it is locked. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(android.text.Editable,%20kotlin.Int))`(`content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` <br /> Gets the state of the meta keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20android.view.KeyEvent))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Gets the state of the meta keys for a specific key event. For input devices that use toggled key modifiers, the \`toggled' state is stored into the text buffer. This method retrieves the meta state for this event, accounting for the stored state. If the event has been created by a device that does not support toggled key modifiers, like a virtual device for example, the stored state is ignored. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state of a particular meta key. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int,%20android.view.KeyEvent))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Gets the state of a particular meta key to use with a particular key event. If the key event has been created by a device that does not support toggled key modifiers, like a virtual keyboard for example, only the meta state in the key event is considered. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Gets the state of the meta keys. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long,%20kotlin.Int))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> Gets the state of a particular meta key. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyDown](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyDown(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Handles presses of the meta keys. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyUp](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyUp(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Handles release of the meta keys. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetaTracker](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#isMetaTracker(kotlin.CharSequence,%20kotlin.Any))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Returns true if this object is one that this class would use to keep track of any meta state in the specified text. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectingMetaTracker](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#isSelectingMetaTracker(kotlin.CharSequence,%20kotlin.Any))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` <br /> Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#onKeyUp(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Handles release of the meta keys. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetLockedMeta](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetLockedMeta(android.text.Spannable))`(`content:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [resetLockedMeta](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetLockedMeta(kotlin.Long))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` <br /> Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetMetaState(android.text.Spannable))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` <br /> Resets all meta state to inactive. <br /> | ||
| From class [BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) |------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [backspace](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener#backspace(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Performs the action that happens when you press the [KeyEvent.KEYCODE_DEL](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_DEL:kotlin.Int) key in a [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#). If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+DEL deletes everything on the line the cursor is on. <br /> | | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [forwardDelete](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener#forwardDelete(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` <br /> Performs the action that happens when you press the [KeyEvent.KEYCODE_FORWARD_DEL](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_FORWARD_DEL:kotlin.Int) key in a [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#). If there is a selection, deletes the selection; otherwise, deletes the character before the cursor, if any; ALT+FORWARD_DEL deletes everything on the line the cursor is on. <br /> | ||
| From class [KeyListener](https://developer.android.com/reference/kotlin/android/text/method/KeyListener) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getInputType](https://developer.android.com/reference/kotlin/android/text/method/KeyListener#getInputType())`()` <br /> Return the type of text that this key listener is manipulating, as per [android.text.InputType](https://developer.android.com/reference/kotlin/android/text/InputType.html#). This is used to determine the mode of the soft keyboard that is shown for the editor. If you return [android.text.InputType#TYPE_NULL](https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int) then*no*soft keyboard will provided. In other words, you must be providing your own key pad for on-screen input and the key listener will be used to handle input from a hard keyboard. If you return any other value, a soft input method will be created when the user puts focus in the editor, which will provide a keypad and also consume hard key events. This means that the key listener will generally not be used, instead the soft input method will take care of managing key input as per the content type returned here. <br /> | ||
| --- | --- | --- | --- | --- | --- | --- | --- |

## Public constructors

### TextKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
TextKeyListener(
    cap: TextKeyListener.Capitalize!, 
    autotext: Boolean)
```

Creates a new TextKeyListener with the specified capitalization and correction properties.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cap` | [TextKeyListener.Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize)!:when, if ever, to automatically capitalize. |
| `autotext` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to automatically do spelling corrections. |

## Public methods

### clear

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun clear(e: Editable!): Unit
```

Clear all the input state (autotext, autocap, multitap, undo) from the specified Editable, going beyond Editable.clear(), which just clears the text but not the input state.

| Parameters ||
|-----|--------------------------------------------------------------------------------------------------------------------------------------------|
| `e` | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!:the buffer whose text and state are to be cleared. |

### getInputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getInputType(): Int
```  

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(): TextKeyListener!
```

Returns a new or existing instance with no automatic capitalization or correction. 

### getInstance

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getInstance(
    autotext: Boolean, 
    cap: TextKeyListener.Capitalize!
): TextKeyListener!
```

Returns a new or existing instance with the specified capitalization and correction properties.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cap` | [TextKeyListener.Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize)!:when, if ever, to automatically capitalize. |
| `autotext` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html):whether to automatically do spelling corrections. |

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

### onKeyOther

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyOther(
    view: View!, 
    content: Editable!, 
    event: KeyEvent!
): Boolean
```  

### onKeyUp

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onKeyUp(
    view: View!, 
    content: Editable!, 
    keyCode: Int, 
    event: KeyEvent!
): Boolean
```  

### onSpanAdded

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSpanAdded(
    s: Spannable!, 
    what: Any!, 
    start: Int, 
    end: Int
): Unit
```  

### onSpanChanged

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSpanChanged(
    s: Spannable!, 
    what: Any!, 
    start: Int, 
    end: Int, 
    st: Int, 
    en: Int
): Unit
```  

### onSpanRemoved

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onSpanRemoved(
    s: Spannable!, 
    what: Any!, 
    start: Int, 
    end: Int
): Unit
```  

### release

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun release(): Unit
```  

### shouldCap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun shouldCap(
    cap: TextKeyListener.Capitalize!, 
    cs: CharSequence!, 
    off: Int
): Boolean
```

Returns whether it makes sense to automatically capitalize at the specified position in the specified text, with the specified rules.

| Parameters ||
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `cap` | [TextKeyListener.Capitalize](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener.Capitalize)!:the capitalization rules to consider. |
| `cs` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the text in which an insertion is being made. |
| `off` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the offset into that text where the insertion is being made. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | whether the character being inserted should be capitalized. |
