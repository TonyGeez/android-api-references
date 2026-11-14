# TextSelection

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextSelection

Kotlin| [Java](https://developer.android.com/reference/android/view/textclassifier/TextSelection "View this page in Java") 
| --- | --- |

```
class TextSelection : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.textclassifier.TextSelection](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#) |

Information about where text selection should be.

## Summary

| Nested classes ||
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection.Builder) Builder used to build [TextSelection](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#) objects. |
| | [Request](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection.Request) A request object for generating TextSelection. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#describeContents())`()` <br /> |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getConfidenceScore](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getConfidenceScore(kotlin.String))`(`entity:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!`)` Returns the confidence score for the specified entity. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getEntity](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getEntity(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the entity at the specified index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEntityCount](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getEntityCount())`()` Returns the number of entities found in the classified text. |
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | [getExtras](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getExtras())`()` Returns the extended data. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getId](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getId())`()` Returns the id, if one exists, for this object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectionEndIndex](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getSelectionEndIndex())`()` Returns the end index of the text selection. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSelectionStartIndex](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getSelectionStartIndex())`()` Returns the start index of the text selection. |
| [TextClassification](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassification)? | [getTextClassification](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#getTextClassification())`()` Returns the text classification result of the suggested selection span. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [toString](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#toString())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` <br /> |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TextSelection](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public methods

### describeContents

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getConfidenceScore

Added in [API level 26](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getConfidenceScore(entity: String!): Float
```

Returns the confidence score for the specified entity. The value ranges from 0 (low confidence) to 1 (high confidence). 0 indicates that the entity was not found for the classified text.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `entity` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)!:Value is [android.view.textclassifier.TextClassifier#TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_UNKNOWN:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_OTHER](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTHER:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_EMAIL](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_PHONE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_PHONE:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_ADDRESS](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_URL](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_URL:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_DATE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_DATE_TIME](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE_TIME:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_FLIGHT_NUMBER](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_FLIGHT_NUMBER:kotlin.String), android.view.textclassifier.TextClassifier.TYPE_DICTIONARY, [android.view.textclassifier.TextClassifier#TYPE_OTP](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTP:kotlin.String), or [android.view.textclassifier.TextClassifier#TYPE_SMS_RETRIEVER_OTP](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_RETRIEVER_OTP:kotlin.String) |

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
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | This value cannot be`null`. Value is [android.view.textclassifier.TextClassifier#TYPE_UNKNOWN](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_UNKNOWN:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_OTHER](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTHER:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_EMAIL](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_EMAIL:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_PHONE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_PHONE:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_ADDRESS](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_ADDRESS:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_URL](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_URL:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_DATE](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_DATE_TIME](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_DATE_TIME:kotlin.String), [android.view.textclassifier.TextClassifier#TYPE_FLIGHT_NUMBER](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_FLIGHT_NUMBER:kotlin.String), android.view.textclassifier.TextClassifier.TYPE_DICTIONARY, [android.view.textclassifier.TextClassifier#TYPE_OTP](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_OTP:kotlin.String), or [android.view.textclassifier.TextClassifier#TYPE_SMS_RETRIEVER_OTP](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextClassifier#TYPE_SMS_RETRIEVER_OTP:kotlin.String) |

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
| [Bundle](https://developer.android.com/reference/kotlin/android/os/Bundle.html#) | This value cannot be`null`. |

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

Returns the text classification result of the suggested selection span. Enables the text classification by calling [TextSelection.Request.Builder.setIncludeTextClassification(boolean)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection.Request.Builder#setIncludeTextClassification(kotlin.Boolean)). If the text classifier does not support it, a`null`is returned. 
**See Also**

- [android.view.textclassifier.TextSelection.Request.Builder#setIncludeTextClassification(boolean)](https://developer.android.com/reference/kotlin/android/view/textclassifier/TextSelection.Request.Builder#setIncludeTextClassification(kotlin.Boolean)) 

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 28](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextSelection!>
```
