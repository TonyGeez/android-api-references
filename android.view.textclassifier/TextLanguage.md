# TextLanguage

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextLanguage

Kotlin| [Java](TextLanguage.md) 
| --- | --- |

```
class TextLanguage : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextLanguage](TextLanguage.md) |

Represents the result of language detection of a piece of text.

This contains a list of locales, each paired with a confidence score, sorted in decreasing order of those scores. E.g., for a given input text, the model may return`[<"en", 0.85>, <"fr", 0.15>]`. This sample result means the model reports that it is 85% likely that the entire text is in English and 15% likely that the entire text is in French, etc. It does not mean that 85% of the input is in English and 15% is in French.

## Summary

| Nested classes ||
|---|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/textclassifier/TextLanguage.Builder.md) Builder used to build TextLanguage objects. |
| | [Request](../android/view/textclassifier/TextLanguage.Request.md) A request object for detecting the language of a piece of text. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](TextLanguage.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getConfidenceScore](TextLanguage.md))`(`locale:` ` [ULocale](../android.icu.util/ULocale.md)`)` Returns the confidence score for the specified language locale. |
| [Bundle](../android.os/Bundle.md) | [getExtras](TextLanguage.md))`()` Returns a bundle containing non-structured extra information about this result. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getId](TextLanguage.md))`()` Returns the id, if one exists, for this object. |
| [ULocale](../android.icu.util/ULocale.md) | [getLocale](TextLanguage.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the language locale at the specified index. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getLocaleHypothesisCount](TextLanguage.md))`()` Returns the number of possible locales for the processed text. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](TextLanguage.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](TextLanguage.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextLanguage](TextLanguage.md)!\> | [CREATOR](TextLanguage.md) <br /> |

## Public methods

### describeContents

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getConfidenceScore

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfidenceScore(locale: ULocale): Float
```

Returns the confidence score for the specified language locale. The value ranges from 0 (low confidence) to 1 (high confidence). 0 indicates that the locale was not found for the processed text.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------|
| `locale` | [ULocale](../android.icu.util/ULocale.md):This value cannot be`null`. |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and 1.0f inclusive |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle
```

Returns a bundle containing non-structured extra information about this result. What is returned in the extras is specific to the [TextClassifier](TextClassifier.md) implementation.

**NOTE:**Do not modify this bundle.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android.os/Bundle.md) | This value cannot be`null`. |

### getId

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String?
```

Returns the id, if one exists, for this object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getLocale

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocale(index: Int): ULocale
```

Returns the language locale at the specified index. Locales are ordered from high confidence to low confidence.

See [getLocaleHypothesisCount()](TextLanguage.md))for the number of locales available.

| Return ||
|------------------------------------------------------------------------------------------|-----------------------------|
| [ULocale](../android.icu.util/ULocale.md) | This value cannot be`null`. |

| Exceptions ||
|---------------------------------------|-----------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is out of range. |

### getLocaleHypothesisCount

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLocaleHypothesisCount(): Int
```

Returns the number of possible locales for the processed text.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### toString

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextLanguage!>
```
