# InputFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputFilter

Kotlin| [Java](../android/text/InputFilter.md) 
| --- | --- |

```
interface InputFilter
```

| [android.text.InputFilter](../android/text/InputFilter.md) |

| Known Direct Subclasses [InputFilter.AllCaps](../android/text/InputFilter.AllCaps.md), [InputFilter.LengthFilter](../android/text/InputFilter.LengthFilter.md), [LoginFilter](../android/text/LoginFilter.md), [NumberKeyListener](../android/text/method/NumberKeyListener.md) |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [InputFilter.AllCaps](../android/text/InputFilter.AllCaps.md) | This filter will capitalize all the lowercase and titlecase letters that are added through edits. | | [InputFilter.LengthFilter](../android/text/InputFilter.LengthFilter.md) | This filter will constrain edits not to make the length of the text greater than the specified length. | | [LoginFilter](../android/text/LoginFilter.md) | Abstract class for filtering login-related text (user names and passwords) | | [NumberKeyListener](../android/text/method/NumberKeyListener.md) | For numeric text entry | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DateKeyListener](../android/text/method/DateKeyListener.md), [DateTimeKeyListener](../android/text/method/DateTimeKeyListener.md), [DialerKeyListener](../android/text/method/DialerKeyListener.md), [DigitsKeyListener](../android/text/method/DigitsKeyListener.md), [LoginFilter.PasswordFilterGMail](../android/text/LoginFilter.PasswordFilterGMail.md), [LoginFilter.UsernameFilterGMail](../android/text/LoginFilter.UsernameFilterGMail.md), [LoginFilter.UsernameFilterGeneric](../android/text/LoginFilter.UsernameFilterGeneric.md), [TimeKeyListener](../android/text/method/TimeKeyListener.md) |------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [DateKeyListener](../android/text/method/DateKeyListener.md) | For entering dates in a text field. | | [DateTimeKeyListener](../android/text/method/DateTimeKeyListener.md) | For entering dates and times in the same text field. | | [DialerKeyListener](../android/text/method/DialerKeyListener.md) | For dialing-only text entry | | [DigitsKeyListener](../android/text/method/DigitsKeyListener.md) | For digits-only text entry | | [LoginFilter.PasswordFilterGMail](../android/text/LoginFilter.PasswordFilterGMail.md) | This filter is compatible with GMail passwords which restricts characters to the Latin-1 (ISO8859-1) char set. | | [LoginFilter.UsernameFilterGMail](../android/text/LoginFilter.UsernameFilterGMail.md) | This filter rejects characters in the user name that are not compatible with GMail account creation. | | [LoginFilter.UsernameFilterGeneric](../android/text/LoginFilter.UsernameFilterGeneric.md) | This filter rejects characters in the user name that are not compatible with Google login. | | [TimeKeyListener](../android/text/method/TimeKeyListener.md) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

InputFilters can be attached to [Editable](../android/text/Editable.md) s to constrain the changes that can be made to them.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AllCaps](../android/text/InputFilter.AllCaps.md) This filter will capitalize all the lowercase and titlecase letters that are added through edits. |
| open | [LengthFilter](../android/text/InputFilter.LengthFilter.md) This filter will constrain edits not to make the length of the text greater than the specified length. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [filter](../android/text/InputFilter.md))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Spanned](../android/text/Spanned.md)!`, `dstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. |

## Public methods

### filter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun filter(
    source: CharSequence!, 
    start: Int, 
    end: Int, 
    dest: Spanned!, 
    dstart: Int, 
    dend: Int
): CharSequence!
```

This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. Return the CharSequence that you would like to have placed there instead, including an empty string if appropriate, or`null`to accept the original replacement. Be careful to not to reject 0-length replacements, as this is what happens when you delete text. Also beware that you should not attempt to make any changes to`dest`from this method; you may only examine it for context. Note: If source is an instance of [Spanned](../android/text/Spanned.md) or [Spannable](../android/text/Spannable.md), the span objects in the source should be copied into the filtered result (i.e. the non-null return value). [TextUtils.copySpansFrom](../android/text/TextUtils.md))can be used for convenience if the span boundary indices would be remaining identical relative to the source.
