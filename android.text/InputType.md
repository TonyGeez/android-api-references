# InputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputType

Kotlin| [Java](InputType.md) 
| --- | --- |

```
interface InputType
```

| [android.text.InputType](InputType.md) |

| Known Direct Subclasses [EditorInfo](../android.view.inputmethod/EditorInfo.md) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [EditorInfo](../android.view.inputmethod/EditorInfo.md) | An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position. | |
| --- | --- | --- | --- | --- | --- | --- |

Bit definitions for an integer defining the basic content type of text held in an [Editable](Editable.md) object. Supported classes may be combined with variations and flags to indicate desired behaviors.

### Examples

A password field with the password visible to the user:
: inputType = TYPE_CLASS_TEXT | TYPE_TEXT_VARIATION_VISIBLE_PASSWORD
| --- | --- |

A multi-line postal address with automatic capitalization:
: inputType = TYPE_CLASS_TEXT | TYPE_TEXT_VARIATION_POSTAL_ADDRESS | TYPE_TEXT_FLAG_MULTI_LINE
| --- | --- | --- |

A time field:
: inputType = TYPE_CLASS_DATETIME | TYPE_DATETIME_VARIATION_TIME
| --- | --- |

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_DATETIME](InputType.md) Class for dates and times. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_NUMBER](InputType.md) Class for numeric text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_PHONE](InputType.md) Class for a phone number. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_TEXT](InputType.md) Class for normal text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATETIME_VARIATION_DATE](InputType.md) Default variation of [TYPE_CLASS_DATETIME](InputType.md): allows entering only a date. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATETIME_VARIATION_NORMAL](InputType.md) Default variation of [TYPE_CLASS_DATETIME](InputType.md): allows entering both a date and time. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATETIME_VARIATION_TIME](InputType.md) Default variation of [TYPE_CLASS_DATETIME](InputType.md): allows entering only a time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MASK_CLASS](InputType.md) Mask of bits that determine the overall class of text being given. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MASK_FLAGS](InputType.md) Mask of bits that provide addition bit flags of options. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MASK_VARIATION](InputType.md) Mask of bits that determine the variation of the base content class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NULL](InputType.md) Special content type for when no explicit type has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_FLAG_DECIMAL](InputType.md) Flag of [TYPE_CLASS_NUMBER](InputType.md): the number is decimal, allowing a decimal point to provide fractional values. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_FLAG_SIGNED](InputType.md) Flag of [TYPE_CLASS_NUMBER](InputType.md): the number is signed, allowing a positive or negative sign at the start. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_VARIATION_NORMAL](InputType.md) Default variation of [TYPE_CLASS_NUMBER](InputType.md): plain normal numeric text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_VARIATION_PASSWORD](InputType.md) Variation of [TYPE_CLASS_NUMBER](InputType.md): entering a numeric password. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_AUTO_COMPLETE](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): the text editor (which means the application) is performing auto-completion of the text being entered based on its own semantics, which it will present to the user as they type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_AUTO_CORRECT](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): the user is entering free-form text that should have auto-correction applied to it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_CAP_CHARACTERS](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): capitalize all characters. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_CAP_SENTENCES](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): capitalize the first character of each sentence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_CAP_WORDS](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): capitalize the first character of every word. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): Let the IME know the text conversion suggestions are required by the application. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_IME_MULTI_LINE](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): the regular text view associated with this should not be multi-line, but when a fullscreen input method is providing text it should use multiple lines if it can. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_MULTI_LINE](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): multiple lines of text can be entered into the field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_NO_SUGGESTIONS](InputType.md) Flag for [TYPE_CLASS_TEXT](InputType.md): the input method does not need to display any dictionary-based candidates. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_EMAIL_ADDRESS](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering an e-mail address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_EMAIL_SUBJECT](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering the subject line of an e-mail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_FILTER](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering text to filter contents of a list etc. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_LONG_MESSAGE](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering the content of a long, possibly formal message such as the body of an e-mail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_NORMAL](InputType.md) Default variation of [TYPE_CLASS_TEXT](InputType.md): plain old normal text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_PASSWORD](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering a password. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_PERSON_NAME](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering the name of a person. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_PHONETIC](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering text for phonetic pronunciation, such as a phonetic name field in contacts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_POSTAL_ADDRESS](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering a postal mailing address. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_SHORT_MESSAGE](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering a short, possibly informal message such as an instant message or a text message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_URI](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering a URI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_VISIBLE_PASSWORD](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering a password, which should be visible to the user. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_WEB_EDIT_TEXT](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering text inside of a web form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering e-mail address inside of a web form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_WEB_PASSWORD](InputType.md) Variation of [TYPE_CLASS_TEXT](InputType.md): entering password inside of a web form. |
| --- | --- |

