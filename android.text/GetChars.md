# GetChars

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GetChars

Kotlin| [Java](https://developer.android.com/reference/android/text/GetChars "View this page in Java") 
| --- | --- |

```
interface GetChars : CharSequence
```

| [android.text.GetChars](https://developer.android.com/reference/kotlin/android/text/GetChars#) |

| Known Direct Subclasses [AlteredCharSequence](https://developer.android.com/reference/kotlin/android/text/AlteredCharSequence), [Editable](https://developer.android.com/reference/kotlin/android/text/Editable), [SpannableString](https://developer.android.com/reference/kotlin/android/text/SpannableString), [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder), [SpannedString](https://developer.android.com/reference/kotlin/android/text/SpannedString) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [AlteredCharSequence](https://developer.android.com/reference/kotlin/android/text/AlteredCharSequence) | An AlteredCharSequence is a CharSequence that is largely mirrored from another CharSequence, except that a specified range of characters are mirrored from a different char array instead. | | [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) | This is the interface for text whose content and markup can be changed (as opposed to immutable text like Strings). | | [SpannableString](https://developer.android.com/reference/kotlin/android/text/SpannableString) | This is the class for text whose content is immutable but to which markup objects can be attached and detached. | | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) | This is the class for text whose content and markup can both be changed. | | [SpannedString](https://developer.android.com/reference/kotlin/android/text/SpannedString) | This is the class for text whose content and markup are immutable. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) |--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------| | [SpannableStringBuilder](https://developer.android.com/reference/kotlin/android/text/SpannableStringBuilder) | This is the class for text whose content and markup can both be changed. | |
| --- | --- | --- | --- | --- | --- | --- |

Please implement this interface if your CharSequence has a getChars() method like the one in String that is faster than calling charAt() multiple times.

## Summary

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getChars](https://developer.android.com/reference/kotlin/android/text/GetChars#getChars(kotlin.Int,%20kotlin.Int,%20kotlin.CharArray,%20kotlin.Int))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [CharArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-array/index.html)!`, `destoff:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Exactly like String. |

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
