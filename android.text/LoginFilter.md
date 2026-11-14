# LoginFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# LoginFilter

Kotlin| [Java](../android/text/LoginFilter.md) 
| --- | --- |

```
abstract class LoginFilter : InputFilter
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.LoginFilter](../android/text/LoginFilter.md) |

| Known Direct Subclasses [LoginFilter.PasswordFilterGMail](../android/text/LoginFilter.PasswordFilterGMail.md), [LoginFilter.UsernameFilterGMail](../android/text/LoginFilter.UsernameFilterGMail.md), [LoginFilter.UsernameFilterGeneric](../android/text/LoginFilter.UsernameFilterGeneric.md) |------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [LoginFilter.PasswordFilterGMail](../android/text/LoginFilter.PasswordFilterGMail.md) | This filter is compatible with GMail passwords which restricts characters to the Latin-1 (ISO8859-1) char set. | | [LoginFilter.UsernameFilterGMail](../android/text/LoginFilter.UsernameFilterGMail.md) | This filter rejects characters in the user name that are not compatible with GMail account creation. | | [LoginFilter.UsernameFilterGeneric](../android/text/LoginFilter.UsernameFilterGeneric.md) | This filter rejects characters in the user name that are not compatible with Google login. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| **This class was deprecated in API level 30.**
|
| Password requirements should not be hardcoded in clients. This class also does not handle non-BMP characters.

Abstract class for filtering login-related text (user names and passwords)

## Summary

| Nested classes ||
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PasswordFilterGMail](../android/text/LoginFilter.PasswordFilterGMail.md) This filter is compatible with GMail passwords which restricts characters to the Latin-1 (ISO8859-1) char set. |
| open | [UsernameFilterGMail](../android/text/LoginFilter.UsernameFilterGMail.md) This filter rejects characters in the user name that are not compatible with GMail account creation. |
| open | [UsernameFilterGeneric](../android/text/LoginFilter.UsernameFilterGeneric.md) This filter rejects characters in the user name that are not compatible with Google login. |
| --- | --- |

| Public methods ||
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [filter](../android/text/LoginFilter.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Spanned](../android/text/Spanned.md)!`, `dstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. |
| abstract [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isAllowed](../android/text/LoginFilter.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Returns whether or not we allow character c. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onInvalidCharacter](../android/text/LoginFilter.md))`(`c:` ` [Char](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char/index.html)`)` Called whenever we encounter an invalid character. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStart](../android/text/LoginFilter.md))`()` Called when we start processing filter. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [onStop](../android/text/LoginFilter.md))`()` Called when we're done processing filter |

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
