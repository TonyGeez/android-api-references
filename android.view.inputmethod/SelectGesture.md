# SelectGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectGesture

Kotlin | [Java](https://developer.android.com/reference/android/view/inputmethod/SelectGesture "View this page in Java") 
| --- | --- |

```
class SelectGesture : PreviewableHandwritingGesture, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) |||
| | ↳ | [android.view.inputmethod.PreviewableHandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/PreviewableHandwritingGesture) ||
| | | ↳ | [android.view.inputmethod.SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#) |
| --- | --- | --- | --- |

A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for selecting an area of text using single rectangle. This class holds the information required for selection of text in toolkit widgets like [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#).

Note: This selects all text *within* the given area. To select a range *between* two areas, use [SelectRangeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectRangeGesture).

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture.Builder) Builder for [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGranularity](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#getGranularity())`()` Returns Granular level on which text should be operated. |
| --- | --- |
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) | [getSelectionArea](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#getSelectionArea())`()` Returns the Selection area [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) in screen coordinates. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |
| --- | --- |

| Properties ||
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [SelectGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true` if this object is the same as the obj argument; `false` otherwise. |

### getGranularity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGranularity(): Int
```

Returns Granular level on which text should be operated.

| Return ||
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.inputmethod.HandwritingGesture#GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int), or [android.view.inputmethod.HandwritingGesture#GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) |

**See Also**

- [#GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int)
- [#GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) 

### getSelectionArea

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectionArea(): RectF
```

Returns the Selection area [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) in screen coordinates. Getter for selection area set with [Builder.setSelectionArea(RectF)](https://developer.android.com/reference/kotlin/android/view/inputmethod/SelectGesture.Builder#setSelectionArea(android.graphics.RectF)).

| Return ||
|--------------------------------------------------------------------------------------|------------------------------|
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) | This value cannot be `null`. |

### hashCode

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun hashCode(): Int
```

| Return ||
|----------------------------------------------------------------------------|------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a hash code value for this object. |

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#).

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. This value cannot be `null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SelectGesture!>
```

Used to make this class parcelable.
