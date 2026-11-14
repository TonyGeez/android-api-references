# FreeTextAnnotation

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# FreeTextAnnotation

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/component/FreeTextAnnotation "View this page in Java") 
| --- | --- |

```
class FreeTextAnnotation : PdfAnnotation
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation) ||
| | ↳ | [android.graphics.pdf.component.FreeTextAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#) |

Represents a free text annotation in a PDF document.

This class allows creating and manipulating free text annotations. A free text annotation in a PDF is a type of annotation that allows you to add text directly onto the page.

If text color is not set using [setTextColor(int)](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#setTextColor(kotlin.Int)), the default text color is black and if the background color is not set using [setBackgroundColor(int)](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#setBackgroundColor(kotlin.Int)), the default background color is white.

## Summary

| Public constructors ||
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [FreeTextAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#FreeTextAnnotation(android.graphics.RectF,%20kotlin.String))`(`bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)`, `textContent:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Creates a new free text annotation with the specified bounds and text content. |

| Public methods ||
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getBackgroundColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#getBackgroundColor())`()` Returns the background color of the freetext annotation. |
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) | [getBounds](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#getBounds())`()` Returns the bounding rectangle of the freetext annotation. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getTextColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#getTextColor())`()` Returns the text color of the freetext annotation. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#getTextContent())`()` Returns the text content of the freetext annotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBackgroundColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#setBackgroundColor(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the background color of the freetext annotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setBounds](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#setBounds(android.graphics.RectF))`(`bounds:` ` [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#)`)` Sets the bounding rectangle of the freetext annotation. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#setTextColor(kotlin.Int))`(`color:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the text color of the annotation. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setTextContent](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/FreeTextAnnotation#setTextContent(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the text content of the annotation. |

| Inherited functions ||
|---|---|
| From class [PdfAnnotation](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation) |----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfAnnotationType](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfAnnotation#getPdfAnnotationType())`()` <br /> Returns the type of the annotation. <br /> | ||

## Public constructors

### FreeTextAnnotation

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
FreeTextAnnotation(
    bounds: RectF, 
    textContent: String)
```

Creates a new free text annotation with the specified bounds and text content.

The default text color and background color will be black and white respectively. Also, transparency of the text color can't be modified i.e. alpha value of the text color will always be 1

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#):The bounding rectangle of the annotation. This value cannot be`null`. |
| `textContent` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text content of the annotation This value cannot be`null`. |

## Public methods

### getBackgroundColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getBackgroundColor(): Int
```

Returns the background color of the freetext annotation.

| Return ||
|----------------------------------------------------------------------------|-----------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The background color. |

### getBounds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getBounds(): RectF
```

Returns the bounding rectangle of the freetext annotation.

| Return ||
|--------------------------------------------------------------------------------------|-----------------------------------------------------|
| [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#) | The bounding rectangle. This value cannot be`null`. |

### getTextColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getTextColor(): Int
```

Returns the text color of the freetext annotation.

| Return ||
|----------------------------------------------------------------------------|-----------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The text color. |

### getTextContent

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getTextContent(): String
```

Returns the text content of the freetext annotation.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The text content. This value cannot be`null`. |

### setBackgroundColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setBackgroundColor(color: Int): Unit
```

Sets the background color of the freetext annotation.

| Parameters ||
|---------|------------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new background color. |

### setBounds

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setBounds(bounds: RectF): Unit
```

Sets the bounding rectangle of the freetext annotation.

| Parameters ||
|----------|----------------------------------------------------------------------------------------------------------------------------------------------|
| `bounds` | [RectF](https://developer.android.com/reference/kotlin/android/graphics/RectF.html#):The new bounding rectangle. This value cannot be`null`. |

### setTextColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setTextColor(color: Int): Unit
```

Sets the text color of the annotation.

Please note that the transparency of the color can't be modified. Alpha value of the text color will always be 1 (i.e. fully opaque) even if a color with different alpha value is set using this method

| Parameters ||
|---------|------------------------------------------------------------------------------------------------|
| `color` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The new text color. |

### setTextContent

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setTextContent(text: String): Unit
```

Sets the text content of the annotation.

| Parameters ||
|--------|------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The new text content. This value cannot be`null`. |
