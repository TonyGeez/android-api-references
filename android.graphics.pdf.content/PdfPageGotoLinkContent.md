# PdfPageGotoLinkContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PdfPageGotoLinkContent

Kotlin| [Java](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) 
| --- | --- |

```
class PdfPageGotoLinkContent : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.content.PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) |

Represents the content associated with a goto link on a page in the PDF document. Goto Link is an internal navigation link which directs the user to a different location within the same pdf document

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md) Represents the content associated with the destination where a goto link is directing |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md))`(`bounds:` ` [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](../android/graphics/RectF.md)!>`, `destination:` ` [PdfPageGotoLinkContent.Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md)`)` Creates a new instance of [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) using the bounds of the goto link and the destination where it is directing |

| Public methods ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/graphics/pdf/content/PdfPageGotoLinkContent.md))`()` <br /> |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android/graphics/RectF.md)!\> | [getBounds](../android/graphics/pdf/content/PdfPageGotoLinkContent.md))`()` Gets the bounds of a [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) represented as a list of [RectF](../android/graphics/RectF.md). |
| [PdfPageGotoLinkContent.Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md) | [getDestination](../android/graphics/pdf/content/PdfPageGotoLinkContent.md))`()` Gets the destination [Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md) of the [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md). |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/graphics/pdf/content/PdfPageGotoLinkContent.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md)!\> | [CREATOR](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) <br /> |

## Public constructors

### PdfPageGotoLinkContent

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
PdfPageGotoLinkContent(
    bounds: MutableList<RectF!>, 
    destination: PdfPageGotoLinkContent.Destination)
```

Creates a new instance of [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) using the bounds of the goto link and the destination where it is directing

| Parameters ||
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android/graphics/RectF.md)!\>:Bounds which envelop the goto link This value cannot be`null`. |
| `destination` | [PdfPageGotoLinkContent.Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md):Destination where the goto link is directing This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|-----------------------------------|
| `java.lang.NullPointerException` | If bounds or destination is null. |
| `java.lang.IllegalArgumentException` | If the bounds list is empty. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getBounds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getBounds(): MutableList<RectF!>
```

Gets the bounds of a [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md) represented as a list of [RectF](../android/graphics/RectF.md). Links which are spread across multiple lines will be surrounded by multiple [RectF](../android/graphics/RectF.md) in order of viewing.

**Note:** Each [RectF](../android/graphics/RectF.md) represents a bound of the goto link in a single line and defines the coordinates of its 4 edges (left, top, right and bottom) in points (1/72"). The developer will need to render the highlighter as well as intercept the touch events for functionalities such as clicking the link.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)< [RectF](../android/graphics/RectF.md)!> | The bounds of the goto link. This value cannot be`null`. |

### getDestination

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getDestination(): PdfPageGotoLinkContent.Destination
```

Gets the destination [Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md) of the [PdfPageGotoLinkContent](../android/graphics/pdf/content/PdfPageGotoLinkContent.md).

| Return ||
|------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [PdfPageGotoLinkContent.Destination](../android/graphics/pdf/content/PdfPageGotoLinkContent.Destination.md) | Destination where goto link is directing the user. This value cannot be`null`. |

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
| `dest` | [Parcel](../android/os/Parcel.md):This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). Value is either`0`or a combination of [android.os.Parcelable#PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md), and android.os.Parcelable.PARCELABLE_ELIDE_DUPLICATES |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
static val CREATOR: Parcelable.Creator<PdfPageGotoLinkContent!>
```
