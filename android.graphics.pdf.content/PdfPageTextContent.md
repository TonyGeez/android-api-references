# PdfPageTextContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PdfPageTextContent

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/content/PdfPageTextContent "View this page in Java") 
| --- | --- |

```
class PdfPageTextContent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.content.PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#) |

Represents a continuous stream of text in a page of a PDF document in the order of viewing.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#PdfPageTextContent(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a new instance of [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#) using the raw text on the page of the document. |
| [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#PdfPageTextContent(kotlin.String,%20kotlin.collections.MutableList))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `bounds:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!>`)` Creates a new instance of [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#) to represent text content within defined bounds represented by a non-empty list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) on the page of the document. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\> | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#getBounds())`()` Gets the bounds for the text content represented as a list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#). |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getText](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#getText())`()` Gets the text content on the document. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### PdfPageTextContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfPageTextContent(text: String)
```

Creates a new instance of [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#) using the raw text on the page of the document. By default, the bounds will be an empty list.

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Text content on the page. This value cannot be`null`. |

| Exceptions ||
|----------------------------------|------------------|
| `java.lang.NullPointerException` | If text is null. |

### PdfPageTextContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfPageTextContent(
    text: String, 
    bounds: MutableList<RectF!>)
```

Creates a new instance of [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent#) to represent text content within defined bounds represented by a non-empty list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) on the page of the document.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):Text content within the bounds. This value cannot be`null`. |
| `bounds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\>:Bounds for the text content This value cannot be`null`. |

| Exceptions ||
|----------------------------------|----------------------------|
| `java.lang.NullPointerException` | If text or bounds is null. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBounds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getBounds(): MutableList<RectF!>
```

Gets the bounds for the text content represented as a list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#). Each [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) represents text content in a single line defined in points (1/72") for its 4 corners. Content spread across multiple lines is represented by list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) in the order of viewing (left to right and top to bottom). If the text content is unbounded then the list will be empty.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!> | The bounds of the text content. This value cannot be`null`. |

### getText

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getText(): String
```

Gets the text content on the document.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The text content on the page. This value cannot be`null`. |

### writeToParcel

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

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

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<PdfPageTextContent!>
```
