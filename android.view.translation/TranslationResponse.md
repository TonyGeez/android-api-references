# TranslationResponse

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TranslationResponse

Kotlin| [Java](../android/view/translation/TranslationResponse.md) 
| --- | --- |

```
class TranslationResponse : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.translation.TranslationResponse](../android/view/translation/TranslationResponse.md) |

Response from the translation service, which contains the translated result.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/translation/TranslationResponse.Builder.md) A builder for [TranslationResponse](../android/view/translation/TranslationResponse.md) |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLATION_STATUS_CONTEXT_UNSUPPORTED](../android/view/translation/TranslationResponse.md) The languages of the request is not available to be translated. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLATION_STATUS_SUCCESS](../android/view/translation/TranslationResponse.md) The translation service was successful in translating. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [TRANSLATION_STATUS_UNKNOWN_ERROR](../android/view/translation/TranslationResponse.md) The translation service returned unknown translation result. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/translation/TranslationResponse.md))`()` <br /> |
| [SparseArray](../android/util/SparseArray.md)\< [TranslationResponseValue](../android/view/translation/TranslationResponseValue.md)!\> | [getTranslationResponseValues](../android/view/translation/TranslationResponse.md))`()` List of translated [TranslationResponseValue](../android/view/translation/TranslationResponseValue.md) s. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTranslationStatus](../android/view/translation/TranslationResponse.md))`()` The translation result status code. |
| --- | --- |
| [SparseArray](../android/util/SparseArray.md)\< [ViewTranslationResponse](../android/view/translation/ViewTranslationResponse.md)!\> | [getViewTranslationResponses](../android/view/translation/TranslationResponse.md))`()` List of translated [ViewTranslationResponse](../android/view/translation/ViewTranslationResponse.md) s. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [isFinalResponse](../android/view/translation/TranslationResponse.md))`()` Whether this response contains complete translated values, or is the final response in a series of partial responses. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/translation/TranslationResponse.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/translation/TranslationResponse.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TranslationResponse](../android/view/translation/TranslationResponse.md)!\> | [CREATOR](../android/view/translation/TranslationResponse.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getTranslationResponseValues

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTranslationResponseValues(): SparseArray<TranslationResponseValue!>
```

List of translated [TranslationResponseValue](../android/view/translation/TranslationResponseValue.md) s. The key of entries in this list will be their respective index in [TranslationRequest.getTranslationRequestValues()](../android/view/translation/TranslationRequest.md)).

| Return ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SparseArray](../android/util/SparseArray.md)< [TranslationResponseValue](../android/view/translation/TranslationResponseValue.md)!> | This value cannot be`null`. |

### getTranslationStatus

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTranslationStatus(): Int
```

The translation result status code.

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.translation.TranslationResponse#TRANSLATION_STATUS_SUCCESS](../android/view/translation/TranslationResponse.md), [android.view.translation.TranslationResponse#TRANSLATION_STATUS_UNKNOWN_ERROR](../android/view/translation/TranslationResponse.md), or [android.view.translation.TranslationResponse#TRANSLATION_STATUS_CONTEXT_UNSUPPORTED](../android/view/translation/TranslationResponse.md) |

### getViewTranslationResponses

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getViewTranslationResponses(): SparseArray<ViewTranslationResponse!>
```

List of translated [ViewTranslationResponse](../android/view/translation/ViewTranslationResponse.md) s. The key of entries in this list will be their respective index in [TranslationRequest.getViewTranslationRequests()](../android/view/translation/TranslationRequest.md)).

| Return ||
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [SparseArray](../android/util/SparseArray.md)< [ViewTranslationResponse](../android/view/translation/ViewTranslationResponse.md)!> | This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TranslationResponse!>
```
