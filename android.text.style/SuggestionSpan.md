# SuggestionSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestionSpan

Kotlin| [Java](https://developer.android.com/reference/android/text/style/SuggestionSpan "View this page in Java") 
| --- | --- |

```
open class SuggestionSpan : CharacterStyle, ParcelableSpan
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.style.CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) ||
| | ↳ | [android.text.style.SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#) |

Holds suggestion candidates for the text enclosed in this span. When such a span is edited in an EditText, double tapping on the text enclosed in this span will display a popup dialog listing suggestion replacement for that text. The user can then replace the original text by one of the suggestions. These spans should typically be created by the input method to provide correction and alternates for the text.

## Summary

| Constants ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [ACTION_SUGGESTION_PICKED](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#ACTION_SUGGESTION_PICKED:kotlin.String) This action is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_AUTO_CORRECTION](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#FLAG_AUTO_CORRECTION:kotlin.Int) Sets this flag if the auto correction is about to be applied to a word/text that the user is typing/composing. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_EASY_CORRECT](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#FLAG_EASY_CORRECT:kotlin.Int) Sets this flag if the suggestions should be easily accessible with few interactions. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_GRAMMAR_ERROR](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#FLAG_GRAMMAR_ERROR:kotlin.Int) Sets this flag if the suggestions apply to a grammar error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_MISSPELLED](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#FLAG_MISSPELLED:kotlin.Int) Sets this flag if the suggestions apply to a misspelled word/text. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [SUGGESTIONS_MAX_SIZE](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SUGGESTIONS_MAX_SIZE:kotlin.Int) <br /> |
| --- | --- |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGESTION_SPAN_PICKED_AFTER](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SUGGESTION_SPAN_PICKED_AFTER:kotlin.String) This is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGESTION_SPAN_PICKED_BEFORE](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SUGGESTION_SPAN_PICKED_BEFORE:kotlin.String) This is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). |
| static [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [SUGGESTION_SPAN_PICKED_HASHCODE](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SUGGESTION_SPAN_PICKED_HASHCODE:kotlin.String) This is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). |
| --- | --- |

| Public constructors ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SuggestionSpan(android.content.Context,%20kotlin.Array,%20kotlin.Int))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `suggestions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SuggestionSpan(android.content.Context,%20java.util.Locale,%20kotlin.Array,%20kotlin.Int,%20java.lang.Class))`(`context:` ` [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!`, `locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `suggestions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `notificationTargetClass:` ` [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)<*>!`)` <br /> |
| [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SuggestionSpan(android.os.Parcel))`(`src:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)!`)` <br /> |
| [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SuggestionSpan(java.util.Locale,%20kotlin.Array,%20kotlin.Int))`(`locale:` ` [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!`, `suggestions:` ` [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>!`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#describeContents())`()` <br /> |
| open [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getFlags())`()` <br /> |
| --- | --- |
| open [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getLocale](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getLocale())`()` <br /> |
| open [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | [getLocaleObject](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getLocaleObject())`()` Returns a well-formed BCP 47 language tag representation of the suggestions, as a [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSpanTypeId](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getSpanTypeId())`()` <br /> |
| --- | --- |
| open [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>! | [getSuggestions](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getSuggestions())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getUnderlineColor](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getUnderlineColor())`()` <br /> |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#hashCode())`()` <br /> |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFlags](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#setFlags(kotlin.Int))`(`flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [updateDrawState](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#updateDrawState(android.text.TextPaint))`(`tp:` ` [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint.html#)!`)` <br /> |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle) |-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [getUnderlying](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#getUnderlying())`()` <br /> Returns "this" for most CharacterStyles, but for CharacterStyles that were generated by [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle)), returns the underlying CharacterStyle. <br /> | | [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)! | [wrap](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle#wrap(android.text.style.CharacterStyle))`(`cs:` ` [CharacterStyle](https://developer.android.com/reference/kotlin/android/text/style/CharacterStyle)!`)` <br /> A given CharacterStyle can only applied to a single region of a given Spanned. If you need to attach the same CharacterStyle to multiple regions, you can use this method to wrap it with a new object that will have the same effect but be a distinct object so that it can also be attached without conflict. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### ACTION_SUGGESTION_PICKED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val ACTION_SUGGESTION_PICKED: String
```

**Deprecated:** *For IMEs to receive this kind of user interaction signals, implement IMEs' own suggestion picker UI instead of relying on [SuggestionSpan](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#). To retrieve bounding boxes for each character of the composing text, use [android.view.inputmethod.CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo.html#).*

This action is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). 

 Value: "android.text.style.SUGGESTION_PICKED"

### FLAG_AUTO_CORRECTION

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_AUTO_CORRECTION: Int
```

Sets this flag if the auto correction is about to be applied to a word/text that the user is typing/composing. This type of suggestion is rendered differently to indicate the auto correction is happening. 

 Value: 4

### FLAG_EASY_CORRECT

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_EASY_CORRECT: Int
```

Sets this flag if the suggestions should be easily accessible with few interactions. This flag should be set for every suggestions that the user is likely to use. 

 Value: 1

### FLAG_GRAMMAR_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_GRAMMAR_ERROR: Int
```

Sets this flag if the suggestions apply to a grammar error. This type of suggestion is rendered differently to highlight the error. 

 Value: 8

### FLAG_MISSPELLED

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_MISSPELLED: Int
```

Sets this flag if the suggestions apply to a misspelled word/text. This type of suggestion is rendered differently to highlight the error. 

 Value: 2

### SUGGESTIONS_MAX_SIZE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGESTIONS_MAX_SIZE: Int
```  

 Value: 5

### SUGGESTION_SPAN_PICKED_AFTER

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGESTION_SPAN_PICKED_AFTER: String
```

**Deprecated:** *See [ACTION_SUGGESTION_PICKED](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#ACTION_SUGGESTION_PICKED:kotlin.String).*

This is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). 

 Value: "after"

### SUGGESTION_SPAN_PICKED_BEFORE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGESTION_SPAN_PICKED_BEFORE: String
```

**Deprecated:** *See [ACTION_SUGGESTION_PICKED](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#ACTION_SUGGESTION_PICKED:kotlin.String).*

This is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). 

 Value: "before"

### SUGGESTION_SPAN_PICKED_HASHCODE

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val SUGGESTION_SPAN_PICKED_HASHCODE: String
```

**Deprecated:** *See [ACTION_SUGGESTION_PICKED](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#ACTION_SUGGESTION_PICKED:kotlin.String).*

This is deprecated in [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int). 

 Value: "hashcode"

## Public constructors

### SuggestionSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SuggestionSpan(
    context: Context!, 
    suggestions: Array<String!>!, 
    flags: Int)
```

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Context for the application |
| `suggestions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Suggestions for the string under the span |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags indicating how this span is handled in TextView |
| --- | --- |

### SuggestionSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SuggestionSpan(
    context: Context!, 
    locale: Locale!, 
    suggestions: Array<String!>!, 
    flags: Int, 
    notificationTargetClass: Class<*>!)
```

| Parameters ||
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `context` | [Context](https://developer.android.com/reference/kotlin/android/content/Context.html#)!:Context for the application |
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:locale Locale of the suggestions |
| `suggestions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Suggestions for the string under the span. Only the first up to [SuggestionSpan.SUGGESTIONS_MAX_SIZE](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#SUGGESTIONS_MAX_SIZE:kotlin.Int) will be considered. Null values not permitted. |
| --- | --- |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags indicating how this span is handled in TextView |
| `notificationTargetClass` | [Class](https://developer.android.com/reference/kotlin/java/lang/Class.html#)\<\*\>!:if not null, this class will get notified when the user selects one of the suggestions. On Android [android.os.Build.VERSION_CODES#Q](https://developer.android.com/reference/kotlin/android/os/Build.VERSION_CODES.html#Q:kotlin.Int) and later this parameter is always ignored. |

### SuggestionSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SuggestionSpan(src: Parcel!)
```  

### SuggestionSpan

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
SuggestionSpan(
    locale: Locale!, 
    suggestions: Array<String!>!, 
    flags: Int)
```

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `locale` | [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)!:Locale of the suggestions |
| `suggestions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!:Suggestions for the string under the span |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags indicating how this span is handled in TextView |
| --- | --- |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The`equals`method implements an equivalence relation on non-null object references:

- It is*reflexive* : for any non-null reference value`x`,`x.equals(x)`should return`true`.
- It is*symmetric* : for any non-null reference values`x`and`y`,`x.equals(y)`should return`true`if and only if`y.equals(x)`returns`true`.
- It is*transitive* : for any non-null reference values`x`,`y`, and`z`, if`x.equals(y)`returns`true`and`y.equals(z)`returns`true`, then`x.equals(z)`should return`true`.
- It is*consistent* : for any non-null reference values`x`and`y`, multiple invocations of`x.equals(y)`consistently return`true`or consistently return`false`, provided no information used in`equals`comparisons on the objects is modified.
- For any non-null reference value`x`,`x.equals(null)`should return`false`.

An equivalence relation partitions the elements it operates on into*equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |
| `o` | This value may be`null`. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getFlags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFlags(): Int
```  

### getLocale

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Deprecated in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocale(): String
```

**Deprecated:** *use [getLocaleObject()](https://developer.android.com/reference/kotlin/android/text/style/SuggestionSpan#getLocaleObject())instead.*

| Return ||
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | the locale of the suggestions. An empty string is returned if no locale is specified. This value cannot be`null`. |

### getLocaleObject

Added in [API level 24](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getLocaleObject(): Locale?
```

Returns a well-formed BCP 47 language tag representation of the suggestions, as a [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) object.

**Caveat** : The returned object is guaranteed to be a a well-formed BCP 47 language tag representation. For example, this method can return an empty locale rather than returning a malformed data when this object is initialized with an malformed [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#) object, e.g.`new Locale(" a ", " b c d ", " "`.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Locale](https://developer.android.com/reference/kotlin/java/util/Locale.html#)? | the locale of the suggestions.`null`is returned if no locale is specified. |

### getSpanTypeId

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSpanTypeId(): Int
```  

### getSuggestions

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSuggestions(): Array<String!>!
```

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!>! | an array of suggestion texts for this span |

### getUnderlineColor

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getUnderlineColor(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The color of the underline for that span, or 0 if there is no underline |

### hashCode

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### setFlags

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun setFlags(flags: Int): Unit
```  

### updateDrawState

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun updateDrawState(tp: TextPaint!): Unit
```  

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SuggestionSpan!>
```
