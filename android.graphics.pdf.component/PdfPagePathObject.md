# PdfPagePathObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions)

# PdfPagePathObject

Kotlin| [Java](../android/graphics/pdf/component/PdfPagePathObject.md) 
| --- | --- |

```
class PdfPagePathObject : PdfPageObject
```

| [kotlin.Any](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-any/index.html) |||
| --- | --- | --- |
| ↳ | [android.graphics.pdf.component.PdfPageObject](../android/graphics/pdf/component/PdfPageObject.md) ||
| | ↳ | [android.graphics.pdf.component.PdfPagePathObject](../android/graphics/pdf/component/PdfPagePathObject.md) |

Represents a path object on a PDF page. This class extends [PdfPageObject](../android/graphics/pdf/component/PdfPageObject.md) and provides methods to access and modify the path's content, such as its shape, fill color, stroke color and line width.

## Summary

| Constants ||
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPagePathObject.md) Fill Mode : Only the interior of the glyphs is filled with the fill color. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md) FillStroke Mode : Both the interior and outline of the glyphs are rendered using the fill abd stroke colors respectively. |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md) Stroke Mode : Only the outline of the glyphs is stroked with the stroke color. |
| --- | --- |
| static [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [RENDER_MODE_UNKNOWN](../android/graphics/pdf/component/PdfPagePathObject.md) Unknown Render Mode. |

| Public constructors ||
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---|
| [PdfPagePathObject](../android/graphics/pdf/component/PdfPagePathObject.md))`(`path:` ` [Path](../android/graphics/Path.md)`)` Constructor for the PdfPagePathObject. |

| Public methods ||
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getFillColor](../android/graphics/pdf/component/PdfPagePathObject.md))`()` Returns the fill color of the object. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getRenderMode](../android/graphics/pdf/component/PdfPagePathObject.md))`()` Returns the android. |
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | [getStrokeColor](../android/graphics/pdf/component/PdfPagePathObject.md))`()` Returns the stroke color of the object. |
| --- | --- |
| [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html) | [getStrokeWidth](../android/graphics/pdf/component/PdfPagePathObject.md))`()` Returns the stroke width of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setFillColor](../android/graphics/pdf/component/PdfPagePathObject.md))`(`fillColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the fill color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setRenderMode](../android/graphics/pdf/component/PdfPagePathObject.md))`(`renderMode:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the android. |
| --- | --- |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeColor](../android/graphics/pdf/component/PdfPagePathObject.md))`(`strokeColor:` ` [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html)`)` Sets the stroke color of the object. |
| [Unit](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) | [setStrokeWidth](../android/graphics/pdf/component/PdfPagePathObject.md))`(`strokeWidth:` ` [Float](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-float/index.html)`)` Sets the stroke width of the object. |
| [Path](../android/graphics/Path.md) | [toPath](../android/graphics/pdf/component/PdfPagePathObject.md))`()` Returns the path of the object. |
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

### PdfPagePathObject

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
PdfPagePathObject(path: Path)
```

Constructor for the PdfPagePathObject. Sets the object type to [PdfPageObjectType.PATH](../android/graphics/pdf/component/PdfPageObjectType.md).

| Parameters ||
|--------|----------------------------------------------------------------------------------------------------------------|
| `path` | [Path](../android/graphics/Path.md):This value cannot be`null`. |

## Public methods

### getFillColor

Added in [API level 36.1](https://developer.android.com/guide/topics/manifest/uses-sdk-element.html#ApiLevels) 
Also in [S Extensions 18](https://developer.android.com/sdkExtensions) 

```
fun getFillColor(): Int
```

Returns the fill color of the object. Returns [Color.BLACK](../android/graphics/Color.md) if #mFillColor is not set.

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
| [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html) | The android.graphics.pdf.component.PdfPagePathObject.RenderMode of the object. Value is [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_UNKNOWN](../android/graphics/pdf/component/PdfPagePathObject.md), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPagePathObject.md), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md), or [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md) |

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

Note: The fillColor cannot be transparent and setting the fillColor will have no effect if android.graphics.pdf.component.PdfPagePathObject.RenderMode is not [RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPagePathObject.md) or [RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md).

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
| `renderMode` | [Int](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-int/index.html):The android.graphics.pdf.component.PdfPagePathObject.RenderMode to be set. Value is [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_UNKNOWN](../android/graphics/pdf/component/PdfPagePathObject.md), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL](../android/graphics/pdf/component/PdfPagePathObject.md), [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md), or [android.graphics.pdf.component.PdfPagePathObject#RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md) |

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

Note: The strokeColor cannot be transparent and setting the strokeColor will have no effect if android.graphics.pdf.component.PdfPagePathObject.RenderMode is not [RENDER_MODE_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md) or [RENDER_MODE_FILL_STROKE](../android/graphics/pdf/component/PdfPagePathObject.md).

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
| [Path](../android/graphics/Path.md) | The path. This value cannot be`null`. |
