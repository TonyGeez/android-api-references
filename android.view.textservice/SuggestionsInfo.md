Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SuggestionsInfo

Kotlin | [Java](../android/view/textservice/SuggestionsInfo.md)
| --- | --- |

```
class SuggestionsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textservice.SuggestionsInfo](../android/view/textservice/SuggestionsInfo.md) |

This class contains a metadata of suggestions from the text service

## Summary

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_DONT_SHOW_UI_FOR_SUGGESTIONS:kotlin.Int` Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service has an alternative way to show UI for the list of correction suggestions to the user. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_HAS_RECOMMENDED_SUGGESTIONS:kotlin.Int` Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service thinks the result suggestions include highly recommended ones. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_IN_THE_DICTIONARY:kotlin.Int` Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the requested word was found in the dictionary in the text service. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_LOOKS_LIKE_GRAMMAR_ERROR:kotlin.Int` Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service thinks the requested sentence contains a grammar error. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_LOOKS_LIKE_TYPO:kotlin.Int` Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service thinks the requested word looks like a typo. |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#SuggestionsInfo(android.os.Parcel)(source: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |
| `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#SuggestionsInfo(kotlin.Int,%20kotlin.Array)(suggestionsAttributes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, suggestions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!)` Constructor. |
| `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#SuggestionsInfo(kotlin.Int,%20kotlin.Array,%20kotlin.Int,%20kotlin.Int)(suggestionsAttributes: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, suggestions: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html<https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!>!, cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sequence: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Constructor. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#describeContents()()` Used to make this class parcelable. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getCookie()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSequence()()` <br /> |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)! | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionAt(kotlin.Int)(i: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsCount()()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#setCookieAndSequence(kotlin.Int,%20kotlin.Int)(cookie: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html, sequence: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Set the cookie and the sequence of SuggestionsInfo which are set to TextInfo from a client application |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SuggestionsInfo](../android/view/textservice/SuggestionsInfo.md)!\> | `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#CREATOR:android.os.Parcelable.Creator` Used to make this class parcelable. |

## Constants

### RESULT_ATTR_DONT_SHOW_UI_FOR_SUGGESTIONS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ATTR_DONT_SHOW_UI_FOR_SUGGESTIONS: Int
```

Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service has an alternative way to show UI for the list of correction suggestions to the user. When this flag is set, the receiver of the result suggestions should mark the erroneous part of the text with a text signifier (for example, underline), but should not show any UI for the list of correction suggestions to the user (for example, in a popup window).

 Value: 16

### RESULT_ATTR_HAS_RECOMMENDED_SUGGESTIONS

Added in [API level 15](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ATTR_HAS_RECOMMENDED_SUGGESTIONS: Int
```

Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service thinks the result suggestions include highly recommended ones.

 Value: 4

### RESULT_ATTR_IN_THE_DICTIONARY

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ATTR_IN_THE_DICTIONARY: Int
```

Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the requested word was found in the dictionary in the text service.

 Value: 1

### RESULT_ATTR_LOOKS_LIKE_GRAMMAR_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ATTR_LOOKS_LIKE_GRAMMAR_ERROR: Int
```

Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service thinks the requested sentence contains a grammar error.

 Value: 8

### RESULT_ATTR_LOOKS_LIKE_TYPO

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val RESULT_ATTR_LOOKS_LIKE_TYPO: Int
```

Flag of the attributes of the suggestions that can be obtained by `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#getSuggestionsAttributes()`: this tells that the text service thinks the requested word looks like a typo.

 Value: 2

## Public constructors

### SuggestionsInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SuggestionsInfo(source: Parcel!)
```

### SuggestionsInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SuggestionsInfo(
    suggestionsAttributes: Int, 
    suggestions: Array<String!>!)
```

Constructor.

| Parameters ||
|---|---|
| `suggestionsAttributes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): from the text service |
| `suggestions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: from the text service |

### SuggestionsInfo

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
SuggestionsInfo(
    suggestionsAttributes: Int, 
    suggestions: Array<String!>!, 
    cookie: Int, 
    sequence: Int)
```

Constructor.

| Parameters ||
|---|---|
| `suggestionsAttributes` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): from the text service. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_IN_THE_DICTIONARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_LOOKS_LIKE_TYPO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_HAS_RECOMMENDED_SUGGESTIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_LOOKS_LIKE_GRAMMAR_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_DONT_SHOW_UI_FOR_SUGGESTIONS:kotlin.Int` |
| `suggestions` | [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)\< [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!\>!: from the text service |
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cookie of the input TextInfo |
| --- | --- |
| `sequence` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cookie of the input TextInfo |

## Public methods

### describeContents

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Used to make this class parcelable.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getCookie

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCookie(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the cookie which may be set by a client application |

### getSequence

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSequence(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the sequence which may be set by a client application |

### getSuggestionAt

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestionAt(i: Int): String!
```

| Parameters ||
|---|---|
| `i` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the id of suggestions |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html!` | the suggestion at the specified id |

### getSuggestionsAttributes

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestionsAttributes(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the attributes of suggestions. This includes whether the spell checker has the word in its dictionary or not and whether the spell checker has confident suggestions for the word or not. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_IN_THE_DICTIONARY:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_LOOKS_LIKE_TYPO:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_HAS_RECOMMENDED_SUGGESTIONS:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_LOOKS_LIKE_GRAMMAR_ERROR:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/view/textservice/SuggestionsInfo#RESULT_ATTR_DONT_SHOW_UI_FOR_SUGGESTIONS:kotlin.Int` |

### getSuggestionsCount

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSuggestionsCount(): Int
```

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the count of the suggestions. If there's no suggestions at all, this method returns -1. Even if this method returns 0, it doesn't necessarily mean that there are no suggestions for the requested word. For instance, the caller could have been asked to limit the maximum number of suggestions returned. |

### setCookieAndSequence

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun setCookieAndSequence(
    cookie: Int, 
    sequence: Int
): Unit
```

Set the cookie and the sequence of SuggestionsInfo which are set to TextInfo from a client application

| Parameters ||
|---|---|
| `cookie` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cookie of an input TextInfo |
| `sequence` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): the cookie of an input TextInfo |

### writeToParcel

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](../android/os/Parcel.md): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 14](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<SuggestionsInfo!>
```

Used to make this class parcelable.
