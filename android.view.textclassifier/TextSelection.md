# TextSelection

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextSelection

Kotlin| [Java](../android/view/textclassifier/TextSelection.md) 
| --- | --- |

```
class TextSelection : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextSelection](../android/view/textclassifier/TextSelection.md) |

Information about where text selection should be.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/textclassifier/TextSelection.Builder.md) Builder used to build [TextSelection](../android/view/textclassifier/TextSelection.md) objects. |
| | [Request](../android/view/textclassifier/TextSelection.Request.md) A request object for generating TextSelection. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/textclassifier/TextSelection.md))`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getConfidenceScore](../android/view/textclassifier/TextSelection.md))`(`entity:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the confidence score for the specified entity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getEntity](../android/view/textclassifier/TextSelection.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the entity at the specified index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEntityCount](../android/view/textclassifier/TextSelection.md))`()` Returns the number of entities found in the classified text. |
| [Bundle](../android/os/Bundle.md) | [getExtras](../android/view/textclassifier/TextSelection.md))`()` Returns the extended data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getId](../android/view/textclassifier/TextSelection.md))`()` Returns the id, if one exists, for this object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectionEndIndex](../android/view/textclassifier/TextSelection.md))`()` Returns the end index of the text selection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectionStartIndex](../android/view/textclassifier/TextSelection.md))`()` Returns the start index of the text selection. |
| [TextClassification](../android/view/textclassifier/TextClassification.md)? | [getTextClassification](../android/view/textclassifier/TextSelection.md))`()` Returns the text classification result of the suggested selection span. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](../android/view/textclassifier/TextSelection.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/textclassifier/TextSelection.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextSelection](../android/view/textclassifier/TextSelection.md)!\> | [CREATOR](../android/view/textclassifier/TextSelection.md) <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getConfidenceScore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfidenceScore(entity: String!): Float
```

Returns the confidence score for the specified entity. The value ranges from 0 (low confidence) to 1 (high confidence). 0 indicates that the entity was not found for the classified text.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `entity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Value is [android.view.textclassifier.TextClassifier#TYPE_UNKNOWN](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_OTHER](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_EMAIL](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_PHONE](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_ADDRESS](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_URL](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_DATE](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_DATE_TIME](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_FLIGHT_NUMBER](../android/view/textclassifier/TextClassifier.md), android.view.textclassifier.TextClassifier.TYPE_DICTIONARY, [android.view.textclassifier.TextClassifier#TYPE_OTP](../android/view/textclassifier/TextClassifier.md), or [android.view.textclassifier.TextClassifier#TYPE_SMS_RETRIEVER_OTP](../android/view/textclassifier/TextClassifier.md) |

| Return ||
|--------------------------------------------------------------------------------|------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is between 0.0f and 1.0f inclusive |

### getEntity

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEntity(index: Int): String
```

Returns the entity at the specified index. Entities are ordered from high confidence to low confidence.

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. Value is [android.view.textclassifier.TextClassifier#TYPE_UNKNOWN](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_OTHER](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_EMAIL](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_PHONE](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_ADDRESS](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_URL](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_DATE](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_DATE_TIME](../android/view/textclassifier/TextClassifier.md), [android.view.textclassifier.TextClassifier#TYPE_FLIGHT_NUMBER](../android/view/textclassifier/TextClassifier.md), android.view.textclassifier.TextClassifier.TYPE_DICTIONARY, [android.view.textclassifier.TextClassifier#TYPE_OTP](../android/view/textclassifier/TextClassifier.md), or [android.view.textclassifier.TextClassifier#TYPE_SMS_RETRIEVER_OTP](../android/view/textclassifier/TextClassifier.md) |

| Exceptions ||
|---------------------------------------|-----------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the specified index is out of range. |

**See Also**

- <https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getEntityCount()> 

### getEntityCount

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEntityCount(): Int
```

Returns the number of entities found in the classified text.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is 0 or greater |

### getExtras

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getExtras(): Bundle
```

Returns the extended data.

**NOTE:**Do not modify this bundle.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------|
| [Bundle](../android/os/Bundle.md) | This value cannot be`null`. |

### getId

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getId(): String?
```

Returns the id, if one exists, for this object.

| Return ||
|-----------------------------------------------------------------------------------|--------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | This value may be`null`. |

### getSelectionEndIndex

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectionEndIndex(): Int
```

Returns the end index of the text selection. 

### getSelectionStartIndex

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectionStartIndex(): Int
```

Returns the start index of the text selection. 

### getTextClassification

Added in [API level 31](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getTextClassification(): TextClassification?
```

Returns the text classification result of the suggested selection span. Enables the text classification by calling [TextSelection.Request.Builder.setIncludeTextClassification(boolean)](../android/view/textclassifier/TextSelection.Request.Builder.md)). If the text classifier does not support it, a`null`is returned. 
**See Also**

- [android.view.textclassifier.TextSelection.Request.Builder#setIncludeTextClassification(boolean)](../android/view/textclassifier/TextSelection.Request.Builder.md)) 

### toString

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun toString(): String
```

| Return ||
|----------------------------------------------------------------------------------|----------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | a string representation of the object. |

### writeToParcel

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextSelection!>
```
