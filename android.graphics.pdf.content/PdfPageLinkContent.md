# PdfPageLinkContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PdfPageLinkContent

Kotlin| [Java](PdfPageLinkContent.md) 
| --- | --- |

```
class PdfPageLinkContent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.content.PdfPageLinkContent](PdfPageLinkContent.md) |

Represents the bounds and link on a page of the PDF document. Weblinks are those links implicitly embedded in PDF pages.**Note:** Only weblinks that are embedded will be supported. Links encoded as plain text will be returned as part of [PdfPageTextContent](PdfPageTextContent.md).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageLinkContent](PdfPageLinkContent.md))`(`bounds:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](../android.graphics/RectF.md)!>`, `uri:` ` [Uri](../android.net/Uri.md)`)` Creates a new instance of [PdfPageLinkContent](PdfPageLinkContent.md) using the embedded [Uri](../android.net/Uri.md) and the bounds of the uri. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](PdfPageLinkContent.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android.graphics/RectF.md)!\> | [getBounds](PdfPageLinkContent.md))`()` Gets the bounds of the embedded weblink represented as a list of [RectF](../android.graphics/RectF.md). |
| [Uri](../android.net/Uri.md) | [getUri](PdfPageLinkContent.md))`()` Gets the weblink on the page of the PDF document. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](PdfPageLinkContent.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PdfPageLinkContent](PdfPageLinkContent.md)!\> | [CREATOR](PdfPageLinkContent.md) <br /> |

## Public constructors

### PdfPageLinkContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfPageLinkContent(
    bounds: MutableList<RectF!>, 
    uri: Uri)
```

Creates a new instance of [PdfPageLinkContent](PdfPageLinkContent.md) using the embedded [Uri](../android.net/Uri.md) and the bounds of the uri.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android.graphics/RectF.md)!\>:Bounds which envelop the URI. This value cannot be`null`. |
| `uri` | [Uri](../android.net/Uri.md):Uri embedded in the PDF document. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------|
| `java.lang.NullPointerException` | If bounds or uri is null. |
| `java.lang.IllegalArgumentException` | If the bounds list is empty. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### getBounds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getBounds(): MutableList<RectF!>
```

Gets the bounds of the embedded weblink represented as a list of [RectF](../android.graphics/RectF.md). Links which are spread across multiple lines will be surrounded by multiple [RectF](../android.graphics/RectF.md) in order of viewing.

**Note:** Each [RectF](../android.graphics/RectF.md) represents a bound of the weblink in a single line and defines the coordinates of its 4 edges (left, top, right and bottom) in points (1/72"). The developer will need to render the highlighter as well as intercept the touch events for functionalities such as clicking the link.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](../android.graphics/RectF.md)!> | The bounds of the link. This value cannot be`null`. |

### getUri

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getUri(): Uri
```

Gets the weblink on the page of the PDF document. Weblinks are those links implicitly embedded in PDF pages.**Note:** Only weblinks that are embedded will be supported. Links encoded as plain text will be returned as part of [PdfPageTextContent](PdfPageTextContent.md).

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](../android.net/Uri.md) | The weblink embedded on the page. This value cannot be`null`. |

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
| `dest` | [Parcel](../android.os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<PdfPageLinkContent!>
```
