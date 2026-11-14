Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GraphemeClusterSegmentFinder

Kotlin | [Java](GraphemeClusterSegmentFinder.md)
| --- | --- |

```
open class GraphemeClusterSegmentFinder : SegmentFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.SegmentFinder](SegmentFinder.md) ||
| | ↳ | [android.text.GraphemeClusterSegmentFinder](GraphemeClusterSegmentFinder.md) |

Implementation of `SegmentFinder` using grapheme clusters as the text segment. Whitespace characters are included as segments.

For example, the text "a pot" would be divided into five text segments: "a", " ", "p", "o", "t".

## Summary

| Inherited constants ||
|---|---|
| From class SegmentFinder |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/SegmentFinder#DONE:kotlin.Int` Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. <br /> | ||

| Public constructors ||
|---|---|
| GraphemeClusterSegmentFinder Constructs a GraphemeClusterSegmentFinder instance for the specified text which uses the provided TextPaint to determine grapheme cluster boundaries. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | nextEndBoundary Returns the character offset of the next text segment end boundary after the specified character offset, or `DONE` if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | nextStartBoundary Returns the character offset of the next text segment start boundary after the specified character offset, or `DONE` if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | previousEndBoundary Returns the character offset of the previous text segment end boundary before the specified character offset, or `DONE` if there are none. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | previousStartBoundary Returns the character offset of the previous text segment start boundary before the specified character offset, or `DONE` if there are none. |

## Public constructors

### GraphemeClusterSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
GraphemeClusterSegmentFinder(
    text: CharSequence, 
    textPaint: TextPaint)
```

Constructs a GraphemeClusterSegmentFinder instance for the specified text which uses the provided TextPaint to determine grapheme cluster boundaries.

| Parameters ||
|---|---|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html): text to be segmented. This value cannot be `null`. |
| `textPaint` | [TextPaint](TextPaint.md): TextPaint used to draw the text. This value cannot be `null`. |

## Public methods

### nextEndBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextEndBoundary(offset: Int): Int
```

Returns the character offset of the next text segment end boundary after the specified character offset, or `DONE` if there are none.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

### nextStartBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun nextStartBoundary(offset: Int): Int
```

Returns the character offset of the next text segment start boundary after the specified character offset, or `DONE` if there are none.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

### previousEndBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun previousEndBoundary(offset: Int): Int
```

Returns the character offset of the previous text segment end boundary before the specified character offset, or `DONE` if there are none.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |

### previousStartBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

```
open fun previousStartBoundary(offset: Int): Int
```

Returns the character offset of the previous text segment start boundary before the specified character offset, or `DONE` if there are none.

| Parameters ||
|---|---|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): Value is 0 or greater |
