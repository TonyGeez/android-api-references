# SelectionBoundary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions)

# SelectionBoundary

Kotlin| [Java](../android/graphics/pdf/models/selection/SelectionBoundary.md) 
| --- | --- |

```
class SelectionBoundary : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.models.selection.SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md) |

Represents one edge of the selected content.

## Summary

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md))`(`point:` ` [Point](../android/graphics/Point.md)`)` Create a new instance of [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md) if the boundary [Point](../android/graphics/Point.md) is known. |
| [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Create a new instance of [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md) if index of boundary is known. |

| Public methods ||
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/graphics/pdf/models/selection/SelectionBoundary.md))`()` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getIndex](../android/graphics/pdf/models/selection/SelectionBoundary.md))`()` Gets the index of the text as determined by the text stream processed. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [getIsRtl](../android/graphics/pdf/models/selection/SelectionBoundary.md))`()` Gets whether the direction of selection is right-to-left (rtl) or reverse. |
| --- | --- |
| [Point](../android/graphics/Point.md)? | [getPoint](../android/graphics/pdf/models/selection/SelectionBoundary.md))`()` Gets the x, y coordinates of the selection boundary in points (1/72"). |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/graphics/pdf/models/selection/SelectionBoundary.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md)!\> | [CREATOR](../android/graphics/pdf/models/selection/SelectionBoundary.md) <br /> |

## Public constructors

### SelectionBoundary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
SelectionBoundary(point: Point)
```

Create a new instance of [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md) if the boundary [Point](../android/graphics/Point.md) is known. Index defaults to -1.

| Parameters ||
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| `point` | [Point](../android/graphics/Point.md):The point of selection boundary. This value cannot be`null`. |

| Exceptions ||
|----------------------------------|-----------------------|
| `java.lang.NullPointerException` | If the point is null. |

### SelectionBoundary

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
SelectionBoundary(index: Int)
```

Create a new instance of [SelectionBoundary](../android/graphics/pdf/models/selection/SelectionBoundary.md) if index of boundary is known. The text returned by [PdfPageTextContent.getText()](../android/graphics/pdf/content/PdfPageTextContent.md))form a "stream" and inside this "stream" each character has an index.**Note:** Point defaults to`null`in this case.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

### getIndex

Added in [API level 35](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 13](https://developer.android.com/sdkExtensions) 

```
fun getIndex(): Int
```

Gets the index of the text as determined by the text stream processed. If the value is -1 then the [getPoint()](../android/graphics/pdf/models/selection/SelectionBoundary.md))will determine the selection boundary.

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

Gets the x, y coordinates of the selection boundary in points (1/72"). These coordinates are represented by a [Point](../android/graphics/Point.md). If the value is`null`then the [getIndex()](../android/graphics/pdf/models/selection/SelectionBoundary.md))will determine the selection boundary.

**Note:**Point (0,0) represents the top-left corner of the page

| Return ||
|---------------------------------------------------------------------------------------|--------------------------------------|
| [Point](../android/graphics/Point.md)? | The point of the selection boundary. |

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
static val CREATOR: Parcelable.Creator<SelectionBoundary!>
```
