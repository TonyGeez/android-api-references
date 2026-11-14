# KeyboardShortcutInfo

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# KeyboardShortcutInfo

Kotlin| [Java](../android/view/KeyboardShortcutInfo.md) 
| --- | --- |

```
class KeyboardShortcutInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.KeyboardShortcutInfo](../android/view/KeyboardShortcutInfo.md) |

Information about a Keyboard Shortcut.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [KeyboardShortcutInfo](../android/view/KeyboardShortcutInfo.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `baseCharacter:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`, `modifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [KeyboardShortcutInfo](../android/view/KeyboardShortcutInfo.md))`(`label:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `keycode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `modifiers:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/KeyboardShortcutInfo.md))`()` <br /> |
| [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html) | [getBaseCharacter](../android/view/KeyboardShortcutInfo.md))`()` Returns the base character that, combined with the modifiers, triggers this shortcut. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getKeycode](../android/view/KeyboardShortcutInfo.md))`()` Returns the base keycode that, combined with the modifiers, triggers this shortcut. |
| --- | --- |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | [getLabel](../android/view/KeyboardShortcutInfo.md))`()` Returns the label to be used to describe this shortcut. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getModifiers](../android/view/KeyboardShortcutInfo.md))`()` Returns the set of modifiers that, combined with the key, trigger this shortcut. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/KeyboardShortcutInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [KeyboardShortcutInfo](../android/view/KeyboardShortcutInfo.md)!\> | [CREATOR](../android/view/KeyboardShortcutInfo.md) <br /> |

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
| `modifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of modifiers that, combined with the key, trigger the shortcut. These should be a combination of [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md) and [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md). |
| --- | --- |

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
| `keycode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The keycode that triggers the shortcut. This should be a valid constant defined in [KeyEvent](../android/view/KeyEvent.md). |
| `modifiers` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The set of modifiers that, combined with the key, trigger the shortcut. These should be a combination of [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md) and [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md). |
| --- | --- |

## Public methods

### describeContents

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getBaseCharacter

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getBaseCharacter(): Char
```

Returns the base character that, combined with the modifiers, triggers this shortcut. If the keycode was set instead, returns [Character.MIN_VALUE](../java/lang/Character.md). 

### getKeycode

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getKeycode(): Int
```

Returns the base keycode that, combined with the modifiers, triggers this shortcut. If the base character was set instead, returns [KeyEvent.KEYCODE_UNKNOWN](../android/view/KeyEvent.md). Valid keycodes are defined as constants in [KeyEvent](../android/view/KeyEvent.md). 

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

Returns the set of modifiers that, combined with the key, trigger this shortcut. These can be a combination of [KeyEvent.META_CTRL_ON](../android/view/KeyEvent.md), [KeyEvent.META_SHIFT_ON](../android/view/KeyEvent.md), [KeyEvent.META_META_ON](../android/view/KeyEvent.md), [KeyEvent.META_ALT_ON](../android/view/KeyEvent.md), [KeyEvent.META_FUNCTION_ON](../android/view/KeyEvent.md) and [KeyEvent.META_SYM_ON](../android/view/KeyEvent.md). 

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<KeyboardShortcutInfo!>
```
