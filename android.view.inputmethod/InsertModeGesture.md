# InsertModeGesture

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# InsertModeGesture

Kotlin| [Java](../android/view/inputmethod/InsertModeGesture.md) 
| --- | --- |

```
class InsertModeGesture : HandwritingGesture, Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.view.inputmethod.HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) ||
| | ↳ | [android.view.inputmethod.InsertModeGesture](../android/view/inputmethod/InsertModeGesture.md) |

A sub-class of [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) for starting an insert mode which inserts a space in the editor to let users hand write freely at the designated insertion point. This class holds the information required for insertion of text in toolkit widgets like [TextView](../android/widget/TextView.md). Once InsertMode gesture is started, it continues until IME calls [CancellationSignal.cancel()](../android/os/CancellationSignal.md))and toolkit can receive cancel using [CancellationSignal.setOnCancelListener(CancellationSignal.OnCancelListener)](../android/os/CancellationSignal.md))obtained from [getCancellationSignal()](../android/view/inputmethod/InsertModeGesture.md)).

## Summary

| Nested classes ||
|---|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/inputmethod/InsertModeGesture.Builder.md) Builder for [InsertModeGesture](../android/view/inputmethod/InsertModeGesture.md). |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||
| From class [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md) <br /> Operate on text per character basis. i.e. each character is selected based on its intersection with selection rectangle. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android/graphics/RectF.md) with [GRANULARITY_CHARACTER](../android/view/inputmethod/HandwritingGesture.md) includes width-wise center of the character, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md) <br /> Operate text per word basis. e.g. if selection includes width-wise center of the word, whole word is selected. Strategy of operating at a granular level is maintained in the UI toolkit. A character/word/line is included if its center is within the gesture rectangle. e.g. if a selection [RectF](../android/graphics/RectF.md) with [GRANULARITY_WORD](../android/view/inputmethod/HandwritingGesture.md) includes width-wise center of the word, it should be selected. Similarly, text in a line should be included in the operation if rectangle includes line height center. Refer to https://www.unicode.org/reports/tr29/#Word_Boundaries for more detail on how word breaks are decided. <br /> | ||

| Public methods ||
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/inputmethod/InsertModeGesture.md))`()` <br /> |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | [equals](../android/view/inputmethod/InsertModeGesture.md))`(`other:` ` [Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html)?`)` <br /> |
| [CancellationSignal](../android/os/CancellationSignal.md) | [getCancellationSignal](../android/view/inputmethod/InsertModeGesture.md))`()` Returns the [CancellationSignal](../android/os/CancellationSignal.md) associated with finishing this gesture. |
| --- | --- |
| [PointF](../android/graphics/PointF.md) | [getInsertionPoint](../android/view/inputmethod/InsertModeGesture.md))`()` Returns the insertion point [PointF](../android/graphics/PointF.md)(in screen coordinates) where space will be created for additional text to be inserted. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [hashCode](../android/view/inputmethod/InsertModeGesture.md))`()` <br /> |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/inputmethod/InsertModeGesture.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Used to package this object into a [Parcel](../android/os/Parcel.md). |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [HandwritingGesture](../android/view/inputmethod/HandwritingGesture.md) |-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)? | [getFallbackText](../android/view/inputmethod/HandwritingGesture.md))`()` <br /> The fallback text that will be committed at current cursor position if there is no applicable text beneath the area of gesture. For example, select can fail if gesture is drawn over area that has no text beneath. example 2: join can fail if the gesture is drawn over text but there is no whitespace. <br /> | ||

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [InsertModeGesture](../android/view/inputmethod/InsertModeGesture.md)!\> | [CREATOR](../android/view/inputmethod/InsertModeGesture.md) Used to make this class parcelable. |

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

### getCancellationSignal

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCancellationSignal(): CancellationSignal
```

Returns the [CancellationSignal](../android/os/CancellationSignal.md) associated with finishing this gesture. Once InsertMode gesture is started, it continues until IME calls [CancellationSignal.cancel()](../android/os/CancellationSignal.md))and toolkit can receive cancel using [CancellationSignal.setOnCancelListener(CancellationSignal.OnCancelListener)](../android/os/CancellationSignal.md)).

| Return ||
|----------------------------------------------------------------------------------------------------------|-----------------------------|
| [CancellationSignal](../android/os/CancellationSignal.md) | This value cannot be`null`. |

### getInsertionPoint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getInsertionPoint(): PointF
```

Returns the insertion point [PointF](../android/graphics/PointF.md)(in screen coordinates) where space will be created for additional text to be inserted.

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
|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](../android/os/Parcel.md):The [Parcel](../android/os/Parcel.md) to be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<InsertModeGesture!>
```

Used to make this class parcelable.
