# android.text.method

# android.text.method

Kotlin| [Java](_package.md)
| --- | --- |

## Interfaces

| [KeyListener](KeyListener.md) | Interface for converting text key events into edit operations on an Editable class. |
| --- | --- |
| [MovementMethod](MovementMethod.md) | Provides cursor positioning, scrolling and text selection functionality in a [TextView](../android.widget/TextView.md). |
| [TransformationMethod](TransformationMethod.md) | TextView uses TransformationMethods to do things like replacing the characters of passwords with dots, or keeping the newline characters from causing line breaks in single-line text fields. |

## Classes

| [ArrowKeyMovementMethod](ArrowKeyMovementMethod.md) | A movement method that provides cursor movement and selection. |
| --- | --- |
| [BaseKeyListener](BaseKeyListener.md) | Abstract base class for key listeners. |
| [BaseMovementMethod](BaseMovementMethod.md) | Base classes for movement methods. |
| [CharacterPickerDialog](CharacterPickerDialog.md) | Dialog for choosing accented characters related to a base character. |
| --- | --- |
| [DateKeyListener](DateKeyListener.md) | For entering dates in a text field. |
| [DateTimeKeyListener](DateTimeKeyListener.md) | For entering dates and times in the same text field. |
| [DialerKeyListener](DialerKeyListener.md) | For dialing-only text entry |
| --- | --- |
| [DigitsKeyListener](DigitsKeyListener.md) | For digits-only text entry |
| [HideReturnsTransformationMethod](HideReturnsTransformationMethod.md) | This transformation method causes any carriage return characters (\\r) to be hidden by displaying them as zero-width non-breaking space characters (\\uFEFF). |
| [LinkMovementMethod](LinkMovementMethod.md) | A movement method that traverses links in the text buffer and scrolls if necessary. |
| --- | --- |
| [MetaKeyKeyListener](MetaKeyKeyListener.md) | This base class encapsulates the behavior for tracking the state of meta keys such as SHIFT, ALT and SYM as well as the pseudo-meta state of selecting text. |
| [MultiTapKeyListener](MultiTapKeyListener.md) | This is the standard key listener for alphabetic input on 12-key keyboards. |
| [NumberKeyListener](NumberKeyListener.md) | For numeric text entry |
| --- | --- |
| [PasswordTransformationMethod](PasswordTransformationMethod.md) | <br /> |
| [QwertyKeyListener](QwertyKeyListener.md) | This is the standard key listener for alphabetic input on qwerty keyboards. |
| [ReplacementTransformationMethod](ReplacementTransformationMethod.md) | This transformation method causes the characters in the [getOriginal](ReplacementTransformationMethod.md))array to be replaced by the corresponding characters in the [getReplacement](ReplacementTransformationMethod.md))array. |
| --- | --- |
| [ScrollingMovementMethod](ScrollingMovementMethod.md) | A movement method that interprets movement keys by scrolling the text buffer. |
| [SingleLineTransformationMethod](SingleLineTransformationMethod.md) | This transformation method causes any newline characters (\\n) to be displayed as spaces instead of causing line breaks, and causes carriage return characters (\\r) to have no appearance. |
| [TextKeyListener](TextKeyListener.md) | This is the key listener for typing normal text. |
| --- | --- |
| [TimeKeyListener](TimeKeyListener.md) | For entering times in a text field. |
| [Touch](Touch.md) | <br /> |
