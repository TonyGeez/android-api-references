# JoinOrSplitGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JoinOrSplitGesture

Kotlin| [Java](../android/view/inputmethod/JoinOrSplitGesture.md) 
| --- | --- |

```
class JoinOrSplitGesture : HandwritingGesture, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) ||
| | ↳ | [android.view.inputmethod.JoinOrSplitGesture](../android/view/inputmethod/JoinOrSplitGesture.md) |

A subclass of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for deleting or inserting whitespace in text. If the gesture is drawn over whitespace, then the whitespace will be deleted. Otherwise, a space will be inserted.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/inputmethod/JoinOrSplitGesture.Builder.md) Builder for [JoinOrSplitGesture](../android/view/inputmethod/JoinOrSplitGesture.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md) <br /> Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android/graphics/RectF.md) with [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md) <br /> Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android/graphics/RectF.md) with [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. Refer to https://www.unicode.org/reports/tr29/#Word_Boundaries for more detail on how word breaks are decided. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/inputmethod/JoinOrSplitGesture.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/view/inputmethod/JoinOrSplitGesture.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [PointF](../android/graphics/PointF.md) | [getJoinOrSplitPoint](../android/view/inputmethod/JoinOrSplitGesture.md))`()` Returns the gesture point in screen coordinates set with [Builder.setJoinOrSplitPoint](../android/view/inputmethod/JoinOrSplitGesture.Builder.md)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/view/inputmethod/JoinOrSplitGesture.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/inputmethod/JoinOrSplitGesture.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android/os/Parcel.md). |

| Inherited functions ||
|---|---|
| From class [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](../android/view/inputmethod/HandwritingGesture.md))`()` <br /> The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. For example, select can fail if gesture is drawn over area that has no text beneath. example 2: join can fail if the gesture is drawn over text but there is no whitespace. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [JoinOrSplitGesture](../android/view/inputmethod/JoinOrSplitGesture.md)!\> | [CREATOR](../android/view/inputmethod/JoinOrSplitGesture.md) Used to make this class parcelable. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) |

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

### getJoinOrSplitPoint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getJoinOrSplitPoint(): PointF
```

Returns the gesture point in screen coordinates set with [Builder.setJoinOrSplitPoint](../android/view/inputmethod/JoinOrSplitGesture.Builder.md)).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [PointF](../android/graphics/PointF.md) | This value cannot be`null`. |

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

Used to package this object into a [Parcel](../android/os/Parcel.md).

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md): [Parcel](../android/os/Parcel.md) to be written This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags used for parceling |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<JoinOrSplitGesture!>
```

Used to make this class parcelable.
