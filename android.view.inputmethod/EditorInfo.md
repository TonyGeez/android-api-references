Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# EditorInfo

```
open class EditorInfo : InputType, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#) |

An EditorInfo describes several attributes of a text editing object that an input method is communicating with (typically an EditText), most importantly the type of text content it contains and the current cursor position.

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_DONE:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "done" operation, typically meaning there is nothing more to input and the IME will be closed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_GO:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "go" operation to take the user to the target of the text they typed. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NEXT:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "next" operation, taking the user to the next field that will accept text. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NONE:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: there is no available action. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_PREVIOUS:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: like `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NEXT:kotlin.Int`, but for moving to the previous field. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_SEARCH:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "search" operation, taking the user to the results of searching for the text they have typed (in whatever context is appropriate). |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_SEND:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "send" operation, delivering the text to its target. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_UNSPECIFIED:kotlin.Int` Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: no specific action has been associated with this editor, let the editor come up with its own if it can. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_FORCE_ASCII:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to request an IME that is capable of inputting ASCII characters. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NAVIGATE_NEXT:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to specify that there is something interesting that a forward navigation can focus on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NAVIGATE_PREVIOUS:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: like `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NAVIGATE_NEXT:kotlin.Int`, but specifies there is something interesting that a backward navigation can focus on. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NO_ACCESSORY_ACTION:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used in conjunction with one of the actions masked by `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`, this indicates that the action should not be available as an accessory button on the right of the extracted text when the input method is full-screen. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NO_ENTER_ACTION:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used in conjunction with one of the actions masked by `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NO_EXTRACT_UI:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to specify that the IME does not need to show its extracted text UI. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NO_FULLSCREEN:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to request that the IME never go into fullscreen mode. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NO_PERSONALIZED_LEARNING:kotlin.Int` Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to request that the IME should not update any personalized data such as typing history and personalized language model based on what the user typed on this text editing object. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int` Set of bits in `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int` that provide alternative actions associated with the "enter" key. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_NULL:kotlin.Int` Generic unspecified type for `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`. |
| --- | --- |

Inherited constants From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int`

Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`

Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point.

<br />

From class `https://developer.android.com/reference/kotlin/android/text/InputType.html#` `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_DATETIME:kotlin.Int`

Class for dates and times. It supports the following variations: `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_DATETIME_VARIATION_NORMAL:kotlin.Int` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_DATETIME_VARIATION_DATE:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_DATETIME_VARIATION_TIME:kotlin.Int`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_NUMBER:kotlin.Int`

Class for numeric text. This class supports the following flags: `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_FLAG_SIGNED:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_FLAG_DECIMAL:kotlin.Int`. It also supports the following variations: `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_VARIATION_NORMAL:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_VARIATION_PASSWORD:kotlin.Int`.

IME authors: If you do not recognize the variation, normal should be assumed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_PHONE:kotlin.Int`

Class for a phone number. This class currently supports no variations or flags.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`

Class for normal text. This class supports the following flags (only one of which should be set): `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_CHARACTERS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_WORDS:kotlin.Int`, and. `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int`. It also supports the following variations: `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_NORMAL:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_URI:kotlin.Int`. If you do not recognize the variation, normal should be assumed.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_DATETIME_VARIATION_DATE:kotlin.Int`

Default variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_DATETIME:kotlin.Int`: allows entering only a date.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_DATETIME_VARIATION_NORMAL:kotlin.Int`

Default variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_DATETIME:kotlin.Int`: allows entering both a date and time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_DATETIME_VARIATION_TIME:kotlin.Int`

Default variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_DATETIME:kotlin.Int`: allows entering only a time.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_MASK_CLASS:kotlin.Int`

Mask of bits that determine the overall class of text being given. Currently supported classes are: `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_NUMBER:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_PHONE:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_DATETIME:kotlin.Int`.

IME authors: If the class is not one you understand, assume `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int` with NO variation or flags.

<br />

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_MASK_FLAGS:kotlin.Int`

Mask of bits that provide addition bit flags of options.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_MASK_VARIATION:kotlin.Int`

Mask of bits that determine the variation of the base content class.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NULL:kotlin.Int`

