# GetChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetChars

Kotlin| [Java](GetChars.md) 
| --- | --- |

```
interface GetChars : CharSequence
```

| [android.text.GetChars](GetChars.md) |

| Known Direct Subclasses [AlteredCharSequence](AlteredCharSequence.md), [Editable](Editable.md), [SpannableString](SpannableString.md), [SpannableStringBuilder](SpannableStringBuilder.md), [SpannedString](SpannedString.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AlteredCharSequence](AlteredCharSequence.md) | An AlteredCharSequence is a CharSequence that is largely mirrored from another CharSequence, except that a specified range of characters are mirrored from a different char array instead. | | [Editable](Editable.md) | This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). | | [SpannableString](SpannableString.md) | This is the class for text whose content is immutable but to which markup objects can be attached and detached. | | [SpannableStringBuilder](SpannableStringBuilder.md) | This is the class for text whose content and markup can both be changed. | | [SpannedString](SpannedString.md) | This is the class for text whose content and markup are immutable. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SpannableStringBuilder](SpannableStringBuilder.md) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [SpannableStringBuilder](SpannableStringBuilder.md) | This is the class for text whose content and markup can both be changed. | |
| --- | --- | --- | --- | --- | --- | --- |

Please implement this interface if your CharSequence has a getChars() method like the one in String that is faster than calling charAt() multiple times.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getChars](GetChars.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `destoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Exactly like String. |

## Public methods

### getChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun getChars(
    start: Int, 
    end: Int, 
    dest: CharArray!, 
    destoff: Int
): Unit
```

Exactly like String.getChars(): copy chars`start`through`end - 1`from this CharSequence into`dest`beginning at offset`destoff`.
