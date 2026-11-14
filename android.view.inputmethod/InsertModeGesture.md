# InsertModeGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InsertModeGesture

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/InsertModeGesture "View this page in Java") 
| --- | --- |

```
class InsertModeGesture : HandwritingGesture, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) ||
| | ↳ | [android.view.inputmethod.InsertModeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#) |

A sub-class of [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. This class holds the information required for insertion of text in toolkit widgets like [TextView](https://developer.android.com/reference/kotlin/android/widget/TextView.html#). Once InsertMode gesture is started, it continues until IME calls [CancellationSignal.cancel()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#cancel())and toolkit can receive cancel using [CancellationSignal.setOnCancelListener(CancellationSignal.OnCancelListener)](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#setOnCancelListener(android.os.CancellationSignal.OnCancelListener))obtained from [getCancellationSignal()](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#getCancellationSignal()).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture.Builder) Builder for [InsertModeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#). |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int) <br /> Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) with [GRANULARITY_CHARACTER](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_CHARACTER:kotlin.Int) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) <br /> Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) with [GRANULARITY_WORD](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#GRANULARITY_WORD:kotlin.Int) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. Refer to https://www.unicode.org/reports/tr29/#Word_Boundaries for more detail on how word breaks are decided. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#describeContents())`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#equals(kotlin.Any))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) | [getCancellationSignal](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#getCancellationSignal())`()` Returns the [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) associated with finishing this gesture. |
| --- | --- |
| [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#) | [getInsertionPoint](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#getInsertionPoint())`()` Returns the insertion point [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)(in screen coordinates) where space will be created for additional text to be inserted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#hashCode())`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#). |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [HandwritingGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](https://developer.android.com/reference/kotlin/android/view/inputmethod/HandwritingGesture#getFallbackText())`()` <br /> The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. For example, select can fail if gesture is drawn over area that has no text beneath. example 2: join can fail if the gesture is drawn over text but there is no whitespace. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [InsertModeGesture](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/InsertModeGesture#CREATOR:android.os.Parcelable.Creator) Used to make this class parcelable. |

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

### getCancellationSignal

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCancellationSignal(): CancellationSignal
```

Returns the [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) associated with finishing this gesture. Once InsertMode gesture is started, it continues until IME calls [CancellationSignal.cancel()](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#cancel())and toolkit can receive cancel using [CancellationSignal.setOnCancelListener(CancellationSignal.OnCancelListener)](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#setOnCancelListener(android.os.CancellationSignal.OnCancelListener)).

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------|
| [CancellationSignal](https://developer.android.com/reference/kotlin/android/os/CancellationSignal.html#) | This value cannot be`null`. |

### getInsertionPoint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInsertionPoint(): PointF
```

Returns the insertion point [PointF](https://developer.android.com/reference/kotlin/android/graphics/PointF.html#)(in screen coordinates) where space will be created for additional text to be inserted.

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
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#) to be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InsertModeGesture!>
```

Used to make this class parcelable.
