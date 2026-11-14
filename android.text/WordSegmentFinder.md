# WordSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WordSegmentFinder

Kotlin| [Java](https://developer.android.com/reference/android/text/WordSegmentFinder "View this page in Java") 
| --- | --- |

```
open class WordSegmentFinder : SegmentFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder) ||
| | ↳ | [android.text.WordSegmentFinder](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder#) |

Implementation of [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder) using words as the text segment. Word boundaries are found using`WordIterator`. Whitespace characters are excluded, so they are not included in any text segments.

For example, the text "Hello, World!" would be subdivided into four text segments: "Hello", ",", "World", "!". The space character does not belong to any text segments.

## Summary

| Inherited constants ||
|---|---|
| From class [SegmentFinder](https://developer.android.com/reference/kotlin/android/text/SegmentFinder) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](https://developer.android.com/reference/kotlin/android/text/SegmentFinder#DONE:kotlin.Int) <br /> Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WordSegmentFinder](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder#WordSegmentFinder(kotlin.CharSequence,%20android.icu.util.ULocale))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `locale:` ` [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#)`)` Constructs a WordSegmentFinder instance for the specified text which uses the provided locale to determine word boundaries. |

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextEndBoundary](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder#nextEndBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment end boundary after the specified character offset, or`DONE`if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextStartBoundary](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder#nextStartBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment start boundary after the specified character offset, or`DONE`if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousEndBoundary](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder#previousEndBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment end boundary before the specified character offset, or`DONE`if there are none. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousStartBoundary](https://developer.android.com/reference/kotlin/android/text/WordSegmentFinder#previousStartBoundary(kotlin.Int))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment start boundary before the specified character offset, or`DONE`if there are none. |

## Public constructors

### WordSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
WordSegmentFinder(
    text: CharSequence, 
    locale: ULocale)
```

Constructs a WordSegmentFinder instance for the specified text which uses the provided locale to determine word boundaries.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html):text to be segmented This value cannot be`null`. |
| `locale` | [ULocale](https://developer.android.com/reference/kotlin/android/icu/util/ULocale.html#):locale used for analyzing the text This value cannot be`null`. |

## Public methods

### nextEndBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextEndBoundary(offset: Int): Int
```

Returns the character offset of the next text segment end boundary after the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### nextStartBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun nextStartBoundary(offset: Int): Int
```

Returns the character offset of the next text segment start boundary after the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### previousEndBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousEndBoundary(offset: Int): Int
```

Returns the character offset of the previous text segment end boundary before the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |

### previousStartBoundary

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun previousStartBoundary(offset: Int): Int
```

Returns the character offset of the previous text segment start boundary before the specified character offset, or`DONE`if there are none.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):Value is 0 or greater |
