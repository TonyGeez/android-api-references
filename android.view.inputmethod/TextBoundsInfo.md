# TextBoundsInfo

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# TextBoundsInfo

Kotlin| [Java](../android/view/inputmethod/TextBoundsInfo.md) 
| --- | --- |

```
class TextBoundsInfo : Parcelable
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.view.inputmethod.TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md) |

The text bounds information of a slice of text in the editor.

This class provides IME the layout information of the text within the range from [getStartIndex()](../android/view/inputmethod/TextBoundsInfo.md))to [getEndIndex()](../android/view/inputmethod/TextBoundsInfo.md)). It's intended to be used by IME as a supplementary API to support handwriting gestures.

## Summary

| Nested classes ||
|---|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/view/inputmethod/TextBoundsInfo.Builder.md) The builder class to create a [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md) object. |

| Constants ||
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CHARACTER_LINEFEED](../android/view/inputmethod/TextBoundsInfo.md) The flag indicating that the character is a linefeed character. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CHARACTER_PUNCTUATION](../android/view/inputmethod/TextBoundsInfo.md) The flag indicating that the character is a punctuation. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_CHARACTER_WHITESPACE](../android/view/inputmethod/TextBoundsInfo.md) The flag indicating that the character is a whitespace. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [FLAG_LINE_IS_RTL](../android/view/inputmethod/TextBoundsInfo.md) The flag indicating that the line this character belongs to has RTL line direction. |

| Inherited constants ||
|---|---|
| From class [Parcelable](../android/os/Parcelable.md) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) <br /> Descriptor bit used with [describeContents()](../android/os/Parcelable.md)): indicates that the Parcelable object's flattened representation includes a file descriptor. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md) <br /> Flag for use with [writeToParcel](../android/os/Parcelable.md)): the object being written is a return value, that is the result of a function such as "`Parcelable someFunction()`", "`void someFunction(out Parcelable)`", or "`void someFunction(inout Parcelable)`". Some implementations may want to release resources at this point. <br /> | ||

| Public methods ||
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [describeContents](../android/view/inputmethod/TextBoundsInfo.md))`()` Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharacterBidiLevel](../android/view/inputmethod/TextBoundsInfo.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` The BiDi level of the character at the given`index`. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getCharacterBounds](../android/view/inputmethod/TextBoundsInfo.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `bounds:` ` [RectF](../android/graphics/RectF.md)`)` Set the bounds of the character at the given`index`to the given [RectF](../android/graphics/RectF.md), in the coordinates of the editor. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getCharacterFlags](../android/view/inputmethod/TextBoundsInfo.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Return the flags associated with the character at the given`index`. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getEndIndex](../android/view/inputmethod/TextBoundsInfo.md))`()` Returns the index of the last character whose bounds information is available in this [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md), exclusive. |
| [SegmentFinder](../android/text/SegmentFinder.md) | [getGraphemeSegmentFinder](../android/view/inputmethod/TextBoundsInfo.md))`()` Returns the [SegmentFinder](../android/text/SegmentFinder.md) that locates the grapheme boundaries. |
| --- | --- |
| [SegmentFinder](../android/text/SegmentFinder.md) | [getLineSegmentFinder](../android/view/inputmethod/TextBoundsInfo.md))`()` Returns the [SegmentFinder](../android/text/SegmentFinder.md) that locates the line boundaries. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getMatrix](../android/view/inputmethod/TextBoundsInfo.md))`(`matrix:` ` [Matrix](../android/graphics/Matrix.md)`)` Set the given [android.graphics.Matrix](../android/graphics/Matrix.md) to be the transformation matrix that is to be applied other positional data in this class. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getOffsetForPosition](../android/view/inputmethod/TextBoundsInfo.md))`(`x:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `y:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Return the index of the closest character to the given position. |
| --- | --- |
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | [getRangeForRect](../android/view/inputmethod/TextBoundsInfo.md))`(`area:` ` [RectF](../android/graphics/RectF.md)`, `segmentFinder:` ` [SegmentFinder](../android/text/SegmentFinder.md)`, `inclusionStrategy:` ` [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md)`)` Finds the range of text which is inside the specified rectangle area. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStartIndex](../android/view/inputmethod/TextBoundsInfo.md))`()` Returns the index of the first character whose bounds information is available in this [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md), inclusive. |
| [SegmentFinder](../android/text/SegmentFinder.md) | [getWordSegmentFinder](../android/view/inputmethod/TextBoundsInfo.md))`()` Returns the [SegmentFinder](../android/text/SegmentFinder.md) that locates the word boundaries. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [writeToParcel](../android/view/inputmethod/TextBoundsInfo.md))`(`dest:` ` [Parcel](../android/os/Parcel.md)`, `flags:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Flatten this object in to a Parcel. |

