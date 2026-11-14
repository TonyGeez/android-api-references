# MetaKeyKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MetaKeyKeyListener

Kotlin| [Java](https://developer.android.com/reference/android/text/method/MetaKeyKeyListener "View this page in Java") 
| --- | --- |

```
abstract class MetaKeyKeyListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#) |

| Known Direct Subclasses [BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) |-------------------------------------------------------------------------------------------------------|----------------------------------------| | [BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) | Abstract base class for key listeners. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener), [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener), [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener), [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener), [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener), [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener), [QwertyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/QwertyKeyListener), [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener), [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener) | For entering dates in a text field. | | [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener) | For entering dates and times in the same text field. | | [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener) | For dialing-only text entry | | [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener) | For digits-only text entry | | [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener) | For numeric text entry | | [QwertyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/QwertyKeyListener) | This is the standard key listener for alphabetic input on qwerty keyboards. | | [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) | This is the key listener for typing normal text. | | [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This base class encapsulates the behavior for tracking the state of meta keys such as SHIFT, ALT and SYM as well as the pseudo-meta state of selecting text.

Key listeners that care about meta state should inherit from this class; you should not instantiate this class directly in a client.

This class provides two mechanisms for tracking meta state that can be used together or independently.

- Methods such as [handleKeyDown(long,int,android.view.KeyEvent)](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyDown(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent))and [getMetaState(long)](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long))operate on a meta key state bit mask.
- Methods such as [onKeyDown(android.view.View,android.text.Editable,int,android.view.KeyEvent)](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#onKeyDown(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))and [getMetaState(java.lang.CharSequence,int)](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int))operate on meta key state flags stored as spans in an [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#) text buffer. The spans only describe the current meta key state of the text editor; they do not carry any positional information.

The behavior of this class varies according to the keyboard capabilities described by the [KeyCharacterMap](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#) of the keyboard device such as the [key modifier behavior](https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap.html#getModifierBehavior()).

[MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#) implements chorded and toggled key modifiers. When key modifiers are toggled into a latched or locked state, the state of the modifier is stored in the [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#) text buffer or in a meta state integer managed by the client. These latched or locked modifiers should be considered to be held**in addition to** those that the keyboard already reported as being pressed in [KeyEvent.getMetaState()](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#getMetaState()). In other words, the [MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#) augments the meta state provided by the keyboard; it does not replace it. This distinction is important to ensure that meta keys not handled by [MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#) such as [KeyEvent.KEYCODE_CAPS_LOCK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_CAPS_LOCK:kotlin.Int) or [KeyEvent.KEYCODE_NUM_LOCK](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#KEYCODE_NUM_LOCK:kotlin.Int) are taken into consideration.

To ensure correct meta key behavior, the following pattern should be used when mapping key codes to characters:
` private char getUnicodeChar(TextKeyListener listener, KeyEvent event, Editable textBuffer) { // Use the combined meta states from the event and the key listener. int metaState = event.getMetaState() | listener.getMetaState(textBuffer); return event.getUnicodeChar(metaState); } `
| --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_LOCKED](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_LOCKED:kotlin.Int) Flag that indicates that the ALT key is locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_ON:kotlin.Int) Flag that indicates that the ALT key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_CAP_LOCKED](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_CAP_LOCKED:kotlin.Int) Flag that indicates that the SHIFT key is locked in CAPS mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SHIFT_ON:kotlin.Int) Flag that indicates that the SHIFT key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_LOCKED](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_LOCKED:kotlin.Int) Flag that indicates that the SYM key is locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_ON:kotlin.Int) Flag that indicates that the SYM key is on. |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#MetaKeyKeyListener())`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustMetaAfterKeypress](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#adjustMetaAfterKeypress(android.text.Spannable))`(`content:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [adjustMetaAfterKeypress](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#adjustMetaAfterKeypress(kotlin.Long))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(android.view.View,%20android.text.Editable,%20kotlin.Int))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(kotlin.Long,%20kotlin.Int))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Clears the state of the specified meta key if it is locked. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#clearMetaKeyState(android.text.Editable,%20kotlin.Int))`(`content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Gets the state of the meta keys. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20android.view.KeyEvent))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Gets the state of the meta keys for a specific key event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the state of a particular meta key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.CharSequence,%20kotlin.Int,%20android.view.KeyEvent))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Gets the state of a particular meta key to use with a particular key event. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Gets the state of the meta keys. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#getMetaState(kotlin.Long,%20kotlin.Int))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the state of a particular meta key. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyDown](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyDown(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Handles presses of the meta keys. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyUp](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#handleKeyUp(kotlin.Long,%20kotlin.Int,%20android.view.KeyEvent))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Handles release of the meta keys. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetaTracker](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#isMetaTracker(kotlin.CharSequence,%20kotlin.Any))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns true if this object is one that this class would use to keep track of any meta state in the specified text. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectingMetaTracker](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#isSelectingMetaTracker(kotlin.CharSequence,%20kotlin.Any))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#onKeyDown(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Handles presses of the meta keys. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#onKeyUp(android.view.View,%20android.text.Editable,%20kotlin.Int,%20android.view.KeyEvent))`(`view:` ` [View](https://developer.android.com/reference/kotlin/android/view/View.html#)!`, `content:` ` [Editable](https://developer.android.com/reference/kotlin/android/text/Editable.html#)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!`)` Handles release of the meta keys. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [resetLockedMeta](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetLockedMeta(kotlin.Long))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetMetaState](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetMetaState(android.text.Spannable))`(`text:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Resets all meta state to inactive. |

