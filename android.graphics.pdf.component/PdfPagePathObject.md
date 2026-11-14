# PdfPagePathObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPagePathObject

Kotlin| [Java](https://developer.android.com/reference/android/graphics/pdf/component/PdfPagePathObject "View this page in Java") 

```
class PdfPagePathObject : PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| ↳ | [android.graphics.pdf.component.PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) ||
| | ↳ | [android.graphics.pdf.component.PdfPagePathObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#) |

Represents a path object on a PDF page. This class extends [PdfPageObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObject) and provides methods to access and modify the path's content, such as its shape, fill color, stroke color and line width.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL:kotlin.Int) Fill Mode : Only the interior of the glyphs is filled with the fill color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL_STROKE:kotlin.Int) FillStroke Mode : Both the interior and outline of the glyphs are rendered using the fill abd stroke colors respectively. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_STROKE:kotlin.Int) Stroke Mode : Only the outline of the glyphs is stroked with the stroke color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_UNKNOWN:kotlin.Int) Unknown Render Mode. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPagePathObject](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#PdfPagePathObject(android.graphics.Path))`(`path:` ` [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#)`)` Constructor for the PdfPagePathObject. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFillColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#getFillColor())`()` Returns the fill color of the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRenderMode](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#getRenderMode())`()` Returns the android. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokeColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#getStrokeColor())`()` Returns the stroke color of the object. |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStrokeWidth](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#getStrokeWidth())`()` Returns the stroke width of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#setFillColor(kotlin.Int))`(`fillColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the fill color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRenderMode](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#setRenderMode(kotlin.Int))`(`renderMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the android. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeColor](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#setStrokeColor(kotlin.Int))`(`strokeColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the stroke color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeWidth](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#setStrokeWidth(kotlin.Float))`(`strokeWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the stroke width of the object. |
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) | [toPath](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#toPath())`()` Returns the path of the object. |

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

### PdfPagePathObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
PdfPagePathObject(path: Path)
```

Constructor for the PdfPagePathObject. Sets the object type to [PdfPageObjectType.PATH](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPageObjectType#PATH:kotlin.Int).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `path` | [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#):This value cannot be`null`. |

## Public methods

### getFillColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getFillColor(): Int
```

Returns the fill color of the object. Returns [Color.BLACK](https://developer.android.com/reference/kotlin/android/graphics/Color.html#BLACK:kotlin.Int) if #mFillColor is not set.

| Return ||
|----------------------------------------------------------------------------|-------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The fill color of the object. |

### getRenderMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getRenderMode(): Int
```

Returns the android.graphics.pdf.component.PdfPagePathObject.RenderMode of the object. Returns android.graphics.pdf.component.PdfPagePathObject.RenderMode#RENDER_MODE_FILL by default if android.graphics.pdf.component.PdfPagePathObject#mRenderMode is not set.

| Return ||
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The android.graphics.pdf.component.PdfPagePathObject.RenderMode of the object. Value is [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_UNKNOWN:kotlin.Int), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL:kotlin.Int), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_STROKE:kotlin.Int), or [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL_STROKE:kotlin.Int) |

### getStrokeColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getStrokeColor(): Int
```

Returns the stroke color of the object.

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

### setFillColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setFillColor(fillColor: Int): Unit
```

Sets the fill color of the object.

Note: The fillColor cannot be transparent and setting the fillColor will have no effect if android.graphics.pdf.component.PdfPagePathObject.RenderMode is not [RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL:kotlin.Int) or [RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL_STROKE:kotlin.Int).

| Parameters ||
|-------------|----------------------------------------------------------------------------------------------------------|
| `fillColor` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The fill color of the object. |

### setRenderMode

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setRenderMode(renderMode: Int): Unit
```

Sets the android.graphics.pdf.component.PdfPagePathObject.RenderMode of the object.

| Parameters ||
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `renderMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The android.graphics.pdf.component.PdfPagePathObject.RenderMode to be set. Value is [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_UNKNOWN](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_UNKNOWN:kotlin.Int), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL:kotlin.Int), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_STROKE:kotlin.Int), or [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL_STROKE:kotlin.Int) |

| Exceptions ||
|--------------------------------------|----------------------------------------|
| `java.lang.IllegalArgumentException` | if the provided renderMode is invalid. |

### setStrokeColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun setStrokeColor(strokeColor: Int): Unit
```

Sets the stroke color of the object.

Note: The strokeColor cannot be transparent and setting the strokeColor will have no effect if android.graphics.pdf.component.PdfPagePathObject.RenderMode is not [RENDER_MODE_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_STROKE:kotlin.Int) or [RENDER_MODE_FILL_STROKE](https://developer.android.com/reference/kotlin/android/graphics/pdf/component/PdfPagePathObject#RENDER_MODE_FILL_STROKE:kotlin.Int).

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

### toPath

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun toPath(): Path
```

Returns the path of the object. The returned path object might be an approximation of the one used to create the original one if the original object has elements with curvature.

Note: The path is immutable because the underlying library does not allow modifying the path once it is created.

| Return ||
|------------------------------------------------------------------------------------|---------------------------------------|
| [Path](https://developer.android.com/reference/kotlin/android/graphics/Path.html#) | The path. This value cannot be`null`. |