## Constants

### TYPE_CLASS_DATETIME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CLASS_DATETIME: Int
```

Class for dates and times. It supports the following variations: [TYPE_DATETIME_VARIATION_NORMAL](InputType.md) [TYPE_DATETIME_VARIATION_DATE](InputType.md), and [TYPE_DATETIME_VARIATION_TIME](InputType.md). 

 Value: 4

### TYPE_CLASS_NUMBER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CLASS_NUMBER: Int
```

Class for numeric text. This class supports the following flags: [TYPE_NUMBER_FLAG_SIGNED](InputType.md) and [TYPE_NUMBER_FLAG_DECIMAL](InputType.md). It also supports the following variations: [TYPE_NUMBER_VARIATION_NORMAL](InputType.md) and [TYPE_NUMBER_VARIATION_PASSWORD](InputType.md).

IME authors: If you do not recognize the variation, normal should be assumed. 

 Value: 2

### TYPE_CLASS_PHONE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CLASS_PHONE: Int
```

Class for a phone number. This class currently supports no variations or flags. 

 Value: 3

### TYPE_CLASS_TEXT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CLASS_TEXT: Int
```

Class for normal text. This class supports the following flags (only one of which should be set): [TYPE_TEXT_FLAG_CAP_CHARACTERS](InputType.md), [TYPE_TEXT_FLAG_CAP_WORDS](InputType.md), and. [TYPE_TEXT_FLAG_CAP_SENTENCES](InputType.md). It also supports the following variations: [TYPE_TEXT_VARIATION_NORMAL](InputType.md), and [TYPE_TEXT_VARIATION_URI](InputType.md). If you do not recognize the variation, normal should be assumed. 

 Value: 1

### TYPE_DATETIME_VARIATION_DATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATETIME_VARIATION_DATE: Int
```

Default variation of [TYPE_CLASS_DATETIME](InputType.md): allows entering only a date. 

 Value: 16

### TYPE_DATETIME_VARIATION_NORMAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATETIME_VARIATION_NORMAL: Int
```

Default variation of [TYPE_CLASS_DATETIME](InputType.md): allows entering both a date and time. 

 Value: 0

### TYPE_DATETIME_VARIATION_TIME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATETIME_VARIATION_TIME: Int
```

Default variation of [TYPE_CLASS_DATETIME](InputType.md): allows entering only a time. 

 Value: 32

### TYPE_MASK_CLASS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MASK_CLASS: Int
```

Mask of bits that determine the overall class of text being given. Currently supported classes are: [TYPE_CLASS_TEXT](InputType.md), [TYPE_CLASS_NUMBER](InputType.md), [TYPE_CLASS_PHONE](InputType.md), [TYPE_CLASS_DATETIME](InputType.md).

IME authors: If the class is not one you understand, assume [TYPE_CLASS_TEXT](InputType.md) with NO variation or flags.

<br />

 Value: 15

### TYPE_MASK_FLAGS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MASK_FLAGS: Int
```

Mask of bits that provide addition bit flags of options. 

 Value: 16773120

### TYPE_MASK_VARIATION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MASK_VARIATION: Int
```

Mask of bits that determine the variation of the base content class. 

 Value: 4080

### TYPE_NULL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NULL: Int
```

Special content type for when no explicit type has been specified. This should be interpreted to mean that the target input connection is not rich, it can not process and show things like candidate text nor retrieve the current text, so the input method will need to run in a limited "generate key events" mode, if it supports it. Note that some input methods may not support it, for example a voice-based input method will likely not be able to generate key events even if this flag is set. 

 Value: 0

### TYPE_NUMBER_FLAG_DECIMAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_FLAG_DECIMAL: Int
```

Flag of [TYPE_CLASS_NUMBER](InputType.md): the number is decimal, allowing a decimal point to provide fractional values. 

 Value: 8192

### TYPE_NUMBER_FLAG_SIGNED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_FLAG_SIGNED: Int
```

Flag of [TYPE_CLASS_NUMBER](InputType.md): the number is signed, allowing a positive or negative sign at the start. 

 Value: 4096

### TYPE_NUMBER_VARIATION_NORMAL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_VARIATION_NORMAL: Int
```

