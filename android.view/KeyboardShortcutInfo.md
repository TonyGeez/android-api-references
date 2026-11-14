# KeyboardShortcutInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyboardShortcutInfo

Kotlin| [Java](https://developer.android.com/reference/android/view/KeyboardShortcutInfo "View this page in Java") 

```
class KeyboardShortcutInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.KeyboardShortcutInfo](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#) |

Information about a Keyboard Shortcut.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyboardShortcutInfo](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#KeyboardShortcutInfo(kotlin.CharSequence,%20kotlin.Char,%20kotlin.Int))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `baseCharacter:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `modifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [KeyboardShortcutInfo](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#KeyboardShortcutInfo(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `keycode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `modifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#describeContents())`()` <br /> |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getBaseCharacter](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#getBaseCharacter())`()` Returns the base character that, combined with the modifiers, triggers this shortcut. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeycode](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#getKeycode())`()` Returns the base keycode that, combined with the modifiers, triggers this shortcut. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getLabel](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#getLabel())`()` Returns the label to be used to describe this shortcut. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#getModifiers())`()` Returns the set of modifiers that, combined with the key, trigger this shortcut. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [KeyboardShortcutInfo](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/KeyboardShortcutInfo#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### KeyboardShortcutInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyboardShortcutInfo(
    label: CharSequence!, 
    baseCharacter: Char, 
    modifiers: Int)
```

| Parameters ||
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The label that identifies the action performed by this shortcut. |
| `baseCharacter` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):The character that triggers the shortcut. |
| `modifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of modifiers that, combined with the key, trigger the shortcut. These should be a combination of [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int) and [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int). |

### KeyboardShortcutInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
KeyboardShortcutInfo(
    label: CharSequence!, 
    keycode: Int, 
    modifiers: Int)
```

| Parameters ||
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `label` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:The label that identifies the action performed by this shortcut. |
| `keycode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The keycode that triggers the shortcut. This should be a valid constant defined in [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent). |
| `modifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of modifiers that, combined with the key, trigger the shortcut. These should be a combination of [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int) and [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int). |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBaseCharacter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBaseCharacter(): Char
```

Returns the base character that, combined with the modifiers, triggers this shortcut. If the keycode was set instead, returns [Character.MIN_VALUE](https://developer.android.com/reference/kotlin/java/lang/Character.html#MIN_VALUE:kotlin.Char). 

### getKeycode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeycode(): Int
```

Returns the base keycode that, combined with the modifiers, triggers this shortcut. If the base character was set instead, returns [KeyEvent.KEYCODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/KeyEvent#KEYCODE_UNKNOWN:kotlin.Int). Valid keycodes are defined as constants in [KeyEvent](https://developer.android.com/reference/kotlin/android/view/KeyEvent). 

### getLabel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLabel(): CharSequence?
```

Returns the label to be used to describe this shortcut.

| Return ||
|------------------------------------------------------------------------------------------------|--------------------------|
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | This value may be`null`. |

### getModifiers

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getModifiers(): Int
```

Returns the set of modifiers that, combined with the key, trigger this shortcut. These can be a combination of [KeyEvent.META_CTRL_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_CTRL_ON:kotlin.Int), [KeyEvent.META_SHIFT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SHIFT_ON:kotlin.Int), [KeyEvent.META_META_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_META_ON:kotlin.Int), [KeyEvent.META_ALT_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_ALT_ON:kotlin.Int), [KeyEvent.META_FUNCTION_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_FUNCTION_ON:kotlin.Int) and [KeyEvent.META_SYM_ON](https://developer.android.com/reference/kotlin/android/view/KeyEvent#META_SYM_ON:kotlin.Int). 

### writeToParcel

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<KeyboardShortcutInfo!>
```
