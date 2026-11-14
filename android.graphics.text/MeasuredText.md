# MeasuredText

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels)

# MeasuredText

Kotlin| [Java](../android/graphics/text/MeasuredText.md) 
| --- | --- |

```
open class MeasuredText
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.text.MeasuredText](../android/graphics/text/MeasuredText.md) |

Result of text shaping of the single paragraph string.

<br />

```kotlin
<code>
  Paint paint = new Paint();
  Paint bigPaint = new Paint();
  bigPaint.setTextSize(paint.getTextSize() * 2.0);
  String text = "Hello, Android.";
  MeasuredText mt = new MeasuredText.Builder(text.toCharArray())
       .appendStyleRun(paint, 7, false)  // Use paint for "Hello, "
       .appendStyleRun(bigPaint, 8, false)  // Use bigPaint for "Android."
       .build();
  </code>
```

<br />

## Summary

| Nested classes ||
|---|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| | [Builder](../android/graphics/text/MeasuredText.Builder.md) Helper class for creating a [MeasuredText](../android/graphics/text/MeasuredText.md). |

| Public methods ||
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getBounds](../android/graphics/text/MeasuredText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `rect:` ` [Rect](../android/graphics/Rect.md)`)` Retrieves the boundary box of the given range |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getCharWidthAt](../android/graphics/text/MeasuredText.md))`(`offset:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the width of the character at the given offset. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [getFontMetricsInt](../android/graphics/text/MeasuredText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `outMetrics:` ` [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md)`)` Retrieves the font metrics of the given range |
| --- | --- |
| open [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getWidth](../android/graphics/text/MeasuredText.md))`(`start:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`, `end:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Returns the width of a given range. |

## Public methods

### getBounds

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getBounds(
    start: Int, 
    end: Int, 
    rect: Rect
): Unit
```

Retrieves the boundary box of the given range

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an inclusive start index of the range Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an exclusive end index of the range Value is 0 or greater |
| `rect` | [Rect](../android/graphics/Rect.md):an output parameter This value cannot be`null`. |
| --- | --- |

### getCharWidthAt

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getCharWidthAt(offset: Int): Float
```

Returns the width of the character at the given offset. 
The units of this value are pixels.

| Parameters ||
|----------|------------------------------------------------------------------------------------------------------------------------------|
| `offset` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an offset of the character. Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is 0.0f or greater The units of this value are pixels. |

### getFontMetricsInt

Added in [API level 33](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getFontMetricsInt(
    start: Int, 
    end: Int, 
    outMetrics: Paint.FontMetricsInt
): Unit
```

Retrieves the font metrics of the given range

| Parameters ||
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an inclusive start index of the range Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an exclusive end index of the range Value is 0 or greater |
| `outMetrics` | [Paint.FontMetricsInt](../android/graphics/Paint.FontMetricsInt.md):an output metrics object This value cannot be`null`. |
| --- | --- |

### getWidth

Added in [API level 29](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 

```
open fun getWidth(
    start: Int, 
    end: Int
): Float
```

Returns the width of a given range. 
The units of this value are pixels.

| Parameters ||
|---------|----------------------------------------------------------------------------------------------------------------------------------------|
| `start` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an inclusive start index of the range Value is 0 or greater |
| `end` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):an exclusive end index of the range Value is 0 or greater |

| Return ||
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | Value is 0.0f or greater The units of this value are pixels. |