Default variation of [TYPE_CLASS_NUMBER](InputType.md): plain normal numeric text. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be dropped when passed through [EditorInfo.makeCompatible(int)](../android.view.inputmethod/EditorInfo.md)). 

 Value: 0

### TYPE_NUMBER_VARIATION_PASSWORD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_VARIATION_PASSWORD: Int
```

Variation of [TYPE_CLASS_NUMBER](InputType.md): entering a numeric password. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be dropped when passed through [EditorInfo.makeCompatible(int)](../android.view.inputmethod/EditorInfo.md)). 

 Value: 16

### TYPE_TEXT_FLAG_AUTO_COMPLETE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_AUTO_COMPLETE: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): the text editor (which means the application) is performing auto-completion of the text being entered based on its own semantics, which it will present to the user as they type. This generally means that the input method should not be showing candidates itself, but can expect the editor to supply its own completions/candidates from [InputMethodSession.displayCompletions()](../android.view.inputmethod/InputMethodSession.md))as a result of the editor calling [InputMethodManager.displayCompletions()](../android.view.inputmethod/InputMethodManager.md)). Note the contrast with [TYPE_TEXT_FLAG_AUTO_CORRECT](InputType.md) and [TYPE_TEXT_FLAG_NO_SUGGESTIONS](InputType.md):`TYPE_TEXT_FLAG_AUTO_COMPLETE`means the editor should show an interface for displaying suggestions, but instead of supplying its own it will rely on the Editor to pass completions/corrections. 

 Value: 65536

### TYPE_TEXT_FLAG_AUTO_CORRECT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_AUTO_CORRECT: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): the user is entering free-form text that should have auto-correction applied to it. Without this flag, the IME will not try to correct typos. You should always set this flag unless you really expect users to type non-words in this field, for example to choose a name for a character in a game. Contrast this with [TYPE_TEXT_FLAG_AUTO_COMPLETE](InputType.md) and [TYPE_TEXT_FLAG_NO_SUGGESTIONS](InputType.md):`TYPE_TEXT_FLAG_AUTO_CORRECT`means that the IME will try to auto-correct typos as the user is typing, but does not define whether the IME offers an interface to show suggestions. 

 Value: 32768

### TYPE_TEXT_FLAG_CAP_CHARACTERS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_CAP_CHARACTERS: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): capitalize all characters. Overrides [TYPE_TEXT_FLAG_CAP_WORDS](InputType.md) and [TYPE_TEXT_FLAG_CAP_SENTENCES](InputType.md). This value is explicitly defined to be the same as [TextUtils.CAP_MODE_CHARACTERS](TextUtils.md). Of course, this only affects languages where there are upper-case and lower-case letters. 

 Value: 4096

### TYPE_TEXT_FLAG_CAP_SENTENCES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_CAP_SENTENCES: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): capitalize the first character of each sentence. This value is explicitly defined to be the same as [TextUtils.CAP_MODE_SENTENCES](TextUtils.md). For example in English it means to capitalize after a period and a space (note that other languages may have different characters for period, or not use spaces, or use different grammatical rules). Of course, this only affects languages where there are upper-case and lower-case letters. 

 Value: 16384

### TYPE_TEXT_FLAG_CAP_WORDS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_CAP_WORDS: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): capitalize the first character of every word. Overrides [TYPE_TEXT_FLAG_CAP_SENTENCES](InputType.md). This value is explicitly defined to be the same as [TextUtils.CAP_MODE_WORDS](TextUtils.md). Of course, this only affects languages where there are upper-case and lower-case letters. 

 Value: 8192

### TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): Let the IME know the text conversion suggestions are required by the application. Text conversion suggestion is for the transliteration languages which has pronunciation characters and target characters. When the user is typing the pronunciation charactes, the IME could provide the possible target characters to the user. When this flag is set, the IME should insert the text conversion suggestions through [Builder.setTextConversionSuggestions(List)](../android/view/inputmethod/TextAttribute.Builder.md))and the [TextAttribute](../android.view.inputmethod/TextAttribute.md) with initialized with the text conversion suggestions is provided by the IME to the application. To receive the additional information, the application needs to implement [InputConnection.setComposingText(CharSequence, int, TextAttribute)](../android.view.inputmethod/InputConnection.md)), [InputConnection.setComposingRegion(int, int, TextAttribute)](../android.view.inputmethod/InputConnection.md)), and [InputConnection.commitText(CharSequence, int, TextAttribute)](../android.view.inputmethod/InputConnection.md)). 

 Value: 1048576

### TYPE_TEXT_FLAG_IME_MULTI_LINE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_IME_MULTI_LINE: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): the regular text view associated with this should not be multi-line, but when a fullscreen input method is providing text it should use multiple lines if it can. 

 Value: 262144

### TYPE_TEXT_FLAG_MULTI_LINE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_MULTI_LINE: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): multiple lines of text can be entered into the field. If this flag is not set, the text field will be constrained to a single line. The IME may also choose not to display an enter key when this flag is not set, as there should be no need to create new lines. 

 Value: 131072

### TYPE_TEXT_FLAG_NO_SUGGESTIONS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_NO_SUGGESTIONS: Int
```

