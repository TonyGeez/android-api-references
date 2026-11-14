Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PageSelection

Kotlin | [Java](PageSelection.md)
| --- | --- |

```
class PageSelection : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.models.selection.PageSelection](PageSelection.md) |

Represents the list of selected content on a particular page of the PDF document. By default, the selection boundary is represented from left to right. **Note:**Currently supports text selection only.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with describeContents: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with writeToParcel: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| PageSelection Creates a new instance of PageSelection for the specified page, the start and stop selection boundary, and the selected text content. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | describeContents Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getPage Gets the particular page for which the selection is highlighted. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PdfPageTextContent](../android.graphics.pdf.content/PdfPageTextContent.md)!\> | getSelectedTextContents Returns the text content within the selection boundaries on the page. |
| --- | --- |
| [SelectionBoundary](SelectionBoundary.md) | getStart Gets the edge from where the selection starts- index is inclusive. |
| [SelectionBoundary](SelectionBoundary.md) | getStop Gets the edge where the selection stops - index is inclusive. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | writeToParcel Flatten this object in to a Parcel. |
| --- | --- |

| Properties ||
|---|---|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [PageSelection](PageSelection.md)!\> | `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/PageSelection#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### PageSelection

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
PageSelection(
    page: Int, 
    start: SelectionBoundary, 
    stop: SelectionBoundary, 
    selectedContents: MutableList<PdfPageTextContent!>)
```

Creates a new instance of PageSelection for the specified page, the start and stop selection boundary, and the selected text content.

| Parameters ||
|---|---|
| `page` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The page number of the selection. |
| `start` | [SelectionBoundary](SelectionBoundary.md): Boundary where the selection starts. This value cannot be `null`. |
| `stop` | [SelectionBoundary](SelectionBoundary.md): Boundary where the selection stops. This value cannot be `null`. |
| --- | --- |
| `selectedContents` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [PdfPageTextContent](../android.graphics.pdf.content/PdfPageTextContent.md)!\>: list of segments of selected text content. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If the page number is negative. |
| `java.lang.NullPointerException` | If start/stop edge or text selection is null. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of writeToParcel, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getPage

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getPage(): Int
```

Gets the particular page for which the selection is highlighted.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The page number on which the current selection resides. |

### getSelectedTextContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getSelectedTextContents(): MutableList<PdfPageTextContent!>
```

Returns the text content within the selection boundaries on the page. In case there are non-continuous selections, this method returns the list of those text content in order of viewing.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent.html#!>` | list of text contents within the selection boundaries. This value cannot be `null`. |

### getStart

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getStart(): SelectionBoundary
```

Gets the edge from where the selection starts- index is inclusive.

| Return ||
|---|---|
| SelectionBoundary | The starting edge of the selection. This value cannot be `null`. |

### getStop

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getStop(): SelectionBoundary
```

Gets the edge where the selection stops - index is inclusive.

| Return ||
|---|---|
| SelectionBoundary | The stopping edge of the selection. This value cannot be `null`. |

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
|---|---|
| `dest` | [Parcel](../android.os/Parcel.md): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<PageSelection!>
```
