# RecognitionPart

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# RecognitionPart

Kotlin| [Java](../android/speech/RecognitionPart.md) 
| --- | --- |

```
class RecognitionPart : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.speech.RecognitionPart](../android/speech/RecognitionPart.md) |

Info about a single recognition part.

A recognition part represents a recognized word or character, as well as any potential adjacent punctuation, that is returned by the [SpeechRecognizer](../android/speech/SpeechRecognizer.md).

Each recognition part is described with a [String](../java/lang/String.md) denoting the raw text. Additionally, if formatting is enabled with [RecognizerIntent.EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md), another [String](../java/lang/String.md) representation exists denoting the formatted text.

If the timestamps are requested with [RecognizerIntent.EXTRA_REQUEST_WORD_TIMING](../android/speech/RecognizerIntent.md), each recognition part will contain a value representing the offset of the beginning of this part from the start of the recognition session in milliseconds.

If the confidence levels are requested with [RecognizerIntent.EXTRA_REQUEST_WORD_CONFIDENCE](../android/speech/RecognizerIntent.md), each recognition part will contain a value describing the level of recognition confidence.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/speech/RecognitionPart.Builder.md) A builder for [RecognitionPart](../android/speech/RecognitionPart.md) |

| Constants ||
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_HIGH](../android/speech/RecognitionPart.md) Highest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_LOW](../android/speech/RecognitionPart.md) Lowest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_MEDIUM](../android/speech/RecognitionPart.md) Medium level of confidence out of five levels. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_MEDIUM_HIGH](../android/speech/RecognitionPart.md) Second-highest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_MEDIUM_LOW](../android/speech/RecognitionPart.md) Second-lowest level of confidence out of five levels. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONFIDENCE_LEVEL_UNKNOWN](../android/speech/RecognitionPart.md) Confidence level not requested. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/speech/RecognitionPart.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/speech/RecognitionPart.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` Indicates whether some other object is "equal to" this one. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getConfidenceLevel](../android/speech/RecognitionPart.md))`()` The level of confidence for this part if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_CONFIDENCE](../android/speech/RecognizerIntent.md). |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFormattedText](../android/speech/RecognitionPart.md))`()` The formatted text version of the recognized part of the result. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getRawText](../android/speech/RecognitionPart.md))`()` The`non-null`raw text version of the recognized part of the result. |
| [Long](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html) | [getTimestampMillis](../android/speech/RecognitionPart.md))`()` Non-negative offset of the beginning of this part from the start of the recognition session in milliseconds if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_TIMING](../android/speech/RecognizerIntent.md). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/speech/RecognitionPart.md))`()` <br /> |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/speech/RecognitionPart.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/speech/RecognitionPart.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [RecognitionPart](../android/speech/RecognitionPart.md)!\> | [CREATOR](../android/speech/RecognitionPart.md) <br /> |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

The level of confidence for this part if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_CONFIDENCE](../android/speech/RecognizerIntent.md).

Otherwise, this should equal [CONFIDENCE_LEVEL_UNKNOWN](../android/speech/RecognitionPart.md).

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.speech.RecognitionPart#CONFIDENCE_LEVEL_UNKNOWN](../android/speech/RecognitionPart.md), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_LOW](../android/speech/RecognitionPart.md), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_LOW](../android/speech/RecognitionPart.md), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_MEDIUM](../android/speech/RecognitionPart.md), [android.speech.RecognitionPart#CONFIDENCE_LEVEL_MEDIUM_HIGH](../android/speech/RecognitionPart.md), or [android.speech.RecognitionPart#CONFIDENCE_LEVEL_HIGH](../android/speech/RecognitionPart.md) |

### getFormattedText

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getFormattedText(): String?
```

The formatted text version of the recognized part of the result. If formatting is enabled with [RecognizerIntent.EXTRA_ENABLE_FORMATTING](../android/speech/RecognizerIntent.md), it has a`non-null`value.

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

Non-negative offset of the beginning of this part from the start of the recognition session in milliseconds if requested with [RecognizerIntent.EXTRA_REQUEST_WORD_TIMING](../android/speech/RecognizerIntent.md).

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<RecognitionPart!>
```
