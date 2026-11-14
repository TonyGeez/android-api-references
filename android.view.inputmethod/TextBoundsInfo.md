# TextBoundsInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextBoundsInfo

Kotlin| [Java](https://developer.android.com/reference/android/view/inputmethod/TextBoundsInfo "View this page in Java") 
| --- | --- |

```
class TextBoundsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#) |

The text bounds information of a slice of text in the editor.

This class provides IME the layout information of the text within the range from [getStartIndex()](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getStartIndex())to [getEndIndex()](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getEndIndex()). It's intended to be used by IME as a supplementary API to support handwriting gestures.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder) The builder class to create a [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#) object. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CHARACTER_LINEFEED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_LINEFEED:kotlin.Int) The flag indicating that the character is a linefeed character. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CHARACTER_PUNCTUATION](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_PUNCTUATION:kotlin.Int) The flag indicating that the character is a punctuation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CHARACTER_WHITESPACE](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_WHITESPACE:kotlin.Int) The flag indicating that the character is a whitespace. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_LINE_IS_RTL](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_LINE_IS_RTL:kotlin.Int) The flag indicating that the line this character belongs to has RTL line direction. |

| Inherited constants ||
|---|---|
| From class [Parcelable](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) <br /> Descriptor bit used with [describeContents()](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#describeContents()): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int) <br /> Flag for use with [writeToParcel](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#writeToParcel(android.os.Parcel,%20kotlin.Int)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#describeContents())`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharacterBidiLevel](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterBidiLevel(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The BiDi level of the character at the given`index`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCharacterBounds](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterBounds(kotlin.Int,%20android.graphics.RectF))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)`)` Set the bounds of the character at the given`index`to the given [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#), in the coordinates of the editor. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharacterFlags](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterFlags(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the flags associated with the character at the given`index`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getEndIndex())`()` Returns the index of the last character whose bounds information is available in this [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#), exclusive. |
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) | [getGraphemeSegmentFinder](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getGraphemeSegmentFinder())`()` Returns the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) that locates the grapheme boundaries. |
| --- | --- |
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) | [getLineSegmentFinder](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getLineSegmentFinder())`()` Returns the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) that locates the line boundaries. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getMatrix](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getMatrix(android.graphics.Matrix))`(`matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)`)` Set the given [android.graphics.Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#) to be the transformation matrix that is to be applied other positional data in this class. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetForPosition](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getOffsetForPosition(kotlin.Float,%20kotlin.Float))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return the index of the closest character to the given position. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRangeForRect](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getRangeForRect(android.graphics.RectF,%20android.text.SegmentFinder,%20android.text.Layout.TextInclusionStrategy))`(`area:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)`, `segmentFinder:` ` [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#)`, `inclusionStrategy:` ` [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy.html#)`)` Finds the range of text which is inside the specified rectangle area. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartIndex](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getStartIndex())`()` Returns the index of the first character whose bounds information is available in this [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#), inclusive. |
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) | [getWordSegmentFinder](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getWordSegmentFinder())`()` Returns the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) that locates the word boundaries. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#writeToParcel(android.os.Parcel,%20kotlin.Int))`(`dest:` ` [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](https://developer.android.com/reference/kotlin/android/os/Parcelable.Creator.html#)\< [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#)!\> | [CREATOR](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#CREATOR:android.os.Parcelable.Creator) The CREATOR to make this class Parcelable. |

## Constants

### FLAG_CHARACTER_LINEFEED

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CHARACTER_LINEFEED: Int
```

The flag indicating that the character is a linefeed character. 

 Value: 2

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterFlags(kotlin.Int)) 

### FLAG_CHARACTER_PUNCTUATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CHARACTER_PUNCTUATION: Int
```

The flag indicating that the character is a punctuation. 

 Value: 4

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterFlags(kotlin.Int)) 

### FLAG_CHARACTER_WHITESPACE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CHARACTER_WHITESPACE: Int
```

The flag indicating that the character is a whitespace. 

 Value: 1

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterFlags(kotlin.Int)) 

### FLAG_LINE_IS_RTL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_LINE_IS_RTL: Int
```

The flag indicating that the line this character belongs to has RTL line direction. It's required that all characters in the same line must have the same direction. 

 Value: 8

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getCharacterFlags(kotlin.Int))

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#writeToParcel(android.os.Parcel,%20kotlin.Int)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#CONTENTS_FILE_DESCRIPTOR:kotlin.Int) bit.