Special content type for when no explicit type has been specified. This should be interpreted to mean that the target input connection is not rich, it can not process and show things like candidate text nor retrieve the current text, so the input method will need to run in a limited "generate key events" mode, if it supports it. Note that some input methods may not support it, for example a voice-based input method will likely not be able to generate key events even if this flag is set.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_FLAG_DECIMAL:kotlin.Int`

Flag of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_NUMBER:kotlin.Int`: the number is decimal, allowing a decimal point to provide fractional values.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_FLAG_SIGNED:kotlin.Int`

Flag of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_NUMBER:kotlin.Int`: the number is signed, allowing a positive or negative sign at the start.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_VARIATION_NORMAL:kotlin.Int`

Default variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_NUMBER:kotlin.Int`: plain normal numeric text. This was added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`. An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be dropped when passed through `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#makeCompatible(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_VARIATION_PASSWORD:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_NUMBER:kotlin.Int`: entering a numeric password. This was added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`. An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be dropped when passed through `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#makeCompatible(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_COMPLETE:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: the text editor (which means the application) is performing auto-completion of the text being entered based on its own semantics, which it will present to the user as they type. This generally means that the input method should not be showing candidates itself, but can expect the editor to supply its own completions/candidates from `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodSession#displayCompletions(kotlin.Array)` as a result of the editor calling `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#displayCompletions(android.view.View,%20kotlin.Array)`. Note the contrast with `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_NO_SUGGESTIONS:kotlin.Int`: `TYPE_TEXT_FLAG_AUTO_COMPLETE` means the editor should show an interface for displaying suggestions, but instead of supplying its own it will rely on the Editor to pass completions/corrections.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: the user is entering free-form text that should have auto-correction applied to it. Without this flag, the IME will not try to correct typos. You should always set this flag unless you really expect users to type non-words in this field, for example to choose a name for a character in a game. Contrast this with `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_COMPLETE:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_NO_SUGGESTIONS:kotlin.Int`: `TYPE_TEXT_FLAG_AUTO_CORRECT` means that the IME will try to auto-correct typos as the user is typing, but does not define whether the IME offers an interface to show suggestions.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_CHARACTERS:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: capitalize all characters. Overrides `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_WORDS:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int`. This value is explicitly defined to be the same as `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_CHARACTERS:kotlin.Int`. Of course, this only affects languages where there are upper-case and lower-case letters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: capitalize the first character of each sentence. This value is explicitly defined to be the same as `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_SENTENCES:kotlin.Int`. For example in English it means to capitalize after a period and a space (note that other languages may have different characters for period, or not use spaces, or use different grammatical rules). Of course, this only affects languages where there are upper-case and lower-case letters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_WORDS:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: capitalize the first character of every word. Overrides `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_CAP_SENTENCES:kotlin.Int`. This value is explicitly defined to be the same as `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_WORDS:kotlin.Int`. Of course, this only affects languages where there are upper-case and lower-case letters.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_ENABLE_TEXT_CONVERSION_SUGGESTIONS:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: Let the IME know the text conversion suggestions are required by the application. Text conversion suggestion is for the transliteration languages which has pronunciation characters and target characters. When the user is typing the pronunciation charactes, the IME could provide the possible target characters to the user. When this flag is set, the IME should insert the text conversion suggestions through `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute.Builder#setTextConversionSuggestions(kotlin.collections.MutableList)` and the `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute` with initialized with the text conversion suggestions is provided by the IME to the application. To receive the additional information, the application needs to implement `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingRegion(kotlin.Int,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`, and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_ENABLE_TEXT_SUGGESTION_SELECTED:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: Let the IME know that conversion candidate selection information is requested by the application. Text conversion suggestion is for the transliteration languages, which have the notions of pronunciation and target characters. When the user actively selects a candidate from the conversion suggestions, notifying when candidate selection is occurring helps assistive technologies generate more effective feedback. When this flag is set, and there is an active selected suggestion, the IME should set that a conversion suggestion is selected android.view.inputmethod.TextAttribute.Builder#setSuggestionSelected(boolean) when initializing the `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAttribute`. To receive this information, the application should implement `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#setComposingRegion(kotlin.Int,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`, and `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitText(kotlin.CharSequence,%20kotlin.Int,%20android.view.inputmethod.TextAttribute)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_IME_MULTI_LINE:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: the regular text view associated with this should not be multi-line, but when a fullscreen input method is providing text it should use multiple lines if it can.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_MULTI_LINE:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: multiple lines of text can be entered into the field. If this flag is not set, the text field will be constrained to a single line. The IME may also choose not to display an enter key when this flag is not set, as there should be no need to create new lines.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_NO_SUGGESTIONS:kotlin.Int`

Flag for `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: the input method does not need to display any dictionary-based candidates. This is useful for text views that do not contain words from the language and do not benefit from any dictionary-based completions or corrections. It overrides the `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int` value when set. Please avoid using this unless you are certain this is what you want. Many input methods need suggestions to work well, for example the ones based on gesture typing. Consider clearing `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int` instead if you just do not want the IME to correct typos. Note the contrast with `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_CORRECT:kotlin.Int` and `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_FLAG_AUTO_COMPLETE:kotlin.Int`: `TYPE_TEXT_FLAG_NO_SUGGESTIONS` means the IME does not need to show an interface to display suggestions. Most IMEs will also take this to mean they do not need to try to auto-correct what the user is typing.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_EMAIL_ADDRESS:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering an e-mail address.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_EMAIL_SUBJECT:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering the subject line of an e-mail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_FILTER:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering text to filter contents of a list etc.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_LONG_MESSAGE:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering the content of a long, possibly formal message such as the body of an e-mail.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_NORMAL:kotlin.Int`

