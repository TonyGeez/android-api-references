Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# CursorAnchorInfo

Kotlin | [Java](https://developer.android.com/reference/android/view/inputmethod/CursorAnchorInfo "View this page in Java")
| --- | --- |

```
class CursorAnchorInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#) |

Positional information about the text insertion point and characters in the composition string.

This class encapsulates locations of the text insertion point and the composition string in the screen coordinates so that IMEs can render their UI components near where the text is actually inserted.

## Summary

| Nested classes ||
|---|---|
| | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo.Builder` Builder for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#`. |

| Constants ||
|---|---|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#FLAG_HAS_INVISIBLE_REGION:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)`: the insertion marker or character bounds have at least one invisible (clipped) region. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#FLAG_HAS_VISIBLE_REGION:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)`: the insertion marker or character bounds have at least one visible region. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#FLAG_IS_RTL:kotlin.Int` Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)`: the insertion marker or character bounds is placed at right-to-left (RTL) character. |
| --- | --- |

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` Descriptor bit used with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()`: indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int` Flag for use with `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`: the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#CursorAnchorInfo(android.os.Parcel)(source: https://developer.android.com/reference/kotlin/android/os/Parcel.html#!)` <br /> |

| Public methods ||
|---|---|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#describeContents()()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Boolean](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#equals(kotlin.Any)(other: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html?)` Indicates whether some other object is "equal to" this one. |
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBounds(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns a new instance of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` that indicates the location of the character specified with the index. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)(index: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the flags associated with the character bounds specified with the index. |
| [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getComposingText()()` Returns the entire composing text. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getComposingTextStart()()` Returns the index where the composing text starts. |
| --- | --- |
| [EditorBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorBoundsInfo)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getEditorBoundsInfo()()` Returns `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorBoundsInfo` for the current editor, or `null` if IME is not subscribed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerBaseline()()` Returns the vertical baseline position of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerBottom()()` Returns the vertical bottom position of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()()` Returns the flag of the insertion marker. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerHorizontal()()` Returns the horizontal start of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerTop()()` Returns the vertical top position of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen. |
| --- | --- |
| [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)! | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()()` Returns a new instance of `https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#` that indicates the transformation matrix that is to be applied other positional data in this class. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getSelectionEnd()()` Returns the index where the selection ends. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getSelectionStart()()` Returns the index where the selection starts. |
| --- | --- |
| [TextAppearanceInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo)? | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getTextAppearanceInfo()()` Returns `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo` for the current editor, or `null` if IME is not subscribed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`. |
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getVisibleLineBounds()()` Returns the list of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`s indicating the locations of the visible line bounds in the editor. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#hashCode()()` Returns a hash code value for the object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#toString()()` Returns a string representation of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)(dest: https://developer.android.com/reference/kotlin/android/os/Parcel.html#, flags: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`. |

| Properties ||
|---|---|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [CursorAnchorInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#)!\> | `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#CREATOR:android.os.Parcelable.Creator` Used to make this class parcelable. |

## Constants

### FLAG_HAS_INVISIBLE_REGION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HAS_INVISIBLE_REGION: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)`: the insertion marker or character bounds have at least one invisible (clipped) region.

 Value: 2

### FLAG_HAS_VISIBLE_REGION

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_HAS_VISIBLE_REGION: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)`: the insertion marker or character bounds have at least one visible region.

 Value: 1

### FLAG_IS_RTL

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val FLAG_IS_RTL: Int
```

Flag for `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getInsertionMarkerFlags()` and `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getCharacterBoundsFlags(kotlin.Int)`: the insertion marker or character bounds is placed at right-to-left (RTL) character.

 Value: 4

## Public constructors

### CursorAnchorInfo

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
CursorAnchorInfo(source: Parcel!)
```

## Public methods

### describeContents

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)`, the return value of this method must include the `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` bit.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. Value is either `0` or - `https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int` |

### equals

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun equals(other: Any?): Boolean
```

Indicates whether some other object is "equal to" this one.

The `equals` method implements an equivalence relation on non-null object references:

- It is *reflexive* : for any non-null reference value `x`, `x.equals(x)` should return `true`.
- It is *symmetric* : for any non-null reference values `x` and `y`, `x.equals(y)` should return `true` if and only if `y.equals(x)` returns `true`.
- It is *transitive* : for any non-null reference values `x`, `y`, and `z`, if `x.equals(y)` returns `true` and `y.equals(z)` returns `true`, then `x.equals(z)` should return `true`.
- It is *consistent* : for any non-null reference values `x` and `y`, multiple invocations of `x.equals(y)` consistently return `true` or consistently return `false`, provided no information used in `equals` comparisons on the objects is modified.
- For any non-null reference value `x`, `x.equals(null)` should return `false`.

An equivalence relation partitions the elements it operates on into *equivalence classes*; all the members of an equivalence class are equal to each other. Members of an equivalence class are substitutable for each other, at least for some purposes.

| Parameters ||
|---|---|
| `obj` | This value may be `null`. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html` | `true` if this object is the same as the obj argument; `false` otherwise. |

### getCharacterBounds

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharacterBounds(index: Int): RectF!
```

Returns a new instance of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#` that indicates the location of the character specified with the index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the character in a Java chars. |

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#!` | the character bounds in local coordinates as a new instance of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`. |

### getCharacterBoundsFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getCharacterBoundsFlags(index: Int): Int
```

Returns the flags associated with the character bounds specified with the index.

| Parameters ||
|---|---|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): index of the character in a Java chars. |

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `0` if no flag is specified. |

### getComposingText

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComposingText(): CharSequence!
```

Returns the entire composing text.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html!` | `null` if there is no composition. |

### getComposingTextStart

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getComposingTextStart(): Int
```

Returns the index where the composing text starts.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `-1` if there is no composing text. |

### getEditorBoundsInfo

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getEditorBoundsInfo(): EditorBoundsInfo?
```

Returns `https://developer.android.com/reference/kotlin/android/view/inputmethod/EditorBoundsInfo` for the current editor, or `null` if IME is not subscribed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_EDITOR_BOUNDS:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

### getInsertionMarkerBaseline

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInsertionMarkerBaseline(): Float
```

Returns the vertical baseline position of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | y coordinate that is compatible with `https://developer.android.com/reference/kotlin/android/text/Layout.html#getLineBaseline(kotlin.Int)`. `java.lang.Float.NaN` if not specified. |

### getInsertionMarkerBottom

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInsertionMarkerBottom(): Float
```

Returns the vertical bottom position of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | y coordinate that is compatible with `https://developer.android.com/reference/kotlin/android/text/Layout.html#getLineBottom(kotlin.Int)`. `java.lang.Float.NaN` if not specified. |

### getInsertionMarkerFlags

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInsertionMarkerFlags(): Int
```

Returns the flag of the insertion marker.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | the flag of the insertion marker. `0` if no flag is specified. |

### getInsertionMarkerHorizontal

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInsertionMarkerHorizontal(): Float
```

Returns the horizontal start of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | x coordinate that is compatible with `https://developer.android.com/reference/kotlin/android/text/Layout.html#getPrimaryHorizontal(kotlin.Int)`. Pay special care to RTL/LTR handling. `java.lang.Float.NaN` if not specified. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/text/Layout.html#getPrimaryHorizontal(kotlin.Int)`

### getInsertionMarkerTop

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getInsertionMarkerTop(): Float
```

Returns the vertical top position of the insertion marker, in the local coordinates that will be transformed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo#getMatrix()` when rendered on the screen.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html` | y coordinate that is compatible with `https://developer.android.com/reference/kotlin/android/text/Layout.html#getLineTop(kotlin.Int)`. `java.lang.Float.NaN` if not specified. |

### getMatrix

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getMatrix(): Matrix!
```

Returns a new instance of `https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#` that indicates the transformation matrix that is to be applied other positional data in this class.

| Return ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#!` | a new instance (copy) of the transformation matrix. |

### getSelectionEnd

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSelectionEnd(): Int
```

Returns the index where the selection ends.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `-1` if there is no selection. |

### getSelectionStart

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getSelectionStart(): Int
```

Returns the index where the selection starts.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `-1` if there is no selection. |

### getTextAppearanceInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getTextAppearanceInfo(): TextAppearanceInfo?
```

Returns `https://developer.android.com/reference/kotlin/android/view/inputmethod/TextAppearanceInfo` for the current editor, or `null` if IME is not subscribed with `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_FILTER_TEXT_APPEARANCE:kotlin.Int` or `https://developer.android.com/reference/kotlin/android/view/inputmethod/InputConnection#CURSOR_UPDATE_MONITOR:kotlin.Int`.

### getVisibleLineBounds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun getVisibleLineBounds(): MutableList<RectF!>
```

Returns the list of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`s indicating the locations of the visible line bounds in the editor.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/RectF.html#!>` | the visible line bounds in the local coordinates as a list of `https://developer.android.com/reference/kotlin/android/graphics/RectF.html#`. This value cannot be `null`. |

**See Also**

- `https://developer.android.com/reference/kotlin/android/view/inputmethod/CursorAnchorInfo.Builder#addVisibleLineBounds(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)`

### hashCode

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun hashCode(): Int
```

Returns a hash code value for the object. This method is supported for the benefit of hash tables such as those provided by `https://developer.android.com/reference/kotlin/java/util/HashMap.html#`.

The general contract of `hashCode` is:

- Whenever it is invoked on the same object more than once during an execution of a Java application, the `hashCode` method must consistently return the same integer, provided no information used in `equals` comparisons on the object is modified. This integer need not remain consistent from one execution of an application to another execution of the same application.
- If two objects are equal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce the same integer result.
- It is *not* required that if two objects are unequal according to the `https://developer.android.com/reference/kotlin/java/lang/Object.html#equals(kotlin.Any)` method, then calling the `hashCode` method on each of the two objects must produce distinct integer results. However, the programmer should be aware that producing distinct integer results for unequal objects may improve the performance of hash tables.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | a hash code value for this object. |

### toString

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun toString(): String
```

Returns a string representation of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html` | a string representation of the object. |

### writeToParcel

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Used to package this object into a `https://developer.android.com/reference/kotlin/android/os/Parcel.html#`.

| Parameters ||
|---|---|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#): The `https://developer.android.com/reference/kotlin/android/os/Parcel.html#` to be written. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The flags used for parceling. |

## Properties

### CREATOR

Added in [API level 21](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
static val CREATOR: Parcelable.Creator<CursorAnchorInfo!>
```

Used to make this class parcelable.
