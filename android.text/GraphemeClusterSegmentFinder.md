Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# GraphemeClusterSegmentFinder

Kotlin | [Java](https://developer.android.com/reference/android/text/GraphemeClusterSegmentFinder "View this page in Java")
| --- | --- |

```
open class GraphemeClusterSegmentFinder : SegmentFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder) ||
| | ↳ | [android.text.GraphemeClusterSegmentFinder](https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder#) |

Implementation of `SegmentFinder` using grapheme clusters as the text segment. Whitespace characters are included as segments.

For example, the text "a pot" would be divided into five text segments: "a", " ", "p", "o", "t".

## Summary

| Inherited constants ||
|---|---|
| From class `https://developer.android.com/reference/kotlin/android/text/SegmentFinder` |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | `https://developer.android.com/reference/kotlin/android/text/SegmentFinder#DONE:kotlin.Int` Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. <br /> | ||

| Public constructors ||
|---|---|
| `https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder#GraphemeClusterSegmentFinder(kotlin.CharSequence,%20android.text.TextPaint)(text: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html, textPaint: https://developer.android.com/reference/kotlin/android/text/TextPaint)` Constructs a GraphemeClusterSegmentFinder instance for the specified text which uses the provided TextPaint to determine grapheme cluster boundaries. |

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder#nextEndBoundary(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character offset of the next text segment end boundary after the specified character offset, or `DONE` if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder#nextStartBoundary(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character offset of the next text segment start boundary after the specified character offset, or `DONE` if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder#previousEndBoundary(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character offset of the previous text segment end boundary before the specified character offset, or `DONE` if there are none. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/text/GraphemeClusterSegmentFinder#previousStartBoundary(kotlin.Int)(offset: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)` Returns the character offset of the previous text segment start boundary before the specified character offset, or `DONE` if there are none. |

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
| `textPaint` | [TextPaint](https://developer.android.com/reference/kotlin/android/text/TextPaint): TextPaint used to draw the text. This value cannot be `null`. |

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