Default variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: plain old normal text.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_PASSWORD:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering a password.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_PERSON_NAME:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering the name of a person.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_PHONETIC:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering text for phonetic pronunciation, such as a phonetic name field in contacts. This is mostly useful for languages where one spelling may have several phonetic readings, like Japanese.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_POSTAL_ADDRESS:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering a postal mailing address.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_SHORT_MESSAGE:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering a short, possibly informal message such as an instant message or a text message.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_URI:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering a URI.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_VISIBLE_PASSWORD:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering a password, which should be visible to the user.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_WEB_EDIT_TEXT:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering text inside of a web form.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering e-mail address inside of a web form. This was added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`. An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be seen as `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_EMAIL_ADDRESS:kotlin.Int` when passed through `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#makeCompatible(kotlin.Int)`.

<br />

`https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_WEB_PASSWORD:kotlin.Int`

Variation of `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_CLASS_TEXT:kotlin.Int`: entering password inside of a web form. This was added in `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#HONEYCOMB:kotlin.Int`. An IME must target this API version or later to see this input type; if it doesn't, a request for this type will be seen as `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_PASSWORD:kotlin.Int` when passed through `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#makeCompatible(kotlin.Int)`.

<br />

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#EditorInfo()()` <br /> |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#dump(android.util.Printer,%20kotlin.String)(pw: https://developer.android.com/reference/kotlin/android/util/Printer.html#!, prefix: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!)` Write debug output of this object. |
| open [AutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getAutofillId()()` Returns the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the view that this `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#` is associated with. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getInitialSelectedText(kotlin.Int)(flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the selected text, if any. |
| open [SurroundingText](https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getInitialSurroundingText(kotlin.Int,%20kotlin.Int,%20kotlin.Int)(beforeLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, afterLength: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Gets the surrounding text around the current cursor, with beforeLength characters of text before the cursor (start of the selection), afterLength characters of text after the cursor (end of the selection), and all of the selected text. |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getInitialTextAfterCursor(kotlin.Int,%20kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get length characters of text after the current cursor position. |
| --- | --- |
| open [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getInitialTextBeforeCursor(kotlin.Int,%20kotlin.Int)(length: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Get length characters of text before the current cursor position. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getInitialToolType()()` Returns the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_UP:kotlin.Int` tool type `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)` responsible for focus on the current editor. |
| open [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [PreviewableHandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture)!\>!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()()` Returns the combination of Stylus handwriting gesture preview types supported by the current `Editor`. |
| --- | --- |
| open [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture)!\>!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGestures()()` Returns the combination of Stylus handwriting gesture types supported by the current `Editor`. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#isStylusHandwritingEnabled()()` Returns `true` when an `Editor` has stylus handwriting enabled. |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#isWritingToolsEnabled()()` Returns `true` when an `Editor` has writing tools enabled. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#makeCompatible(kotlin.Int)(targetSdkVersion: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Ensure that the data in this EditorInfo is compatible with an application that was developed against the given target API version. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setAutofillId(android.view.autofill.AutofillId)(autofillId: https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#?)` Sets the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the view that this `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#` is associated with. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setInitialSurroundingSubText(kotlin.CharSequence,%20kotlin.Int)(subText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, subTextStart: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Editors may use this method to provide initial input text to IMEs. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setInitialSurroundingText(kotlin.CharSequence)(sourceText: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)` Editors may use this method to provide initial input text to IMEs. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setInitialToolType(kotlin.Int)(toolType: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_UP:kotlin.Int` tool type `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setStylusHandwritingEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set `true` if the `Editor` has `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` enabled. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setSupportedHandwritingGesturePreviews(kotlin.collections.MutableSet)(gestures: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture!>!>)` Set the Handwriting gesture previews supported by the current `Editor`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setSupportedHandwritingGestures(kotlin.collections.MutableList)(gestures: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture!>!>)` Set the Handwriting gestures supported by the current `Editor`. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setWritingToolsEnabled(kotlin.Boolean)(enabled: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)` Set `false` if `Editor` opts-out of writing tools, that enable IMEs to replace text with generative AI text. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [EditorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#CREATOR:android.os.Parcelable.Creator` Used to make this class parcelable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionId:kotlin.Int` If `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionLabel:kotlin.CharSequence` has been given, this is the id for that command when the user presses its button that is delivered back with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performEditorAction(kotlin.Int)`. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionLabel:kotlin.CharSequence` In some cases an IME may be able to display an arbitrary label for a command the user can perform, which you can specify here. |
| --- | --- |
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#contentMimeTypes:kotlin.Array` List of acceptable MIME types for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitContent(android.view.inputmethod.InputContentInfo,%20kotlin.Int,%20android.os.Bundle)`. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#extras:android.os.Bundle` Any extra data to supply to the input method. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#fieldId:kotlin.Int` Identifier for the editor's field. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#fieldName:kotlin.String` Additional name for the editor's field. |
| [LocaleList](https://developer.android.com/reference/kotlin/android/os/LocaleList.html#)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#hintLocales:android.os.LocaleList` List of the languages that the user is supposed to switch to no matter what input method subtype is currently used. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#hintText:kotlin.CharSequence` The "hint" text of the text view, typically shown in-line when the text is empty to tell the user what to enter. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int` Extended type information for the editor, to help the IME better integrate with it. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialCapsMode:kotlin.Int` The capitalization mode of the first character being edited in the text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelEnd:kotlin.Int` The text offset of the end of the selection at the time editing begins; -1 if not known. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#initialSelStart:kotlin.Int` The text offset of the start of the selection at the time editing begins; -1 if not known. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#inputType:kotlin.Int` The content type of the text box, whose bits are defined by `https://developer.android.com/reference/kotlin/android/text/InputType.html#`. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#label:kotlin.CharSequence` A label to show to the user describing the text they are writing. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#packageName:kotlin.String` Name of the package that owns this editor. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#privateImeOptions:kotlin.String` A string supplying additional information options that are private to a particular IME implementation. |

## Constants

### IME_ACTION_DONE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_DONE: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "done" operation, typically meaning there is nothing more to input and the IME will be closed.

 Value: 6

### IME_ACTION_GO

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_GO: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "go" operation to take the user to the target of the text they typed. Typically used, for example, when entering a URL.

 Value: 2

### IME_ACTION_NEXT

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_NEXT: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "next" operation, taking the user to the next field that will accept text.

 Value: 5

### IME_ACTION_NONE

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_NONE: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: there is no available action.

 Value: 1

### IME_ACTION_PREVIOUS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_PREVIOUS: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: like `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NEXT:kotlin.Int`, but for moving to the previous field. This will normally not be used to specify an action (since it precludes `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NEXT:kotlin.Int`), but can be returned to the app if it sets `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NAVIGATE_PREVIOUS:kotlin.Int`.

 Value: 7

### IME_ACTION_SEARCH

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_SEARCH: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "search" operation, taking the user to the results of searching for the text they have typed (in whatever context is appropriate).

 Value: 3

### IME_ACTION_SEND

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_SEND: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: the action key performs a "send" operation, delivering the text to its target. This is typically used when composing a message in IM or SMS where sending is immediate.

 Value: 4

### IME_ACTION_UNSPECIFIED

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_ACTION_UNSPECIFIED: Int
```

Bits of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`: no specific action has been associated with this editor, let the editor come up with its own if it can.

 Value: 0

### IME_FLAG_FORCE_ASCII

Added in [API level 16](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_FORCE_ASCII: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to request an IME that is capable of inputting ASCII characters. The intention of this flag is to ensure that the user can type Roman alphabet characters in a `https://developer.android.com/reference/kotlin/android/widget/TextView.html#`. It is typically used for an account ID or password input. A lot of the time, IMEs are already able to input ASCII even without being told so (such IMEs already respect this flag in a sense), but there are cases when this is not the default. For instance, users of languages using a different script like Arabic, Greek, Hebrew or Russian typically have a keyboard that can't input ASCII characters by default. Applications need to be aware that the flag is not a guarantee, and some IMEs may not respect it. However, it is strongly recommended for IME authors to respect this flag especially when their IME could end up with a state where only languages using non-ASCII are enabled.

 Value: -2147483648

### IME_FLAG_NAVIGATE_NEXT

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NAVIGATE_NEXT: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to specify that there is something interesting that a forward navigation can focus on. This is like using `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NEXT:kotlin.Int`, except allows the IME to be multiline (with an enter key) as well as provide forward navigation. Note that some IMEs may not be able to do this, especially when running on a small screen where there is little space. In that case it does not need to present a UI for this option. Like `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_NEXT:kotlin.Int`, if the user selects the IME's facility to forward navigate, this will show up in the application at `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performEditorAction(kotlin.Int)`.

 Value: 134217728

### IME_FLAG_NAVIGATE_PREVIOUS

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NAVIGATE_PREVIOUS: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: like `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NAVIGATE_NEXT:kotlin.Int`, but specifies there is something interesting that a backward navigation can focus on. If the user selects the IME's facility to backward navigate, this will show up in the application as an `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_ACTION_PREVIOUS:kotlin.Int` at `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performEditorAction(kotlin.Int)`.

 Value: 67108864

### IME_FLAG_NO_ACCESSORY_ACTION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NO_ACCESSORY_ACTION: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used in conjunction with one of the actions masked by `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`, this indicates that the action should not be available as an accessory button on the right of the extracted text when the input method is full-screen. Note that by setting this flag, there can be cases where the action is simply never available to the user. Setting this generally means that you think that in fullscreen mode, where there is little space to show the text, it's not worth taking some screen real estate to display the action and it should be used instead to show more text.

 Value: 536870912

### IME_FLAG_NO_ENTER_ACTION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NO_ENTER_ACTION: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used in conjunction with one of the actions masked by `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_MASK_ACTION:kotlin.Int`. If this flag is not set, IMEs will normally replace the "enter" key with the action supplied. This flag indicates that the action should not be available in-line as a replacement for the "enter" key. Typically this is because the action has such a significant impact or is not recoverable enough that accidentally hitting it should be avoided, such as sending a message. Note that `https://developer.android.com/reference/kotlin/android/widget/TextView.html#` will automatically set this flag for you on multi-line text views.

 Value: 1073741824

### IME_FLAG_NO_EXTRACT_UI

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NO_EXTRACT_UI: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to specify that the IME does not need to show its extracted text UI. For input methods that may be fullscreen, often when in landscape mode, this allows them to be smaller and let part of the application be shown behind, through transparent UI parts in the fullscreen IME. The part of the UI visible to the user may not be responsive to touch because the IME will receive touch events, which may confuse the user; use `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#IME_FLAG_NO_FULLSCREEN:kotlin.Int` instead for a better experience. Using this flag is discouraged and it may become deprecated in the future. Its meaning is unclear in some situations and it may not work appropriately on older versions of the platform.

 Value: 268435456

### IME_FLAG_NO_FULLSCREEN

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NO_FULLSCREEN: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to request that the IME never go into fullscreen mode. By default, IMEs may go into full screen mode when they think it's appropriate, for example on small screens in landscape orientation where displaying a software keyboard may occlude such a large portion of the screen that the remaining part is too small to meaningfully display the application UI. If this flag is set, compliant IMEs will never go into full screen mode, and always leave some space to display the application UI. Applications need to be aware that the flag is not a guarantee, and some IMEs may ignore it.

 Value: 33554432

### IME_FLAG_NO_PERSONALIZED_LEARNING

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_FLAG_NO_PERSONALIZED_LEARNING: Int
```

Flag of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`: used to request that the IME should not update any personalized data such as typing history and personalized language model based on what the user typed on this text editing object. Typical use cases are:

- When the application is in a special mode, where user's activities are expected to be not recorded in the application's history. Some web browsers and chat applications may have this kind of modes.
- When storing typing history does not make much sense. Specifying this flag in typing games may help to avoid typing history from being filled up with words that the user is less likely to type in their daily life. Another example is that when the application already knows that the expected input is not a valid word (e.g. a promotion code that is not a valid word in any natural language).

<br />

Applications need to be aware that the flag is not a guarantee, and some IMEs may not respect it.

 Value: 16777216

### IME_MASK_ACTION

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_MASK_ACTION: Int
```

Set of bits in `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int` that provide alternative actions associated with the "enter" key. This both helps the IME provide better feedback about what the enter key will do, and also allows it to provide alternative mechanisms for providing that command.

 Value: 255

### IME_NULL

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val IME_NULL: Int
```

Generic unspecified type for `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#imeOptions:kotlin.Int`.

 Value: 0

## Public constructors

### EditorInfo

```
EditorInfo()
```

## Public methods

### describeContents

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### dump

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun dump(
    pw: Printer!, 
    prefix: String!
): Unit
```

Write debug output of this object.

### getAutofillId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getAutofillId(): AutofillId?
```

Returns the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the view that this `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#` is associated with. The value is filled in with the result of `https://developer.android.com/reference/kotlin/android/view/View.html#getAutofillId()` on the view that is being edited. Note: For virtual view(e.g. Compose or Webview), default behavior is the autofillId is the id of the container view, unless the virtual view provider sets the virtual id when the InputMethodManager calls `https://developer.android.com/reference/kotlin/android/view/View.html#onCreateInputConnection(android.view.inputmethod.EditorInfo)` on the container view.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#?` | This value may be `null`. |

### getInitialSelectedText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialSelectedText(flags: Int): CharSequence?
```

Gets the selected text, if any. May be `null` when the protocol is not supported or the selected text is way too long.

| Parameters ||
|---|---|
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either 0 or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text that is currently selected, if any. It could be an empty string when there is no text selected. When `null` is returned, the selected text might be too long or this protocol is not supported. |

### getInitialSurroundingText

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialSurroundingText(
    beforeLength: Int, 
    afterLength: Int, 
    flags: Int
): SurroundingText?
```

Gets the surrounding text around the current cursor, with beforeLength characters of text before the cursor (start of the selection), afterLength characters of text after the cursor (end of the selection), and all of the selected text.

The initial surrounding text for return could be trimmed if oversize. Fundamental trimming rules are:

- The text before the cursor is the most important information to IMEs.
- The text after the cursor is the second important information to IMEs.
- The selected text is the least important information but it shall NEVER be truncated. When it is too long, just drop it.

For example, the subText can be viewed as TextBeforeCursor + Selection + TextAfterCursor. The result could be:

1. (maybeTrimmedAtHead)TextBeforeCursor + Selection + TextAfterCursor(maybeTrimmedAtTail)
2. (maybeTrimmedAtHead)TextBeforeCursor + TextAfterCursor(maybeTrimmedAtTail)

| Parameters ||
|---|---|
| `beforeLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text before the cursor. Value is 0 or greater |
| `afterLength` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text after the cursor. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either `0` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` |
| --- | --- |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText?` | an `https://developer.android.com/reference/kotlin/android/view/inputmethod/SurroundingText` object describing the surrounding text and state of selection, or `null` if the editor or system could not support this protocol. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if `beforeLength` or `afterLength` is negative. |

### getInitialTextAfterCursor

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialTextAfterCursor(
    length: Int, 
    flags: Int
): CharSequence?
```

Get length characters of text after the current cursor position. May be `null` when the protocol is not supported.

| Parameters ||
|---|---|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either 0 or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text after the cursor position; the length of the returned text might be less than length. When there is no text after the cursor, an empty string will be returned. It could also be `null` when the editor or system could not support this protocol. |

### getInitialTextBeforeCursor

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialTextBeforeCursor(
    length: Int, 
    flags: Int
): CharSequence?
```

Get length characters of text before the current cursor position. May be `null` when the protocol is not supported.

| Parameters ||
|---|---|
| `length` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The expected length of the text. Value is 0 or greater |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Supplies additional options controlling how the text is returned. May be either 0 or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int`. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#GET_TEXT_WITH_STYLES:kotlin.Int` |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html?` | the text before the cursor position; the length of the returned text might be less than length. When there is no text before the cursor, an empty string will be returned. It could also be `null` when the editor or system could not support this protocol. |

### getInitialToolType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getInitialToolType(): Int
```

Returns the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_UP:kotlin.Int` tool type `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)` responsible for focus on the current editor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | toolType `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)`. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_FINGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_MOUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_ERASER:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setInitialToolType(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#onUpdateEditorToolType(kotlin.Int)`

### getSupportedHandwritingGesturePreviews

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedHandwritingGesturePreviews(): MutableSet<Class<out PreviewableHandwritingGesture!>!>
```

Returns the combination of Stylus handwriting gesture preview types supported by the current `Editor`. For an editor that supports Stylus Handwriting. `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)`, it also declares supported gesture previews.

Note: A supported gesture `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGestures()` may not have preview supported `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()`.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture!>!>` | Set of supported gesture preview classes. One of `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectRangeGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteRangeGesture`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGestures()`

### getSupportedHandwritingGestures

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun getSupportedHandwritingGestures(): MutableList<Class<out HandwritingGesture!>!>
```

Returns the combination of Stylus handwriting gesture types supported by the current `Editor`. For an editor that supports Stylus Handwriting. `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)`, it also declares supported gestures.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/java/lang/Class.html#<out https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture!>!>` | List of supported gesture classes including any of `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()`

### isStylusHandwritingEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isStylusHandwritingEnabled(): Boolean
```

Returns `true` when an `Editor` has stylus handwriting enabled. `false` by default.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setStylusHandwritingEnabled(kotlin.Boolean)`
- `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#isStylusHandwritingAvailable()`

### isWritingToolsEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun isWritingToolsEnabled(): Boolean
```

Returns `true` when an `Editor` has writing tools enabled. `true` by default for all editors. Toolkits can optionally disable them where not relevant e.g. passwords, number input, etc.
**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setWritingToolsEnabled(kotlin.Boolean)`

### makeCompatible

Added in [API level 11](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun makeCompatible(targetSdkVersion: Int): Unit
```

Ensure that the data in this EditorInfo is compatible with an application that was developed against the given target API version. This can impact the following input types: `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_WEB_EMAIL_ADDRESS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_TEXT_VARIATION_WEB_PASSWORD:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_VARIATION_NORMAL:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_NUMBER_VARIATION_PASSWORD:kotlin.Int`.

This is called by the framework for input method implementations; you should not generally need to call it yourself.

| Parameters ||
|---|---|
| `targetSdkVersion` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The API version number that the compatible application was developed against. |

### setAutofillId

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setAutofillId(autofillId: AutofillId?): Unit
```

Sets the `https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#` of the view that this `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#` is associated with.

| Parameters ||
|---|---|
| `autofillId` | [AutofillId](https://developer.android.com/reference/kotlin/android/view/autofill/AutofillId.html#)?: This value may be `null`. |

### setInitialSurroundingSubText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInitialSurroundingSubText(
    subText: CharSequence, 
    subTextStart: Int
): Unit
```

Editors may use this method to provide initial input text to IMEs. As the surrounding text could be used to provide various input assistance, we recommend editors to provide the complete initial input text in its `https://developer.android.com/reference/kotlin/android/view/View.html#onCreateInputConnection(android.view.inputmethod.EditorInfo)` callback. When trimming the input text is needed, call this method instead of `setInitialSurroundingText(CharSequence)` and provide the trimmed position info. Always try to include the selected text within `subText` to give the system best flexibility to choose where and how to trim `subText` when necessary. Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, spans that do not implement `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` will be automatically dropped.

| Parameters ||
|---|---|
| `subText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The input text. When it was trimmed, `subTextStart` must be provided correctly. This value cannot be `null`. |
| `subTextStart` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The position that the input text got trimmed. For example, when the editor wants to trim out the first 10 chars, subTextStart should be 10. |

### setInitialSurroundingText

Added in [API level 30](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInitialSurroundingText(sourceText: CharSequence): Unit
```

Editors may use this method to provide initial input text to IMEs. As the surrounding text could be used to provide various input assistance, we recommend editors to provide the complete initial input text in its `https://developer.android.com/reference/kotlin/android/view/View.html#onCreateInputConnection(android.view.inputmethod.EditorInfo)` callback. The supplied text will then be processed to serve `getInitialTextBeforeCursor`, `getInitialSelectedText`, and `getInitialTextBeforeCursor`. System is allowed to trim `sourceText` for various reasons while keeping the most valuable data to IMEs. Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#S:kotlin.Int`, spans that do not implement `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` will be automatically dropped.

**Editor authors:**Providing the initial input text helps reducing IPC calls for IMEs to provide many modern features right after the connection setup. We recommend calling this method in your implementation.

| Parameters ||
|---|---|
| `sourceText` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): The complete input text. This value cannot be `null`. |

### setInitialToolType

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setInitialToolType(toolType: Int): Unit
```

Set the initial `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#ACTION_UP:kotlin.Int` tool type `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)`. that brought focus to the view.

| Parameters ||
|---|---|
| `toolType` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is one of the following: - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_FINGER:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_STYLUS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_MOUSE:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#TOOL_TYPE_ERASER:kotlin.Int` |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getInitialToolType()`
- `https://developer.android.com/reference/kotlin/android/view/MotionEvent.html#getToolType(kotlin.Int)`
- `https://developer.android.com/reference/kotlin/android/inputmethodservice/InputMethodService.html#onUpdateEditorToolType(kotlin.Int)`

### setStylusHandwritingEnabled

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setStylusHandwritingEnabled(enabled: Boolean): Unit
```

Set `true` if the `Editor` has `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)` enabled. `false` by default, `Editor` must set it `true` to indicate that it supports stylus handwriting.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): `true` if stylus handwriting is enabled. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/View.html#setAutoHandwritingEnabled(kotlin.Boolean)`

### setSupportedHandwritingGesturePreviews

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSupportedHandwritingGesturePreviews(gestures: MutableSet<Class<out PreviewableHandwritingGesture!>!>): Unit
```

Set the Handwriting gesture previews supported by the current `Editor`. For an editor that supports Stylus Handwriting `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)`, it is also recommended that it declares supported gesture previews.

Note: A supported gesture `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGestures()` may not have preview supported `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()`.

If editor doesn't support one of the declared types, gesture preview will be ignored.

| Parameters ||
|---|---|
| `gestures` | [MutableSet](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-set/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [PreviewableHandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture)!\>!\>: Set of supported gesture classes. One of `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectRangeGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteRangeGesture`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setSupportedHandwritingGestures(kotlin.collections.MutableList)`

### setSupportedHandwritingGestures

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setSupportedHandwritingGestures(gestures: MutableList<Class<out HandwritingGesture!>!>): Unit
```

Set the Handwriting gestures supported by the current `Editor`. For an editor that supports Stylus Handwriting `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#startStylusHandwriting(android.view.View)`, it is also recommended that it declares supported gestures.

If editor doesn't support one of the declared types, IME will not send those Gestures to the editor. Instead they will fallback to using normal text input.

Note: A supported gesture may not have preview supported `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#getSupportedHandwritingGesturePreviews()`.

| Parameters ||
|---|---|
| `gestures` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<out [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture)!\>!\>: List of supported gesture classes including any of `https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertGesture`, `https://developer.android.com/reference/kotlin/android/view/inputmethod/DeleteGesture`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#setSupportedHandwritingGesturePreviews(kotlin.collections.MutableSet)`

### setWritingToolsEnabled

Added in [API level 36](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun setWritingToolsEnabled(enabled: Boolean): Unit
```

Set `false` if `Editor` opts-out of writing tools, that enable IMEs to replace text with generative AI text.

| Parameters ||
|---|---|
| `enabled` | [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html): set `true` to enabled or `false to disable` support. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#isWritingToolsEnabled()`

### writeToParcel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<EditorInfo!>
```

Used to make this class parcelable.

### actionId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var actionId: Int
```

If `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionLabel:kotlin.CharSequence` has been given, this is the id for that command when the user presses its button that is delivered back with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#performEditorAction(kotlin.Int)`.

### actionLabel

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var actionLabel: CharSequence!
```

In some cases an IME may be able to display an arbitrary label for a command the user can perform, which you can specify here. This is typically used as the label for the action to use in-line as a replacement for the "enter" key (see `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#actionId:kotlin.Int`). Remember the key where this will be displayed is typically very small, and there are significant localization challenges to make this fit in all supported languages. Also you can not count absolutely on this being used, as some IMEs may ignore this.

### contentMimeTypes

Added in [API level 25](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var contentMimeTypes: Array<String!>?
```

List of acceptable MIME types for `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitContent(android.view.inputmethod.InputContentInfo,%20kotlin.Int,%20android.os.Bundle)`.

`null` or an empty array means that `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#commitContent(android.view.inputmethod.InputContentInfo,%20kotlin.Int,%20android.os.Bundle)` is not supported in this editor.

### extras

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var extras: Bundle!
```

Any extra data to supply to the input method. This is for extended communication with specific input methods; the name fields in the bundle should be scoped (such as "com.mydomain.im.SOME_FIELD") so that they don't conflict with others. This field can be filled in from the `https://developer.android.com/reference/kotlin/android/R.attr.html#editorExtras:kotlin.Int` attribute of a TextView.

### fieldId

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var fieldId: Int
```

Identifier for the editor's field. This is optional, and may be 0. By default it is filled in with the result of `https://developer.android.com/reference/kotlin/android/view/View.html#getId()` on the View that is being edited.

### fieldName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var fieldName: String!
```

Additional name for the editor's field. This can supply additional name information for the field. By default it is null. The actual contents have no meaning.

### hintLocales

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var hintLocales: LocaleList?
```

List of the languages that the user is supposed to switch to no matter what input method subtype is currently used. This special "hint" can be used mainly for, but not limited to, multilingual users who want IMEs to switch language context automatically.

`null` means that no special language "hint" is needed.

**Editor authors:** Specify this only when you are confident that the user will switch to certain languages in this context no matter what input method subtype is currently selected. Otherwise, keep this `null`. Explicit user actions and/or preferences would be good signals to specify this special "hint", For example, a chat application may be able to put the last used language at the top of `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#hintLocales:android.os.LocaleList` based on whom the user is going to talk, by remembering what language is used in the last conversation. Do not specify `https://developer.android.com/reference/kotlin/android/widget/TextView.html#getTextLocales()` only because it is used for text rendering.
**See Also**

- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#setImeHintLocales(android.os.LocaleList)`
- `https://developer.android.com/reference/kotlin/android/widget/TextView.html#getImeHintLocales()`

### hintText

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var hintText: CharSequence!
```

The "hint" text of the text view, typically shown in-line when the text is empty to tell the user what to enter.

### imeOptions

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var imeOptions: Int
```

Extended type information for the editor, to help the IME better integrate with it.

### initialCapsMode

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var initialCapsMode: Int
```

The capitalization mode of the first character being edited in the text. Values may be any combination of `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_CHARACTERS:kotlin.Int`, `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_WORDS:kotlin.Int`, and `https://developer.android.com/reference/kotlin/android/text/TextUtils.html#CAP_MODE_SENTENCES:kotlin.Int`, though you should generally just take a non-zero value to mean "start out in caps mode".

### initialSelEnd

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var initialSelEnd: Int
```

The text offset of the end of the selection at the time editing begins; -1 if not known. Keep in mind that, without knowing the cursor position, many IMEs will not be able to offer their full feature set and may behave in unpredictable ways: pass the actual cursor position here if possible at all.

Also, this needs to be the cursor position **right now** , not at some point in the past, even if input is starting in the same text field as before. When the app is filling this object, input is about to start by definition, and this value will override any value the app may have passed to `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateSelection(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` before.

### initialSelStart

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var initialSelStart: Int
```

The text offset of the start of the selection at the time editing begins; -1 if not known. Keep in mind that, without knowing the cursor position, many IMEs will not be able to offer their full feature set and may even behave in unpredictable ways: pass the actual cursor position here if possible at all.

Also, this needs to be the cursor position **right now** , not at some point in the past, even if input is starting in the same text field as before. When the app is filling this object, input is about to start by definition, and this value will override any value the app may have passed to `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputMethodManager#updateSelection(android.view.View,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int,%20kotlin.Int)` before.

### inputType

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var inputType: Int
```

The content type of the text box, whose bits are defined by `https://developer.android.com/reference/kotlin/android/text/InputType.html#`.
**See Also**

- `https://developer.android.com/reference/kotlin/android/text/InputType.html#`
- `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_MASK_CLASS:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_MASK_VARIATION:kotlin.Int`
- `https://developer.android.com/reference/kotlin/android/text/InputType.html#TYPE_MASK_FLAGS:kotlin.Int`

### label

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var label: CharSequence!
```

A label to show to the user describing the text they are writing.

### packageName

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var packageName: String!
```

Name of the package that owns this editor.

**IME authors:** In API level 22 `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#LOLLIPOP_MR1:kotlin.Int` and prior, do not trust this package name. The system had not verified the consistency between the package name here and application's uid. Consider to use `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputBinding#getUid()`, which is trustworthy. Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, the system verifies the consistency between this package name and application uid before `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorInfo#` is passed to the input method.

**Editor authors:** Starting from `https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#M:kotlin.Int`, the application is no longer able to establish input connections if the package name provided here is inconsistent with application's uid.

### privateImeOptions

Added in [API level 3](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
var privateImeOptions: String!
```

A string supplying additional information options that are private to a particular IME implementation. The string must be scoped to a package owned by the implementation, to ensure there are no conflicts between implementations, but other than that you can put whatever you want in it to communicate with the IME. For example, you could have a string that supplies an argument like `"com.example.myapp.SpecialMode=3"`. This field is can be filled in from the `https://developer.android.com/reference/kotlin/android/R.attr.html#privateImeOptions:kotlin.Int` attribute of a TextView.
