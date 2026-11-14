# MetaKeyKeyListener

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MetaKeyKeyListener

Kotlin| [Java](MetaKeyKeyListener.md) 
| --- | --- |

```
abstract class MetaKeyKeyListener
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.method.MetaKeyKeyListener](MetaKeyKeyListener.md) |

| Known Direct Subclasses [BaseKeyListener](BaseKeyListener.md) |-------------------------------------------------------------------------------------------------------|----------------------------------------| | [BaseKeyListener](BaseKeyListener.md) | Abstract base class for key listeners. | |
| --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DateKeyListener](DateKeyListener.md), [DateTimeKeyListener](DateTimeKeyListener.md), [DialerKeyListener](DialerKeyListener.md), [DigitsKeyListener](DigitsKeyListener.md), [MultiTapKeyListener](MultiTapKeyListener.md), [NumberKeyListener](NumberKeyListener.md), [QwertyKeyListener](QwertyKeyListener.md), [TextKeyListener](TextKeyListener.md), [TimeKeyListener](TimeKeyListener.md) |---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------| | [DateKeyListener](DateKeyListener.md) | For entering dates in a text field. | | [DateTimeKeyListener](DateTimeKeyListener.md) | For entering dates and times in the same text field. | | [DialerKeyListener](DialerKeyListener.md) | For dialing-only text entry | | [DigitsKeyListener](DigitsKeyListener.md) | For digits-only text entry | | [MultiTapKeyListener](MultiTapKeyListener.md) | This is the standard key listener for alphabetic input on 12-key keyboards. | | [NumberKeyListener](NumberKeyListener.md) | For numeric text entry | | [QwertyKeyListener](QwertyKeyListener.md) | This is the standard key listener for alphabetic input on qwerty keyboards. | | [TextKeyListener](TextKeyListener.md) | This is the key listener for typing normal text. | | [TimeKeyListener](TimeKeyListener.md) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

This base class encapsulates the behavior for tracking the state of meta keys such as SHIFT, ALT and SYM as well as the pseudo-meta state of selecting text.

Key listeners that care about meta state should inherit from this class; you should not instantiate this class directly in a client.

This class provides two mechanisms for tracking meta state that can be used together or independently.

- Methods such as [handleKeyDown(long,int,android.view.KeyEvent)](MetaKeyKeyListener.md))and [getMetaState(long)](MetaKeyKeyListener.md))operate on a meta key state bit mask.
- Methods such as [onKeyDown(android.view.View,android.text.Editable,int,android.view.KeyEvent)](MetaKeyKeyListener.md))and [getMetaState(java.lang.CharSequence,int)](MetaKeyKeyListener.md))operate on meta key state flags stored as spans in an [Editable](../android.text/Editable.md) text buffer. The spans only describe the current meta key state of the text editor; they do not carry any positional information.

The behavior of this class varies according to the keyboard capabilities described by the [KeyCharacterMap](../android.view/KeyCharacterMap.md) of the keyboard device such as the [key modifier behavior](../android.view/KeyCharacterMap.md)).

[MetaKeyKeyListener](MetaKeyKeyListener.md) implements chorded and toggled key modifiers. When key modifiers are toggled into a latched or locked state, the state of the modifier is stored in the [Editable](../android.text/Editable.md) text buffer or in a meta state integer managed by the client. These latched or locked modifiers should be considered to be held**in addition to** those that the keyboard already reported as being pressed in [KeyEvent.getMetaState()](../android.view/KeyEvent.md)). In other words, the [MetaKeyKeyListener](MetaKeyKeyListener.md) augments the meta state provided by the keyboard; it does not replace it. This distinction is important to ensure that meta keys not handled by [MetaKeyKeyListener](MetaKeyKeyListener.md) such as [KeyEvent.KEYCODE_CAPS_LOCK](../android.view/KeyEvent.md) or [KeyEvent.KEYCODE_NUM_LOCK](../android.view/KeyEvent.md) are taken into consideration.

To ensure correct meta key behavior, the following pattern should be used when mapping key codes to characters:
` private char getUnicodeChar(TextKeyListener listener, KeyEvent event, Editable textBuffer) { // Use the combined meta states from the event and the key listener. int metaState = event.getMetaState() | listener.getMetaState(textBuffer); return event.getUnicodeChar(metaState); } `
| --- | --- |

## Summary

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_LOCKED](MetaKeyKeyListener.md) Flag that indicates that the ALT key is locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_ALT_ON](MetaKeyKeyListener.md) Flag that indicates that the ALT key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_CAP_LOCKED](MetaKeyKeyListener.md) Flag that indicates that the SHIFT key is locked in CAPS mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SHIFT_ON](MetaKeyKeyListener.md) Flag that indicates that the SHIFT key is on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_LOCKED](MetaKeyKeyListener.md) Flag that indicates that the SYM key is locked. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [META_SYM_ON](MetaKeyKeyListener.md) Flag that indicates that the SYM key is on. |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------|---|
| [MetaKeyKeyListener](MetaKeyKeyListener.md))`()` <br /> |

