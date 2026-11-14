Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextSnapshot

Kotlin | [Java](https://developer.android.com/reference/android/view/inputmethod/TextSnapshot "View this page in Java")

```
class TextSnapshot
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.inputmethod.TextSnapshot](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#) |

An immutable data snapshot of text editing state.

## Summary

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#TextSnapshot(android.view.inputmethod.SurroundingText,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)(surroundingText: https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText, compositionStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, compositionEnd: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, cursorCapsMode: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new instance of `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#` |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#getCompositionEnd()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#getCompositionStart()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#getCursorCapsMode()()` The capitalization mode of the first character being edited in the text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#getSelectionEnd()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#getSelectionStart()()` <br /> |
| [SurroundingText](https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#getSurroundingText()()` <br /> |

## Public constructors

### TextSnapshot

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
TextSnapshot(
    surroundingText: SurroundingText, 
    compositionStart: Int, 
    compositionEnd: Int, 
    cursorCapsMode: Int)
```

Creates a new instance of `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextSnapshot#`

| Parameters ||
|---|---|
| `surroundingText` | [SurroundingText](https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText): `https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText` of the current edit field. This value cannot be `null`. |
| `compositionStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The start index of the composing text. `-1` if there is no composing text. Value is -1 or greater |
| `compositionEnd` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The end index of the composing text. `-1` if there is no composing text. Value is -1 or greater |
| `cursorCapsMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The capitalization mode of the first character being edited in the text. See `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialCapsMode:kotlin.Int`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `compositionStart` and/or `compositionEnd` is less than `-1`. |
| `java.lang.NullPointerException` | if `surroundingText` is `null`. |

## Public methods

### getCompositionEnd

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCompositionEnd(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The end index of the composing text. `-1` if there is no composing text. Value is -1 or greater |

### getCompositionStart

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCompositionStart(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The end index of the composing text. `-1` if there is no composing text. Value is -1 or greater |

### getCursorCapsMode

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCursorCapsMode(): Int
```

The capitalization mode of the first character being edited in the text.

Values may be any combination of the following values:

- `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_CHARACTERS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_WORDS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_SENTENCES:kotlin.Int`

You should generally just take a non-zero value to mean "start out in caps mode" though.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialCapsMode:kotlin.Int`

### getSelectionEnd

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSelectionEnd(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The end index of the selection range. `-1` if it is not available. Value is -1 or greater |

### getSelectionStart

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSelectionStart(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The start index of the selection range. `-1` if it is not available. Value is -1 or greater |

### getSurroundingText

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSurroundingText(): SurroundingText
```

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText` | `https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText` of the current edit field. This value cannot be `null`. |