| Properties ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Parcelable.Creator](../android/os/Parcelable.Creator.md)\< [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md)!\> | [CREATOR](../android/view/inputmethod/TextBoundsInfo.md) The CREATOR to make this class Parcelable. |

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
- [#getCharacterFlags(int)](../android/view/inputmethod/TextBoundsInfo.md)) 

### FLAG_CHARACTER_PUNCTUATION

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CHARACTER_PUNCTUATION: Int
```

The flag indicating that the character is a punctuation. 

 Value: 4

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](../android/view/inputmethod/TextBoundsInfo.md)) 

### FLAG_CHARACTER_WHITESPACE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_CHARACTER_WHITESPACE: Int
```

The flag indicating that the character is a whitespace. 

 Value: 1

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](../android/view/inputmethod/TextBoundsInfo.md)) 

### FLAG_LINE_IS_RTL

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val FLAG_LINE_IS_RTL: Int
```

The flag indicating that the line this character belongs to has RTL line direction. It's required that all characters in the same line must have the same direction. 

 Value: 8

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setCharacterFlags(int[])](https://developer.android.com/reference/kotlin/android/view/inputmethod/TextBoundsInfo.Builder#setCharacterFlags(kotlin.IntArray))
- [#getCharacterFlags(int)](../android/view/inputmethod/TextBoundsInfo.md))

## Public methods

### describeContents

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun describeContents(): Int
```

Describe the kinds of special objects contained in this Parcelable instance's marshaled representation. For example, if the object will include a file descriptor in the output of [writeToParcel(android.os.Parcel,int)](../android/view/inputmethod/TextBoundsInfo.md)), the return value of this method must include the [CONTENTS_FILE_DESCRIPTOR](../android/os/Parcelable.md) bit.

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

Set the bounds of the character at the given`index`to the given [RectF](../android/graphics/RectF.md), in the coordinates of the editor.

| Parameters ||
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the queried character. |
| `bounds` | [RectF](../android/graphics/RectF.md):the [RectF](../android/graphics/RectF.md) used to receive the result. This value cannot be`null`. |

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

- The [FLAG_CHARACTER_WHITESPACE](../android/view/inputmethod/TextBoundsInfo.md) flag, indicating the character is a whitespace.
- The [FLAG_CHARACTER_LINEFEED](../android/view/inputmethod/TextBoundsInfo.md) flag, indicating the character is a linefeed.
- The [FLAG_CHARACTER_PUNCTUATION](../android/view/inputmethod/TextBoundsInfo.md) flag, indicating the character is a punctuation.
- The [FLAG_LINE_IS_RTL](../android/view/inputmethod/TextBoundsInfo.md) flag, indicating the line this character belongs to has RTL line direction. All characters in the same line must have the same line direction. Check [getLineSegmentFinder()](../android/view/inputmethod/TextBoundsInfo.md))for more information of line boundaries.

<br />

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):the index of the queried character. |

| Return ||
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the flags associated with the queried character. Value is either`0`or a combination of [android.view.inputmethod.TextBoundsInfo#FLAG_CHARACTER_WHITESPACE](../android/view/inputmethod/TextBoundsInfo.md), [android.view.inputmethod.TextBoundsInfo#FLAG_CHARACTER_LINEFEED](../android/view/inputmethod/TextBoundsInfo.md), [android.view.inputmethod.TextBoundsInfo#FLAG_CHARACTER_PUNCTUATION](../android/view/inputmethod/TextBoundsInfo.md), and [android.view.inputmethod.TextBoundsInfo#FLAG_LINE_IS_RTL](../android/view/inputmethod/TextBoundsInfo.md) |

| Exceptions ||
|---------------------------------------|--------------------------------------------------------------------|
| `java.lang.IndexOutOfBoundsException` | if the given`index`is out of the range from the`start`to the`end`. |

**See Also**

- [#FLAG_CHARACTER_WHITESPACE](../android/view/inputmethod/TextBoundsInfo.md)
- [#FLAG_CHARACTER_LINEFEED](../android/view/inputmethod/TextBoundsInfo.md)
- [#FLAG_CHARACTER_PUNCTUATION](../android/view/inputmethod/TextBoundsInfo.md)
- [#FLAG_LINE_IS_RTL](../android/view/inputmethod/TextBoundsInfo.md) 

### getEndIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getEndIndex(): Int
```

Returns the index of the last character whose bounds information is available in this [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md), exclusive. 
**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setStartAndEnd(int, int)](../android/view/inputmethod/TextBoundsInfo.Builder.md)) 

### getGraphemeSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getGraphemeSegmentFinder(): SegmentFinder
```

Returns the [SegmentFinder](../android/text/SegmentFinder.md) that locates the grapheme boundaries.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SegmentFinder](../android/text/SegmentFinder.md) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setGraphemeSegmentFinder(SegmentFinder)](../android/view/inputmethod/TextBoundsInfo.Builder.md)) 

### getLineSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getLineSegmentFinder(): SegmentFinder
```

Returns the [SegmentFinder](../android/text/SegmentFinder.md) that locates the line boundaries.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SegmentFinder](../android/text/SegmentFinder.md) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setLineSegmentFinder(SegmentFinder)](../android/view/inputmethod/TextBoundsInfo.Builder.md)) 

### getMatrix

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getMatrix(matrix: Matrix): Unit
```

Set the given [android.graphics.Matrix](../android/graphics/Matrix.md) to be the transformation matrix that is to be applied other positional data in this class.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `matrix` | [Matrix](../android/graphics/Matrix.md):This value cannot be`null`. |

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

Return the index of the closest character to the given position. It's similar to the text layout API [Layout.getOffsetForHorizontal(int, float)](../android/text/Layout.md)). And it's mainly used to find the cursor index (the index of the character before which the cursor should be placed) for the given position. It's guaranteed that the returned index is a grapheme break. Check [getGraphemeSegmentFinder()](../android/view/inputmethod/TextBoundsInfo.md))for more information.

It's assumed that the editor lays out text in horizontal lines from top to bottom and each line is laid out according to the display algorithm specified in [unicode bidirectional algorithm](https://unicode.org/reports/tr9/#Basic_Display_Algorithm).

This method won't check the text ranges whose line information is missing. For example, the [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md)'s range is from index 5 to 15. If the associated [SegmentFinder](../android/text/SegmentFinder.md) only identifies one line range from 7 to 12. Then this method won't check the text in the ranges of \[5, 7) and \[12, 15).

Under the following conditions, this method will return -1 indicating that no valid character is found:

- The given`y`coordinate is above the first line or below the last line (the first line or the last line is identified by the [SegmentFinder](../android/text/SegmentFinder.md) returned from [getLineSegmentFinder()](../android/view/inputmethod/TextBoundsInfo.md))).
- There is no character in this [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md).

<br />

| Parameters ||
|-----|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| `x` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the x coordinates of the interested location, in the editor's coordinates. |
| `y` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):the y coordinates of the interested location, in the editor's coordinates. |

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the index of the character whose position is closest to the given location. It will return -1 if it can't find a character. |

