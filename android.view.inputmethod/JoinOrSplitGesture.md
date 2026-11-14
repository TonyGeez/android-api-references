# JoinOrSplitGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# JoinOrSplitGesture

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/JoinOrSplitGesture "View this page in Java") 
| --- | --- |

```
class JoinOrSplitGesture : HandwritingGesture, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) ||
| | ↳ | [android.view.inputmethod.JoinOrSplitGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#) |

A subclass of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for deleting or inserting whitespace in text. If the gesture is drawn over whitespace, then the whitespace will be deleted. Otherwise, a space will be inserted.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture.Builder) Builder for [JoinOrSplitGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int) <br /> Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) with [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) <br /> Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) with [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. Refer to https://www.unicode.org/reports/tr29/#Word_Boundaries for more detail on how word breaks are decided. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#) | [getJoinOrSplitPoint](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#getJoinOrSplitPoint())`()` Returns the gesture point in screen coordinates set with [Builder.setJoinOrSplitPoint](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture.Builder#setJoinOrSplitPoint(android.graphics.PointF)). |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |

| Inherited functions ||
|---|---|
| From class [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#getFallbackText())`()` <br /> The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. For example, select can fail if gesture is drawn over area that has no text beneath. example 2: join can fail if the gesture is drawn over text but there is no whitespace. <br /> | ||

| Properties ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [JoinOrSplitGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either`0`or [android.os.Parcelable#CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) |

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

Returns the gesture point in screen coordinates set with [Builder.setJoinOrSplitPoint](https://developer.android.com/reference/kotlin/android/view/inputmethod/JoinOrSplitGesture.Builder#setJoinOrSplitPoint(android.graphics.PointF)).

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------|
| [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#) | This value cannot be`null`. |

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
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):flags used for parceling |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<JoinOrSplitGesture!>
```

Used to make this class parcelable.
