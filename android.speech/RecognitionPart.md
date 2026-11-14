# RecognitionPart

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognitionPart

Kotlin| [Java](https://developer.android.com/reference/android/speech/RecognitionPart "View this page in Java") 
| --- | --- |

```
class RecognitionPart : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.RecognitionPart](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#) |

Info about a single recognition part.

A recognition part represents a recognized word or character, as well as any potential adjacent punctuation, that is returned by the [SpeechRecognizer](https://developer.android.com/reference/kotlin/android/speech/SpeechRecognizer).

Each recognition part is described with a [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) denoting the raw text. Additionally, if formatting is enabled with [RecognizerIntent.EXTRA_ENABLE_FORMATTING](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_FORMATTING:kotlin.String), another [String](https://developer.android.com/reference/kotlin/java/lang/String.html#) representation exists denoting the formatted text.

If the timestamps are requested with [RecognizerIntent.EXTRA_REQUEST_WORD_TIMING](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_REQUEST_WORD_TIMING:kotlin.String), each recognition part will contain a value representing the offset of the beginning of this part from the start of the recognition session in milliseconds.

If the confidence levels are requested with [RecognizerIntent.EXTRA_REQUEST_WORD_CONFIDENCE](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_REQUEST_WORD_CONFIDENCE:kotlin.String), each recognition part will contain a value describing the level of recognition confidence.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart.Builder) A builder for [RecognitionPart](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#) |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_HIGH](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_HIGH:kotlin.Int) Highest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_LOW](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_LOW:kotlin.Int) Lowest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_MEDIUM](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_MEDIUM:kotlin.Int) Medium level of confidence out of five levels. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_MEDIUM_HIGH](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_HIGH:kotlin.Int) Second-highest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_MEDIUM_LOW](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_LOW:kotlin.Int) Second-lowest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_UNKNOWN:kotlin.Int) Confidence level not requested. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConfidenceLevel](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#getConfidenceLevel())`()` The level of confidence for this part if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_CONFIDENCE](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_REQUEST_WORD_CONFIDENCE:kotlin.String). |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFormattedText](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#getFormattedText())`()` The formatted text version of the recognized part of the result. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getRawText](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#getRawText())`()` The`non-null`raw text version of the recognized part of the result. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#getTimestampMillis())`()` Non-negative offset of the beginning of this part from the start of the recognition session in milliseconds if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_TIMING](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_REQUEST_WORD_TIMING:kotlin.String). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#hashCode())`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [RecognitionPart](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CREATOR:android.os.Parcelable.Creator) <br /> |

## Constants

### CONFIDENCE_LEVEL_HIGH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIDENCE_LEVEL_HIGH: Int
```

Highest level of confidence out of five levels. 

 Value: 5

### CONFIDENCE_LEVEL_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIDENCE_LEVEL_LOW: Int
```

Lowest level of confidence out of five levels. 

 Value: 1

### CONFIDENCE_LEVEL_MEDIUM

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIDENCE_LEVEL_MEDIUM: Int
```

Medium level of confidence out of five levels. 

 Value: 3

### CONFIDENCE_LEVEL_MEDIUM_HIGH

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIDENCE_LEVEL_MEDIUM_HIGH: Int
```

Second-highest level of confidence out of five levels. 

 Value: 4

### CONFIDENCE_LEVEL_MEDIUM_LOW

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIDENCE_LEVEL_MEDIUM_LOW: Int
```

Second-lowest level of confidence out of five levels. 

 Value: 2

### CONFIDENCE_LEVEL_UNKNOWN

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CONFIDENCE_LEVEL_UNKNOWN: Int
```

Confidence level not requested. 

 Value: 0

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
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

### getConfidenceLevel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfidenceLevel(): Int
```

The level of confidence for this part if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_CONFIDENCE](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_REQUEST_WORD_CONFIDENCE:kotlin.String).

Otherwise, this should equal [CONFIDENCE_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_UNKNOWN:kotlin.Int).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.speech.RecognitionPart#CONFIDENCE_LEVEL_UNKNOWN](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_UNKNOWN:kotlin.Int), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_LOW](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_LOW:kotlin.Int), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_LOW](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_LOW:kotlin.Int), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_MEDIUM](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_MEDIUM:kotlin.Int), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_HIGH](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_HIGH:kotlin.Int), or [android.speech.RecognitionPart#CONFIDENCE_LEVEL_HIGH](https://developer.android.com/reference/kotlin/android/speech/RecognitionPart#CONFIDENCE_LEVEL_HIGH:kotlin.Int) |

### getFormattedText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormattedText(): String?
```

The formatted text version of the recognized part of the result. If formatting is enabled with [RecognizerIntent.EXTRA_ENABLE_FORMATTING](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_ENABLE_FORMATTING:kotlin.String), it has a`non-null`value.

Otherwise, it should be`null`by default. 

### getRawText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRawText(): String
```

The`non-null`raw text version of the recognized part of the result. 

### getTimestampMillis

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTimestampMillis(): Long
```

Non-negative offset of the beginning of this part from the start of the recognition session in milliseconds if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_TIMING](https://developer.android.com/reference/kotlin/android/speech/RecognizerIntent#EXTRA_REQUEST_WORD_TIMING:kotlin.String).

Otherwise, this should equal 0. 

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### toString

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RecognitionPart!>
```
