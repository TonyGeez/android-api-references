# InputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InputType

Kotlin| [Java](https://developer.android.com/reference/android/text/InputType "View this page in Java") 

```
interface InputType
```

| [android.text.InputType](https://developer.android.com/reference/kotlin/android/text/InputType#) |

| Known Direct Subclasses [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#) |--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#) | An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position. | |

Bit definitions for an integer defining the basic content type of text held in an [Editable](https://developer.android.com/reference/kotlin/android/text/Editable) object. Supported classes may be combined with variations and flags to indicate desired behaviors.

### Examples

A password field with the password visible to the user:
: inputType = TYPE_CLASS_TEXT | TYPE_TEXT_VARIATION_VISIBLE_PASSWORD

A multi-line postal address with automatic capitalization:
: inputType = TYPE_CLASS_TEXT | TYPE_TEXT_VARIATION_POSTAL_ADDRESS | TYPE_TEXT_FLAG_MULTI_LINE

A time field:
: inputType = TYPE_CLASS_DATETIME | TYPE_DATETIME_VARIATION_TIME

<br />

## Summary

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int) Class for dates and times. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int) Class for numeric text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_PHONE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_PHONE:kotlin.Int) Class for a phone number. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int) Class for normal text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATETIME_VARIATION_DATE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_DATETIME_VARIATION_DATE:kotlin.Int) Default variation of [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int): allows entering only a date. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATETIME_VARIATION_NORMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_DATETIME_VARIATION_NORMAL:kotlin.Int) Default variation of [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int): allows entering both a date and time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_DATETIME_VARIATION_TIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_DATETIME_VARIATION_TIME:kotlin.Int) Default variation of [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int): allows entering only a time. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MASK_CLASS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_MASK_CLASS:kotlin.Int) Mask of bits that determine the overall class of text being given. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MASK_FLAGS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_MASK_FLAGS:kotlin.Int) Mask of bits that provide addition bit flags of options. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_MASK_VARIATION](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_MASK_VARIATION:kotlin.Int) Mask of bits that determine the variation of the base content class. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NULL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NULL:kotlin.Int) Special content type for when no explicit type has been specified. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_FLAG_DECIMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_FLAG_DECIMAL:kotlin.Int) Flag of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): the number is decimal, allowing a decimal point to provide fractional values. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_FLAG_SIGNED](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_FLAG_SIGNED:kotlin.Int) Flag of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): the number is signed, allowing a positive or negative sign at the start. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_VARIATION_NORMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_VARIATION_NORMAL:kotlin.Int) Default variation of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): plain normal numeric text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_NUMBER_VARIATION_PASSWORD](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_VARIATION_PASSWORD:kotlin.Int) Variation of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): entering a numeric password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_AUTO_COMPLETE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_COMPLETE:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the text editor (which means the application) is performing auto-completion of the text being entered based on its own semantics, which it will present to the user as they type. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_AUTO_CORRECT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the user is entering free-form text that should have auto-correction applied to it. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_CAP_CHARACTERS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_CHARACTERS:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): capitalize all characters. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_CAP_SENTENCES](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): capitalize the first character of each sentence. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_CAP_WORDS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_WORDS:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): capitalize the first character of every word. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): Let the IME know the text conversion suggestions are required by the application. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_IME_MULTI_LINE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_IME_MULTI_LINE:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the regular text view associated with this should not be multi-line, but when a fullscreen input method is providing text it should use multiple lines if it can. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_MULTI_LINE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_MULTI_LINE:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): multiple lines of text can be entered into the field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_FLAG_NO_SUGGESTIONS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_NO_SUGGESTIONS:kotlin.Int) Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the input method does not need to display any dictionary-based candidates. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_EMAIL_ADDRESS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_EMAIL_ADDRESS:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering an e-mail address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_EMAIL_SUBJECT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_EMAIL_SUBJECT:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering the subject line of an e-mail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_FILTER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_FILTER:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering text to filter contents of a list etc. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_LONG_MESSAGE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_LONG_MESSAGE:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering the content of a long, possibly formal message such as the body of an e-mail. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_NORMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_NORMAL:kotlin.Int) Default variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): plain old normal text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_PASSWORD](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_PASSWORD:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a password. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_PERSON_NAME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_PERSON_NAME:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering the name of a person. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_PHONETIC](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_PHONETIC:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering text for phonetic pronunciation, such as a phonetic name field in contacts. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_POSTAL_ADDRESS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_POSTAL_ADDRESS:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a postal mailing address. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_SHORT_MESSAGE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_SHORT_MESSAGE:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a short, possibly informal message such as an instant message or a text message. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_URI](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_URI:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a URI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_VISIBLE_PASSWORD](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_VISIBLE_PASSWORD:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a password, which should be visible to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_WEB_EDIT_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_WEB_EDIT_TEXT:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering text inside of a web form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering e-mail address inside of a web form. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TYPE_TEXT_VARIATION_WEB_PASSWORD](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_WEB_PASSWORD:kotlin.Int) Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering password inside of a web form. |

