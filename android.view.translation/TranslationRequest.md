# TranslationRequest

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationRequest

Kotlin | [Java](../android/view/translation/TranslationRequest.md) 
| --- | --- |

```
class TranslationRequest : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.TranslationRequest](../android/view/translation/TranslationRequest.md) |

Translation request sent to the translation service by the [android.view.translation.Translator](../android/view/translation/Translator.md) which contains the text to be translated.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/translation/TranslationRequest.Builder.md) A builder for [TranslationRequest](../android/view/translation/TranslationRequest.md) |

| Constants ||
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_DICTIONARY_RESULT](../android/view/translation/TranslationRequest.md) Indicates this request wants to receive the dictionary result. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) Indicates this request is willing to accept partial responses. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md) Indicates this request wants to receive the standard translation result. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_TRANSLITERATION_RESULT](../android/view/translation/TranslationRequest.md) Indicates this request wants to receive the transliteration result. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/translation/TranslationRequest.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFlags](../android/view/translation/TranslationRequest.md))`()` Request flags. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [TranslationRequestValue](../android/view/translation/TranslationRequestValue.md)!\> | [getTranslationRequestValues](../android/view/translation/TranslationRequest.md))`()` List of [TranslationRequestValue](../android/view/translation/TranslationRequestValue.md) s to be translated. |
| --- | --- |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [ViewTranslationRequest](../android/view/translation/ViewTranslationRequest.md)!\> | [getViewTranslationRequests](../android/view/translation/TranslationRequest.md))`()` List of [ViewTranslationRequest](../android/view/translation/ViewTranslationRequest.md) s to be translated. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/translation/TranslationRequest.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/translation/TranslationRequest.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TranslationRequest](../android/view/translation/TranslationRequest.md)!\> | [CREATOR](../android/view/translation/TranslationRequest.md) <br /> |

## Constants

### FLAG_DICTIONARY_RESULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_DICTIONARY_RESULT: Int
```

Indicates this request wants to receive the dictionary result.

See [TranslationResponseValue.EXTRA_DEFINITIONS](../android/view/translation/TranslationResponseValue.md) for more detail on the structure of the returned data. 
Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](../android/view/translation/TranslationRequest.md), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) 

 Value: 2

### FLAG_PARTIAL_RESPONSES

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_PARTIAL_RESPONSES: Int
```

Indicates this request is willing to accept partial responses.

The partial responses can be accessed by [TranslationResponse.getTranslationResponseValues()](../android/view/translation/TranslationResponse.md)) or [TranslationResponse.getViewTranslationResponses()](../android/view/translation/TranslationResponse.md)). These responses will each contain only a subset of the corresponding translated values.

The are no guarantees to the number of translated values or the order in which these values are returned in the [TranslationResponse](../android/view/translation/TranslationResponse.md).

This flag denotes the client can expect multiple partial responses, but there may not necessarily be multiple responses.

Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](../android/view/translation/TranslationRequest.md), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) 

 Value: 8

### FLAG_TRANSLATION_RESULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_TRANSLATION_RESULT: Int
```

Indicates this request wants to receive the standard translation result. 
Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](../android/view/translation/TranslationRequest.md), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) 

 Value: 1

### FLAG_TRANSLITERATION_RESULT

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_TRANSLITERATION_RESULT: Int
```

Indicates this request wants to receive the transliteration result.

This returns a CharSequence representation of the transliteration of the translated text. See [TranslationResponseValue.getTransliteration()](../android/view/translation/TranslationResponseValue.md)). 
Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](../android/view/translation/TranslationRequest.md), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) 

 Value: 4

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getFlags

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFlags(): Int
```

Request flags. [FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md) by default.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is either `0` or a combination of [android.view.translation.TranslationRequest#FLAG_TRANSLATION_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_DICTIONARY_RESULT](../android/view/translation/TranslationRequest.md), [android.view.translation.TranslationRequest#FLAG_TRANSLITERATION_RESULT](../android/view/translation/TranslationRequest.md), and [android.view.translation.TranslationRequest#FLAG_PARTIAL_RESPONSES](../android/view/translation/TranslationRequest.md) |

### getTranslationRequestValues

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTranslationRequestValues(): MutableList<TranslationRequestValue!>
```

List of [TranslationRequestValue](../android/view/translation/TranslationRequestValue.md) s to be translated. The index of entries in this list will be their respective key in the [android.util.SparseArray](../android/util/SparseArray.md) returned by calling [TranslationResponse.getTranslationResponseValues()](../android/view/translation/TranslationResponse.md)).

| Return ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [TranslationRequestValue](../android/view/translation/TranslationRequestValue.md)!> | This value cannot be `null`. |

### getViewTranslationRequests

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getViewTranslationRequests(): MutableList<ViewTranslationRequest!>
```

List of [ViewTranslationRequest](../android/view/translation/ViewTranslationRequest.md) s to be translated. The index of entries in this list will be their respective key in the [android.util.SparseArray](../android/util/SparseArray.md) returned by calling [TranslationResponse.getViewTranslationResponses()](../android/view/translation/TranslationResponse.md)).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [ViewTranslationRequest](../android/view/translation/ViewTranslationRequest.md)!> | This value cannot be `null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either `0` or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TranslationRequest!>
```
