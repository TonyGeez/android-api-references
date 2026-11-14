# PdfPageTextObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageTextObject

Kotlin| [Java](../android/graphics/pdf/component/PdfPageTextObject.md) 
| --- | --- |

```
class PdfPageTextObject : PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfPageObject](../android/graphics/pdf/component/PdfPageObject.md) ||
| | ↳ | [android.graphics.pdf.component.PdfPageTextObject](../android/graphics/pdf/component/PdfPageTextObject.md) |

Represents a text object on a PDF page. This class extends PageObject and provides methods to access and modify the text content.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPageTextObject.md) Fill Mode : Only the interior of the glyphs is filled with the fill color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md) FillStroke Mode : Both the interior and outline of the glyphs are rendered using the fill abd stroke colors respectively. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md) Stroke Mode : Only the outline of the glyphs is stroked with the stroke color. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_UNKNOWN](../android/graphics/pdf/component/PdfPageTextObject.md) Unknown Render Mode. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageTextObject](../android/graphics/pdf/component/PdfPageTextObject.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `font:` ` [PdfPageTextObjectFont](../android/graphics/pdf/component/PdfPageTextObjectFont.md)`, `fontSize:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor for the PdfPageTextObject. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFillColor](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the fill color of the object. |
| [PdfPageTextObjectFont](../android/graphics/pdf/component/PdfPageTextObjectFont.md) | [getFont](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the font of the text. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFontSize](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the font size of the object. |
| --- | --- |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRenderMode](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the render mode of the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokeColor](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the stroke color of the object. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStrokeWidth](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the stroke width of the object. |
| --- | --- |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getText](../android/graphics/pdf/component/PdfPageTextObject.md))`()` Returns the text content of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillColor](../android/graphics/pdf/component/PdfPageTextObject.md))`(`fillColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the fill color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRenderMode](../android/graphics/pdf/component/PdfPageTextObject.md))`(`renderMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the android. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeColor](../android/graphics/pdf/component/PdfPageTextObject.md))`(`strokeColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the stroke color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeWidth](../android/graphics/pdf/component/PdfPageTextObject.md))`(`strokeWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the stroke width of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](../android/graphics/pdf/component/PdfPageTextObject.md))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the text content of the object. |
| --- | --- |

| Inherited functions ||
|---|---|
| From class [PdfPageObject](../android/graphics/pdf/component/PdfPageObject.md) |-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getMatrix](../android/graphics/pdf/component/PdfPageObject.md))`()` <br /> Returns the transformation matrix of the object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfObjectType](../android/graphics/pdf/component/PdfPageObject.md))`()` <br /> Returns the type of the page object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatrix](../android/graphics/pdf/component/PdfPageObject.md))`(`matrix:` ` [Matrix](../android/graphics/Matrix.md)`)` <br /> Sets the transformation matrix of the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transform](../android/graphics/pdf/component/PdfPageObject.md))`(`a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `c:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `d:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `e:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Transform the page object The matrix is composed as: |a c e| |b d f| and can be used to scale, rotate, shear and translate the |page_object|. <br /> | ||

## Constants

### RENDER_MODE_FILL

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val RENDER_MODE_FILL: Int
```

Fill Mode : Only the interior of the glyphs is filled with the fill color. 

 Value: 0

### RENDER_MODE_FILL_STROKE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val RENDER_MODE_FILL_STROKE: Int
```

FillStroke Mode : Both the interior and outline of the glyphs are rendered using the fill abd stroke colors respectively. 

 Value: 2

### RENDER_MODE_STROKE

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val RENDER_MODE_STROKE: Int
```

Stroke Mode : Only the outline of the glyphs is stroked with the stroke color. 

 Value: 1

### RENDER_MODE_UNKNOWN

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
static val RENDER_MODE_UNKNOWN: Int
```

Unknown Render Mode. 

 Value: -1

## Public constructors

### PdfPageTextObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
PdfPageTextObject(
    text: String, 
    font: PdfPageTextObjectFont, 
    fontSize: Float)
```

Constructor for the PdfPageTextObject. Sets the object type to TEXT and initializes the text color to black.

| Parameters ||
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `font` | [PdfPageTextObjectFont](../android/graphics/pdf/component/PdfPageTextObjectFont.md):The font of the text. This value cannot be`null`. |
| `fontSize` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The font size of the text. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |
| --- | --- |

## Public methods

### getFillColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getFillColor(): Int
```

Returns the fill color of the object. Returns [android.graphics.Color#BLACK](../android/graphics/Color.md) by default if not set.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The fill color of the object. |

### getFont

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getFont(): PdfPageTextObjectFont
```

Returns the font of the text.

| Return ||
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [PdfPageTextObjectFont](../android/graphics/pdf/component/PdfPageTextObjectFont.md) | A copy of the font object. This value cannot be`null`. |

### getFontSize

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getFontSize(): Float
```

Returns the font size of the object.

| Return ||
|--------------------------------------------------------------------------------|----------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The font size. |

### getRenderMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getRenderMode(): Int
```

Returns the render mode of the object.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The render mode of the object. Value is [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_UNKNOWN](../android/graphics/pdf/component/PdfPageTextObject.md), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPageTextObject.md), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md), or [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md) |

### getStrokeColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getStrokeColor(): Int
```

Returns the stroke color of the object. Returns [android.graphics.Color#BLACK](../android/graphics/Color.md) by default if not set.

| Return ||
|----------------------------------------------------------------------------|---------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The stroke color of the object. |

### getStrokeWidth

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getStrokeWidth(): Float
```

Returns the stroke width of the object.

| Return ||
|--------------------------------------------------------------------------------|---------------------------------|
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | The stroke width of the object. |

### getText

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getText(): String
```

Returns the text content of the object.

| Return ||
|----------------------------------------------------------------------------------|-----------------------------------------------|
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | The text content. This value cannot be`null`. |

### setFillColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setFillColor(fillColor: Int): Unit
```

Sets the fill color of the object. Setting the fillColor will have no effect if android.graphics.pdf.component.PdfPageTextObject.RenderMode is not [RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPageTextObject.md) or [RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------|
| `fillColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The fill color of the object. |

### setRenderMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setRenderMode(renderMode: Int): Unit
```

Sets the android.graphics.pdf.component.PdfPageTextObject.RenderMode of the object.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `renderMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The android.graphics.pdf.component.PdfPageTextObject.RenderMode to be set. Value is [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_UNKNOWN](../android/graphics/pdf/component/PdfPageTextObject.md), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPageTextObject.md), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md), or [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md) |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided renderMode is invalid. |

### setStrokeColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setStrokeColor(strokeColor: Int): Unit
```

Sets the stroke color of the object. Setting the strokeColor will have no effect if android.graphics.pdf.component.PdfPageTextObject.RenderMode is not [RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md) or [RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPageTextObject.md).

| Parameters ||
|---------------|------------------------------------------------------------------------------------------------------------|
| `strokeColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The stroke color of the object. |

### setStrokeWidth

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setStrokeWidth(strokeWidth: Float): Unit
```

Sets the stroke width of the object.

| Parameters ||
|---------------|----------------------------------------------------------------------------------------------------------------|
| `strokeWidth` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The stroke width of the object. |

### setText

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setText(text: String): Unit
```

Sets the text content of the object.

| Parameters ||
|--------|---------------------------------------------------------------------------------------------------------------------------------------|
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):The text content to set. This value cannot be`null`. |
