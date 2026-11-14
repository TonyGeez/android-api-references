# SelectRangeGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SelectRangeGesture

Kotlin| [Java](SelectRangeGesture.md) 
| --- | --- |

```
class SelectRangeGesture : PreviewableHandwritingGesture, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||||
| --- | --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](HandwritingGesture.md) |||
| | ↳ | [android.view.inputmethod.PreviewableHandwritingGesture](PreviewableHandwritingGesture.md) ||
| | | ↳ | [android.view.inputmethod.SelectRangeGesture](SelectRangeGesture.md) |
| --- | --- | --- | --- |

A subclass of [HandwritingGesture](HandwritingGesture.md) for selecting a range of text by defining start and end rectangles. This can be useful when the range cannot be defined with a single rectangle. This class holds the information required for selection of text in toolkit widgets like [TextView](../android.widget/TextView.md).

Note: this selects text within a range*between* two given areas. To select all text*within* a single area, use [SelectGesture](SelectGesture.md)

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/inputmethod/SelectRangeGesture.Builder.md) Builder for [SelectRangeGesture](SelectRangeGesture.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android.os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android.os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android.os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android.os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](SelectRangeGesture.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](SelectRangeGesture.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getGranularity](SelectRangeGesture.md))`()` Returns Granular level on which text should be operated. |
| --- | --- |
| [RectF](../android.graphics/RectF.md) | [getSelectionEndArea](SelectRangeGesture.md))`()` Returns the Selection end area [RectF](../android.graphics/RectF.md) in screen coordinates. |
| [RectF](../android.graphics/RectF.md) | [getSelectionStartArea](SelectRangeGesture.md))`()` Returns the Selection start area [RectF](../android.graphics/RectF.md) in screen coordinates. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](SelectRangeGesture.md))`()` <br /> |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](SelectRangeGesture.md))`(`dest:` ` [Parcel](../android.os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android.os/Parcel.md). |

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [SelectRangeGesture](SelectRangeGesture.md)!\> | [CREATOR](SelectRangeGesture.md) Used to make this class parcelable. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android.os/Parcelable.md) |

### equals

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun equals(other: Any?): Boolean
```

| Parameters ||
|-------|---------------------------------------------|
| `obj` | the reference object with which to compare. |

| Return ||
|------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `true`if this object is the same as the obj argument;`false`otherwise. |

### getGranularity

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGranularity(): Int
```

Returns Granular level on which text should be operated.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | Value is [android.view.inputmethod.HandwritingGesture#GRANULARITY_CHARACTER](HandwritingGesture.md), or [android.view.inputmethod.HandwritingGesture#GRANULARITY_WORD](HandwritingGesture.md) |

**See Also**

- [#GRANULARITY_CHARACTER](HandwritingGesture.md)
- [#GRANULARITY_WORD](HandwritingGesture.md) 

### getSelectionEndArea

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectionEndArea(): RectF
```

Returns the Selection end area [RectF](../android.graphics/RectF.md) in screen coordinates. Getter for selection area set with [Builder.setSelectionEndArea(RectF)](../android/view/inputmethod/SelectRangeGesture.Builder.md)).

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------|
| [RectF](../android.graphics/RectF.md) | This value cannot be`null`. |

### getSelectionStartArea

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getSelectionStartArea(): RectF
```

Returns the Selection start area [RectF](../android.graphics/RectF.md) in screen coordinates. Getter for selection area set with [Builder.setSelectionStartArea(RectF)](../android/view/inputmethod/SelectRangeGesture.Builder.md)).

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------|
| [RectF](../android.graphics/RectF.md) | This value cannot be`null`. |

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

Used to package this object into a [Parcel](../android.os/Parcel.md).

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android.os/Parcel.md):The [Parcel](../android.os/Parcel.md) to be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<SelectRangeGesture!>
```

Used to make this class parcelable.
