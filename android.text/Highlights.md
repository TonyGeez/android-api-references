# Highlights

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# Highlights

Kotlin| [Java](../android/text/Highlights.md) 
| --- | --- |

```
open class Highlights
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.text.Highlights](../android/text/Highlights.md) |

A class that represents of the highlight of the text.

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/text/Highlights.Builder.md) A builder for the Highlights. |

| Public methods ||
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Paint](../android/graphics/Paint.md) | [getPaint](../android/text/Highlights.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns a paint used for the i-th highlight. |
| open [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | [getRanges](../android/text/Highlights.md))`(`index:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns ranges of the i-th highlight. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getSize](../android/text/Highlights.md))`()` Returns the number of highlight. |
| --- | --- |

## Public methods

### getPaint

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getPaint(index: Int): Paint
```

Returns a paint used for the i-th highlight.

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index of the highlight. Must be between 0 and [getSize()](../android/text/Highlights.md)) |

| Return ||
|--------------------------------------------------------------------------------------|------------------|
| [Paint](../android/graphics/Paint.md) | the paint object |

**See Also**

- [android.text.Highlights.Builder#addRange(Paint, int, int)](../android/text/Highlights.Builder.md))
- [android.text.Highlights.Builder#addRanges(Paint, int...)](../android/text/Highlights.Builder.md)) 

### getRanges

Added in [API level 34](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getRanges(index: Int): IntArray
```

Returns ranges of the i-th highlight. Ranges are represented of flattened inclusive start and exclusive end integers array. The inclusive start offset of the`i`-th range is stored in`2 * i`-th of the array. The exclusive end offset of the`i`-th range is stored in`2* i + 1`-th of the array. For example, the two ranges: (1, 2) and (3, 4) are flattened into single int array \[1, 2, 3, 4\].

| Parameters ||
|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `index` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an index of the highlight. Must be between 0 and [getSize()](../android/text/Highlights.md)) |

| Return ||
|---------------------------------------------------------------------------------------|-----------------------|
| [IntArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int-array/index.html) | the flattened ranges. |

**See Also**

- [android.text.Highlights.Builder#addRange(Paint, int, int)](../android/text/Highlights.Builder.md))
- [android.text.Highlights.Builder#addRanges(Paint, int...)](../android/text/Highlights.Builder.md)) 

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

- [android.text.Highlights.Builder#addRange(Paint, int, int)](../android/text/Highlights.Builder.md))
- [android.text.Highlights.Builder#addRanges(Paint, int...)](../android/text/Highlights.Builder.md))
