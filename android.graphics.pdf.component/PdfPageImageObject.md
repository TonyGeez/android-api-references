# PdfPageImageObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageImageObject

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/component/PdfPageImageObject "View this page in Java") 
| --- | --- |

```
class PdfPageImageObject : PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) ||
| | ↳ | [android.graphics.pdf.component.PdfPageImageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject#) |

Represents an image object on a PDF page. This class extends [PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) and provides methods to access and modify the image content.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageImageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject#PdfPageImageObject(android.graphics.Bitmap))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`)` Constructor for the PdfPageImageObject. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | [getBitmap](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject#getBitmap())`()` Returns the bitmap image of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBitmap](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageImageObject#setBitmap(android.graphics.Bitmap))`(`bitmap:` ` [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#)`)` Sets the bitmap image of the object. |

| Inherited functions ||
|---|---|
| From class [PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) |-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getMatrix](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#getMatrix())`()` <br /> Returns the transformation matrix of the object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfObjectType](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#getPdfObjectType())`()` <br /> Returns the type of the page object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatrix](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#setMatrix(android.graphics.Matrix))`(`matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)`)` <br /> Sets the transformation matrix of the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transform](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#transform(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `c:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `d:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `e:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Transform the page object The matrix is composed as: |a c e| |b d f| and can be used to scale, rotate, shear and translate the |page_object|. <br /> | ||

## Public constructors

### PdfPageImageObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
PdfPageImageObject(bitmap: Bitmap)
```

Constructor for the PdfPageImageObject. Sets the object type to IMAGE.

| Parameters ||
|----------|--------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if bitmap config is not ARGB_8888. |

## Public methods

### getBitmap

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getBitmap(): Bitmap
```

Returns the bitmap image of the object.

| Return ||
|----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#) | The bitmap image of the object. This value cannot be`null`. |

### setBitmap

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setBitmap(bitmap: Bitmap): Unit
```

Sets the bitmap image of the object.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](https://developer.android.com/reference/kotlin/android/graphics/Bitmap.html#):The bitmap image to set. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if bitmap config is not ARGB_8888. |
