# ClipboardManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClipboardManager

Kotlin| [Java](https://developer.android.com/reference/android/text/ClipboardManager "View this page in Java") 
| --- | --- |

```
abstract class ClipboardManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.ClipboardManager](https://developer.android.com/reference/kotlin/android/text/ClipboardManager#) |

| Known Direct Subclasses [ClipboardManager](https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#) |-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [ClipboardManager](https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#) | Interface to the clipboard service, for placing and retrieving text in the global clipboard. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 11.**
|
| Old text-only interface to the clipboard. See [android.content.ClipboardManager](https://developer.android.com/reference/kotlin/android/content/ClipboardManager.html#) for the modern API.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [ClipboardManager](https://developer.android.com/reference/kotlin/android/text/ClipboardManager#ClipboardManager())`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](https://developer.android.com/reference/kotlin/android/text/ClipboardManager#getText())`()` Returns the text on the clipboard. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasText](https://developer.android.com/reference/kotlin/android/text/ClipboardManager#hasText())`()` Returns true if the clipboard contains text; false otherwise. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/android/text/ClipboardManager#setText(kotlin.CharSequence))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the contents of the clipboard to the specified text. |
| --- | --- |

## Public constructors

### ClipboardManager

```
ClipboardManager()
```

## Public methods

### getText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getText(): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

Returns the text on the clipboard. It will eventually be possible to store types other than text too, in which case this will return null if the type cannot be coerced to text. 

### hasText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun hasText(): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns true if the clipboard contains text; false otherwise. 

### setText

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun setText(text: CharSequence!): Unit
```

**Deprecated:** *Deprecated in Java.*

Sets the contents of the clipboard to the specified text.
