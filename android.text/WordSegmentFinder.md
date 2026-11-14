# WordSegmentFinder

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# WordSegmentFinder

Kotlin| [Java](../android/text/WordSegmentFinder.md) 
| --- | --- |

```
open class WordSegmentFinder : SegmentFinder
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.text.SegmentFinder](../android/text/SegmentFinder.md) ||
| | ↳ | [android.text.WordSegmentFinder](../android/text/WordSegmentFinder.md) |

Implementation of [SegmentFinder](../android/text/SegmentFinder.md) using words as the text segment. Word boundaries are found using`WordIterator`. Whitespace characters are excluded, so they are not included in any text segments.

For example, the text "Hello, World!" would be subdivided into four text segments: "Hello", ",", "World", "!". The space character does not belong to any text segments.

## Summary

| Inherited constants ||
|---|---|
| From class [SegmentFinder](../android/text/SegmentFinder.md) |----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [DONE](../android/text/SegmentFinder.md) <br /> Return value of previousStartBoundary(int), previousEndBoundary(int), nextStartBoundary(int), and nextEndBoundary(int) when there are no boundaries of the specified type in the specified direction. <br /> | ||

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [WordSegmentFinder](../android/text/WordSegmentFinder.md))`(`text:` ` [CharSequence](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-char-sequence/index.html)`, `locale:` ` [ULocale](../android/icu/util/ULocale.md)`)` Constructs a WordSegmentFinder instance for the specified text which uses the provided locale to determine word boundaries. |

| Public methods ||
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextEndBoundary](../android/text/WordSegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment end boundary after the specified character offset, or`DONE`if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [nextStartBoundary](../android/text/WordSegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the next text segment start boundary after the specified character offset, or`DONE`if there are none. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousEndBoundary](../android/text/WordSegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment end boundary before the specified character offset, or`DONE`if there are none. |
| --- | --- |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [previousStartBoundary](../android/text/WordSegmentFinder.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the character offset of the previous text segment start boundary before the specified character offset, or`DONE`if there are none. |

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
| `locale` | [ULocale](../android/icu/util/ULocale.md):locale used for analyzing the text This value cannot be`null`. |

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
