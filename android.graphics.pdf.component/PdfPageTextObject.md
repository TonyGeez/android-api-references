# PdfPageTextObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPageTextObject

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/component/PdfPageTextObject "View this page in Java") 

```
class PdfPageTextObject : PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.pdf.component.PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) ||
| | ↳ | [android.graphics.pdf.component.PdfPageTextObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#) |

Represents a text object on a PDF page. This class extends PageObject and provides methods to access and modify the text content.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL:kotlin.Int) Fill Mode : Only the interior of the glyphs is filled with the fill color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL_STROKE:kotlin.Int) FillStroke Mode : Both the interior and outline of the glyphs are rendered using the fill abd stroke colors respectively. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_STROKE:kotlin.Int) Stroke Mode : Only the outline of the glyphs is stroked with the stroke color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_UNKNOWN:kotlin.Int) Unknown Render Mode. |

| Public constructors ||
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPageTextObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#PdfPageTextObject(kotlin.String,%20android.graphics.pdf.component.PdfPageTextObjectFont,%20kotlin.Float))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, `font:` ` [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont)`, `fontSize:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Constructor for the PdfPageTextObject. |

| Public methods ||
|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFillColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getFillColor())`()` Returns the fill color of the object. |
| [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont) | [getFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getFont())`()` Returns the font of the text. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getFontSize](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getFontSize())`()` Returns the font size of the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRenderMode](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getRenderMode())`()` Returns the render mode of the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokeColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getStrokeColor())`()` Returns the stroke color of the object. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStrokeWidth](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getStrokeWidth())`()` Returns the stroke width of the object. |
| [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) | [getText](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#getText())`()` Returns the text content of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#setFillColor(kotlin.Int))`(`fillColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the fill color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRenderMode](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#setRenderMode(kotlin.Int))`(`renderMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the android. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#setStrokeColor(kotlin.Int))`(`strokeColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the stroke color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeWidth](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#setStrokeWidth(kotlin.Float))`(`strokeWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the stroke width of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setText](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#setText(kotlin.String))`(`text:` ` [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`)` Sets the text content of the object. |

| Inherited functions ||
|---|---|
| From class [PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) |-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| | [FloatArray](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float-array/index.html) | [getMatrix](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#getMatrix())`()` <br /> Returns the transformation matrix of the object. <br /> | | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getPdfObjectType](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#getPdfObjectType())`()` <br /> Returns the type of the page object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setMatrix](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#setMatrix(android.graphics.Matrix))`(`matrix:` ` [Matrix](https://developer.android.com/reference/kotlin/android/graphics/Matrix.html#)`)` <br /> Sets the transformation matrix of the object. <br /> | | [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [transform](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject#transform(kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float,%20kotlin.Float))`(`a:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `b:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `c:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `d:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `e:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`, `f:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` <br /> Transform the page object The matrix is composed as: |a c e| |b d f| and can be used to scale, rotate, shear and translate the |page_object|. <br /> | ||

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
| `font` | [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont):The font of the text. This value cannot be`null`. |
| `fontSize` | [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html):The font size of the text. |
| `text` | [String](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html):This value cannot be`null`. |

## Public methods

### getFillColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getFillColor(): Int
```

Returns the fill color of the object. Returns [android.graphics.Color#BLACK](https://developer.android.com/reference/kotlin/android/graphics/Color.html#BLACK:kotlin.Int) by default if not set.

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
| [PdfPageTextObjectFont](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObjectFont) | A copy of the font object. This value cannot be`null`. |

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The render mode of the object. Value is [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_UNKNOWN:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_STROKE:kotlin.Int), or [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL_STROKE:kotlin.Int) |

### getStrokeColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getStrokeColor(): Int
```

Returns the stroke color of the object. Returns [android.graphics.Color#BLACK](https://developer.android.com/reference/kotlin/android/graphics/Color.html#BLACK:kotlin.Int) by default if not set.

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

Sets the fill color of the object. Setting the fillColor will have no effect if android.graphics.pdf.component.PdfPageTextObject.RenderMode is not [RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL:kotlin.Int) or [RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL_STROKE:kotlin.Int).

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
| `renderMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The android.graphics.pdf.component.PdfPageTextObject.RenderMode to be set. Value is [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_UNKNOWN:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL:kotlin.Int), [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_STROKE:kotlin.Int), or [android.graphics.pdf.component.PdfPageTextObject#RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL_STROKE:kotlin.Int) |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided renderMode is invalid. |

### setStrokeColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setStrokeColor(strokeColor: Int): Unit
```

Sets the stroke color of the object. Setting the strokeColor will have no effect if android.graphics.pdf.component.PdfPageTextObject.RenderMode is not [RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_STROKE:kotlin.Int) or [RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageTextObject#RENDER_MODE_FILL_STROKE:kotlin.Int).

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