Flag for [TYPE_CLASS_TEXT](InputType.md): the input method does not need to display any dictionary-based candidates. This is useful for text views that do not contain words from the language and do not benefit from any dictionary-based completions or corrections. It overrides the [TYPE_TEXT_FLAG_AUTO_CORRECT](InputType.md) value when set. Please avoid using this unless you are certain this is what you want. Many input methods need suggestions to work well, for example the ones based on gesture typing. Consider clearing [TYPE_TEXT_FLAG_AUTO_CORRECT](InputType.md) instead if you just do not want the IME to correct typos. Note the contrast with [TYPE_TEXT_FLAG_AUTO_CORRECT](InputType.md) and [TYPE_TEXT_FLAG_AUTO_COMPLETE](InputType.md):`TYPE_TEXT_FLAG_NO_SUGGESTIONS`means the IME does not need to show an interface to display suggestions. Most IMEs will also take this to mean they do not need to try to auto-correct what the user is typing. 

 Value: 524288

### TYPE_TEXT_VARIATION_EMAIL_ADDRESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_EMAIL_ADDRESS: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering an e-mail address. 

 Value: 32

### TYPE_TEXT_VARIATION_EMAIL_SUBJECT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_EMAIL_SUBJECT: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering the subject line of an e-mail. 

 Value: 48

### TYPE_TEXT_VARIATION_FILTER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_FILTER: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering text to filter contents of a list etc. 

 Value: 176

### TYPE_TEXT_VARIATION_LONG_MESSAGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_LONG_MESSAGE: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering the content of a long, possibly formal message such as the body of an e-mail. 

 Value: 80

### TYPE_TEXT_VARIATION_NORMAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_NORMAL: Int
```

Default variation of [TYPE_CLASS_TEXT](InputType.md): plain old normal text. 

 Value: 0

### TYPE_TEXT_VARIATION_PASSWORD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_PASSWORD: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering a password. 

 Value: 128

### TYPE_TEXT_VARIATION_PERSON_NAME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_PERSON_NAME: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering the name of a person. 

 Value: 96

### TYPE_TEXT_VARIATION_PHONETIC

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_PHONETIC: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering text for phonetic pronunciation, such as a phonetic name field in contacts. This is mostly useful for languages where one spelling may have several phonetic readings, like Japanese. 

 Value: 192

### TYPE_TEXT_VARIATION_POSTAL_ADDRESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_POSTAL_ADDRESS: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering a postal mailing address. 

 Value: 112

### TYPE_TEXT_VARIATION_SHORT_MESSAGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_SHORT_MESSAGE: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering a short, possibly informal message such as an instant message or a text message. 

 Value: 64

### TYPE_TEXT_VARIATION_URI

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_URI: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering a URI. 

 Value: 16

### TYPE_TEXT_VARIATION_VISIBLE_PASSWORD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_VISIBLE_PASSWORD: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering a password, which should be visible to the user. 

 Value: 144

### TYPE_TEXT_VARIATION_WEB_EDIT_TEXT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_WEB_EDIT_TEXT: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering text inside of a web form. 

 Value: 160

### TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering e-mail address inside of a web form. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be seen as [TYPE_TEXT_VARIATION_EMAIL_ADDRESS](InputType.md) when passed through [EditorInfo.makeCompatible(int)](../android.view.inputmethod/EditorInfo.md)). 

 Value: 208

### TYPE_TEXT_VARIATION_WEB_PASSWORD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_WEB_PASSWORD: Int
```

Variation of [TYPE_CLASS_TEXT](InputType.md): entering password inside of a web form. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](../android/os/Build.VERSION_CODES.md). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be seen as [TYPE_TEXT_VARIATION_PASSWORD](InputType.md) when passed through [EditorInfo.makeCompatible(int)](../android.view.inputmethod/EditorInfo.md)). 

 Value: 224