| Protected methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetLockedMeta](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#resetLockedMeta(android.text.Spannable))`(`content:` ` [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable.html#)!`)` Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. |

## Constants

### META_ALT_LOCKED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_ALT_LOCKED: Int
```

Flag that indicates that the ALT key is locked. 

 Value: 512

### META_ALT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_ALT_ON: Int
```

Flag that indicates that the ALT key is on. Value equals [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_ALT_ON:kotlin.Int). 

 Value: 2

### META_CAP_LOCKED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_CAP_LOCKED: Int
```

Flag that indicates that the SHIFT key is locked in CAPS mode. 

 Value: 256

### META_SHIFT_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_SHIFT_ON: Int
```

Flag that indicates that the SHIFT key is on. Value equals [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SHIFT_ON:kotlin.Int). 

 Value: 1

### META_SYM_LOCKED

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_SYM_LOCKED: Int
```

Flag that indicates that the SYM key is locked. 

 Value: 1024

### META_SYM_ON

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val META_SYM_ON: Int
```

Flag that indicates that the SYM key is on. Value equals [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#META_SYM_ON:kotlin.Int). 

 Value: 4

## Public constructors

### MetaKeyKeyListener

```
MetaKeyKeyListener()
```

## Public methods

### adjustMetaAfterKeypress

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun adjustMetaAfterKeypress(content: Spannable!): Unit
```

Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). 

### adjustMetaAfterKeypress

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun adjustMetaAfterKeypress(state: Long): Long
```

Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). Takes the current state, returns the new state. 

### clearMetaKeyState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearMetaKeyState(
    view: View!, 
    content: Editable!, 
    states: Int
): Unit
```  

### clearMetaKeyState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun clearMetaKeyState(
    state: Long, 
    which: Int
): Long
```

Clears the state of the specified meta key if it is locked.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `state` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the meta key state |
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):meta keys to clear, may be a combination of [META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SHIFT_ON:kotlin.Int), [META_ALT_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_ALT_ON:kotlin.Int) or [META_SYM_ON](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener#META_SYM_ON:kotlin.Int). |

### clearMetaKeyState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun clearMetaKeyState(
    content: Editable!, 
    states: Int
): Unit
```  

### getMetaState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMetaState(text: CharSequence!): Int
```

Gets the state of the meta keys.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the buffer in which the meta key would have been pressed. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an integer in which each bit set to one represents a pressed or locked meta key. |

### getMetaState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMetaState(
    text: CharSequence!, 
    event: KeyEvent!
): Int
```

Gets the state of the meta keys for a specific key event. For input devices that use toggled key modifiers, the \`toggled' state is stored into the text buffer. This method retrieves the meta state for this event, accounting for the stored state. If the event has been created by a device that does not support toggled key modifiers, like a virtual device for example, the stored state is ignored.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the buffer in which the meta key would have been pressed. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:the event for which to evaluate the meta state. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an integer in which each bit set to one represents a pressed or locked meta key. |

### getMetaState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMetaState(
    text: CharSequence!, 
    meta: Int
): Int
```

Gets the state of a particular meta key.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `meta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):META_SHIFT_ON, META_ALT_ON, META_SYM_ON |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the buffer in which the meta key would have been pressed. |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 if inactive, 1 if active, 2 if locked. |

### getMetaState

Added in [API level 19](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMetaState(
    text: CharSequence!, 
    meta: Int, 
    event: KeyEvent!
): Int
```

Gets the state of a particular meta key to use with a particular key event. If the key event has been created by a device that does not support toggled key modifiers, like a virtual keyboard for example, only the meta state in the key event is considered.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `meta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):META_SHIFT_ON, META_ALT_ON, META_SYM_ON |
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the buffer in which the meta key would have been pressed. |
| `event` | [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent.html#)!:the event for which to evaluate the meta state. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 if inactive, 1 if active, 2 if locked. |

### getMetaState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMetaState(state: Long): Int
```

Gets the state of the meta keys.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------|
| `state` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the current meta state bits. |

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | an integer in which each bit set to one represents a pressed or locked meta key. |

### getMetaState

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static fun getMetaState(
    state: Long, 
    meta: Int
): Int
```

Gets the state of a particular meta key.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------|
| `state` | [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html):the current state bits. |
| `meta` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):META_SHIFT_ON, META_ALT_ON, or META_SYM_ON |

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | 0 if inactive, 1 if active, 2 if locked. |

### handleKeyDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun handleKeyDown(
    state: Long, 
    keyCode: Int, 
    event: KeyEvent!
): Long
```

Handles presses of the meta keys. 

### handleKeyUp

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun handleKeyUp(
    state: Long, 
    keyCode: Int, 
    event: KeyEvent!
): Long
```

Handles release of the meta keys. 

### isMetaTracker

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isMetaTracker(
    text: CharSequence!, 
    what: Any!
): Boolean
```

Returns true if this object is one that this class would use to keep track of any meta state in the specified text. 

### isSelectingMetaTracker

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun isSelectingMetaTracker(
    text: CharSequence!, 
    what: Any!
): Boolean
```

Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. 

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

Handles release of the meta keys. 

### resetLockedMeta

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun resetLockedMeta(state: Long): Long
```

Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. 

### resetMetaState

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun resetMetaState(text: Spannable!): Unit
```

Resets all meta state to inactive.

## Protected methods

### resetLockedMeta

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open static fun resetLockedMeta(content: Spannable!): Unit
```

Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key.
