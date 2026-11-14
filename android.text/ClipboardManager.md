# ClipboardManager

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# ClipboardManager

Kotlin| [Java](ClipboardManager.md) 
| --- | --- |

```
abstract class ClipboardManager
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.ClipboardManager](ClipboardManager.md) |

| Known Direct Subclasses [ClipboardManager](../android.content/ClipboardManager.md) |-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------| | [ClipboardManager](../android.content/ClipboardManager.md) | Interface to the clipboard service, for placing and retrieving text in the global clipboard. | |
| --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 11.**
|
| Old text-only interface to the clipboard. See [android.content.ClipboardManager](../android.content/ClipboardManager.md) for the modern API.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------|---|
| [ClipboardManager](ClipboardManager.md))`()` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [getText](ClipboardManager.md))`()` Returns the text on the clipboard. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [hasText](ClipboardManager.md))`()` Returns true if the clipboard contains text; false otherwise. |
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](ClipboardManager.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`)` Sets the contents of the clipboard to the specified text. |
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
