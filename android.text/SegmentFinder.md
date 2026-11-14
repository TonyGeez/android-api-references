# SegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SegmentFinder

Kotlin| [Java](https://developer.android.com/reference/android/text/SegmentFinder "View this page in Java") 

```
abstract class SegmentFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#) |

| Known Direct Subclasses [GraphemeClusterSegmentFinder](https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder), [SegmentFinder.PrescribedSegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.PrescribedSegmentFinder), [WordSegmentFinder](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder) |--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------| | [GraphemeClusterSegmentFinder](https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder) | Implementation of`SegmentFinder`using grapheme clusters as the text segment. | | [SegmentFinder.PrescribedSegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.PrescribedSegmentFinder) | The default [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#) implementation based on given segment ranges. | | [WordSegmentFinder](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder) | Implementation of [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#) using words as the text segment. | |

Finds text segment boundaries within text. Subclasses can implement different types of text segments. Grapheme clusters and words are examples of possible text segments. These are implemented by [GraphemeClusterSegmentFinder](https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder) and [WordSegmentFinder](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder).

Text segments may not overlap, so every character belongs to at most one text segment. A character may belong to no text segments.

For example, WordSegmentFinder subdivides the text "Hello, World!" into four text segments: "Hello", ",", "World", "!". The space character does not belong to any text segments.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PrescribedSegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder.PrescribedSegmentFinder) The default [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#) implementation based on given segment ranges. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#DONE:kotlin.Int) Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------|---|
| [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#SegmentFinder())`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextEndBoundary](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#nextEndBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment end boundary after the specified character offset, or`DONE`if there are none. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextStartBoundary](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#nextStartBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment start boundary after the specified character offset, or`DONE`if there are none. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousEndBoundary](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#previousEndBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment end boundary before the specified character offset, or`DONE`if there are none. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousStartBoundary](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#previousStartBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment start boundary before the specified character offset, or`DONE`if there are none. |

## Constants

### DONE

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
static val DONE: Int
```

Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. 

 Value: -1

## Public constructors

### SegmentFinder

```
SegmentFinder()
```

## Public methods

### nextEndBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextEndBoundary(offset: Int): Int
```

Returns the character offset of the next text segment end boundary after the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### nextStartBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun nextStartBoundary(offset: Int): Int
```

Returns the character offset of the next text segment start boundary after the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### previousEndBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previousEndBoundary(offset: Int): Int
```

Returns the character offset of the previous text segment end boundary before the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### previousStartBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
abstract fun previousStartBoundary(offset: Int): Int
```

Returns the character offset of the previous text segment start boundary before the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |
