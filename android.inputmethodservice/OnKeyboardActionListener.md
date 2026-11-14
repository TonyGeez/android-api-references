# KeyboardView.OnKeyboardActionListener

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# OnKeyboardActionListener

Kotlin| [Java](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md) 
| --- | --- |

```
interface OnKeyboardActionListener
```

| [android.inputmethodservice.KeyboardView.OnKeyboardActionListener](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md) |

| **This interface was deprecated in API level 29.**
|
| Deprecated in Java.

Listener for virtual keyboard events.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onKey](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`(`primaryCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `keyCodes:` ` [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!`)` Send a key press to the listener. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onPress](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`(`primaryCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the user presses a key. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onRelease](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`(`primaryCode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Called when the user releases a key. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onText](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sends a sequence of characters to the listener. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swipeDown](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`()` Called when the user quickly moves the finger from up to down. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swipeLeft](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`()` Called when the user quickly moves the finger from right to left. |
| --- | --- |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swipeRight](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`()` Called when the user quickly moves the finger from left to right. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [swipeUp](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))`()` Called when the user quickly moves the finger from down to up. |

## Public methods

### onKey

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onKey(
    primaryCode: Int, 
    keyCodes: IntArray!
): Unit
```

**Deprecated:** *Deprecated in Java.*

Send a key press to the listener.

| Parameters ||
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primaryCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):this is the key that was pressed |
| `keyCodes` | [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)!:the codes for all the possible alternative keys with the primary code being the first. If the primary key code is a single character such as an alphabet or number or symbol, the alternatives will include other characters that may be on the same key or adjacent keys. These codes are useful to correct for accidental presses of a key adjacent to the intended key. |

### onPress

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onPress(primaryCode: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the user presses a key. This is sent before the [onKey](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))is called. For keys that repeat, this is only called once.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `primaryCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the unicode of the key being pressed. If the touch is not on a valid key, the value will be zero. |

### onRelease

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onRelease(primaryCode: Int): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the user releases a key. This is sent after the [onKey](../android/inputmethodservice/KeyboardView.OnKeyboardActionListener.md))is called. For keys that repeat, this is only called once.

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------|
| `primaryCode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the code of the key that was released |

### onText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun onText(text: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sends a sequence of characters to the listener.

| Parameters ||
|--------|--------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!:the sequence of characters to be displayed. |

### swipeDown

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun swipeDown(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the user quickly moves the finger from up to down. 

### swipeLeft

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun swipeLeft(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the user quickly moves the finger from right to left. 

### swipeRight

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun swipeRight(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the user quickly moves the finger from left to right. 

### swipeUp

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun swipeUp(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when the user quickly moves the finger from down to up.
