# KeyCharacterMap

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyCharacterMap

Kotlin | [Java](KeyCharacterMap.md) 
| --- | --- |

```
open class KeyCharacterMap : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.KeyCharacterMap](KeyCharacterMap.md) |

Describes the keys provided by a keyboard device and their associated labels.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [KeyData](../android/view/KeyCharacterMap.KeyData.md) Describes the character mappings associated with a key. |
| open | [UnavailableException](../android/view/KeyCharacterMap.UnavailableException.md) Thrown by [KeyCharacterMap.load](KeyCharacterMap.md)) when a key character map could not be loaded. |

| Constants ||
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [ALPHA](KeyCharacterMap.md) A keyboard with all the letters, and maybe some numbers. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [BUILT_IN_KEYBOARD](KeyCharacterMap.md) The id of the device's primary built in keyboard is always 0. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMBINING_ACCENT](KeyCharacterMap.md) <br /> |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [COMBINING_ACCENT_MASK](KeyCharacterMap.md) Mask the return value from [get(int,int)](KeyCharacterMap.md)) with this value to get a printable representation of the accent character of a "dead key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FULL](KeyCharacterMap.md) A full PC-style keyboard. |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [HEX_INPUT](KeyCharacterMap.md) This private-use character is used to trigger Unicode character input by hex digits. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODIFIER_BEHAVIOR_CHORDED](KeyCharacterMap.md) Modifier keys may be chorded with character keys. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [MODIFIER_BEHAVIOR_CHORDED_OR_TOGGLED](KeyCharacterMap.md) Modifier keys may be chorded with character keys or they may toggle into latched or locked states when pressed independently. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [NUMERIC](KeyCharacterMap.md) A numeric (12-key) keyboard. |
| --- | --- |
| static [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [PICKER_DIALOG_INPUT](KeyCharacterMap.md) This private-use character is used to bring up a character picker for miscellaneous symbols. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PREDICTIVE](KeyCharacterMap.md) A keyboard with all the letters, but with more than one letter per key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SPECIAL_FUNCTION](KeyCharacterMap.md) A keyboard that is only used to control special functions rather than for typing. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [VIRTUAL_KEYBOARD](KeyCharacterMap.md) The id of a generic virtual keyboard with a full layout that can be used to synthesize key events. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](KeyCharacterMap.md))`()` <br /> |
| open static [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [deviceHasKey](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Queries the framework about whether any physical keys exist on any currently attached input devices that are capable of producing the given key code. |
| open static [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | [deviceHasKeys](KeyCharacterMap.md))`(`keyCodes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Queries the framework about whether any physical keys exist on any currently attached input devices that are capable of producing the given array of key codes. |
| --- | --- |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](KeyCharacterMap.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [get](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the Unicode character generated by the specified key and meta key state combination. |
| open static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getDeadChar](KeyCharacterMap.md))`(`accent:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `c:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Get the character that is produced by combining the dead key producing accent with the key producing character c. |
| --- | --- |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getDisplayLabel](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the primary character for this key. |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [KeyEvent](KeyEvent.md)!\>! | [getEvents](KeyCharacterMap.md))`(`chars:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Get an array of KeyEvent objects that if put into the input stream could plausibly generate the provided sequence of characters. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getKeyData](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `results:` ` [KeyCharacterMap.KeyData](../android/view/KeyCharacterMap.KeyData.md)!`)` Get the character conversion data for a given key code. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeyboardType](KeyCharacterMap.md))`()` Gets the keyboard type. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMatch](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `chars:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`)` Gets the first character in the character array that can be generated by the specified key code. |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getMatch](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `chars:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `metaState:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the first character in the character array that can be generated by the specified key code. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifierBehavior](KeyCharacterMap.md))`()` Gets a constant that describes the behavior of this keyboard's modifier keys such as [KeyEvent.KEYCODE_SHIFT_LEFT](KeyEvent.md). |
| open [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getNumber](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Gets the number or symbol associated with the key. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isPrintingKey](KeyCharacterMap.md))`(`keyCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns true if the specified key produces a glyph. |
| --- | --- |
| open static [KeyCharacterMap](KeyCharacterMap.md)! | [load](KeyCharacterMap.md))`(`deviceId:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Loads the key character maps for the keyboard with the specified device id. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](KeyCharacterMap.md))`(`out:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Protected methods ||
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [finalize](KeyCharacterMap.md))`()` <br /> |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [KeyCharacterMap](KeyCharacterMap.md)!\> | [CREATOR](KeyCharacterMap.md) <br /> |

