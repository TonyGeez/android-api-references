Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfAnnotation

Kotlin | [Java](https://developer.android.com/reference/android/graphics/pdf/component/PdfAnnotation "View this page in Java")

```
abstract class PdfAnnotation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| ↳ | [android.graphics.pdf.component.PdfAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation#) |

| Known Direct Subclasses [FreeTextAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation), [HighlightAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/HighlightAnnotation), [StampAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation) |---|---| | [FreeTextAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation) | Represents a free text annotation in a PDF document. | | [HighlightAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/HighlightAnnotation) | Represents a highlight annotation in a PDF document. | | [StampAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/StampAnnotation) | Represents a stamp annotation in a PDF document. | |

Represents a PDF annotation on a page of a PDF document. This abstract class provides a base implementation for different types of PDF annotations such as text (`https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation`), highlight (`https://developer.android.com/reference/kotlin/android/graphics/pdf/component/HighlightAnnotation`) etc

## Summary

| Public methods ||
|---|---|
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation#getPdfAnnotationType()()` Returns the type of the annotation. |

## Public methods

### getPdfAnnotationType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
open fun getPdfAnnotationType(): Int
```

Returns the type of the annotation.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The annotation type. See `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotationType` for possible values. Value is one of the following: - `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotationType#UNKNOWN:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotationType#FREETEXT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotationType#HIGHLIGHT:kotlin.Int` - `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotationType#STAMP:kotlin.Int` |
