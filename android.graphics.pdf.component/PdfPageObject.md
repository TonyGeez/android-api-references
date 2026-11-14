Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageObject

Kotlin | [Java](PdfPageObject.md)
| --- | --- |

```
abstract class PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) ||
| --- | --- |
| ↳ | [android.graphics.pdf.component.PdfPageObject](PdfPageObject.md) |

| Known Direct Subclasses [PdfPageImageObject](PdfPageImageObject.md), [PdfPagePathObject](PdfPagePathObject.md), [PdfPageTextObject](PdfPageTextObject.md) |---|---| | [PdfPageImageObject](PdfPageImageObject.md) | Represents an image object on a PDF page. | | [PdfPagePathObject](PdfPagePathObject.md) | Represents a path object on a PDF page. | | [PdfPageTextObject](PdfPageTextObject.md) | Represents a text object on a PDF page. | |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

Represents a page object on a page of a pdf document. This abstract class provides a base implementation for different types of PDF page objects.

## Summary

| Public methods ||
|---|---|
| open [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#getMatrix()()` Returns the transformation matrix of the object. |
| open [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#getPdfObjectType()()` Returns the type of the page object. |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#setMatrix(android.graphics.Matrix)(matrix: https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)` Sets the transformation matrix of the object. |
| --- | --- |
| open [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | `https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#transform(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float)(a: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, b: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, c: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, d: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, e: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html, f: https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)` Transform the page object The matrix is composed as: |a c e| |b d f| and can be used to scale, rotate, shear and translate the |page_object|. |

## Public methods

### getMatrix

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
open fun getMatrix(): FloatArray
```

Returns the transformation matrix of the object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html` | The transformation matrix of the object. This value cannot be `null`. |

### getPdfObjectType

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
open fun getPdfObjectType(): Int
```

Returns the type of the page object.

| Return ||
|---|---|
| `https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html` | The type of the page object. |

### setMatrix

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
open fun setMatrix(matrix: Matrix): Unit
```

Sets the transformation matrix of the object.

| Parameters ||
|---|---|
| `matrix` | [Matrix](../android.graphics/Matrix.md): The transformation matrix of the object. This value cannot be `null`. |

### transform

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

```
open fun transform(
    a: Float, 
    b: Float, 
    c: Float, 
    d: Float, 
    e: Float, 
    f: Float
): Unit
```

Transform the page object The matrix is composed as: |a c e| |b d f| and can be used to scale, rotate, shear and translate the |page_object|.
| --- | --- | --- | --- | --- | --- | --- |