| Public methods ||
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [adjustMetaAfterKeypress](MetaKeyKeyListener.md))`(`content:` ` [Spannable](../android.text/Spannable.md)!`)` Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [adjustMetaAfterKeypress](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call this method after you handle a keypress so that the meta state will be reset to unshifted (if it is not still down) or primed to be reset to unshifted (once it is released). |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](MetaKeyKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |
| open [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [clearMetaKeyState](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `which:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Clears the state of the specified meta key if it is locked. |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [clearMetaKeyState](MetaKeyKeyListener.md))`(`content:` ` [Editable](../android.text/Editable.md)!`, `states:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Gets the state of the meta keys. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Gets the state of the meta keys for a specific key event. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the state of a particular meta key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Gets the state of a particular meta key to use with a particular key event. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Gets the state of the meta keys. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getMetaState](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `meta:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the state of a particular meta key. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyDown](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Handles presses of the meta keys. |
| --- | --- |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [handleKeyUp](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Handles release of the meta keys. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isMetaTracker](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns true if this object is one that this class would use to keep track of any meta state in the specified text. |
| openstatic [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isSelectingMetaTracker](MetaKeyKeyListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `what:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)!`)` Returns true if this object is one that this class would use to keep track of the selecting meta state in the specified text. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyDown](MetaKeyKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Handles presses of the meta keys. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [onKeyUp](MetaKeyKeyListener.md))`(`view:` ` [View](../android.view/View.md)!`, `content:` ` [Editable](../android.text/Editable.md)!`, `keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `event:` ` [KeyEvent](../android.view/KeyEvent.md)!`)` Handles release of the meta keys. |
| openstatic [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [resetLockedMeta](MetaKeyKeyListener.md))`(`state:` ` [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)`)` Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. |
| --- | --- |
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetMetaState](MetaKeyKeyListener.md))`(`text:` ` [Spannable](../android.text/Spannable.md)!`)` Resets all meta state to inactive. |

| Protected methods ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| openstatic [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [resetLockedMeta](MetaKeyKeyListener.md))`(`content:` ` [Spannable](../android.text/Spannable.md)!`)` Call this if you are a method that ignores the locked meta state (arrow keys, for example) and you handle a key. |

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

Flag that indicates that the ALT key is on. Value equals [KeyEvent.META_ALT_ON](../android.view/KeyEvent.md). 

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

Flag that indicates that the SHIFT key is on. Value equals [KeyEvent.META_SHIFT_ON](../android.view/KeyEvent.md). 

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

Flag that indicates that the SYM key is on. Value equals [KeyEvent.META_SYM_ON](../android.view/KeyEvent.md). 

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
| `which` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):meta keys to clear, may be a combination of [META_SHIFT_ON](MetaKeyKeyListener.md), [META_ALT_ON](MetaKeyKeyListener.md) or [META_SYM_ON](MetaKeyKeyListener.md). |

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
| `event` | [KeyEvent](../android.view/KeyEvent.md)!:the event for which to evaluate the meta state. |

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
| `event` | [KeyEvent](../android.view/KeyEvent.md)!:the event for which to evaluate the meta state. |
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
