# SegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# SegmentFinder

Kotlin| [Java](SegmentFinder.md) 
| --- | --- |

```
abstract class SegmentFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.SegmentFinder](SegmentFinder.md) |

| Known Direct Subclasses [GraphemeClusterSegmentFinder](GraphemeClusterSegmentFinder.md), [SegmentFinder.PrescribedSegmentFinder](../android/text/SegmentFinder.PrescribedSegmentFinder.md), [WordSegmentFinder](WordSegmentFinder.md) |--------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------| | [GraphemeClusterSegmentFinder](GraphemeClusterSegmentFinder.md) | Implementation of`SegmentFinder`using grapheme clusters as the text segment. | | [SegmentFinder.PrescribedSegmentFinder](../android/text/SegmentFinder.PrescribedSegmentFinder.md) | The default [SegmentFinder](SegmentFinder.md) implementation based on given segment ranges. | | [WordSegmentFinder](WordSegmentFinder.md) | Implementation of [SegmentFinder](SegmentFinder.md) using words as the text segment. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Finds text segment boundaries within text. Subclasses can implement different types of text segments. Grapheme clusters and words are examples of possible text segments. These are implemented by [GraphemeClusterSegmentFinder](GraphemeClusterSegmentFinder.md) and [WordSegmentFinder](WordSegmentFinder.md).

Text segments may not overlap, so every character belongs to at most one text segment. A character may belong to no text segments.

For example, WordSegmentFinder subdivides the text "Hello, World!" into four text segments: "Hello", ",", "World", "!". The space character does not belong to any text segments.

## Summary

| Nested classes ||
|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open | [PrescribedSegmentFinder](../android/text/SegmentFinder.PrescribedSegmentFinder.md) The default [SegmentFinder](SegmentFinder.md) implementation based on given segment ranges. |

| Constants ||
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](SegmentFinder.md) Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. |

| Public constructors ||
|-----------------------------------------------------------------------------------------------------------------------|---|
| [SegmentFinder](SegmentFinder.md))`()` <br /> |

| Public methods ||
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextEndBoundary](SegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment end boundary after the specified character offset, or`DONE`if there are none. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextStartBoundary](SegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment start boundary after the specified character offset, or`DONE`if there are none. |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousEndBoundary](SegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment end boundary before the specified character offset, or`DONE`if there are none. |
| --- | --- |
| abstract [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousStartBoundary](SegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment start boundary before the specified character offset, or`DONE`if there are none. |

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
