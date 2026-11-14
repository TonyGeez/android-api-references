# TranslationRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationRequest

Kotlin | [Java](https://developer.android.com/reference/android/view/translation/TranslationRequest "View this page in Java") 

```
class TranslationRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.translation.TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#) |

Translation request sent to the translation service by the [android.view.translation.Translator](https://developer.android.com/reference/kotlin/android/view/translation/Translator) which contains the text to be translated.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest.Builder) A builder for [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#) |

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DICTIONARY_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_DICTIONARY_RESULT:kotlin.Int) Indicates this request wants to receive the dictionary result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) Indicates this request is willing to accept partial responses. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int) Indicates this request wants to receive the standard translation result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_TRANSLITERATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLITERATION_RESULT:kotlin.Int) Indicates this request wants to receive the transliteration result. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#getFlags())`()` Request flags. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TranslationRequestValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequestValue)!\> | [getTranslationRequestValues](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#getTranslationRequestValues())`()` List of [TranslationRequestValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequestValue) s to be translated. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest)!\> | [getViewTranslationRequests](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#getViewTranslationRequests())`()` List of [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest) s to be translated. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### FLAG_DICTIONARY_RESULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DICTIONARY_RESULT: Int
```

Indicates this request wants to receive the dictionary result.

See [TranslationResponseValue.EXTRA_DEFINITIONS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#EXTRA_DEFINITIONS:kotlin.String) for more detail on the structure of the returned data. 
Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_DICTIONARY_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLITERATION_RESULT:kotlin.Int), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) 

 Value: 2

### FLAG_PARTIAL_RESPONSES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_PARTIAL_RESPONSES: Int
```

Indicates this request is willing to accept partial responses.

The partial responses can be accessed by [TranslationResponse.getTranslationResponseValues()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getTranslationResponseValues()) or [TranslationResponse.getViewTranslationResponses()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getViewTranslationResponses()). These responses will each contain only a subset of the corresponding translated values.

The are no guarantees to the number of translated values or the order in which these values are returned in the [TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse).

This flag denotes the client can expect multiple partial responses, but there may not necessarily be multiple responses.

Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_DICTIONARY_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLITERATION_RESULT:kotlin.Int), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) 

 Value: 8

### FLAG_TRANSLATION_RESULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_TRANSLATION_RESULT: Int
```

Indicates this request wants to receive the standard translation result. 
Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_DICTIONARY_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLITERATION_RESULT:kotlin.Int), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) 

 Value: 1

### FLAG_TRANSLITERATION_RESULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_TRANSLITERATION_RESULT: Int
```

Indicates this request wants to receive the transliteration result.

This returns a CharSequence representation of the transliteration of the translated text. See [TranslationResponseValue.getTransliteration()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue#getTransliteration()). 
Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_DICTIONARY_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLITERATION_RESULT:kotlin.Int), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) 

 Value: 4

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Request flags. [FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int) by default.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLATION_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_DICTIONARY_RESULT:kotlin.Int), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_TRANSLITERATION_RESULT:kotlin.Int), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#FLAG_PARTIAL_RESPONSES:kotlin.Int) |

### getTranslationRequestValues

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTranslationRequestValues(): MutableList<TranslationRequestValue!>
```

List of [TranslationRequestValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequestValue) s to be translated. The index of entries in this list will be their respective key in the [android.util.SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#) returned by calling [TranslationResponse.getTranslationResponseValues()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getTranslationResponseValues()).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TranslationRequestValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequestValue)!> | This value cannot be `null`. |

### getViewTranslationRequests

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getViewTranslationRequests(): MutableList<ViewTranslationRequest!>
```

List of [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest) s to be translated. The index of entries in this list will be their respective key in the [android.util.SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#) returned by calling [TranslationResponse.getViewTranslationResponses()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getViewTranslationResponses()).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ViewTranslationRequest](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationRequest)!> | This value cannot be `null`. |

### toString

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TranslationRequest!>
```
