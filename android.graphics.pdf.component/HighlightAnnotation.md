Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# HighlightAnnotation

Kotlin | [Java](HighlightAnnotation.md)
| --- | --- |

```
class HighlightAnnotation : PdfAnnotation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfAnnotation](PdfAnnotation.md) ||
| | ↳ | [android.graphics.pdf.component.HighlightAnnotation](HighlightAnnotation.md) |

Represents a highlight annotation in a PDF document.

If the highlight color is not explicitly set using #setColor(android.graphics.Color), the default color is yellow.

## Summary

| Public constructors ||
|---|---|
| HighlightAnnotation Creates a new highlight annotation with the specified bounds list. |

| Public methods ||
|---|---|
| [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android.graphics/RectF.md)!\> | getBoundsList Returns the bounding rectangles of the highlight annotation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | getColor Returns the highlight color of the annotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setBoundsList Sets the bounding rectangles of the highlight annotation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | setColor Sets the highlight color of the annotation. |

| Inherited functions ||
|---|---|
| From class PdfAnnotation |---|---| | `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | getPdfAnnotationType Returns the type of the annotation. <br /> | ||

## Public constructors

### HighlightAnnotation

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
HighlightAnnotation(boundsList: MutableList<RectF!>)
```

Creates a new highlight annotation with the specified bounds list.

The default highlight color is yellow

| Parameters ||
|---|---|
| `boundsList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android.graphics/RectF.md)!\>: The bounding rectangle of the annotation. This value cannot be `null`. |

## Public methods

### getBoundsList

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun getBoundsList(): MutableList<RectF!>
```

Returns the bounding rectangles of the highlight annotation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html<https://developer.android.com/reference/kotlin/android/graphics/RectF.html#!>` | The bounding rectangles. This value cannot be `null`. |

### getColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun getColor(): Int
```

Returns the highlight color of the annotation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The highlight color. |

### setBoundsList

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun setBoundsList(boundsList: MutableList<RectF!>): Unit
```

Sets the bounding rectangles of the highlight annotation. Each rect in the list mBoundsList represent an absolute position of highlight inside the page of the document

| Parameters ||
|---|---|
| `boundsList` | [MutableList](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-mutable-list/index.html)\< [RectF](../android.graphics/RectF.md)!\>: The new bounding rectangles. This value cannot be `null`. |

| Exceptions ||
|---|---|
| `java.lang.IllegalArgumentException` | if the given bounds list is empty |

### setColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
fun setColor(color: Int): Unit
```

Sets the highlight color of the annotation.

| Parameters ||
|---|---|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html): The new highlight color. |
