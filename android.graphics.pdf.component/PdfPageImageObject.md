# PdfPageImageObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageImageObject

Kotlin| [Java](PdfPageImageObject.md) 
| --- | --- |

```
class PdfPageImageObject : PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfPageObject](PdfPageObject.md) ||
| | ↳ | [android.graphics.pdf.component.PdfPageImageObject](PdfPageImageObject.md) |

Represents an image object on a PDF page. This class extends [PdfPageObject](PdfPageObject.md) and provides methods to access and modify the image content.

## Summary

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageImageObject](PdfPageImageObject.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)`)` Constructor for the PdfPageImageObject. |

| Public methods ||
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bitmap](../android.graphics/Bitmap.md) | [getBitmap](PdfPageImageObject.md))`()` Returns the bitmap image of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBitmap](PdfPageImageObject.md))`(`bitmap:` ` [Bitmap](../android.graphics/Bitmap.md)`)` Sets the bitmap image of the object. |

| Inherited functions ||
|---|---|
| From class [PdfPageObject](PdfPageObject.md) |-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getMatrix](PdfPageObject.md))`()` <br /> Returns the transformation matrix of the object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfObjectType](PdfPageObject.md))`()` <br /> Returns the type of the page object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatrix](PdfPageObject.md))`(`matrix:` ` [Matrix](../android.graphics/Matrix.md)`)` <br /> Sets the transformation matrix of the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transform](PdfPageObject.md))`(`a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `c:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `d:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `e:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Transform the page object The matrix is composed as: |a c e| |b d f| and can be used to scale, rotate, shear and translate the |page_object|. <br /> | ||

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
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md):This value cannot be`null`. |

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
| [Bitmap](../android.graphics/Bitmap.md) | The bitmap image of the object. This value cannot be`null`. |

### setBitmap

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setBitmap(bitmap: Bitmap): Unit
```

Sets the bitmap image of the object.

| Parameters ||
|----------|---------------------------------------------------------------------------------------------------------------------------------------------|
| `bitmap` | [Bitmap](../android.graphics/Bitmap.md):The bitmap image to set. This value cannot be`null`. |

| Exceptions ||
|--------------------------------------|------------------------------------|
| `java.lang.IllegalArgumentException` | if bitmap config is not ARGB_8888. |