## Constants

### ALPHA

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ALPHA: Int
```

A keyboard with all the letters, and maybe some numbers.

An alphabetic keyboard supports text entry directly but may have a condensed layout with a small form factor. In contrast to a [full keyboard](KeyCharacterMap.md), some symbols may only be accessible using special on-screen character pickers. In addition, to improve typing speed and accuracy, the framework provides special affordances for alphabetic keyboards such as auto-capitalization and toggled / locked shift and alt keys.

This type of keyboard is generally designed for thumb typing. 

 Value: 3

### BUILT_IN_KEYBOARD

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val BUILT_IN_KEYBOARD: Int
```

**Deprecated:** *This constant should no longer be used because there is no guarantee that a device has a built-in keyboard that can be used for typing text. There might not be a built-in keyboard, the built-in keyboard might be a [NUMERIC](KeyCharacterMap.md) or [SPECIAL_FUNCTION](KeyCharacterMap.md) keyboard, or there might be multiple keyboards installed including external keyboards. When interpreting key presses received from the framework, applications should use the device id specified in the [KeyEvent](KeyEvent.md) received. When synthesizing key presses for delivery elsewhere or when translating key presses from unknown keyboards, applications should use the special [VIRTUAL_KEYBOARD](KeyCharacterMap.md) device id.*

The id of the device's primary built in keyboard is always 0. 

 Value: 0

### COMBINING_ACCENT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMBINING_ACCENT: Int
```  

 Value: -2147483648

### COMBINING_ACCENT_MASK

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val COMBINING_ACCENT_MASK: Int
```

Mask the return value from [get(int,int)](KeyCharacterMap.md)) with this value to get a printable representation of the accent character of a "dead key." 

 Value: 2147483647

### FULL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FULL: Int
```

A full PC-style keyboard.

A full keyboard behaves like a PC keyboard. All symbols are accessed directly by pressing keys on the keyboard without on-screen support or affordances such as auto-capitalization.

This type of keyboard is generally designed for full two hand typing. 

 Value: 4

### HEX_INPUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val HEX_INPUT: Char
```

This private-use character is used to trigger Unicode character input by hex digits. 

 Value: '\uef00'

### MODIFIER_BEHAVIOR_CHORDED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODIFIER_BEHAVIOR_CHORDED: Int
```

Modifier keys may be chorded with character keys. 

 Value: 0

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#getModifierBehavior()> 

### MODIFIER_BEHAVIOR_CHORDED_OR_TOGGLED

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val MODIFIER_BEHAVIOR_CHORDED_OR_TOGGLED: Int
```

Modifier keys may be chorded with character keys or they may toggle into latched or locked states when pressed independently. 

 Value: 1

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/KeyCharacterMap#getModifierBehavior()> 

### NUMERIC

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val NUMERIC: Int
```

A numeric (12-key) keyboard.

A numeric keyboard supports text entry using a multi-tap approach. It may be necessary to tap a key multiple times to generate the desired letter or symbol.

This type of keyboard is generally designed for thumb typing. 

 Value: 1

### PICKER_DIALOG_INPUT

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PICKER_DIALOG_INPUT: Char
```

This private-use character is used to bring up a character picker for miscellaneous symbols. 

 Value: '\uef01'

### PREDICTIVE

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val PREDICTIVE: Int
```

A keyboard with all the letters, but with more than one letter per key.

This type of keyboard is generally designed for thumb typing. 

 Value: 2

### SPECIAL_FUNCTION

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SPECIAL_FUNCTION: Int
```

A keyboard that is only used to control special functions rather than for typing.

A special function keyboard consists only of non-printing keys such as HOME and POWER that are not actually used for typing. 

 Value: 5

### VIRTUAL_KEYBOARD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val VIRTUAL_KEYBOARD: Int
```

The id of a generic virtual keyboard with a full layout that can be used to synthesize key events. Typically used with [getEvents](KeyCharacterMap.md)). 

 Value: -1

## Public methods

### describeContents

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### deviceHasKey

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun deviceHasKey(keyCode: Int): Boolean
```

Queries the framework about whether any physical keys exist on any currently attached input devices that are capable of producing the given key code.

| Parameters ||
|-----------|----------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code to query. |

| Return ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if at least one attached keyboard supports the specified key code. |

### deviceHasKeys

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun deviceHasKeys(keyCodes: IntArray!): BooleanArray!
```

Queries the framework about whether any physical keys exist on any currently attached input devices that are capable of producing the given array of key codes.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------|
| `keyCodes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!: The array of key codes to query. |

