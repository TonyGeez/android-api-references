# PdfPageLinkContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PdfPageLinkContent

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/content/PdfPageLinkContent "View this page in Java") 

```
class PdfPageLinkContent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.pdf.content.PdfPageLinkContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#) |

Represents the bounds and link on a page of the PDF document. Weblinks are those links implicitly embedded in PDF pages.**Note:** Only weblinks that are embedded will be supported. Links encoded as plain text will be returned as part of [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent).

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageLinkContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#PdfPageLinkContent(kotlin.collections.MutableList,%20android.net.Uri))`(`bounds:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!>`, `uri:` ` [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#)`)` Creates a new instance of [PdfPageLinkContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#) using the embedded [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) and the bounds of the uri. |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#describeContents())`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\> | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#getBounds())`()` Gets the bounds of the embedded weblink represented as a list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#). |
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | [getUri](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#getUri())`()` Gets the weblink on the page of the PDF document. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PdfPageLinkContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### PdfPageLinkContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfPageLinkContent(
    bounds: MutableList<RectF!>, 
    uri: Uri)
```

Creates a new instance of [PdfPageLinkContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageLinkContent#) using the embedded [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) and the bounds of the uri.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\>:Bounds which envelop the URI. This value cannot be`null`. |
| `uri` | [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#):Uri embedded in the PDF document. This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getBounds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getBounds(): MutableList<RectF!>
```

Gets the bounds of the embedded weblink represented as a list of [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#). Links which are spread across multiple lines will be surrounded by multiple [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) in order of viewing.

**Note:** Each [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) represents a bound of the weblink in a single line and defines the coordinates of its 4 edges (left, top, right and bottom) in points (1/72"). The developer will need to render the highlighter as well as intercept the touch events for functionalities such as clicking the link.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!> | The bounds of the link. This value cannot be`null`. |

### getUri

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getUri(): Uri
```

Gets the weblink on the page of the PDF document. Weblinks are those links implicitly embedded in PDF pages.**Note:** Only weblinks that are embedded will be supported. Links encoded as plain text will be returned as part of [PdfPageTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent).

| Return ||
|-----------------------------------------------------------------------------|---------------------------------------------------------------|
| [Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html#) | The weblink embedded on the page. This value cannot be`null`. |

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
static val CREATOR: Parcelable.Creator<PdfPageLinkContent!>
```