**See Also**

- [android.text.Layout#getOffsetForHorizontal(int, float)](../android/text/Layout.md)) 

### getRangeForRect

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getRangeForRect(
    area: RectF, 
    segmentFinder: SegmentFinder, 
    inclusionStrategy: Layout.TextInclusionStrategy
): IntArray?
```

Finds the range of text which is inside the specified rectangle area. This method is a counterpart of the [Layout.getRangeForRect(RectF, SegmentFinder, Layout.TextInclusionStrategy)](../android/text/Layout.md)).

It's assumed that the editor lays out text in horizontal lines from top to bottom and each line is laid out according to the display algorithm specified in [unicode bidirectional algorithm](https://unicode.org/reports/tr9/#Basic_Display_Algorithm).

This method won't check the text ranges whose line information is missing. For example, the [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md)'s range is from index 5 to 15. If the associated line [SegmentFinder](../android/text/SegmentFinder.md) only identifies one line range from 7 to 12. Then this method won't check the text in the ranges of \[5, 7) and \[12, 15).

| Parameters ||
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `area` | [RectF](../android/graphics/RectF.md):area for which the text range will be found This value cannot be`null`. |
| `segmentFinder` | [SegmentFinder](../android/text/SegmentFinder.md):SegmentFinder for determining the ranges of text to be considered as a text segment This value cannot be`null`. |
| `inclusionStrategy` | [Layout.TextInclusionStrategy](../android/text/Layout.TextInclusionStrategy.md):strategy for determining whether a text segment is inside the specified area This value cannot be`null`. |
| --- | --- |

| Return ||
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html)? | the text range stored in a two element int array. The first element is the start (inclusive) of the text range, and the second element is the end (exclusive) character offsets of the text range, or null if there are no text segments inside the area. |

**See Also**

- [android.text.Layout#getRangeForRect(RectF, SegmentFinder, Layout.TextInclusionStrategy)](../android/text/Layout.md)) 

### getStartIndex

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getStartIndex(): Int
```

Returns the index of the first character whose bounds information is available in this [TextBoundsInfo](../android/view/inputmethod/TextBoundsInfo.md), inclusive. 
**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setStartAndEnd(int, int)](../android/view/inputmethod/TextBoundsInfo.Builder.md)) 

### getWordSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
fun getWordSegmentFinder(): SegmentFinder
```

Returns the [SegmentFinder](../android/text/SegmentFinder.md) that locates the word boundaries.

| Return ||
|--------------------------------------------------------------------------------------------------|-----------------------------|
| [SegmentFinder](../android/text/SegmentFinder.md) | This value cannot be`null`. |

**See Also**

- [android.view.inputmethod.TextBoundsInfo.Builder#setWordSegmentFinder(SegmentFinder)](../android/view/inputmethod/TextBoundsInfo.Builder.md)) 

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
| `dest` | [Parcel](../android/os/Parcel.md):The Parcel in which the object should be written. This value cannot be`null`. |
| `flags` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Additional flags about how the object should be written. May be 0 or [PARCELABLE_WRITE_RETURN_VALUE](../android/os/Parcelable.md). |

## Properties

### CREATOR

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val CREATOR: Parcelable.Creator<TextBoundsInfo!>
```

The CREATOR to make this class Parcelable.
