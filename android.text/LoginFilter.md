# LoginFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoginFilter

Kotlin| [Java](https://developer.android.com/reference/android/text/LoginFilter "View this page in Java") 

```
abstract class LoginFilter : InputFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.LoginFilter](https://developer.android.com/reference/kotlin/android/text/LoginFilter#) |

| Known Direct Subclasses [LoginFilter.PasswordFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.PasswordFilterGMail), [LoginFilter.UsernameFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGMail), [LoginFilter.UsernameFilterGeneric](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGeneric) |------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [LoginFilter.PasswordFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.PasswordFilterGMail) | This filter is compatible with GMail passwords which restricts characters to the Latin-1 (ISO8859-1) char set. | | [LoginFilter.UsernameFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGMail) | This filter rejects characters in the user name that are not compatible with GMail account creation. | | [LoginFilter.UsernameFilterGeneric](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGeneric) | This filter rejects characters in the user name that are not compatible with Google login. | |

| **This class was deprecated in API level 30.**
|
| Password requirements should not be hardcoded in clients. This class also does not handle non-BMP characters.

Abstract class for filtering login-related text (user names and passwords)

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PasswordFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.PasswordFilterGMail) This filter is compatible with GMail passwords which restricts characters to the Latin-1 (ISO8859-1) char set. |
| open | [UsernameFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGMail) This filter rejects characters in the user name that are not compatible with GMail account creation. |
| open | [UsernameFilterGeneric](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGeneric) This filter rejects characters in the user name that are not compatible with Google login. |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [filter](https://developer.android.com/reference/kotlin/android/text/LoginFilter#filter(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.text.Spanned,%20kotlin.Int,%20kotlin.Int))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)!`, `dstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAllowed](https://developer.android.com/reference/kotlin/android/text/LoginFilter#isAllowed(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns whether or not we allow character c. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvalidCharacter](https://developer.android.com/reference/kotlin/android/text/LoginFilter#onInvalidCharacter(kotlin.Char))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Called whenever we encounter an invalid character. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](https://developer.android.com/reference/kotlin/android/text/LoginFilter#onStart())`()` Called when we start processing filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](https://developer.android.com/reference/kotlin/android/text/LoginFilter#onStop())`()` Called when we're done processing filter |

## Public methods

### filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun filter(
    source: CharSequence!, 
    start: Int, 
    end: Int, 
    dest: Spanned!, 
    dstart: Int, 
    dend: Int
): CharSequence!
```

**Deprecated:** *Deprecated in Java.*

This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. Returns the CharSequence that we want placed there instead, including an empty string if appropriate, or`null`to accept the original replacement. Be careful to not to reject 0-length replacements, as this is what happens when you delete text. 

### isAllowed

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun isAllowed(c: Char): Boolean
```

**Deprecated:** *Deprecated in Java.*

Returns whether or not we allow character c. Subclasses must override this method. 

### onInvalidCharacter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onInvalidCharacter(c: Char): Unit
```

**Deprecated:** *Deprecated in Java.*

Called whenever we encounter an invalid character.

| Parameters ||
|-----|----------------------------------------------------------------------------------------------------|
| `c` | [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html):the invalid character |

### onStart

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStart(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when we start processing filter. 

### onStop

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun onStop(): Unit
```

**Deprecated:** *Deprecated in Java.*

Called when we're done processing filter
