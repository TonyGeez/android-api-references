# InputFilter

Added in [API level 1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputFilter

Kotlin| [Java](https://developer.android.com/reference/android/text/InputFilter "View this page in Java") 
| --- | --- |

```
interface InputFilter
```

| [android.text.InputFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter#) |

| Known Direct Subclasses [InputFilter.AllCaps](https://developer.android.com/reference/kotlin/android/text/InputFilter.AllCaps), [InputFilter.LengthFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter.LengthFilter), [LoginFilter](https://developer.android.com/reference/kotlin/android/text/LoginFilter), [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener) |------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------| | [InputFilter.AllCaps](https://developer.android.com/reference/kotlin/android/text/InputFilter.AllCaps) | This filter will capitalize all the lowercase and titlecase letters that are added through edits. | | [InputFilter.LengthFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter.LengthFilter) | This filter will constrain edits not to make the length of the text greater than the specified length. | | [LoginFilter](https://developer.android.com/reference/kotlin/android/text/LoginFilter) | Abstract class for filtering login-related text (user names and passwords) | | [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener) | For numeric text entry | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

| Known Indirect Subclasses [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener), [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener), [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener), [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener), [LoginFilter.PasswordFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.PasswordFilterGMail), [LoginFilter.UsernameFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGMail), [LoginFilter.UsernameFilterGeneric](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGeneric), [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) |------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------| | [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener) | For entering dates in a text field. | | [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener) | For entering dates and times in the same text field. | | [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener) | For dialing-only text entry | | [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener) | For digits-only text entry | | [LoginFilter.PasswordFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.PasswordFilterGMail) | This filter is compatible with GMail passwords which restricts characters to the Latin-1 (ISO8859-1) char set. | | [LoginFilter.UsernameFilterGMail](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGMail) | This filter rejects characters in the user name that are not compatible with GMail account creation. | | [LoginFilter.UsernameFilterGeneric](https://developer.android.com/reference/kotlin/android/text/LoginFilter.UsernameFilterGeneric) | This filter rejects characters in the user name that are not compatible with Google login. | | [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) | For entering times in a text field. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

InputFilters can be attached to [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) s to constrain the changes that can be made to them.

## Summary

| Nested classes ||
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [AllCaps](https://developer.android.com/reference/kotlin/android/text/InputFilter.AllCaps) This filter will capitalize all the lowercase and titlecase letters that are added through edits. |
| open | [LengthFilter](https://developer.android.com/reference/kotlin/android/text/InputFilter.LengthFilter) This filter will constrain edits not to make the length of the text greater than the specified length. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | [filter](https://developer.android.com/reference/kotlin/android/text/InputFilter#filter(kotlin.CharSequence,%20kotlin.Int,%20kotlin.Int,%20android.text.Spanned,%20kotlin.Int,%20kotlin.Int))`(`source:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)!`, `start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dest:` ` [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned)!`, `dstart:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `dend:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. |

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

This method is called when the buffer is going to replace the range`dstart ... dend`of`dest`with the new text from the range`start ... end`of`source`. Return the CharSequence that you would like to have placed there instead, including an empty string if appropriate, or`null`to accept the original replacement. Be careful to not to reject 0-length replacements, as this is what happens when you delete text. Also beware that you should not attempt to make any changes to`dest`from this method; you may only examine it for context. Note: If source is an instance of [Spanned](https://developer.android.com/reference/kotlin/android/text/Spanned) or [Spannable](https://developer.android.com/reference/kotlin/android/text/Spannable), the span objects in the source should be copied into the filtered result (i.e. the non-null return value). [TextUtils.copySpansFrom](https://developer.android.com/reference/kotlin/android/text/TextUtils#copySpansFrom(android.text.Spanned,%20kotlin.Int,%20kotlin.Int,%20java.lang.Class,%20android.text.Spannable,%20kotlin.Int))can be used for convenience if the span boundary indices would be remaining identical relative to the source.
