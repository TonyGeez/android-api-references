# android.text.method

# android.text.method

Kotlin| [Java](../android/text/method/_package.md)
| --- | --- |

## Interfaces

| [KeyListener](../android/text/method/KeyListener.md) | Interface for converting text key events into edit operations on an Editable class. |
| --- | --- |
| [MovementMethod](../android/text/method/MovementMethod.md) | Provides cursor positioning, scrolling and text selection functionality in a [TextView](../android/widget/TextView.md). |
| [TransformationMethod](../android/text/method/TransformationMethod.md) | TextView uses TransformationMethods to do things like replacing the characters of passwords with dots, or keeping the newline characters from causing line breaks in single-line text fields. |

## Classes

| [ArrowKeyMovementMethod](../android/text/method/ArrowKeyMovementMethod.md) | A movement method that provides cursor movement and selection. |
| --- | --- |
| [BaseKeyListener](../android/text/method/BaseKeyListener.md) | Abstract base class for key listeners. |
| [BaseMovementMethod](../android/text/method/BaseMovementMethod.md) | Base classes for movement methods. |
| [CharacterPickerDialog](../android/text/method/CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. |
| --- | --- |
| [DateKeyListener](../android/text/method/DateKeyListener.md) | For entering dates in a text field. |
| [DateTimeKeyListener](../android/text/method/DateTimeKeyListener.md) | For entering dates and times in the same text field. |
| [DialerKeyListener](../android/text/method/DialerKeyListener.md) | For dialing-only text entry |
| --- | --- |
| [DigitsKeyListener](../android/text/method/DigitsKeyListener.md) | For digits-only text entry |
| [HideReturnsTransformationMethod](../android/text/method/HideReturnsTransformationMethod.md) | This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF). |
| [LinkMovementMethod](../android/text/method/LinkMovementMethod.md) | A movement method that traverses links in the text buffer and scrolls if necessary. |
| --- | --- |
| [MetaKeyKeyListener](../android/text/method/MetaKeyKeyListener.md) | This base class encapsulates the behavior for tracking the state of meta keys such as SHIFT, ALT and SYM as well as the pseudo-meta state of selecting text. |
| [MultiTapKeyListener](../android/text/method/MultiTapKeyListener.md) | This is the standard key listener for alphabetic input on 12-key keyboards. |
| [NumberKeyListener](../android/text/method/NumberKeyListener.md) | For numeric text entry |
| --- | --- |
| [PasswordTransformationMethod](../android/text/method/PasswordTransformationMethod.md) | <br /> |
| [QwertyKeyListener](../android/text/method/QwertyKeyListener.md) | This is the standard key listener for alphabetic input on qwerty keyboards. |
| [ReplacementTransformationMethod](../android/text/method/ReplacementTransformationMethod.md) | This transformation method causes the characters in the [getOriginal](../android/text/method/ReplacementTransformationMethod.md))array to be replaced by the corresponding characters in the [getReplacement](../android/text/method/ReplacementTransformationMethod.md))array. |
| --- | --- |
| [ScrollingMovementMethod](../android/text/method/ScrollingMovementMethod.md) | A movement method that interprets movement keys by scrolling the text buffer. |
| [SingleLineTransformationMethod](../android/text/method/SingleLineTransformationMethod.md) | This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance. |
| [TextKeyListener](../android/text/method/TextKeyListener.md) | This is the key listener for typing normal text. |
| --- | --- |
| [TimeKeyListener](../android/text/method/TimeKeyListener.md) | For entering times in a text field. |
| [Touch](../android/text/method/Touch.md) | <br /> |
