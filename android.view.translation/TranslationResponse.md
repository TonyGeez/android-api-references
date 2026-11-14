# TranslationResponse

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationResponse

Kotlin| [Java](https://developer.android.com/reference/android/view/translation/TranslationResponse "View this page in Java") 

```
class TranslationResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.view.translation.TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#) |

Response from the translation service, which contains the translated result.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse.Builder) A builder for [TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#) |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLATION_STATUS_CONTEXT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#TRANSLATION_STATUS_CONTEXT_UNSUPPORTED:kotlin.Int) The languages of the request is not available to be translated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLATION_STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#TRANSLATION_STATUS_SUCCESS:kotlin.Int) The translation service was successful in translating. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLATION_STATUS_UNKNOWN_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#TRANSLATION_STATUS_UNKNOWN_ERROR:kotlin.Int) The translation service returned unknown translation result. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#describeContents())`()` <br /> |
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue)!\> | [getTranslationResponseValues](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getTranslationResponseValues())`()` List of translated [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue) s. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTranslationStatus](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getTranslationStatus())`()` The translation result status code. |
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)\< [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse)!\> | [getViewTranslationResponses](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#getViewTranslationResponses())`()` List of translated [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse) s. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinalResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#isFinalResponse())`()` Whether this response contains complete translated values, or is the final response in a series of partial responses. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### TRANSLATION_STATUS_CONTEXT_UNSUPPORTED

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSLATION_STATUS_CONTEXT_UNSUPPORTED: Int
```

The languages of the request is not available to be translated. 

 Value: 2

### TRANSLATION_STATUS_SUCCESS

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSLATION_STATUS_SUCCESS: Int
```

The translation service was successful in translating. 

 Value: 0

### TRANSLATION_STATUS_UNKNOWN_ERROR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val TRANSLATION_STATUS_UNKNOWN_ERROR: Int
```

The translation service returned unknown translation result. 

 Value: 1

## Public methods

### describeContents

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getTranslationResponseValues

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTranslationResponseValues(): SparseArray<TranslationResponseValue!>
```

List of translated [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue) s. The key of entries in this list will be their respective index in [TranslationRequest.getTranslationRequestValues()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#getTranslationRequestValues()).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)< [TranslationResponseValue](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponseValue)!> | This value cannot be`null`. |

### getTranslationStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTranslationStatus(): Int
```

The translation result status code.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.translation.TranslationResponse#TRANSLATION_STATUS_SUCCESS](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#TRANSLATION_STATUS_SUCCESS:kotlin.Int), [android.view.translation.TranslationResponse#TRANSLATION_STATUS_UNKNOWN_ERROR](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#TRANSLATION_STATUS_UNKNOWN_ERROR:kotlin.Int), or [android.view.translation.TranslationResponse#TRANSLATION_STATUS_CONTEXT_UNSUPPORTED](https://developer.android.com/reference/kotlin/android/view/translation/TranslationResponse#TRANSLATION_STATUS_CONTEXT_UNSUPPORTED:kotlin.Int) |

### getViewTranslationResponses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getViewTranslationResponses(): SparseArray<ViewTranslationResponse!>
```

List of translated [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse) s. The key of entries in this list will be their respective index in [TranslationRequest.getViewTranslationRequests()](https://developer.android.com/reference/kotlin/android/view/translation/TranslationRequest#getViewTranslationRequests()).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SparseArray](https://developer.android.com/reference/kotlin/android/util/SparseArray.html#)< [ViewTranslationResponse](https://developer.android.com/reference/kotlin/android/view/translation/ViewTranslationResponse)!> | This value cannot be`null`. |

### isFinalResponse

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun isFinalResponse(): Boolean
```

Whether this response contains complete translated values, or is the final response in a series of partial responses.

This is`true`by default. 

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
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TranslationResponse!>
```