| Return ||
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | a bitmask indicating the set of special object types marshaled by this Parcelable object instance. |

### getCharacterBidiLevel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCharacterBidiLevel(index: Int): Int
```

The BiDi level of the character at the given`index`. 
BiDi level is defined by [the unicode bidirectional algorithm](https://unicode.org/reports/tr9/#Basic_Display_Algorithm). One can determine whether a character's direction is right-to-left (RTL) or left-to-right (LTR) by checking the last bit of the BiDi level. If it's 1, the character is RTL, otherwise the character is LTR. The BiDi level of a character must be in the range of \[0, 125\].

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the queried character. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the BiDi level of the character, which is an integer in the range of \[0, 125\]. Value is between 0 and 125 inclusive |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the given`index`is out of the range from the`start`to the`end`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterBidiLevel(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterBidiLevel(kotlin.IntArray)) 

### getCharacterBounds

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCharacterBounds(
    index: Int, 
    bounds: RectF
): Unit
```

Set the bounds of the character at the given`index`to the given [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#), in the coordinates of the editor.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the queried character. |
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#):the [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) used to receive the result. This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the given`index`is out of the range from the`start`to the`end`. |

### getCharacterFlags

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getCharacterFlags(index: Int): Int
```

Return the flags associated with the character at the given`index`. The flags contain the following information:

- The [FLAG_CHARACTER_WHITESPACE](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_WHITESPACE:kotlin.Int) flag, indicating the character is a whitespace.
- The [FLAG_CHARACTER_LINEFEED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_LINEFEED:kotlin.Int) flag, indicating the character is a linefeed.
- The [FLAG_CHARACTER_PUNCTUATION](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_PUNCTUATION:kotlin.Int) flag, indicating the character is a punctuation.
- The [FLAG_LINE_IS_RTL](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_LINE_IS_RTL:kotlin.Int) flag, indicating the line this character belongs to has RTL line direction. All characters in the same line must have the same line direction. Check [getLineSegmentFinder()](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getLineSegmentFinder())for more information of line boundaries.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the queried character. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the flags associated with the queried character. Value is either`0`or a combination of [android.view.inputmethod.TextBoundsInfo#FLAG_CHARACTER_WHITESPACE](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_WHITESPACE:kotlin.Int), [android.view.inputmethod.TextBoundsInfo#FLAG_CHARACTER_LINEFEED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_LINEFEED:kotlin.Int), [android.view.inputmethod.TextBoundsInfo#FLAG_CHARACTER_PUNCTUATION](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_PUNCTUATION:kotlin.Int), and [android.view.inputmethod.TextBoundsInfo#FLAG_LINE_IS_RTL](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_LINE_IS_RTL:kotlin.Int) |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the given`index`is out of the range from the`start`to the`end`. |

**See Also**

- [#FLAG_CHARACTER_WHITESPACE](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_WHITESPACE:kotlin.Int)
- [#FLAG_CHARACTER_LINEFEED](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_LINEFEED:kotlin.Int)
- [#FLAG_CHARACTER_PUNCTUATION](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_CHARACTER_PUNCTUATION:kotlin.Int)
- [#FLAG_LINE_IS_RTL](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#FLAG_LINE_IS_RTL:kotlin.Int) 

### getEndIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndIndex(): Int
```

Returns the index of the last character whose bounds information is available in this [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#), exclusive. 
**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setStartAndEnd(int, int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setStartAndEnd(kotlin.Int,%20kotlin.Int)) 

### getGraphemeSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGraphemeSegmentFinder(): SegmentFinder
```

Returns the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) that locates the grapheme boundaries.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setGraphemeSegmentFinder(SegmentFinder)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setGraphemeSegmentFinder(android.text.SegmentFinder)) 

### getLineSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineSegmentFinder(): SegmentFinder
```

Returns the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) that locates the line boundaries.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setLineSegmentFinder(SegmentFinder)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setLineSegmentFinder(android.text.SegmentFinder)) 

### getMatrix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatrix(matrix: Matrix): Unit
```

Set the given [android.graphics.Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#) to be the transformation matrix that is to be applied other positional data in this class.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `matrix` | [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#):This value cannot be`null`. |

| Return ||
|------------------------------------------------------------------------------|-----------------------------|
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | This value cannot be`null`. |

### getOffsetForPosition

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getOffsetForPosition(
    x: Float, 
    y: Float
): Int
```

