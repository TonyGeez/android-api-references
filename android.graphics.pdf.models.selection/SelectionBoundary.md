# SelectionBoundary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# SelectionBoundary

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/models/selection/SelectionBoundary "View this page in Java") 
| --- | --- |

```
class SelectionBoundary : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.models.selection.SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#) |

Represents one edge of the selected content.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#SelectionBoundary(android.graphics.Point))`(`point:` ` [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)`)` Create a new instance of [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#) if the boundary [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) is known. |
| [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#SelectionBoundary(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new instance of [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#) if index of boundary is known. |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#describeContents())`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#getIndex())`()` Gets the index of the text as determined by the text stream processed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getIsRtl](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#getIsRtl())`()` Gets whether the direction of selection is right-to-left (rtl) or reverse. |
| --- | --- |
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)? | [getPoint](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#getPoint())`()` Gets the x, y coordinates of the selection boundary in points (1/72"). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#CREATOR:android.os.Parcelable.Creator) <br /> |

## Public constructors

### SelectionBoundary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
SelectionBoundary(point: Point)
```

Create a new instance of [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#) if the boundary [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#) is known. Index defaults to -1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `point` | [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#):The point of selection boundary. This value cannot be`null`. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | If the point is null. |

### SelectionBoundary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
SelectionBoundary(index: Int)
```

Create a new instance of [SelectionBoundary](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#) if index of boundary is known. The text returned by [PdfPageTextContent.getText()](https://developer.android.com/reference/kotlin/android/graphics/pdf/content/PdfPageTextContent.html#getText())form a "stream" and inside this "stream" each character has an index.**Note:** Point defaults to`null`in this case.

| Parameters ||
|---------|-------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):index of the selection boundary. |

| Exceptions ||
|--------------------------------------|---------------------------|
| `java.lang.IllegalArgumentException` | If the index is negative. |

## Public methods

### describeContents

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### getIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getIndex(): Int
```

Gets the index of the text as determined by the text stream processed. If the value is -1 then the [getPoint()](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#getPoint())will determine the selection boundary.

| Return ||
|----------------------------------------------------------------------------|----------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | index of the selection boundary. |

### getIsRtl

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getIsRtl(): Boolean
```

Gets whether the direction of selection is right-to-left (rtl) or reverse. The value of isRtl is determined by the underlying native layer using the start and stop boundaries.

| Return ||
|------------------------------------------------------------------------------------|----------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | The direction of selection |

### getPoint

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getPoint(): Point?
```

Gets the x, y coordinates of the selection boundary in points (1/72"). These coordinates are represented by a [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#). If the value is`null`then the [getIndex()](https://developer.android.com/reference/kotlin/android/graphics/pdf/models/selection/SelectionBoundary#getIndex())will determine the selection boundary.

**Note:**Point (0,0) represents the top-left corner of the page

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------|
| [Point](https://developer.android.com/reference/kotlin/android/graphics/Point.html#)? | The point of the selection boundary. |

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
static val CREATOR: Parcelable.Creator<SelectionBoundary!>
```
