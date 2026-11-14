Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# PageMatchBounds

Kotlin | [Java](https://developer.android.com/reference/android/graphics/pdf/models/PageMatchBounds "View this page in Java")
| --- | --- |

```
class PageMatchBounds : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.models.PageMatchBounds](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#) |

Represents the bounds of a single search match on a page of the PDF document.

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#PageMatchBounds(kotlin.collections.MutableList,%20kotlin.Int)(bounds: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/RectF.html#!>, textStartIndex: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Creates a new instance of `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#` for the text match found on the page. |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\> | `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#getBounds()()` Represents the `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` bounds of a match. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#getTextStartIndex()()` Gets the starting index of the match found on the page. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Flatten this object in to a Parcel. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [PageMatchBounds](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#)!\> | `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#CREATOR:android.os.Parcelable.Creator` <br /> |

## Public constructors

### PageMatchBounds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
PageMatchBounds(
    bounds: MutableList<RectF!>, 
    textStartIndex: Int)
```

Creates a new instance of `https://developer.android.com/reference/kotlin/android/graphics/pdf/models/PageMatchBounds#` for the text match found on the page. The match is represented by bounds of the text match and the starting index of the character "stream" (0-based index).

| Parameters ||
|---|---|
| `bounds` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\>: Bounds of the text match. This value cannot be `null`. |
| `textStartIndex` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): starting index of the text match. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | If bounds list is empty or if the text starting index is negative. |
| `java.lang.NullPointerException` | If bounds if null. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### getBounds

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getBounds(): MutableList<RectF!>
```

Represents the `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` bounds of a match. Matches which are spread across multiple lines will be represented by multiple `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` in order of viewing.

**Note:** The bounds only represent the coordinates of the bounds of a single line using `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`. The developer will need to render the highlighter as well as intercept the touch events for any additional UI interactions.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/RectF.html#!>` | list of bounds for the match on the page. This value cannot be `null`. |

### getTextStartIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
fun getTextStartIndex(): Int
```

Gets the starting index of the match found on the page. Characters in a page form a "stream" and inside the stream, each character has an index starting from 0.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the starting index of the match on the page. |

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
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Additional flags about how the object should be written. May be 0 or `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int`. Value is either `0` or a combination of the following: - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` |

## Properties

### CREATOR

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

```
static val CREATOR: Parcelable.Creator<PageMatchBounds!>
```