| Return ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BooleanArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean-array/index.html)! | A new array of the same size as the key codes array whose elements are set to true if at least one attached keyboard supports the corresponding key code at the same index in the key codes array. |

### equals

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### get

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun get(
    keyCode: Int, 
    metaState: Int
): Int
```

Gets the Unicode character generated by the specified key and meta key state combination.

Returns the Unicode character that the specified key would produce when the specified meta bits (see [MetaKeyKeyListener](../android.text.method/MetaKeyKeyListener.md)) were active.

Returns 0 if the key is not one that is used to type Unicode characters.

If the return value has bit [COMBINING_ACCENT](KeyCharacterMap.md) set, the key is a "dead key" that should be combined with another to actually produce a character -- see [getDeadChar](KeyCharacterMap.md)) -- after masking with [COMBINING_ACCENT_MASK](KeyCharacterMap.md).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The meta key modifier state. |

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The associated character or combining accent, or 0 if none. |

### getDeadChar

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun getDeadChar(
    accent: Int, 
    c: Int
): Int
```

Get the character that is produced by combining the dead key producing accent with the key producing character c. For example, getDeadChar('\`', 'e') returns è. getDeadChar('\^', ' ') returns '\^' and getDeadChar('\^', '\^') returns '\^'.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------|
| `accent` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The accent character. eg. '\`' |
| `c` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The basic character. |

| Return ||
|----------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The combined character, or 0 if the characters cannot be combined. |

### getDisplayLabel

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getDisplayLabel(keyCode: Int): Char
```

Gets the primary character for this key. In other words, the label that is physically printed on it.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |

| Return ||
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The display label character, or 0 if none (eg. for non-printing keys). |

### getEvents

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getEvents(chars: CharArray!): Array<KeyEvent!>!
```

Get an array of KeyEvent objects that if put into the input stream could plausibly generate the provided sequence of characters. It is not guaranteed that the sequence is the only way to generate these events or that it is optimal.

This function is primarily offered for instrumentation and testing purposes. It may fail to map characters to key codes. In particular, the key character map for the [built-in keyboard](KeyCharacterMap.md) device id may be empty. Consider using the key character map associated with the [virtual keyboard](KeyCharacterMap.md) device id instead.

For robust text entry, do not use this function. Instead construct a [KeyEvent](KeyEvent.md) with action code [KeyEvent.ACTION_MULTIPLE](KeyEvent.md) that contains the desired string using [KeyEvent.KeyEvent(long, String, int, int)](KeyEvent.md)).

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The sequence of characters to generate. |

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [KeyEvent](KeyEvent.md)!>! | An array of [KeyEvent](KeyEvent.md) objects, or null if the given char array can not be generated using the current key character map. |

| Exceptions ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [IllegalArgumentException](../java.lang/IllegalArgumentException.md) if the passed array of characters is null. |

### getKeyData

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyData(
    keyCode: Int, 
    results: KeyCharacterMap.KeyData!
): Boolean
```

**Deprecated:** *instead use [KeyCharacterMap.getDisplayLabel(int)](KeyCharacterMap.md)), [KeyCharacterMap.getNumber(int)](KeyCharacterMap.md)) or [KeyCharacterMap.get(int, int)](KeyCharacterMap.md)).*

Get the character conversion data for a given key code.

| Parameters ||
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The keyCode to query. |
| `results` | [KeyCharacterMap.KeyData](../android/view/KeyCharacterMap.KeyData.md)!: A [KeyData](../android/view/KeyCharacterMap.KeyData.md) instance that will be filled with the results. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the key was mapped. If the key was not mapped, results is not modified. |

### getKeyboardType

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getKeyboardType(): Int
```

Gets the keyboard type. Returns [NUMERIC](KeyCharacterMap.md), [PREDICTIVE](KeyCharacterMap.md), [ALPHA](KeyCharacterMap.md), [FULL](KeyCharacterMap.md) or [SPECIAL_FUNCTION](KeyCharacterMap.md).

Different keyboard types have different semantics. Refer to the documentation associated with the keyboard type constants for details.

| Return ||
|----------------------------------------------------------------------------|--------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The keyboard type. |

### getMatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMatch(
    keyCode: Int, 
    chars: CharArray!
): Char
```

Gets the first character in the character array that can be generated by the specified key code.

This is a convenience function that returns the same value as [getMatch(keyCode, chars, 0)](KeyCharacterMap.md)).

| Parameters ||
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The keycode. |
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The array of matching characters to consider. |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The matching associated character, or 0 if none. |

| Exceptions ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [IllegalArgumentException](../java.lang/IllegalArgumentException.md) if the passed array of characters is null. |

### getMatch

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getMatch(
    keyCode: Int, 
    chars: CharArray!, 
    metaState: Int
): Char
```

Gets the first character in the character array that can be generated by the specified key code. If there are multiple choices, prefers the one that would be generated with the specified meta key modifier state.

| Parameters ||
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |
| `chars` | [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!: The array of matching characters to consider. |
| `metaState` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The preferred meta key modifier state. |
| --- | --- |

| Return ||
|------------------------------------------------------------------------------|--------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The matching associated character, or 0 if none. |

| Exceptions ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [IllegalArgumentException](../java.lang/IllegalArgumentException.md) if the passed array of characters is null. |

### getModifierBehavior

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getModifierBehavior(): Int
```

Gets a constant that describes the behavior of this keyboard's modifier keys such as [KeyEvent.KEYCODE_SHIFT_LEFT](KeyEvent.md).

Currently there are two behaviors that may be combined:

- Chorded behavior: When the modifier key is pressed together with one or more character keys, the keyboard inserts the modified keys and then resets the modifier state when the modifier key is released.
- Toggled behavior: When the modifier key is pressed and released on its own it first toggles into a latched state. When latched, the modifier will apply to next character key that is pressed and will then reset itself to the initial state. If the modifier is already latched and the modifier key is pressed and release on its own again, then it toggles into a locked state. When locked, the modifier will apply to all subsequent character keys that are pressed until unlocked by pressing the modifier key on its own one more time to reset it to the initial state. Toggled behavior is useful for small profile keyboards designed for thumb typing.

This function currently returns [MODIFIER_BEHAVIOR_CHORDED](KeyCharacterMap.md) when the [keyboard type](KeyCharacterMap.md)) is [FULL](KeyCharacterMap.md) or [SPECIAL_FUNCTION](KeyCharacterMap.md) and [MODIFIER_BEHAVIOR_CHORDED_OR_TOGGLED](KeyCharacterMap.md) otherwise. In the future, the function may also take into account global keyboard accessibility settings, other user preferences, or new device capabilities.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The modifier behavior for this keyboard. |

**See Also**

- [#MODIFIER_BEHAVIOR_CHORDED](KeyCharacterMap.md)
- [#MODIFIER_BEHAVIOR_CHORDED_OR_TOGGLED](KeyCharacterMap.md) 

### getNumber

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getNumber(keyCode: Int): Char
```

Gets the number or symbol associated with the key.

The character value is returned, not the numeric value. If the key is not a number, but is a symbol, the symbol is retuned.

This method is intended to to support dial pads and other numeric or symbolic entry on keyboards where certain keys serve dual function as alphabetic and symbolic keys. This method returns the number or symbol associated with the key independent of whether the user has pressed the required modifier.

For example, on one particular keyboard the keys on the top QWERTY row generate numbers when ALT is pressed such that ALT-Q maps to '1'. So for that keyboard when [getNumber](KeyCharacterMap.md)) is called with [KeyEvent.KEYCODE_Q](KeyEvent.md) it returns '1' so that the user can type numbers without pressing ALT when it makes sense.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |

| Return ||
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | The associated numeric or symbolic character, or 0 if none. |

### isPrintingKey

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun isPrintingKey(keyCode: Int): Boolean
```

Returns true if the specified key produces a glyph.

| Parameters ||
|-----------|-------------------------------------------------------------------------------------------|
| `keyCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The key code. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | True if the key is a printing key. |

### load

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open static fun load(deviceId: Int): KeyCharacterMap!
```

Loads the key character maps for the keyboard with the specified device id.

| Parameters ||
|------------|------------------------------------------------------------------------------------------------------------|
| `deviceId` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The device id of the keyboard. |

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------------|
| [KeyCharacterMap](KeyCharacterMap.md)! | The associated key character map. |

| Exceptions ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [UnavailableException](../android/view/KeyCharacterMap.UnavailableException.md) if the key character map could not be loaded because it was malformed or the default key character map is missing from the system. |

### writeToParcel

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    out: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | The Parcel in which the object should be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Protected methods

### finalize

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
protected open fun finalize(): Unit
```

| Exceptions ||
|-----------------------|---------------------------------------|
| `java.lang.Throwable` | the `Exception` raised by this method |

## Properties

### CREATOR

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<KeyCharacterMap!>
```
