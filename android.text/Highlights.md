# Highlights

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Highlights

Kotlin| [Java](https://developer.android.com/reference/android/text/Highlights "View this page in Java") 

```
open class Highlights
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.text.Highlights](https://developer.android.com/reference/kotlin/android/text/Highlights#) |

A class that represents of the highlight of the text.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Builder](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder) A builder for the Highlights. |

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) | [getPaint](https://developer.android.com/reference/kotlin/android/text/Highlights#getPaint(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a paint used for the i-th highlight. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getRanges](https://developer.android.com/reference/kotlin/android/text/Highlights#getRanges(kotlin.Int))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns ranges of the i-th highlight. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](https://developer.android.com/reference/kotlin/android/text/Highlights#getSize())`()` Returns the number of highlight. |

## Public methods

### getPaint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPaint(index: Int): Paint
```

Returns a paint used for the i-th highlight.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index of the highlight. Must be between 0 and [getSize()](https://developer.android.com/reference/kotlin/android/text/Highlights#getSize()) |

| Return ||
|--------------------------------------------------------------------------------------|------------------|
| [Paint](https://developer.android.com/reference/kotlin/android/graphics/Paint.html#) | the paint object |

**See Also**

- [android.text.Highlights.Builder#addRange(Paint, int, int)](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder#addRange(android.graphics.Paint,%20kotlin.Int,%20kotlin.Int))
- [android.text.Highlights.Builder#addRanges(Paint, int...)](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder#addRanges(android.graphics.Paint,%20kotlin.Int)) 

### getRanges

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRanges(index: Int): IntArray
```

Returns ranges of the i-th highlight. Ranges are represented of flattened inclusive start and exclusive end integers array. The inclusive start offset of the`i`-th range is stored in`2 * i`-th of the array. The exclusive end offset of the`i`-th range is stored in`2* i + 1`-th of the array. For example, the two ranges: (1, 2) and (3, 4) are flattened into single int array \[1, 2, 3, 4\].

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index of the highlight. Must be between 0 and [getSize()](https://developer.android.com/reference/kotlin/android/text/Highlights#getSize()) |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the flattened ranges. |

**See Also**

- [android.text.Highlights.Builder#addRange(Paint, int, int)](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder#addRange(android.graphics.Paint,%20kotlin.Int,%20kotlin.Int))
- [android.text.Highlights.Builder#addRanges(Paint, int...)](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder#addRanges(android.graphics.Paint,%20kotlin.Int)) 

### getSize

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getSize(): Int
```

Returns the number of highlight.

| Return ||
|----------------------------------------------------------------------------|--------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | the number of highlight. |

**See Also**

- [android.text.Highlights.Builder#addRange(Paint, int, int)](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder#addRange(android.graphics.Paint,%20kotlin.Int,%20kotlin.Int))
- [android.text.Highlights.Builder#addRanges(Paint, int...)](https://developer.android.com/reference/kotlin/android/text/Highlights.Builder#addRanges(android.graphics.Paint,%20kotlin.Int))