## Constants

### TYPE_CLASS_DATETIME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CLASS_DATETIME: Int
```

Class for dates and times. It supports the following variations: [TYPE_DATETIME_VARIATION_NORMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_DATETIME_VARIATION_NORMAL:kotlin.Int) [TYPE_DATETIME_VARIATION_DATE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_DATETIME_VARIATION_DATE:kotlin.Int), and [TYPE_DATETIME_VARIATION_TIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_DATETIME_VARIATION_TIME:kotlin.Int). 

 Value: 4

### TYPE_CLASS_NUMBER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_CLASS_NUMBER: Int
```

Class for numeric text. This class supports the following flags: [TYPE_NUMBER_FLAG_SIGNED](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_FLAG_SIGNED:kotlin.Int) and [TYPE_NUMBER_FLAG_DECIMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_FLAG_DECIMAL:kotlin.Int). It also supports the following variations: [TYPE_NUMBER_VARIATION_NORMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_VARIATION_NORMAL:kotlin.Int) and [TYPE_NUMBER_VARIATION_PASSWORD](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_NUMBER_VARIATION_PASSWORD:kotlin.Int).

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

Class for normal text. This class supports the following flags (only one of which should be set): [TYPE_TEXT_FLAG_CAP_CHARACTERS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_CHARACTERS:kotlin.Int), [TYPE_TEXT_FLAG_CAP_WORDS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_WORDS:kotlin.Int), and. [TYPE_TEXT_FLAG_CAP_SENTENCES](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int). It also supports the following variations: [TYPE_TEXT_VARIATION_NORMAL](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_NORMAL:kotlin.Int), and [TYPE_TEXT_VARIATION_URI](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_URI:kotlin.Int). If you do not recognize the variation, normal should be assumed. 

 Value: 1

### TYPE_DATETIME_VARIATION_DATE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATETIME_VARIATION_DATE: Int
```

Default variation of [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int): allows entering only a date. 

 Value: 16

### TYPE_DATETIME_VARIATION_NORMAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATETIME_VARIATION_NORMAL: Int
```

Default variation of [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int): allows entering both a date and time. 

 Value: 0

### TYPE_DATETIME_VARIATION_TIME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_DATETIME_VARIATION_TIME: Int
```

Default variation of [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int): allows entering only a time. 

 Value: 32

### TYPE_MASK_CLASS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_MASK_CLASS: Int
```

Mask of bits that determine the overall class of text being given. Currently supported classes are: [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int), [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int), [TYPE_CLASS_PHONE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_PHONE:kotlin.Int), [TYPE_CLASS_DATETIME](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_DATETIME:kotlin.Int).

IME authors: If the class is not one you understand, assume [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int) with NO variation or flags.

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

Flag of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): the number is decimal, allowing a decimal point to provide fractional values. 

 Value: 8192

### TYPE_NUMBER_FLAG_SIGNED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_FLAG_SIGNED: Int
```

Flag of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): the number is signed, allowing a positive or negative sign at the start. 

 Value: 4096

### TYPE_NUMBER_VARIATION_NORMAL

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_VARIATION_NORMAL: Int
```

