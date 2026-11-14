# android.text.method

# android.text.method

Kotlin| [Java](https://developer.android.com/reference/android/text/method/package-summary "View this page in Java")
| --- | --- |

## Interfaces

| [KeyListener](https://developer.android.com/reference/kotlin/android/text/method/KeyListener) | Interface for converting text key events into edit operations on an Editable class. |
| --- | --- |
| [MovementMethod](https://developer.android.com/reference/kotlin/android/text/method/MovementMethod) | Provides cursor positioning, scrolling and text selection functionality in a [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#). |
| [TransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/TransformationMethod) | TextView uses TransformationMethods to do things like replacing the characters of passwords with dots, or keeping the newline characters from causing line breaks in single-line text fields. |

## Classes

| [ArrowKeyMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ArrowKeyMovementMethod) | A movement method that provides cursor movement and selection. |
| --- | --- |
| [BaseKeyListener](https://developer.android.com/reference/kotlin/android/text/method/BaseKeyListener) | Abstract base class for key listeners. |
| [BaseMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/BaseMovementMethod) | Base classes for movement methods. |
| [CharacterPickerDialog](https://developer.android.com/reference/kotlin/android/text/method/CharacterPickerDialog) | Dialog for choosing accented characters related to a base character. |
| --- | --- |
| [DateKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateKeyListener) | For entering dates in a text field. |
| [DateTimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DateTimeKeyListener) | For entering dates and times in the same text field. |
| [DialerKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DialerKeyListener) | For dialing-only text entry |
| --- | --- |
| [DigitsKeyListener](https://developer.android.com/reference/kotlin/android/text/method/DigitsKeyListener) | For digits-only text entry |
| [HideReturnsTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/HideReturnsTransformationMethod) | This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF). |
| [LinkMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/LinkMovementMethod) | A movement method that traverses links in the text buffer and scrolls if necessary. |
| --- | --- |
| [MetaKeyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MetaKeyKeyListener) | This base class encapsulates the behavior for tracking the state of meta keys such as SHIFT, ALT and SYM as well as the pseudo-meta state of selecting text. |
| [MultiTapKeyListener](https://developer.android.com/reference/kotlin/android/text/method/MultiTapKeyListener) | This is the standard key listener for alphabetic input on 12-key keyboards. |
| [NumberKeyListener](https://developer.android.com/reference/kotlin/android/text/method/NumberKeyListener) | For numeric text entry |
| --- | --- |
| [PasswordTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/PasswordTransformationMethod) | <br /> |
| [QwertyKeyListener](https://developer.android.com/reference/kotlin/android/text/method/QwertyKeyListener) | This is the standard key listener for alphabetic input on qwerty keyboards. |
| [ReplacementTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod) | This transformation method causes the characters in the [getOriginal](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getOriginal())array to be replaced by the corresponding characters in the [getReplacement](https://developer.android.com/reference/kotlin/android/text/method/ReplacementTransformationMethod#getReplacement())array. |
| --- | --- |
| [ScrollingMovementMethod](https://developer.android.com/reference/kotlin/android/text/method/ScrollingMovementMethod) | A movement method that interprets movement keys by scrolling the text buffer. |
| [SingleLineTransformationMethod](https://developer.android.com/reference/kotlin/android/text/method/SingleLineTransformationMethod) | This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance. |
| [TextKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TextKeyListener) | This is the key listener for typing normal text. |
| --- | --- |
| [TimeKeyListener](https://developer.android.com/reference/kotlin/android/text/method/TimeKeyListener) | For entering times in a text field. |
| [Touch](https://developer.android.com/reference/kotlin/android/text/method/Touch) | <br /> |