Return the index of the closest character to the given position. It's similar to the text layout API [Layout.getOffsetForHorizontal(int, float)](https://developer.android.com/reference/kotlin/android/text/Layout.html#getOffsetForHorizontal(kotlin.Int,%20kotlin.Float)). And it's mainly used to find the cursor index (the index of the character before which the cursor should be placed) for the given position. It's guaranteed that the returned index is a grapheme break. Check [getGraphemeSegmentFinder()](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getGraphemeSegmentFinder())for more information.

It's assumed that the editor lays out text in horizontal lines from top to bottom and each line is laid out according to the display algorithm specified in [unicode bidirectional algorithm](https://unicode.org/reports/tr9/#Basic_Display_Algorithm).

This method won't check the text ranges whose line information is missing. For example, the [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#)'s range is from index 5 to 15. If the associated [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) only identifies one line range from 7 to 12. Then this method won't check the text in the ranges of \[5, 7) and \[12, 15).

Under the following conditions, this method will return -1 indicating that no valid character is found:

- The given`y`coordinate is above the first line or below the last line (the first line or the last line is identified by the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) returned from [getLineSegmentFinder()](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#getLineSegmentFinder())).
- There is no character in this [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#).

<br />

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the x coordinates of the interested location, in the editor's coordinates. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the y coordinates of the interested location, in the editor's coordinates. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the character whose position is closest to the given location. It will return -1 if it can't find a character. |

**See Also**

- [android.text.Layout#getOffsetForHorizontal(int, float)](https://developer.android.com/reference/kotlin/android/text/Layout.html#getOffsetForHorizontal(kotlin.Int,%20kotlin.Float)) 

### getRangeForRect

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangeForRect(
    area: RectF, 
    segmentFinder: SegmentFinder, 
    inclusionStrategy: Layout.TextInclusionStrategy
): IntArray?
```

Finds the range of text which is inside the specified rectangle area. This method is a counterpart of the [Layout.getRangeForRect(RectF, SegmentFinder, Layout.TextInclusionStrategy)](https://developer.android.com/reference/kotlin/android/text/Layout.html#getRangeForRect(android.graphics.RectF,%20android.text.SegmentFinder,%20android.text.Layout.TextInclusionStrategy)).

It's assumed that the editor lays out text in horizontal lines from top to bottom and each line is laid out according to the display algorithm specified in [unicode bidirectional algorithm](https://unicode.org/reports/tr9/#Basic_Display_Algorithm).

This method won't check the text ranges whose line information is missing. For example, the [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#)'s range is from index 5 to 15. If the associated line [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) only identifies one line range from 7 to 12. Then this method won't check the text in the ranges of \[5, 7) and \[12, 15).

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `area` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#):area for which the text range will be found This value cannot be`null`. |
| `segmentFinder` | [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#):SegmentFinder for determining the ranges of text to be considered as a text segment This value cannot be`null`. |
| `inclusionStrategy` | [Layout.TextInclusionStrategy](https://developer.android.com/reference/kotlin/android/text/Layout.TextInclusionStrategy.html#):strategy for determining whether a text segment is inside the specified area This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the text range stored in a two element int array. The first element is the start (inclusive) of the text range, and the second element is the end (exclusive) character offsets of the text range, or null if there are no text segments inside the area. |

**See Also**

- [android.text.Layout#getRangeForRect(RectF, SegmentFinder, Layout.TextInclusionStrategy)](https://developer.android.com/reference/kotlin/android/text/Layout.html#getRangeForRect(android.graphics.RectF,%20android.text.SegmentFinder,%20android.text.Layout.TextInclusionStrategy)) 

### getStartIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartIndex(): Int
```

Returns the index of the first character whose bounds information is available in this [TextBoundsInfo](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo#), inclusive. 
**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setStartAndEnd(int, int)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setStartAndEnd(kotlin.Int,%20kotlin.Int)) 

### getWordSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWordSegmentFinder(): SegmentFinder
```

Returns the [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) that locates the word boundaries.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.html#) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setWordSegmentFinder(SegmentFinder)](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setWordSegmentFinder(android.text.SegmentFinder)) 

### writeToParcel

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun writeToParcel(
    dest: Parcel, 
    flags: Int
): Unit
```

Flatten this object in to a Parcel.

| Parameters ||
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `dest` | [Parcel](https://developer.android.com/reference/kotlin/android/os/Parcel.html#):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](https://developer.android.com/reference/kotlin/android/os/Parcelable.html#PARCELABLE_WRITE_RETURN_VALUE:kotlin.Int). |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextBoundsInfo!>
```

The CREATOR to make this class Parcelable.