Default variation of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): plain normal numeric text. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be dropped when passed through [EditorInfo.makeCompatible(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#makeCompatible(kotlin.Int)). 

 Value: 0

### TYPE_NUMBER_VARIATION_PASSWORD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_NUMBER_VARIATION_PASSWORD: Int
```

Variation of [TYPE_CLASS_NUMBER](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_NUMBER:kotlin.Int): entering a numeric password. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be dropped when passed through [EditorInfo.makeCompatible(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#makeCompatible(kotlin.Int)). 

 Value: 16

### TYPE_TEXT_FLAG_AUTO_COMPLETE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_AUTO_COMPLETE: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the text editor (which means the application) is performing auto-completion of the text being entered based on its own semantics, which it will present to the user as they type. This generally means that the input method should not be showing candidates itself, but can expect the editor to supply its own completions/candidates from [InputMethodSession.displayCompletions()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession.html#displayCompletions(kotlin.Array))as a result of the editor calling [InputMethodManager.displayCompletions()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager.html#displayCompletions(android.view.View,%20kotlin.Array)). Note the contrast with [TYPE_TEXT_FLAG_AUTO_CORRECT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int) and [TYPE_TEXT_FLAG_NO_SUGGESTIONS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_NO_SUGGESTIONS:kotlin.Int):`TYPE_TEXT_FLAG_AUTO_COMPLETE`means the editor should show an interface for displaying suggestions, but instead of supplying its own it will rely on the Editor to pass completions/corrections. 

 Value: 65536

### TYPE_TEXT_FLAG_AUTO_CORRECT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_AUTO_CORRECT: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the user is entering free-form text that should have auto-correction applied to it. Without this flag, the IME will not try to correct typos. You should always set this flag unless you really expect users to type non-words in this field, for example to choose a name for a character in a game. Contrast this with [TYPE_TEXT_FLAG_AUTO_COMPLETE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_COMPLETE:kotlin.Int) and [TYPE_TEXT_FLAG_NO_SUGGESTIONS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_NO_SUGGESTIONS:kotlin.Int):`TYPE_TEXT_FLAG_AUTO_CORRECT`means that the IME will try to auto-correct typos as the user is typing, but does not define whether the IME offers an interface to show suggestions. 

 Value: 32768

### TYPE_TEXT_FLAG_CAP_CHARACTERS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_CAP_CHARACTERS: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): capitalize all characters. Overrides [TYPE_TEXT_FLAG_CAP_WORDS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_WORDS:kotlin.Int) and [TYPE_TEXT_FLAG_CAP_SENTENCES](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int). This value is explicitly defined to be the same as [TextUtils.CAP_MODE_CHARACTERS](https://developer.android.com/reference/kotlin/android/text/TextUtils#CAP_MODE_CHARACTERS:kotlin.Int). Of course, this only affects languages where there are upper-case and lower-case letters. 

 Value: 4096

### TYPE_TEXT_FLAG_CAP_SENTENCES

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_CAP_SENTENCES: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): capitalize the first character of each sentence. This value is explicitly defined to be the same as [TextUtils.CAP_MODE_SENTENCES](https://developer.android.com/reference/kotlin/android/text/TextUtils#CAP_MODE_SENTENCES:kotlin.Int). For example in English it means to capitalize after a period and a space (note that other languages may have different characters for period, or not use spaces, or use different grammatical rules). Of course, this only affects languages where there are upper-case and lower-case letters. 

 Value: 16384

### TYPE_TEXT_FLAG_CAP_WORDS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_CAP_WORDS: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): capitalize the first character of every word. Overrides [TYPE_TEXT_FLAG_CAP_SENTENCES](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int). This value is explicitly defined to be the same as [TextUtils.CAP_MODE_WORDS](https://developer.android.com/reference/kotlin/android/text/TextUtils#CAP_MODE_WORDS:kotlin.Int). Of course, this only affects languages where there are upper-case and lower-case letters. 

 Value: 8192

### TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): Let the IME know the text conversion suggestions are required by the application. Text conversion suggestion is for the transliteration languages which has pronunciation characters and target characters. When the user is typing the pronunciation charactes, the IME could provide the possible target characters to the user. When this flag is set, the IME should insert the text conversion suggestions through [Builder.setTextConversionSuggestions(List)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute.Builder.html#setTextConversionSuggestions(kotlin.collections.MutableList))and the [TextAttribute](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute.html#) with initialized with the text conversion suggestions is provided by the IME to the application. To receive the additional information, the application needs to implement [InputConnection.setComposingText(CharSequence, int, TextAttribute)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#setComposingText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)), [InputConnection.setComposingRegion(int, int, TextAttribute)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#setComposingRegion(kotlin.Int,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)), and [InputConnection.commitText(CharSequence, int, TextAttribute)](https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection.html#commitText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)). 

 Value: 1048576

### TYPE_TEXT_FLAG_IME_MULTI_LINE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_IME_MULTI_LINE: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the regular text view associated with this should not be multi-line, but when a fullscreen input method is providing text it should use multiple lines if it can. 

 Value: 262144

### TYPE_TEXT_FLAG_MULTI_LINE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_MULTI_LINE: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): multiple lines of text can be entered into the field. If this flag is not set, the text field will be constrained to a single line. The IME may also choose not to display an enter key when this flag is not set, as there should be no need to create new lines. 

 Value: 131072

### TYPE_TEXT_FLAG_NO_SUGGESTIONS

Added in [API level 5](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_FLAG_NO_SUGGESTIONS: Int
```

Flag for [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): the input method does not need to display any dictionary-based candidates. This is useful for text views that do not contain words from the language and do not benefit from any dictionary-based completions or corrections. It overrides the [TYPE_TEXT_FLAG_AUTO_CORRECT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int) value when set. Please avoid using this unless you are certain this is what you want. Many input methods need suggestions to work well, for example the ones based on gesture typing. Consider clearing [TYPE_TEXT_FLAG_AUTO_CORRECT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int) instead if you just do not want the IME to correct typos. Note the contrast with [TYPE_TEXT_FLAG_AUTO_CORRECT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int) and [TYPE_TEXT_FLAG_AUTO_COMPLETE](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_FLAG_AUTO_COMPLETE:kotlin.Int):`TYPE_TEXT_FLAG_NO_SUGGESTIONS`means the IME does not need to show an interface to display suggestions. Most IMEs will also take this to mean they do not need to try to auto-correct what the user is typing. 

 Value: 524288

### TYPE_TEXT_VARIATION_EMAIL_ADDRESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_EMAIL_ADDRESS: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering an e-mail address. 

 Value: 32

### TYPE_TEXT_VARIATION_EMAIL_SUBJECT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_EMAIL_SUBJECT: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering the subject line of an e-mail. 

 Value: 48

### TYPE_TEXT_VARIATION_FILTER

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_FILTER: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering text to filter contents of a list etc. 

 Value: 176

### TYPE_TEXT_VARIATION_LONG_MESSAGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_LONG_MESSAGE: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering the content of a long, possibly formal message such as the body of an e-mail. 

 Value: 80

### TYPE_TEXT_VARIATION_NORMAL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_NORMAL: Int
```

Default variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): plain old normal text. 

 Value: 0

### TYPE_TEXT_VARIATION_PASSWORD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_PASSWORD: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a password. 

 Value: 128

### TYPE_TEXT_VARIATION_PERSON_NAME

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_PERSON_NAME: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering the name of a person. 

 Value: 96

### TYPE_TEXT_VARIATION_PHONETIC

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_PHONETIC: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering text for phonetic pronunciation, such as a phonetic name field in contacts. This is mostly useful for languages where one spelling may have several phonetic readings, like Japanese. 

 Value: 192

### TYPE_TEXT_VARIATION_POSTAL_ADDRESS

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_POSTAL_ADDRESS: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a postal mailing address. 

 Value: 112

### TYPE_TEXT_VARIATION_SHORT_MESSAGE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_SHORT_MESSAGE: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a short, possibly informal message such as an instant message or a text message. 

 Value: 64

### TYPE_TEXT_VARIATION_URI

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_URI: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a URI. 

 Value: 16

### TYPE_TEXT_VARIATION_VISIBLE_PASSWORD

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_VISIBLE_PASSWORD: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering a password, which should be visible to the user. 

 Value: 144

### TYPE_TEXT_VARIATION_WEB_EDIT_TEXT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_WEB_EDIT_TEXT: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering text inside of a web form. 

 Value: 160

### TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering e-mail address inside of a web form. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be seen as [TYPE_TEXT_VARIATION_EMAIL_ADDRESS](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_EMAIL_ADDRESS:kotlin.Int) when passed through [EditorInfo.makeCompatible(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#makeCompatible(kotlin.Int)). 

 Value: 208

### TYPE_TEXT_VARIATION_WEB_PASSWORD

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TYPE_TEXT_VARIATION_WEB_PASSWORD: Int
```

Variation of [TYPE_CLASS_TEXT](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_CLASS_TEXT:kotlin.Int): entering password inside of a web form. This was added in [android.os.Build.VERSION_CODES#HONEYCOMB](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int). An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be seen as [TYPE_TEXT_VARIATION_PASSWORD](https://developer.android.com/reference/kotlin/android/text/InputType#TYPE_TEXT_VARIATION_PASSWORD:kotlin.Int) when passed through [EditorInfo.makeCompatible(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo.html#makeCompatible(kotlin.Int)). 

 Value: 224
